<h3>Why we need any framework?</h3>
We can simply create any kind of static (once loaded  ntng changes) websites using html, css, js
so why do we need it . Bolo bolo bolo 
React solves for issues of dynamic sites.
Know that react too converts code into html, css and js under the hood.

To get more about react try to get 2 stuff of react
<br>
<strong>(Interview question)</strong> <br>
<b>1) state </b>-> In React, state is a built-in object used to store and manage a component's dynamic data.
It allows components to create and maintain their own data, making the UI responsive to user interactions.
<b>2) component</b> -> In react dividing the repeating section of code into single function and then according to the value we
re render it

Return, we cannot return multiple things in react
re-rendering -> A state variable that is being used inside a component chnages, then parent componenet re-render triggers all children re-rendering

Knock knock -> 
1) In react rendering either you create a separate component to improve performance
2) use (memo) -> skips re-rendering if dom is not manipulated.
Performance is improved to a great extent

Got to know more about
1) Why react should return as a single parent with multiple child instead of multiple parent with multiple child
2) Using memo for rendering improves the performance as well as better optimization(lots i=of heavy terms but good from interview perspective)
3) Key -> should always use when using map or filter or any other function that
renders multiple stuffs
4) Then wrapper component in which we use child component

Two jargons before we start.
1) Side effect -> affecting other components
2) Hooks ->

UseEffect()
We do not want rendering should go always,
instead rendering be done once in case of some special cases.
Also it has dependency array and useeffect is updated or rendered when this dependency changes.
It can take multiple values as it is known as dependency array.

Got to know more about usecallback and the most important stuff
1) prop drilling
2) never use prop drilling get to know about context api and then learn stuff like redux.
Now most of my reacts theory is done . Now its time to visit github react project understand how the code is wriiteen allong side
if possible work on some open source project. Best thing go for projects which offer bounties.
It motivate you if you cannot make it , remember you created a industry level project atleast
which differentiate you from the rest of the people


<h3>1) Why react should return as a single parent with multiple child instead of multiple parent with multiple child</h3>
<p>React mein humesha ek hi parent element return karna padta hai kyunki React ka rule hai ki har component sirf ek root element return kare. Agar aap multiple elements ko bina kisi wrapper ke return karoge, toh React error dega.
Kyun sirf ek parent?
1) React ka virtual DOM ek hi root node se kaam karta hai — usse pata hota hai ki kaha se comparison shuru karna hai.
2) Agar multiple elements honge bina kisi wrapper ke, toh structure ambiguous ho jata hai.
3) Performance aur consistency ke liye bhi ye zaroori hai
</p>
<h3>React reconciliation ek process hai jisme React old virtual DOM aur new virtual DOM ko compare karta hai aur decide karta hai ki actual DOM mein kya changes karne hain — taaki performance fast rahe aur unnecessary updates na ho.</h3>
<p>
Jab bhi aap React component ko update karte ho (jaise state ya props badalte ho), React:<br>
1) Naya virtual DOM banata hai (jo naye data ke hisaab se hai).<br>
2) Fir old virtual DOM se compare karta hai (diffing algorithm use karke).<br>
3) Jo cheezein badli hain sirf unhi ko real DOM mein update karta hai — ye hi process reconciliation kehlata hai<br></p>
<h4>React fragments</h4>
