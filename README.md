<h1 align =“ center”>RekSai</ h1>

<p>
  <img src="https://img.shields.io/badge/Language-Python/3.x-blue" />
  <img src="https://img.shields.io/badge/Version-1.0-blue" />
  <a href="https://plat.wgpsec.org">
    <img src="https://img.shields.io/badge/Dependence-WgpSec%20Plat-green" target="_blank" />
  </a>
</p>

> 一个信息收集的轮子！



## 开始使用

1. 除了`python3`你不需要自己安装任何一个东西，它能够自动帮你部署所有的环境和工具，除了第一次加载比较慢以外:smile:

2. 工具的原理是通过用户输入的`URL`进行信息收集，包括但不限于whois，域名对应的IP，端口、敏感目录、C段、C段的IP对应端口等

3. 但是只能在Liunx下使用！

4. 使用的时候先去server酱注册一个账号，绑定微信，将授权码放在下面，server地址：http://sc.ftqq.com/：

   ![](https://cdn.jsdelivr.net/gh/Abao520/imaegs@main/20201110/peizhi.4ox1yakcog3k.png)

   ![](https://cdn.jsdelivr.net/gh/Abao520/imaegs@main/20201110/server.30jk5ihyl6yo.png)
   
   ![](https://cdn.jsdelivr.net/gh/Abao520/imaegs@main/20201110/Screenshot_2020-11-10-14-51-59-560_com.tencent.mm.6q0b2xsiw2yo.jpg)

## 使用方式

1. 语法：

   * 单个扫描

   ```python
   python3 RekSai.py
   ```

   * 批量

   ```python
   nohup python3 RekSai.py &
   ```

   > 使用批量的方式需要在当前目录下添加一个url.txt文件，并且需要配置一下server酱！

   

   进入工具以后，你只需要输入自己的想要扫描的`URL`就行了。

   理论上支持加上端口，比如`www.baidu.com:8080`但是避免一些不必要的问题出现，还是不要用的好 /dog

2. 如果你发现你的域名是上面的格式，但是确实没有回显的话，那么请一定要`Issue`到github上。

3. CDN的判断基本上算是没啥篮子用，CDN的判断和C段的扫描挂钩，但是我整不出CDN的判断。所以只要C段IP超过10个默认就不扫描C段的IP端口了，你可以在总结文本中找到C段IP。

4. 目前不支持二级或者三级域名，后面会慢慢优化

5. 总结的信息保存在`$PWD/result/输入的域名/sumary.txt`中

6. 不建议扫描国外的网站，会很慢，当然你加代理的话，当我没说

## 使用截图：

* 域名失活：
  ![1.png](https://cdn.jsdelivr.net/gh/Abao520/imaegs@main/20201110/1.77gb7darp9mo.png)

* 国外：
  ![2](https://cdn.jsdelivr.net/gh/Abao520/imaegs@main/20201110/2.4s2kzvfwvd34.png)
  ![3](https://cdn.jsdelivr.net/gh/Abao520/imaegs@main/20201110/3.54v016w1ga9s.png)
  ![4](images/4.png)
  ![5](https://cdn.jsdelivr.net/gh/Abao520/imaegs@main/20201110/4.75hik8wc0rcw.png)

* ![6](https://cdn.jsdelivr.net/gh/Abao520/imaegs@main/20201110/6.23vb4844dbz4.png)

  总结文件：
  ![7](https://cdn.jsdelivr.net/gh/Abao520/imaegs@main/20201110/7.53yb6vy1btkw.png)

* 国内：

  ![8](https://cdn.jsdelivr.net/gh/Abao520/imaegs@main/20201110/8.6n5wl7qykutc.png)
  ![9](https://cdn.jsdelivr.net/gh/Abao520/imaegs@main/20201110/9.13x3ixpglxy8.png)

  ![10](https://cdn.jsdelivr.net/gh/Abao520/imaegs@main/20201110/10.59b79lpeiveo.png)

  

国内明显快很多



## TODO



1. 规范域名的输入
   ~~具体实现：用户输入域名或者ip使用正则提取出域名和ip，再分别使用http和https协议进行测活，保存到self.domain中~~

2. 联动nmap和xray
   具体实现：创建新方法getxary，在getpotr方法下使用nmap方法探测对应的服务

3. 优化输出
   具体实现：将得到的信息具体的输出位html格式，类似xray的输出

4. 模块化添加工具
   具体实现：创建模块化方法，下载工具和将工具和前面的联动起来，起到更多功能的实现

5. 添加JSFinder
   具体实现：在子域收集下面多加上这个需求，然后进行测活和输出

6. 添加批量扫描
   ~~具体实现：可能需要重构一些代码，或者重新开发新版本出来进行操作，一个作为日常收集，一个作为批量扫描，为爬虫添加UA池和代理ip功能~~

7. 优化：优化变量名称，优化扫描，线程，优化用户体验，不输出过多无用的log

## 💡免责声明

不能使用该工具进行非法活动，下载该工具就表示同意此条款，后续与作者无关