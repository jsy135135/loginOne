# loginOne
同一个用户，不能够同时在不同的客户端登录
# 实现原理
<p>登录和判断登录原理，还是和之前的业务逻辑是一样的,在之前的业务逻辑上，做了一些增加和改变</p>
<p>1、用户user表增加last_session_id（用户最好登录记录的session_id）</p>
<p>2、在判断用户是否登录是，先判断session_id和上次登录的是否一致
如果不一致，就清空用户的session信息,提示用户已经在别处登录。
同时，session被清空之后，用户也被判断为未登录。也就基本实现了，T用户
下线的功能（一端登录，另外一端T下线）</p>
<p>3、判断用户是否登录，还是判断session里存的的用户id或者用户名称来实现</p>

![image](https://github.com/jsy135135/loginOne/raw/master/demo.gif)
