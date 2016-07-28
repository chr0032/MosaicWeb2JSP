
1. Spring Starter Project 생성
	
	- Name : MosaicWeb2
	- Type : Gradle(BuildShip)
	- Packaging : war
	- Group : com.hybrid
	- Artifact : MosaicWeb2
	- Package : com.hybrid
	
	- Dependencies : web 선택

2. 형상관리 

	- Remote repository 생성(github)
	- Local repository 생성	
		- >> git status (현재 상태 파악)
		- >> git log (현재 상태 확인)
		- >> dir /A > .gitignore
		- >> notepad .gitignore
		- >> git init (처음에만)
		- >> git add *
		- >> git commit -m "first commit"
	- Local ==> Remote push(최초 동기화)
		- >> git remote -v (remote 정보 확인)
		- >> git remote remove origin (remove 정보 제거)
		- >> git remote add origin https://github.com/chr0032/MosaicWeb2.git
		- >> git push -u origin master (처음에만)
		- >> git status
	- 개발자2  Clone 수행 
		- >> git clone https://github.com/chr0032/MosaicWeb2.git
		- >> git clone https://github.com/chr0032/MosaicWeb2.git MosaicWebDev (MosaicWeb 겹침우려)
		- >> Eclipse Gradle Import	
		
		
	