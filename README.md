# sentinel持久化到nacos    

###### 在rule添加以下文件实现nacos配置
|-- rule  
|   |-- nacos  
|   |   |-- auth  
|   |   |-- degrade  
|   |   |-- flow  
|   |   |-- hotparamrule  
|   |   |-- systemrule  
|   |   |-- NacosConfig nacos访问地址

###### 在以下文件中修改:1.将sentinelApiClient.fetch***()改为对应的ruleProvider.getRules。2.修改publishRules方法，使用rulePublisher.publish
|-- controller   
|   |-- AppController  
|   |-- AuthController  
|   |-- AuthorityRuleController  
|   |-- DegradeController  
|   |-- DemoController  
|   |-- FlowControllerV1  
|   |-- MachineRegistryController  
|   |-- MetricController  
|   |-- ParamFlowRuleController  
|   |-- ResourceController  
|   |-- SystemController
