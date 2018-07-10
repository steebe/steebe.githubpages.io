---
layout: post
title:  "JavaScript Noteables"
date:   2018-07-05 08:00:00 -0400
categories: jekyll update
---

# Concepts

## Short-circuit Evaluation
In any line that evaluates multiple conditions, JS does its best to short-
circuit what needs to be evaluated.
```JavaScript
// LHS is evaluated and returned (RHS ignored)
console.log("me" || "you");

// LHS is evaluated as true BEFORE RHS is evaluated and returned
console.log("you" || "me");

// 1st condition evaluated as false yields third condition evaluation & return
console.log(0 ? ("me || me") : ("you" && "you"))
```

## Automatic Type Conversion (Via Type Coercion)
JS does its best to allow any types to be compared and returned. Its interpreter
performs _type coercion_ on the values it is "confused" about.

```JavaScript
console.log(8 * null);  // converts null to 0, returns 0
console.log("5" - 1);   // converts "5" to 5, returns 4
console.log("5" + 1);   // converts 1 to "1", returns "51"
console.log("five" * 2);// cannot perform conversion on "five", returns NaN
```

Note that the type coercion being performed is heavily dependent on the
_operation_; The values being evaluated and converted are secondary in
comparison.
