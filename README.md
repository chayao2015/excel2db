Excel转二进制工具
===

目的：
---
游戏开放中有原型数据，而原型数据经常都是通过excel进行编写，关于程序如何去读取excel中的数据，方法有很多种，比如:<br>
1.将excel导入mysql中，然后由程序去读取数据库,但是客户端无法读取数据库，经常还要重新给客户端导出xml，比较麻烦<br>
2.客户端服务器直接读取excel，excel是比较大的，不适合存放在客户端<br>

excel2db-write
---
将excel转成ndb文件(二进制文件),格式参考：二进制格式文档<br>
读取excel，根据定义好的格式写入ndb文件中，同时根据指定不同的语言生成各自的bean类<br>
使用：
pom.xml打包，将target中的zip包拷贝出来，根据附录1中的参数说明填写参数,提供了测试的excel见附录2

excel2db-read
---
提供java版本的解析ndb文件，并将结果映射到bean中

excel2db-browse
---
提供查看ndb文件的客户端，将ndb文件拖入到窗口中查看

附录
---
1.bat中参数说明：<br>
language     指定语言支持java,csharp<br>
beanRoot     指定bean的生成路径,一般都是指定到我们项目中<br>
packageRoot  指定bean的包路径<br>
excelPath    指定excel的存放路径<br>
ndbPath      指定ndb的存放路径<br>

2.test.xls  指定了excel的格式,兼容excel2003和2007<br>
第三行指定类型分别有:int,float,long,string,double,ints,floats,longs,strings,doubles<br>
