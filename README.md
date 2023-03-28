# Spring---Annotation-Based-Configuration
it became possible to configure the dependency injection using annotations. Annotation injection is performed before XML injection

1. @Configuration: Indicates that a class is a configuration class and contains one or more bean definitions.

2. @ComponentScan: Scans the specified package and its sub-packages for classes marked with the @Component, @Service, @Repository, or @Controller annotations, and registers them as Spring beans.

3. @Bean: Indicates that a method returns a bean instance, which is registered with the Spring container. This method can also specify the dependencies required by the bean.

4. @Autowired: Injects a bean dependency by type. You can use this annotation to autowire dependencies in constructor arguments, method parameters, or fields.
    @Autowired on Properties
    ```java
    @Autowired
    privateSpellCheckerspellChecker;
    ```
    
    @Autowired on Constructors
    
    ```java
    @Autowired
    publicTextEditor(SpellCheckerspellChecker){
    System.out.println("Inside TextEditor constructor.");
    this.spellChecker=spellChecker;
     }


5. @Qualifier: Used along with @Autowired to specify the name of the bean to inject, in case there are multiple beans of the same type.
      ```java
      @Autowired
      @Qualifier("student1")
      privateStudentstudent;

      <!-- Definition for student1 bean -->
      <beanid="student1"class="com.tutorialspoint.Student">
      <propertyname="name"value="Zara"/>
      <propertyname="age"value="11"/>
      </bean>
      ```

6. @Value: Used to inject a value into a bean property. The value can be a string or a SpEL expression.

5. @Profile: Indicates that a bean should be created only if a specific profile is active. You can activate a profile by setting the spring.profiles.active property in your application.properties file.
