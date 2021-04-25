# Entry 4
##### 4/24/2021

## Sources
<p>During this week, I start to try out the code I see before in the video. I successfully set up my firebase with the help of the Video [Getting Started with Firebase on the Web](https://www.youtube.com/watch?v=k1D0_wFlXgo) and the help of other friends on Slack. And so I followed the video [Firebase - Ultimate Beginner’s Guide](https://www.youtube.com/watch?v=9kRgVxULbag) and learned how to use the firebase authentication to let the user login.</p>
<hr>
<p>I am currently at stage 4 of the Engineering Design Process- Plan the most promising solution on search system for my website, I want to let the user choose their school, area, personal interest; then the user can search for each other on the search system by putting in the school name, a subject they favored, or area they are in.</p>

<p>I start to refer to other websites such as google classroom, Duolingo, and Twitter to see the most promising solution, and I realize I just need to ask and store the information when the user first logs in to my website and pulls them out when other users search. For example, when the user first logs in to my website, the website will ask the user what school they are in, what subject they like, and create an object and store all the user information for that account then pull that information out when other users search.</p>

## Knowledge
<hr>
<p>I learned about firebase Authentication this weekend, with this I can allow users to sign in to my website using one or more(maybe in the future) sign-in methods, including email address and password sign-in, and federated identity providers such as Google Sign-in and Facebook Login(maybe in the future).</p>
<p>This is the model I made with Firebase Authentication that allows the user to log in with their Google account: <p>
``` javascript
  function googleLogin(){
      const provider = new firebase.auth.GoogleAuthProvider();
      
      firebase.auth().signInWithPopup(provider)
      
                    .then(result => {
                        const user = result.user;
                        document.write(`Hellow ${user.displayName}`);
                        console.log(user)
                    })
                    .catch(console.log)
  }
```
<p>This bunch of code allows the user to log in with their Google account and print out their userName with the message.</p>
<p>first, I define the provider that I am using, which is the google auth provider</p>

``` javascript
firebase.auth().signInWithPopup(provider)
```
<p>second, reference the firebase off library and call sign in with pop-up, passing at that “provider” as an argument.</p>
<p>since this operation happens asynchronously which will return a promise, and with that promise, we can attach .then to it and use the user as a variable to do something like a document. write print out the Hellow with the user’s name. (all the user information will come from the actual Google account.</p>
``` javascript
.then(result => {
                        const user = result.user;
                        document.write(`Hellow ${user.displayName}`);
                        console.log(user)
                    })
                    .catch(console.log)
  }
```

## Skills
<hr>
<p>The skills I use are How to Google and Communication.</p>
<p>I use the skill Communication, when I face a problem and lose direction on how to set up my firebase base, I ask for help from Slack and my teacher. They help me alot during my learning.</p>
<p>I use the skill How to Google, when I don’t know how to access and use firebase authentication, I search up on google and found some videos that teach beginners like me to use firebase.</p>
[Previous](entry03.md) | [Next](entry05.md)

[Home](../README.md)