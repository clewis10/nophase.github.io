---
sidebar_position: 3930
title: 🎪🎪🎪-1️⃣🛢 DB ➜ MariaDB
---

# Mysql


 


⬛️⬛️⬛️⬛️⬛️⬛️⬛️⬛️⬛️⬛️⬛️⬛️⬛️⬛️⬛️⬛️⬛️------⬛️⬛️⬛️⬛️⬛️⬛️⬛️⬛️⬛️⬛️⬛️⬛️⬛️⬛️⬛️⬛️⬛️⬛⬛️⬛️
🔵🔵🔵🔵🔵🔵🔵🔵🔵🔵🔵🔵🔵🔵🔵🔵🔵 MySQL🔵🔵🔵🔵🔵🔵🔵🔵🔵🔵🔵🔵🔵🔵🔵🔵🔵🔵🔵🔵
⬛️⬛️⬛️⬛️⬛️⬛️⬛️⬛️⬛️⬛️⬛️⬛️⬛️⬛️⬛️⬛️⬛️------⬛️⬛️⬛️⬛️⬛️⬛️⬛️⬛️⬛️⬛️⬛️⬛️⬛️⬛️⬛️⬛️⬛️⬛️⬛️⬛️

🔸 数据库操作
		• 创建数据库   create database wpj1105;
		• 删除数据库   drop database wpj1105;
		• 使用数据库   use wpj1105;
		• 显示数据库   show databases;


🔸 判断
		drop database if exists wpj1105;  	# 如果某数据库存在就删除
		drop table if exists student;  		# 如果某表存在就删除


🔸 表	
	⦿ 创建表
			create table student(
			id int auto_increment primary key,
			name varchar(50),
			sex varchar(20),
			date varchar(50),
			content varchar(100)
			)default charset=utf8;


	⦿ 删除表         drop table student;
	⦿ 查看表的结构   describe student;  #可以简写为desc student;


🔸 插入数据
		这个就要看user_token 表结构了 
		+-------+-------+---------+-------------+-------------+
		| id    | token | user_id | create_time | expire_time |
		+-------+-------+---------+-------------+-------------+
		|    12 |       |       0 |           0 |           0 |

		语法: INSERT INTO table_name ( field1, field2,...fieldN ) VALUES ( value1, value2,...valueN );
		实例: insert into user_token (id,token,user_id,create_time,expire_time) VALUES (98,1,2,3,4);
		这个例子肯定是对的


🔸修改某一条数据
	update student set sex=’男’ where id=4;

🔸修改某字段数据
	UPDATE table_name SET field1=new-value1,
	UPDATE user SET transfer_enable=21474836480



🔸 删除某表某条记录
	删除一条记录: delete from 表名 where id=1;


🔸 删除某表所有记录(保留结构)
	use ss-vps1;
	show tables;
	DELETE FROM `22`;
	DELETE FROM `ss_node_online_log`;
	❗️❗️ 表名外面 必须加上 `` . 这个不是单引号. 而是ESC键下面的符号. ❗️❗️

	顺便把 ss-vps1 里的无用数据都删除了吧 
	DELETE FROM `ss_checkin_log`;
	DELETE FROM `ss_node_info_log`;
	DELETE FROM `user_traffic_log`;


