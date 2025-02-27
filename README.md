
## 部署
[![Vercel](https://vercel.com/button)](https://vercel.com/import/project?template=https://github.com/gaboolic/vercel-reverse-proxy)


## 使用方法
1 部署。部署有两种方法，一是直接点击上方按钮一键部署，二是可以先fork本项目，再登录[vercel](https://vercel.com/)网站新建
![新建项目](img/newproject.png)

2 绑定自己的域名(不是必须，使用vercel自带的子域名也可以，但是自带的域名vercel.app在国内网络环境不好的情况下不可用) 可以申请[tk免费域名](http://www.dot.tk/)或者薅小域名注册商首年免费羊毛
![绑定域名](img/domain.png)
绑定域名时按照vercel上的说明配置即可，其实就是在你的域名上配了一个子域名，cname到vercel服务器

3 访问 域名/proxy/url  或者/httpproxy/url即可。
映射规则为/proxy/url映射到https接口，/httpproxy/url映射到http接口

## 示例
例1 访问https://替换为你自己的域名.com/proxy/api.openai.com/v1/chat/completions 
实际上会替换为https://api.openai.com/v1/chat/completions
![demo1](img/demo1.png)

例2 访问https://替换为你自己的域名.com/proxy/raw.githubusercontent.com/gaboolic/vercel-reverse-proxy/main/vercel.json
实际上会替换为https://raw.githubusercontent.com/gaboolic/vercel-reverse-proxy/main/vercel.json
![demo2](img/demo2.png)
映射规则为/proxy/url映射到https接口，/httpproxy/url映射到http接口

也可用于github下载加速。假如原始链接是https://objects.githubusercontent.com/github-production-release-asset-2e65be/xxxxxx 
改为https://替换为你自己的域名.com/proxy/objects.githubusercontent.com/github-production-release-asset-2e65be/xxxxxx 就可以加速了。下图是github原始链接和加速后对比。可以看到效果杠杠的，每秒50kb小水管变成了每秒2mb的大水管
![github-download](img/github-download.png)

例3 访问https://替换为你自己的域名.com/proxy/www.google.com/search?q=vercel-reverse-proxy
实际上会替换为https://www.google.com/search?q=vercel-reverse-proxy
![demo3](img/demo3.png)
代理google搜索结果页面
