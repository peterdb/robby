Robby
=====

Robby is a Swing application automation solution, heavily inspired by Geb.

It can be used as a functional/acceptance testing solution.

Usage
=====

Here is what a simple Robby script looks like...

```groovy
import robby.Robby

Robby.drive {
    launch "com.acme.FooBarApp"

    assert $("statusBar").text() == "Please login"

    $("loginDialog").with {
        username = "Road"
        password = "Runner"
        $("loginButton").click()
    }
    
    assert $("statusBar").text() == "Login successful"
}
```

This is what is known as the scripting style.
