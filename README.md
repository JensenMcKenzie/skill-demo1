1. 
```
git clone https://github.com/ucsd-cse15l-f22/skill-demo1

cd skill-demo1

git clone https://github.com/ucsd-cse15l-f22/skill-demo1; cd skill-demo1
```

2. FOR WINDOWS
```
javac -cp ".;lib/hamcrest-core-1.3.jar;lib/junit-4.13.2.jar" *.java

java -cp ".;lib/junit-4.13.2.jar;lib/hamcrest-core-1.3.jar" org.junit.runner.JUnitCore TestDocSearch

javac -cp ".;lib/hamcrest-core-1.3.jar;lib/junit-4.13.2.jar" *.java; java -cp ".;lib/junit-4.13.2.jar;lib/hamcrest-core-1.3.jar" org.junit.runner.JUnitCore TestDocSearch
```

3.
- Fix line 12 to assert equals on the total file count (1391)

4.
```
javac DocSearchServer.java Server.java
java DocSearchServer 4555

javac DocSearchServer.java Server.java; java DocSearchServer 4555
```

5. Into search bar

http://localhost:4555

http://localhost:4555/search?q=science

---
6. scp into remote then run programs
```
scp <filenames> username@ieng6.ucsd.edu:~/

scp DocSearchServer.java Server.java cs15lfa22cf@ieng6.ucsd.edu:~/

ssh cs15lfa22cf@ieng6.ucsd.edu "javac DocSearchServer.java Server.java; java DocSearchServer 4555"

scp DocSearchServer.java Server.java cs15lfa22cf@ieng6.ucsd.edu:~/; ssh cs15lfa22cf@ieng6.ucsd.edu "javac DocSearchServer.java Server.java; java DocSearchServer 4555"

ALTERNATIVE
ssh cs15lfa22cf@ieng6.ucsd.edu "git clone https://github.com/ucsd-cse15l-f22/skill-demo1"; scp DocSearchServer.java Server.java cs15lfa22cf@ieng6.ucsd.edu:~/skill-demo1/; ssh cs15lfa22cf@ieng6.ucsd.edu "cd skill-demo1; javac DocSearchServer.java Server.java; java DocSearchServer 4555"
```

Test all 3 computers

May have to ssh into remote and git clone the original link

---

7. Type addresses into local host

http://ieng6-201.ucsd.edu:4556/

http://ieng6-202.ucsd.edu:4556/

http://ieng6-203.ucsd.edu:4556/

---

http://ieng6-201.ucsd.edu:4556/search?q=science

http://ieng6-202.ucsd.edu:4556/search?q=science

http://ieng6-203.ucsd.edu:4556/search?q=science

---
8. Change local server to filter by file name
Change line 47 condition to
`f.toString().contains(parameters[1])`

Recompile
```
javac DocSearchServer.java Server.java
java DocSearchServer 4555

javac DocSearchServer.java Server.java; java DocSearchServer 4555
```

http://localhost:4555

http://localhost:4555/search?q=rr74

---

9. Put the change into the remote server
```
scp DocSearchServer.java Server.java cs15lfa22cf@ieng6.ucsd.edu:~/skill-demo1/; ssh cs15lfa22cf@ieng6.ucsd.edu "cd skill-demo1; javac DocSearchServer.java Server.java; java DocSearchServer 4557"
```
http://ieng6-201.ucsd.edu:4557/

http://ieng6-202.ucsd.edu:4557/

http://ieng6-203.ucsd.edu:4557/

---

http://ieng6-201.ucsd.edu:4557/search?q=rr74

http://ieng6-202.ucsd.edu:4557/search?q=rr74

http://ieng6-203.ucsd.edu:4557/search?q=rr74