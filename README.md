## Purpose

Technical Documentation for ISO Scheduler syntax

## Symbols

Symbols used come from ISO-8601 format
```
 Y - year
 Q - Quarter
 M - month
 W - week
 D - day
 h - hour
 m - minute
 s - second
```
Symbols can be combined for `of` effect
``` 
 DY - Day of Year
 mh - Minute of hour
 MQ - Month of quarter
```

## Operators

```
==  - equal
>   - greater than
>=  - greater than or equal
<   - less than
<=  - less than or equal
><  - not
*:* - step
*-* - range
*,* - list
```


## Examples

**Every Saturday and Sunday**

```
5,6dW
```
**1st minute of every fifth hour every saturday in the month of february on leap years only**
```
!LY 1M 5dW 1:5h 1m
```
**Every month after February**
```
*M M>2
```
**Every other hour of every 4th saturday of every 5th year**
```
1:2h 1:5Y 5dW dW=1:4 
```
