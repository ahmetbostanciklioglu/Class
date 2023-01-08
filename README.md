# Class



**Basic Class:**
```
class Class {
    var property1: String
    var property2: String
    
    init(property12: String, property22: String) {
        self.property1 = property12
        self.property2 = property22
    }
}

var classObject = Class(property12: "Ahmet", property22: "Alex")
classObject.property1
classObject.property2
```


**Empty Class Crating:**
```
class EmptyClass {
}
var emptyClassObject = EmptyClass()
```


**Class Example:**
```
class Class2 {
    var property1 = 0
    var property2 = "Ahmet"
    var property3 = "Alex"
    init(property1: Int) {
        self.property1 = property1
    }
}
let class2Object = Class2(property1: 12)
```

**Class Inheritance:**
```
class SuperClass {
    var property: Int = 1
    var property2: Int = 3
    init(property: Int, property2 : Int) {
        self.property  = property
        self.property2 = property2
    }
    
    func overridingFunc() -> String{
        return "Override func"
    }
}
let superClassObject = SuperClass(property: 2, property2: 5)


class ChildClass : SuperClass {
    //MARK: property override
    override init(property: Int, property2: Int) {
        super.init(property: property, property2: property2)
    }
    
    //MARK: method override
    override func overridingFunc() -> String {
        return "method of child class"
    }
}
let childClassObject = ChildClass(property: 8, property2: 8)
childClassObject.overridingFunc()
```


**Final Class:**
```
final class FinalClass {
    var property1: String
    var property2: String
    
    init(property1: String, property2: String) {
        self.property1 = property1
        self.property2 = property2
    }
}
```

**Class of property copying:**
```
class CopyingObject {
    var property = "Ahmet"
}

var copyingObject1 = CopyingObject()
print(copyingObject1.property)

var copyingObject2 = copyingObject1
copyingObject2.property = "Alex"
print(copyingObject1.property)
```


**Class Deinitializers:**
```
class Deinitializers {
    var property = "Ahmet"
    init() {
        print("\(property) - 1")
    }
    
    deinit {
        print("\(property) - 2")
    }
}

for _ in 4...5 {
    let indez = Deinitializers()
}
```

**Mutable of class:**
```
class mutableClass {
    var property:  String = "Ahmet"
}

let constantClassObject = mutableClass()
constantClassObject.property = "Alex"
print(constantClassObject.property)
```

**Mutable struct:**
```
struct mutableStruct {
    var property = "Alli"
    mutating func mutableFunc(property: String) {
        self.property = property
    }
}
var constantStructObject = mutableStruct()
constantStructObject.mutableFunc(property: "Alex")
```

