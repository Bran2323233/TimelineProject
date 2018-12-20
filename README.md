# TimelineProject
桌面应用版内部有数据库连接操作，请各位自行更改 我使用的是mysql数据库  
数据库有两张表  
第一张表名为  users  
里面有 account 和 password 两个属性 都为varchar 类型 长度255 其中account不为null 且为主键  
第二张表名为  infos  
里面有 account information image time 四个属性 前三个都为varchar类型 长度为255 time为timestamp类型   
其中 除了image以外全部不为空 无主键。  
  
infos表的mysql语句  
CREATE TABLE `infos` (  
  `account` varchar(255) NOT NULL,  
  `information` varchar(255) NOT NULL,  
  `image` varchar(255) DEFAULT NULL,  
  `time` timestamp NOT NULL  
) ENGINE=MyISAM DEFAULT CHARSET=utf8;  
  
users表的mysql语句  
CREATE TABLE `users` (  
  `account` varchar(255) NOT NULL,  
  `password` varchar(255) DEFAULT NULL,  
  PRIMARY KEY (`account`)  
) ENGINE=MyISAM DEFAULT CHARSET=utf8;  

