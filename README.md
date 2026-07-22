### 【安装说明】
* 打开你的 2022.3.22f1版本 VRChat Unity工程，将"PePoToonBRP.unitypackage"文件导入进去，如果导入成功，"Assets"文件夹内会有一个"PePoToon"文件夹，这就是我的着色器了。<br>
* 你注意到"PePoToon"文件夹内还有一个"Test_YouCanDeleteThis"文件夹，里面有一个"New Scene"场景，打开它，里面展示了一些PePoToon着色器的特色功能。<br>
* 将PePoToon文件夹放入Unity项目Assets文件夹内的任意位置，可能需要重启Unity项目。除非你已含有PePoToon同名着色器，否则一般不会出现问题。
* 只适配了Unity 2022.3.22f1版本，其他版本可能存在问题。只支持前向渲染，不支持延迟渲染。只支持英文和简体中文，根据你的电脑语言自动切换。
* 您应当把PePoToon看作是Unity标准着色器的外轮廓版本，而非LilToon的平替。PePoToon是基于真实光照开发的，无法实现华丽的特效。
### 【一些问题】
* 由于Unity内置管线不支持2500以上渲染队列的接收阴影，为了让透明物体接收阴影，可以将半透明物体的Render Queue从3000改为2460（LilToon的透明模式就是2460队列），
并打开ZWrite（不勾选会导致天空盒遮住物体，因为天空盒的队列是2500.5），缺点是该材质物体后面队列大于等于2460的物体无法渲染。
