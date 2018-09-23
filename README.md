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
### 按照冒号分割，打印第1列和第7列。
<pre><code>
cat a.txt | awk  -F  ‘:’ ‘{print $1”\t”$7}’
</code></pre>
