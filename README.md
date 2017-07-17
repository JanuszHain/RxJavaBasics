# RxJavaBasics

RxJava basic examples (some may be not trivial tho) with explanation.
Names of objects don't correspond with real objects (like class name Car, Human, etc).
Objects created are designed to only inform about what's going on, not to show real life examples.
Some examples are designed to be used as template to deal with async solutions.

## What you need to know first

You need to know how Rx works.
The project will tell you differences between methods in RxJava, but will not tell you from scratch how it works.

I don't use libraries other than I need (with one exception: retrolambda).
I don't use fragments.
I don't use MVP structure.

The reason is to make code for everyone, even for people not knowing libraries, fragments or MVP.

As mentioned above you need to know retrolambda also - it is easy one and makes RxJava easier to read and write.
If you don't know retrolambda read it below or search for some tutorial.

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

Retrolambda seems scarry when combained with RxJava, but it is simple mechanism.

Example in Java:

```
interface OnDoSomethingListener{
  void doSomething(String arg1, String arg2);
}
```

Now we can create listener like:

```
OnDoSomethingListener listener = new OnDoSomethingListener(){
    @Override
    public void doSomething(String arg1, String arg2) {
        
    }
}
```

Or using retrolambda easier way:

```
OnDoSomethingListener listener = (arg1, arg2) -> { //this is doSomething(String arg1, String arg2)

}
```

Note that this interface got only one method (so we know which method hides under lambda).
In case of more methods you can't use retrolambda!
