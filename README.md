# ReScript FAQ
This is a simple ReScript FAQ consisting of questions, answers and snippets. When I first migrated to ReScript, I posted a number of questions to the [ReScript forums](https://forum.rescript-lang.com/) to figure things out. Initially having issues with bindings, I moved past it rather quickly. There are still things that might not be obvious to newcomers. Some of these quirks may be encountered rather early on, and to ensure a smooth transition into the ReScript way of doing things, I put together this FAQ.

### 1. How can I use environment variables in ReScript?

Method 1
```rescript
let secret = Node.Process.process["env"]->Js.Dict.get("secret")
```

Method 2
```rescript
external secret: option<string> = "process.env.MONGO_URI"
```
