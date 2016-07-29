
* ó�� ������ git status �ؼ� clean�� �ȵǸ� (MosaicWeb����)
1. git add *
2. git commit -m "���� ����"
3. git push
4. dev���� git pull


1. Spring Starter Project ����

   - Name : MosaicWeb
   - Type : Gradle(Buildship)
   - Packaging : war
   - Group : com.hybrid
   - Artifact : MosaicWeb
   - Package : com.hybrid
   
   - Dependencies ���� : Web - Web

2. �������

   - Remote Repository ���� (github)
   - Local Repository ����
      - >> git status
      - >> git log
      - >> dir /A > .gitignore
      - >> notepad .gitignore ����
      - >> git init
      - >> git add *
      - >> git commit -m "first commit" 
   - Local ====push===> Remote (���� ����ȭ)
      - >> git remote add origin https://github.com/chr0032/MosaicWeb.git
      - >> git remote -v
      - >> git remote remove origin (remote����)
      - >> git remote add origin https://github.com/chr0032/MosaicWeb.git
      - >> git push -u origin master (ó�� �Ҷ��� �� ���Ĵ� git push)
   - ������ 2�� Clone ����
      - >> git clone https://github.com/chr0032/MosaicWeb.git (D:\03_Src\jsp\MosaicWeb ����)
      - >> git clone https://github.com/chr0032/MosaicWeb.git MosaicWebDev (D:\03_Src\jsp ���� �����ϸ� MosaicWebDev ���ϵ� ���� Ŭ�е� ��)
      - >> Eclipse Gradle Import (��Ŭ���� �󿡼� ���� Ȯ�� ����)     
   - ������ 1(master)�� ������� ����
      - >> git add .
      - >> git status
      - >> git push
   - ������ 2�� ������� �޾ƿ���
      - >> git pull
      
3. HTML ����

   - ���� ���ʿ�
   - mkdir src/main/webapp ���� ����
   - notepad src/main/webapp/Hello.html
   - gradle bootRun 
   - Firefox ==> http://localhost:8080/Hello.html
      
4. JSP ����

   - mvnrepository.com  >> search : tomcat jasper
   - build.gradle dependency : providedRuntime group: 'org.apache.tomcat.embed', name: 'tomcat-embed-jasper', version: '8.5.4'
   - Eclipse -> Gradle Refresh
   - notepad src/main/webapp/Hello.jsp
   - gradle bootRun
   - Firefox ==> http://localhost:8080/Hello.jsp
   
5. Servlet ����   
   
   - MosaicWebApplication.java << @ServletComponentScan �߰�
   - com.hybrid.servlet.HelloServlet.java ����
   - Eclipse -> project -> Project Pacets 
   - >> Dynamic WebModule (version : 3.1)
   - >> java(version : 1.8)
   - >> javascript(version : 1.0)
   - gradle bootRun
   - Firefox ==> http://localhost:8080/HelloServlet
   
6. Springloaded ���� (���ε� ���)
   
   - Terminal���� tree /f ���� ������ ���� HelloServlet.class�� �ΰ��� �ִµ� Eclipse�� �����ϴ� ���� Gradle�� �����ϴ� ���� �����ش�.
   - mvnrepository.com >> search : springloaded
   - build.gradle�� ���� (�� ��)
   ->> (���� dependencies) classpath("org.springframework:springloaded:1.2.6.RELEASE") 
   ->> (�Ʒ��� dependencies) compile group: 'org.springframework', name: 'springloaded', version: '1.2.6.RELEASE'
   - Eclipse Output Directory ����
   -    bin ==> build/classes/main
   - ������2�� Project -> Properties ���� �ΰ��� ������ �ʿ���
   - 1. Project Facets-> 
   
  7. Mybatis ����
  
   - mvnrepository.com >> search : spring boot mybatis
   - build.gradle�� Dependency ����
 
		- compile group: 'org.mybatis.spring.boot', name: 		'mybatis-spring-boot-starter', 
		  version: '1.1.1'
		- compile files('src/main/webapp/WEB-INF/lib/ojdbc7.jar');

   - application.properties
   
   		- >> spring.datasource.driver-class-name=oracle.jdbc.OracleDriver
		- >> spring.datasource.url=jdbc:oracle:thin:@52.78.14.61:1521:orcl
		- >> spring.datasource.username=scott
		- >> spring.datasource.password=tiger
   		
   - Eclipse Gradle Reflesh ����   
   - gradle bootRun
   
   - notepad src/main/java/com/hybrid/mapper/DeptMapper.java �������̽� ����   
   - notepad src/main/java/com/hybrid/dao/DeptDao.java Ŭ���� ����   
   