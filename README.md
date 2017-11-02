# enum.js
A simple implementation of a Java-like enum in javascript.

## Example Usages
    let myEnum = Enum.create ("A", "B", "C");
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

## Build Notes
I use Nashorn (jjs) from the Java9 SDK to integrate basic testing into the command line maven build. Similarly, 
the test.html file at the root here runs the test harness on the enum class definition, and spews
the results into the console window.
