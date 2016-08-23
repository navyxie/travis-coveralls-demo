# travis-ci and coveralls demo

当项目托管在github时，可以利用[travis-ci](https://travis-ci.org)来进行集成测试，并且通过[coveralls](https://coveralls.io/)来显示项目的代码测试覆盖率。这样整个项目给人的感觉会比较可靠稳定。效果图如下所示：
![效果显示](./images/result.jpg) 
第一个红框build passing 代表项目测试通过，第二个红框代表项目测试的覆盖率。

**下面介绍配置完成这个配置的步骤 （7个步骤，很简单）：**

1 配置你在github上项目，开启travis-ci hook,如下图：
  ![配置你在github上项目，开启travis-ci hook](./images/jc-1.jpg)
2 登录（使用你的github账户授权登录，可能需要翻墙）[https://travis-ci.org](https://travis-ci.org)官网去开启项目，如下图：
  ![登录https://travis-ci.org](./images/jc-2.jpg)
3 登录（使用你的github账户授权登录，可能需要翻墙）[https://coveralls.io](https://coveralls.io)官网去获取项目的token，如下图：
  ![登录https://coveralls.io](./images/jc-3.jpg)
  ![登录https://coveralls.io](./images/jc-4.jpg)
4 配置.coveralls.yml文件，你的代码覆盖率将会根据配置文件（repo_token）更新到对应的项目，如下图：
  ![配置.coveralls.yml文件](./images/jc-5.jpg
5 配置.travis.yml文件，当提交代码到github时，会自动触发travis hook，根据该配置文件运行项目的测试代码，如下图：
  ![配置.travis.yml文件](./images/jc-6.jpg)
6 配置你的package.json文件，通过npm script 运行你的测试，如下图：
  ![配置你的package.json文件](./images/jc-7.jpg)
7 为你的README.md文件添加测试结果和覆盖率的显示，如下图
  ![为你的README.md文件添加测试结果和覆盖率的显示](./images/jc-8.jpg)

**上面7个步骤完成后，可以提交你的代码了，你会看到一些变化：**


- 回到github的项目主页，你会看到项目多了下图显示：
  ![效果显示](./images/result.jpg)
- github的该项目webhook那里，第一个步骤配置的Travis已经高亮，如下图：
  ![效果github配置显示](./images/rs-2.jpg)
- Travis-ci会有这个项目测试的详细信息，如下图：
  ![显示Travis-ci效果](./images/rs-3.jpg)
- github的该项目webhook那里，第一个步骤配置的Travis已经高亮，如下图：
  ![效果显示](./images/rs-4.jpg)

全文到此结束！！！

附一个项目的完整例子[https://github.com/navyxie/access-token-api](https://github.com/navyxie/access-token-api)
