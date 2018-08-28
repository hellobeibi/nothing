# nothing
不知道要做什么，也不知道会做什么，特在此记录，不定期更新

##2018-08-27

	遇到问题 ，@RequestBody MultiValueMap 报415错误，解决：
	   <mvc:annotation-driven>
	        <mvc:message-converters register-defaults="false">
	            <!-- 将StringHttpMessageConverter的默认编码设为UTF-8 -->
	            <bean class="org.springframework.http.converter.StringHttpMessageConverter">
	                <constructor-arg value="UTF-8"/>
	            </bean>
	            <ref bean="jacksonMessageConverter" />
	            <!--application/x-www-form-urlencoded 支持-->
	            <bean class = "org.springframework.http.converter.FormHttpMessageConverter"/>
	        </mvc:message-converters>
	    </mvc:annotation-driven>


	<a>标签 通过 target='_blank' 方法打开的新页面 ，调用原页面的方法，使用 window.opener.xxxFun :参考。http://www.w3school.com.cn/jsref/prop_win_opener.asp