---
title: bootstrapping
date: Nov 1, 2022
---

<img src="../imgs/bootstrap.png" alt="bootstrap" style="height: 300px;"/>

**Readers who understand compiler bootstrapping can jump directly below the split line to see it.**

There is an interesting concept in the process of building compilers called bootstrapping（[Bootstrapping](https://en.wikipedia.org/wiki/Bootstrapping_(compilers)). To wit, suppose I want to create an X language, then I must write a compiler or interpreter for the X language, and if this compiler is written in the X language, then the process of writing the X language compiler in the X language is a bootstrap. Of course, the reality is not so simple, because when the compiler is written, the X language does not exist, so it is not possible to write a compiler in the X language, which is caught in a predicament of the chicken or the egg first. The common practice is:

* complete a part of the compiler for the X language in another language (e.g. C), which does not need to be too complex, but only needs to be able to compile a core subset of the X language.
* write the X language compiler in X. The problem we faced before was that there was no compiler that could turn the X language source code into binary code, but since at this point we have a compiler written in C, we can get the binary code of the compiler written in X.
* Throw in the C implementation of the compiler, with the X language implementation of the compiler to continue to expand the iteration of the next version of the compiler until complete.

For uncommon practices see [link](https://www.zhihu.com/question/28513473/answer/76068366)。

---

Well the science is over, these are actually not what I want to say, what I want to say is that I suddenly realized today that the concept of self-raising is important in life.

For example, the process of learning English should be the process of lifting, but how many people have been learning English for more than ten years and still haven't started lifting? The bootstrapping process of learning English should be such that at first we use Chinese to learn English, and then when we have learned a core subset of English, we should use English to interpret English, and a simple way to do this is to use an English-English dictionary. Another example is when you go abroad and talk to someone, when the other person says a word you don't understand, you shouldn't take out your cell phone and ask them to spell out the word letter by letter and then look up the Chinese meaning of the word on your cell phone, the correct way to do it would be to ask them to explain the word using other words in English.

Thinking about it differently, C represents a comfort zone, while X represents new territory. The process of bootstrapping may be a bit more painful, but it will also allow one to grow faster.

(The End)