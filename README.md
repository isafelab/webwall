iSafeLab 成员主要均为安全研究爱好者，代码可能不是特别好，如有不当，还望斧正。

 > 本项目由于非商业项目，如需二开请自行研究，参数已经封装的妥妥的，如果只是站长请直接开启使用即可

# 关于
WebWall是一款基于 PHP（有其他语言的可以pull进来） 的轻量型 WEB防火墙，旨在于进一步加强对全国中小网站的安全防护，提高网站安全防护能力

考虑到性能和简单性，这个脚本只提供了基础的功能防护（简单和误报的均衡)，提供最基础的SQL注入、XSS防护、Oday等情况。

如有遇到 Webwall 被 Bypass绕过 或者其他BUG(如误杀)的情况及时 邮件+Issues+（一切能联系的到的方式）

不要过度依赖本模块，弱密码、代码逻辑错误等不在本防火墙防御内（网络安全不是一个文件就能解决的问题）

 > 本项目为开源项目，未收取任何费用，使用问题请借助 Issues 提交 或者通过群友互助
 
 ## 白名单问题
 非开发者(如cms开发者)强烈不建议设置白名单，强烈建议把白名单留空

  如程序中包含 /admin /admin.php /wp-admin /dede 这种路径导致被拦截

  我只想问一句，后台页面不改的吗。。。（有时间写个wiki讲解一下后台怎么弄会安全一点）
 
  ## 安装及使用
  将下载的 isafeLab-Waf.zip 解压后，得到 isafeLab 文件夹，并上传至网站根目录

  在全局加载的文件中( 示例网站根目录下: index.php 或 config.php )，加入如下代码：
  
```php
if(is_file($_SERVER['DOCUMENT_ROOT'].'/isafeLab/isafe-Waf.php')){
    require_once($_SERVER['DOCUMENT_ROOT'].'/isafeLab/isafe-Waf.php');
} //注意文件路径
```
