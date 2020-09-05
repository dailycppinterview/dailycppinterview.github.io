## TODO

Email
	Nice header
	Nice footer
Backend
	Figure out what's the problem with mails
	Unsubsribe
	Monthly subscribtion ending
Webpage
	DONE Update main message
	Done Update title
	Get a flavcion / icon
	Add T&C
	Add Privacy page
	Do SEO
	DONE CrossReference from sandordargo.com
	DONE Crossreference from dev.to
LinkediN
Twitter
Face share


- Signup forms 
- Write about what I provide
- Show a question solution pair
- Write about myself

----
<!-- Remove buttons -->
<!-- Change columns -->
<!-- Replace pictures -->
<!-- Copyright -->
<!-- Replace footer -->
<!-- Remove header bar -->
Create admin page
<!-- Amazon registration for emails -->
<!-- Amazon for hosting the db -->
	mail
	<!-- problems -->
	<!-- users -->
		<!-- uid -->
		<!-- email -->
		<!-- purchased -->
		<!-- createdd -->
		<!-- pid -->
		<!-- lastSent (date) -->
		<!-- unsubscrive -->
		<!-- deactivated -->
Create admin page
<!-- Register website -->
<!-- Stripe integration -->
Launch
	- Twitter
	- Facebook
	- Linkedin
	- Dev.to
	- producthunt
	- some other pages...

stripe -> amazon
email -> my name
email hello
email signature
email format


Start creating questions immediately
How to accept payment and get information
Create page on github
<!-- Create mailing list -->
<!-- DB and email send online -->
Buy domain
Launch
	- Twitter
	- Facebook
	- Linkedin
	- Dev.to
	- producthunt
	- some other pages...


How to get the subscribers on a daily basis



dailyinterviewpro.com

admin page

title
desc => everyone 
sol => pro

text file =>

text to highlighted HTML: hilite.me

no js, because of email clients

domain: namecheap

host: ibm cloud

mysql
mail
problem: pid, text

users:
uid, email, purchased, created, pid, lastSent, unsubscribe, deactivated


landing page: kajabi.com

sendinblue for sending emails, or to store email?

zapier for automating from kajabi to sendinblue

Amazon ses to send the email out





Create website
- some data about the course
- some data about me
- sign up form

Once a day zapier sends the mails to ...

Server hosting a mail, db
crontab jobs





Sign up for free your daily C++ quiz. Join and get a daily question.

How does it work?

You sign up with your e-mail address and you get a question in your mailbox every day. A question that was asked in interviews. You try to answer the question or solve the problem. It'll stretch your skills, you will learn and grow.
Those who sign up for the PRO version will also receive detailed answers and when applicable with ready-to-run code, complexity analysis.



Daily coding interview practice. It's free.
Join Ex-Google & Ex-Facebook staff software engineer TechLead with daily interview programming problems.

Here's how it works:

Sign up to receive a real interview question in your mailbox daily.
Try to solve the problem!  It's fun and sharpens your interviewing skills.
(PRO) Receive solutions with complete analysis, time-space complexity, and runnable code.


===
"TechLead" is Patrick Shyu - ex-Google/ex-Facebook Tech Lead, multi-millionaire app entrepreneur, digital nomad, Silicon Valley native, and senior software engineer.  He's held roles in full-stack web development and mobile engineering. He has conducted over 100 interviews at Google, and has worked in the tech industry for over a decade from startups to Fortune 500 companies.


Sandor is a senior software engineer in the world's leafing reservation platform provider, and besides a writer, confernce speaker. He's been a C++ engineer since 2013. Sandor has been working on C++ teams providing company-wide used APIs just as well reservation systems that most probably you already used during travelling. His passion on knowledge sharing also led him to work on the interview questions they ask from new hires.

===

What is the difference between function overloading and function overriding?

Function overriding is a term related to polymorphism. If you declare a virtual function in a base class with a certain implementation, in a derived class you can override it's behaviour in case you uses the very same signature. In case, the virtual keyword is missing in the base class, it's still possible to create a function with the same signature in the derived class, but it doesn't override it. Since C++11 there is also the override specifier which helps you to make sure that you don't mistakenly failed to override a base class function. You can find [more details here](http://sandordargo.com/blog/2018/07/05/cpp-override).

Function overriding enables you to provide specific implementation of the function that is already defined in its base class.

On the other hand, overloading has nothing to with polymorphism. When you have two functions with the same name, some return type, but different number or types of parameters, or qualifiers.

Here is an example for overloading based on parameters

```cpp
void myFunction(int a);
void myFunction(double a);
void myFunction(int a, int b);
```

And here is another example based on qualifiers:

```cpp
class MyClass {
public:
	void doSomething() const;
	void doSomething();
};
```
Or actually, it possible to overload your function based on whether their hosting objects are rvalue of lvalue references. 

```cpp
class MyClass {
public:
  // ...
  void doSomething() &; // used when *this is a lvalue
  void doSomething() &&; // used when *this is a rvalue
};
```

You can learn more about this [here](http://sandordargo.com/blog/2018/11/25/override-r-and-l0-values).


# Landing Page Jekyll theme

Jekyll theme based on [landing-page bootstrap theme ](http://startbootstrap.com/templates/landing-page/)

## How to use
 - Place a image in `/img/services/`
 - Create posts to display your services. Use the follow as an example:

```txt
---
layout: default
img: ipad.png
category: Services
title: The service title
---
The description of this service
```

## Demo
View this jekyll theme in action [here](https://swcool.github.io/landing-page-theme)

## Screenshot
![screenshot](https://raw.githubusercontent.com/swcool/landing-page-theme/master/img/screenshot.png)

===

For more Jekyll details, read [documentation](http://jekyllrb.com/).
This Jekyll theme used [Freelancer Jekyll theme](https://github.com/jeromelachaud/freelancer-theme/) as reference.

## License
The contents of this repository are licensed under the [Apache
2.0](http://www.apache.org/licenses/LICENSE-2.0.html).

## Version
1.0.1
