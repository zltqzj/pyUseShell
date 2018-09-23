# pyUseShell

### python代码
<pre><code>
import os,sys
arg0= sys.argv[1]
arg1 = sys.argv[2]
os.system('./hello.sh '+arg0+' '+arg1)
</code></pre>
### shell代码
<pre><code>
#!/bin/bash
echo "hello world ${1} ${2}"
exit 0
</code></pre>

### python调用shell
<pre><code>
 python d.py zhao jian
</code></pre>

### 执行结果
<pre><code>
hello world zhao jian
</code></pre>


## awk示例
### 按照冒号分割，打印第1列和第7列
<pre><code>
cat a.txt | awk  -F  ‘:’ ‘{print $1”\t”$7}’
</code></pre>
### 搜索b.txt有root关键字的所有行
<pre><code>
awk -F: '/root/' b.txt
</code></pre>

### 统计/etc/passwd:文件名，每行的行号，每行的列数，对应的完整行内容
<pre><code>
awk  -F ':'  '{printf("filename:%10s,linenumber:%s,columns:%s,linecontent:%s\n",FILENAME,NR,NF,$0)}' /etc/passwd
</code></pre>


### 如果第一个域大于第二个域
<pre><code>
awk '{if($1>$2) print $1 "bad";else print "ok"}' b.txt
</code></pre>

