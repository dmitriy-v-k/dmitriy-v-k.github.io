---
layout: post
title: "My first post"
date: 2017-04-28
no-continue: true
---

Hi All! It's my first post in my new blog. 
After I've read some interesting ideas about OOP I've created my first repository on github and 
called [CSimplest](https://github.com/dmitriy-v-k/dmitriy-v-k.github.io "Simplest C# trueOOP Framework"). It's "true-OOP" framework via C#.
In blog's pages I'll try write my things about OOP and my framework. 

Small exsample:
```var paramsRq = new RqWithResponse(
    new RqIIS(Request),
    new RsWithHeaders(
        new RsParametric((parameters) => 
            new RsJson(
                new RsIIS(Response),
                new Users().FindById(parameters["name"])
            ),
            new RqWithParamsInPath(
                new RqIIS(Request),
                new Regex(@"~/params/(?<name>\w+)/(?<secondName>\w+)")
            ).Parameters()
        ),
        new List<KeyValuePair<string, string>>()
        {
            new KeyValuePair<string, string>("test","test")
        }
    )
);```

I hope you will be interested!
