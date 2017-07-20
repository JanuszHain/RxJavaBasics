# RxJavaBasics

RxJava basic examples (some may be not trivial though) with explanations.
Names of objects don't correspond with real life objects (like a class named Car, Human, etc).
Objects created are designed only to inform about what's going on, not to show real life examples.
Some examples are designed to be used as a template to deal with async solutions.

## What you need to know first

You need to know how Rx works.
The project will tell you differences between methods in RxJava, but will not tell you from scratch how it works.

I don't use libraries other than those I need (with one exception: retrolambda).
I don't use fragments.
I don't use MVP structure.

The reason is to make code for everyone, even for people not acquainted with libraries, fragments or MVP.

As mentioned above you need to know retrolambda as well - it is an easy one and makes RxJava easier to read and write.
If you don't know retrolambda, read up on it below or search for some tutorials.

## Getting Started

TODO

### Prerequisites

TODO

## License

-------

    Copyright 2017 Janusz Hain

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

       http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.

## Retrolambda

Retrolambda seems scary when combined with RxJava, but it is a simple mechanism.

Example in Java:

```
interface OnDoSomethingListener{
  void doSomething(String arg1, String arg2);
}
```

Now we can create listener like so:

```
OnDoSomethingListener listener = new OnDoSomethingListener(){
    @Override
    public void doSomething(String arg1, String arg2) {
        
    }
}
```

Or using retrolambda the easier way:

```
OnDoSomethingListener listener = (arg1, arg2) -> { //this is doSomething(String arg1, String arg2)

}
```

Note that this interface has only one method (so we know which method hides under lambda).
In case of more methods you can't use retrolambda!
