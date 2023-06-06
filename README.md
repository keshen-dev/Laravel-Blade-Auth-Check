# Laravel Blade Auth Check

This repository provides examples and guidance on how to check if a user is authenticated (logged in) within a Laravel Blade template. It demonstrates using both the Auth facade and the auth helper function.

```
<!DOCTYPE html>
<html>
<head>
    <title>Laravel Blade Authentication Check</title>
</head>
<body>
    @if (Auth::check())
        <h1>Welcome, {{ Auth::user()->name }}!</h1>
        <p>You are logged in. Here's your exclusive content.</p>
        <!-- You can put your content for logged-in users here. -->
    @else
        <h1>Welcome, Guest!</h1>
        <p>You are not logged in. Please <a href="/login">log in</a> to see exclusive content.</p>
        <!-- You can put your content for guests here. -->
    @endif
</body>
</html>
```

In this example, Auth::check() is used to determine if the user is logged in. If they are, it displays a welcome message along with their name (retrieved using Auth::user()->name) and some exclusive content. If they're not logged in, it instead displays a welcome message for guests and a prompt to log in.

Remember to replace "/login" with the actual route to your login page.
