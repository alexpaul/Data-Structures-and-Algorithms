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

## 2. Case Study - Print the Elements of a Linked List 

[HackerRank - Print the Elements of a Linked List](https://www.hackerrank.com/challenges/print-the-elements-of-a-linked-list/problem)

#### JavaScript 

```javascript 
// Complete the printLinkedList function below.

/*
 * For your reference:
 *
 * SinglyLinkedListNode {
 *     int data;
 *     SinglyLinkedListNode next;
 * }
 *
 */
function printLinkedList(head) {    
    while(head != null) {
        console.log(head.data);
        head = head.next;  
    }
}
```

After running the code **Congratulations!**

#### Swift

```swift 
// Complete the printLinkedList function below.

/*
 * For your reference:
 *
 * SinglyLinkedListNode {
 *     data: Int
 *     next: SinglyLinkedListNode?
 * }
 *
 */
func printLinkedList(head: SinglyLinkedListNode?) -> Void {
    var head = head 
    while let currentNode = head {
        print(currentNode.data)
        head = currentNode.next
    } 
}
```

After running the code **Compiler error :(**   

[Swift discussion thread](https://www.hackerrank.com/challenges/print-the-elements-of-a-linked-list/forum/comments/457354)


#### Some Quick Takeaways 

* JavaScript has autocomplete support, Swift does not. 
* JavaScript runs tests much faster. 
* Swift encounters way more edge case run issues within the HackerRank compiler. 
