## Automate-Answer-Evalution-System
● A database is created at first along with a student table. (employee.db)

```sql
import sqlite3  
  
con = sqlite3.connect("employee.db")  
print("Database opened successfully")  
  
con.execute("create table Employees (id INTEGER PRIMARY KEY AUTOINCREMENT, name TEXT NOT NULL, roll TEXT UNIQUE NOT NULL, email TEXT NOT NULL, marks_short TEXT NOT NULL, marks_des TEXT NOT NULL)")  
  
print("Table created successfully")  
  
con.close()
```

● An interface is built up using python flask to accept answers from students.

● There are two types of questions namely- Short type and Descriptive type.

● For evaluating Short questions we have taken 3 parameters into consideration. They are

keyword matching,
grammar checking (using API)
```javascript
def GrammerChecker(answer):
    req = requests.get("https://api.textgears.com/check.php?text=" + answer + "&key=JmcxHCCPZ7jfXLF6")
    no_of_errors = len(req.json()['errors'])
    #print(no_of_errors)
    if no_of_errors > 5 :
        g = 0
    else:
        g = 1
    return g
```

synonym checking(You need to download 'GoogleNews-vectors-negative300.bin' from https://s3.amazonaws.com/dl4j-distribution/GoogleNews-vectors-negative300.bin.gz).

● For evaluating Descriptive questions we have taken 1 more parameter i.e length

checking. Suppose for writing an essay if the given word limit is 400 words and a student

has written everything relevant but the essay has ended within 300 words, then marks

will be deducted considering the word limit.

● After evaluation, the student will not be able to see his/her marks but the marks will be

stored in the database.

● Total marks and other relevant information will be accessed by the institution/admin end.

## Demo

[![Watch the video](Screenshot/Screenshot%20(1005).png)](https://youtu.be/vt5fpE0bzSY)
