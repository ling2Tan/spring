spring aop
<bean id="minstrel" class="com.springinaction.knights.Minstrel"/>
<aop:config>
 <aop:aspect ref="minstrel">
  <aop:pointcut id="embark" expression="execution(* *.embarkOnQuest(..))"/>
  <aop:before pointcut-ref="embark" method="singBeforeQuest"/>
  <aop:after pointcut-ref="embark" method="singAfterQuest"/>
 </aop:aspect>
</aop:config>

