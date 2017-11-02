# enum.js
A simple implementation of a Java-like enum in javascript.

## Example Usages
    let myEnum = Enum.create (["A", "B", "C"]);
    let anObject = {};
    anObject[myEnum.A] = myEnum.A.value;
    
    for (let e in myEnum) {
        console.log ("myEnum." + e + " has value " + e.value);
    }
    
    let e = myEnum.B;
    let reverseLookup = myEnum.values[e.value];
    if (reverseLookup === e) {
        console.log ("check");
    }
    
    switch (e) {
        case myEnum.A:
            break;
        case myEnum.B:
            break;
        case myEnum.C:
            break;
    }
