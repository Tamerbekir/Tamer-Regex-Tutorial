# Regex Tutorial: Email Validation

## Introduction

This tutorial is a complete guide to what a Regex is, how it is used, and what it can be used for. While there are multiple Regex's that one can use, this tutorial will cover the *Email Validation regex*. We will go through a step by step by explanation to better understand these unique patterns and how they can be an essential tool in a developers kit.


## Summary
The regex pattern we go over and discuss in this tutorial is the *Email Validation*
which looks like this:

/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/

I know the jumble of numbers, symbols and words can seem a bit intimidating and confusing, but by the end of this tutorial, you will have a better understanding of what it all means.

First and foremost, this unique pattern ensures that the string matches the standard  of an email address. For example, mikewalsh@email.com. This is what out regex pattern is looking for, and if the string matches this pattern, it is valid. If not, it is invalid.

For those who are new the Javascript, a string is a series of characters when referring to code. 

So, let us begin to break down the regex little by little so we can understand how it works!


# Table of Contents
- [Delimiters](#Delimiters)
- [The Email  dName](#TheEmailName)
- [Literal Character](#LiteralCharacter)
- [Domain Name](#DomainName)
- [Top-Level Domain](#Top-LevelDomain)
- [About the Author](#AbouttheAuthor)

# Delimiters
^ and $
The ^ and $ are *anchors* in the regex pattern that are placed at the start and end of a string, or otherwise known as delimiters. The delimiters are giving the user an indication as to what this regex is looking for. This will make sure that the entire string must abide to the pattern in the the Email Validation regex and that no characters which are not supposed to be there end up either *before* or *after* the end of the email address. Think about the delimiters like a set of rules, and in order for the regex to valid the email address, it must abide by these rules.

# The Email Name

`([a-z0-9_.-]+)`

Now that we went over the delimiters, let us take a look at the local part of the email. Everything we see here inside the parentheses must match the local part of the email address, which is everything before the "@" symbol. So, let us take a closer look.

Let us start off by taking a look *inside* the [brackets].

First we se lowercase letters (a-z)- this means the regex will look for all lowercase letters `a` through `z` in the email address. The local part of the email address *must* have a lowercase letter to meet the regex criteria.

Secondly, we digits `(0-9)`- this means the regex will look for all numbers `0` through `9` in the email address. The local part of the email address *must* have a number to meet the regex criteria.

Third, we see underscores `( _ )`, periods `( . )`, and hyphens `( - )`. The local part of the email address *must* have a one of these symbols letter.

Now, that we established what is inside the parentheses and that the local part of the email, we can now see a plus sign `( + ) `outside of the bracket. This means the local part of the email address *must* one or more of these characters must be present.

For example: the email address *mike.walsh123@mail.com* will work as the local part because it has a lowercase letter, a number, and a period. It meets the criteria by having one or more of these characters.

What email wouldn't work? The email *mike..walsh123@mail.com* would not work because our pattern does not allow consecutive dots `( . )`.

So, in summary, everything within the brackets must be present in the local part of the email address and in any order the uses wishes to have their local part of their email. The plus `( + )` sign outside of the brackets means that one or more of these characters must be present.

# Literal Character

The "@" symbol

The "@" symbol is what is called the *literal character* in the regex. It must appear exactly once in an email address, separating the local part and the domain name (@gmail.com, @hotmail.com, etc).


# Domain Name

`([\da-z.-]+)`

This portion of the regex captures the domain name of the email (@gmail.com, @hotmail.com, etc). It allows `0` through `9` but in this case it is written `*/d*`. It also allows lowercase letters ( a-z ), a period `( . )`, a hyphen `( - )`. Like the local part we discussed earlier, the plus sign `( + )` indicates that one or more of these characters are required in order for the Email Validation to work.

For example: the email address *mike.walsh@123email.com* will work as the local part because it has a lowercase letter, `a-z`, a number that is `0-9,` and a period. It meets the criteria by having one or more of these characters.

What email wouldn't work? The email *mike.walsh@123_mail.com* would not work because our pattern does not allow underscores `( _ )`.



# Top-Level Domain

`([a-z.]{2,6})`

The last part of the regex explains the top-level domain name- or, in other words the ".com" portion of an email address. 

First, let us look inside the brackets again. We will see what we saw before- letters `a` through `z`, which means the end of the domain name must include these letters for it to match. Then, also found inside the brackets is a period `( . )`, which means this also *must* be included in the end of the domain name.

Second, we take a look inside the curly braces and we see numbers '2' and '6', which means the top-level domain (or end of the email) *must* be between `2-6`characters long. If the top-level domain is less than `2` characters long or greater than `6` characters, it will not match the email validation regex.

So, in summary, it only allows lowercase letters `(a-z)` and periods `( . )`, as well as an end domain consisting between `2-6` characters long which are necessary for email validation to work.

For example: the email address *mike.walsh@mai.com* will work as the local part because it has a lowercase letter, `a-z`, a number that is `0-9`, and a period and it has an end domain of 3 characters which meets the criteria.

 What email wouldn't work? The email *mike.walsh@T.com* would not work because the end domain only consist of 1 character. 

# About the Author
My name is Tamer Bekir and I am a junior software developer! I began my journey into software development in 2023 and have been learning and improving my skills ever since then. While I am always growing and learning, I have so far familiarized and worked with back-end and front-end coding which has been a very fun and challenging experience. 

This guide is for all developers, whether senior or junior. By following this guide, you will be able to create a regex that will validate an email address. I hope you found this article helpful and I hope you are able to use this regex in your own projects. 

I am happy I am now able to guide others in the same path I have taken and I hope you enjoy this article as much as I did writing it. 

Feel feel to checkout my <a href="https://github.com/Tamerbekir"> GitHub</a>.