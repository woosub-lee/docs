### This document

This document covers both `Codable` and `Async`, the two primary concepts in Vapor 3. Understanding these 2 concepts is essential, even for existing Vapor 1 and 2 users.

# Codable

Codable is any type that's both `Encodable` and `Decodable`. Encodable types can be serialized to a format, and Decodable types can be deserialized from a format.

If you only want your type to be serializable to another type, then you conform to `Encodable`. This will allow serializing this type to other formats such as JSON, XML, MySQL rows, MongoDB/BSON and more. But not backwards.

If you want to be able to construct your type from the raw data, you can conform your type to `Decodable`. This will allow converting serialized data to your model (the reverse of `Encodable`), allowing JSON, XML, MySQL and MongoDB data to construct your model. This will not allow serialization.

If you want both serialization and deserialization, you can conform to `Codable`.

For the best experience you should conform one of the above protocols in the *definition* of your `struct` or `class`. This way the compiler can infer the protocol requirements automatically. Conforming to these protocols in an extension will require you to manually implement the protocol requirements.

```swift
struct User: Codable {
  var username: String
  var age: Int
}
```

With this addition, the above struct can now be (de-)serialized between JSON, XML, MongoDB BSON, MySQL and more!

# Async

Asynchronous is event driven programming. Asynchronous shines best in a real world scenario and is much more scalable and performant than synchronous code. To support Asynchronous code we introduce [Futures](../async/promise-future-introduction.md) in Vapor 3.

We recommend reading the basics when you're interacting with [REST APIs](../http/client.md) and [databases](databases.md).
