# sonarqube-docker-dotnet-poc

 - install java https://download.oracle.com/java/17/latest/jdk-17_windows-x64_bin.msi
 - install dotnet-sonarscanner

```bash
dotnet tool install --global dotnet-sonarscanner
```

 - issues with wsl2 / ubuntu / docker
 - this doesn't solve https://githubmemory.com/repo/bitnami/bitnami-docker-sonarqube/issues/21
 - logs into /opt/bitnami/sonarqube/logs/
 
 - docker desktop issues:

```bash
wsl -d docker-desktop
sysctl -w vm.max_map_count=262144
```
 - docker-compose up
 - http://localhost:9000/ -> admin|bitnami

 - create project | create token | .net | sessionstart | build  | sessionend
 - create project | create token | node | exec bat in the project.json folder

 - example
```bash
dotnet sonarscanner begin /k:"dotnettest" /d:sonar.host.url="http://localhost:9000"  /d:sonar.login="dc985ad9175e93f23cd7ebfbe9bbf67c5e825a0d"
```
