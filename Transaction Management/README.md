## Transaction Management Interview Questions

#### 1️⃣ How to implement transaction in Spring/Hibernate ?

➡️ When you intregrate your Hibernate with Spring Boot project then you don't need to use Hibernate Transaction Management.

You can use Spring declarative transaction management using `@Transactional` annotation.

#### 2️⃣ What is @Transactional ?

➡️ `@Transactional` is use in method/class level to achive database transaction.

It's allows us to set following conditions for our transaction:

❇️ `Propagation, Isolation, Timeout, Read-Only and Rollback`

#### 3️⃣ How to work @Transactional internally ?

➡️ Spring creates a proxy or manipulates the class byte-code, to manage the creation, commit and rollback of the transaction.

```bash
  createTransactionIfNecessary();
  try {
    addEmployee();
    commitTransactionAfterReturning();
  } catch(Exception e) {
    rollbackTransactionAfterThrowing();
    throw e;
  }
```
#### 4️⃣ Where we can use @Transactional ?

➡️ We can use this annotation on following in the 'lowest to highest priority' order:

**Interface:** By default all the methods will be transactional in the interface.

**Super Class:** By default all the public methods will be transactional in the super class as well as child class.

**Interface Method:** Specific interface method will be transactional.
Super Class Method: Specific super class as well as child class method will be transactional.

**Method:** Any Specific method will be transactional in a class.

🍁 If we have class level & method level, then method level is the highest priority.

#### 5️⃣ 
➡️ 
