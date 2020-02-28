# npm-create-demo
自己创建一个可以引入的本地npm包
Npm link参考：https://www.jianshu.com/p/aaa7db89a5b2 
(3)我们将自己写好的插件，如果需要什么强依赖的包，需要提前通过npm i xxx --production，引入到项目里
①【因为在此种npm link模式下，他只会在我们插件自己的项目node_modules目录中寻找所依赖的包，而不是引入他的项目！！！！并且，此种模式下如果不在原插件中进行引入依赖，那么在引入他的项目中运行npm i 等安装依赖包的命令，就会自动将该依赖删除。需要我们重新在引用插件的项目中运行npm link 插件项目名(并且依赖仍是未安装的)】
如果不是npm link引用方式，而是已经上传到npm上了，就正常npm install 包名，然后npm i --production安装所需依赖，require('包名')，然后正常使用即可
