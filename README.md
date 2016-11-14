# SqlLearning
just learning sql

<li>按指定条件查询无重复的记录</li>
select dinstinct Id from stu;
<li>查询某个最大值、最小值</li>
select Max(Id) from stu;
select Min(Id) from stu;
<li>查询的记录依次按某些记录排序</li>
select * from stu order by Id desc;
<li>查询的记录分组</li>
select id,max(name) from stu group by(Id);
<li>查询的行数</li>
select count(*) from stu
<li>多个表的记录合并</li>
select id from stu 
union
select id from sco
<li>从多个表中获取数据（内、左、右 关联）</li>
内连接：不符合条件的，就不在结果集里
select * from stu as s1 inner join  sco as s2 on s1.id!= s2.id
左连接：左边的全显示，右边的没有就为null
select * from stu as s1 left join  sco as s2 on s1.id= s2.id
右连接：右边的全显示，左边的没有就为null
select * from stu as s1 right join  sco as s2 on s1.id= s2.id
