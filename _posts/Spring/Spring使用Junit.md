---
layout: post
category : Spring
tagline: Spring
tags : [Spring,Junit]
---
{% include JB/setup %}
# Spring使用Junit

需要导入以下几个包

	1.	JUnit 4  
	1.	Spring Test （Spring框架中的test包） 
	3.	Spring 相关其他依赖包（context等包）

测试代码：

```
@RunWith(SpringJUnit4ClassRunner.class)
@ContextConfiguration(value = "classpath:spring-servlet.xml")
public class SpringTest {
	@Autowired
	private StudentMapper studentMapper;
	@Test
	public void testMap() {
    	StudentEntity se = new StudentEntity();
    	Map<String, Object> param = new HashMap<String, Object>();
    	param.put("studentID", "123457");
    	se = studentMapper.getByMap(param);
    	System.out.println(se);
	}
}


```
    @ContextConfiguration(value = { "classpath:conf/te_bean.xml", "file:src/main/webapp/WEB-INF/applicationContext.xml" })