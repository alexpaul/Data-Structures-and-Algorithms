# HackerRank 


## 1. Printing to the conosle

```swift 
let stdout = ProcessInfo.processInfo.environment["OUTPUT_PATH"]!
FileManager.default.createFile(atPath: stdout, contents: nil, attributes: nil)
let fileHandle = FileHandle(forWritingAtPath: stdout)!

// Complete the Challenge
func challenge(arr: [[Int]]) -> Int {
    // nothing printed to the console
    print("Hello") 

    // will print to the console using "fileHandle"
    fileHandle.write("HackerRank Challenge\n".data(using: .utf8)!)
    
    return 0
}
```
