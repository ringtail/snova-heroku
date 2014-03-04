snova-heroku
============
a little guide for deploying snova on heroku
###  snova vs goagent
snova is a tool just like goagent.but goagent is a little sick.your data flow is limit blow 1G a day because of GAE.  snova is unlimited.

### deploying snova on heroku
First, you need a heroku id and install toolkit
<pre>
<code>

    git clone this repo
    
    cd  snova
    
    heroku login
    
    git init 
    
    git commit -m 'add some comment'
    
    heroku create appname 
    
    git push heroku master   
    
</code>
</pre>
and you need add you url into the client config file   
<pre>
<code>
[C4]
Enable=1  #change this value to 1
Listen=localhost:48102
WorkerNode[0]= #add the heroku's app url to this part
WorkerNode[1] = #add some other app url to this part
ReadTimeout = 25
MaxConn = 3
WSConnKeepAlive = 1800
Compressor=Snappy

[SPAC]
Enable=1  #change this value to 1
Default=C4 #set value to C4

</code>
</pre>

###enjoy it 
<a mailto="zhongwei.lzw@alibaba-inc.com">Mail Me</a>




