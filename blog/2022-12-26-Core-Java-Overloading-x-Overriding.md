---
title : Java - Overloading x Overriding
path: /developerJava
date: 2022-12-26
summary: Let's learn the difference - overloading x overriding.
tags: ['design', 'backend']
---

![background](./images/blog_bg_4.jpg)

Overloading vs Overriding

### Difference between method overloading and method overriding in java?

| Method Overloading | Method Overriding |
| ------------------ | ----------------- |
| 1. Method Overloading occurs with in the same class.| 1. Method Overriding occurs between two classes superclass and subclass|
|2. Since it involves with only one class inheritance is not involved.| 1. Since method overriding occurs between superclass and subclass inheritance is involved.|
|3. In overloading return type need not be the same. | 3. In overriding return type must be same.|
|4. Parameters must be different when we do overloading.|4. Parameters must be same.|
|5. Static polymorphism can be achieved using method overloading.| 5. Dynamic polymorphism can be achieved using method overriding.|
|6. In overloading one method can't hide the another.| 6. In overriding subclass method hides that of the superclass method.|

### Overloading example:

```Java
class Dog{

    // Same Method Name. Different Parameter.
    public void bark(){
        System.out.println("woof");
    }
    
    // overloading method
    public void bark(int num){
        for(int i = 0; i < num; i++){
            System.out.println("woof");
        }
    }

}
```

### Overriding example:
```Java
class Dog{
    // Same Method Name, Same Parameter.
    public void bark(){
        System.out.println("woof");
    }
}

class Hound extends Dog{
    public void sniff(){
        System.out.println("sniff");
    }

    // Same Method Name, Same Parameter.
    @Override
    public void bark(){
        System.out.println("bowl");
    }
}
```