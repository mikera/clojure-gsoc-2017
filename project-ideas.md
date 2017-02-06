# Project ideas 2017

## Information for students

These ideas were contributed by our developers and users.
They are sometimes vague or incomplete.
If you wish to submit a proposal based on these ideas, you may wish to contact the developers and find out more about the particular suggestion you are considering.

Being accepted as a Google Summer of Code student is quite competitive.
Accepted students typically have thoroughly researched the technologies of their proposed project and have been in frequent contact with potential mentors.
Simply copying and pasting an idea from here will not work.
Likewise, creating a completely new idea without first consulting potential mentors is unlikely to work out.

If there is no specific contact given you can ask questions on the [Clojure mailing list](http://groups.google.com/group/clojure) or the [Clojurians slack](http://clojurians.net).

## Adding a proposal

The preferred way to add a proposal is to submit a pull request with your idea added to this document.
Please add your idea to one of the sections below (create a new section if you like) using the following template:

```markdown
#### Project Title

**Brief explanation:**
A few sentences describing the problem to solve.

**Expected results:**
What should the student be able to produce by the end of the project.
This includes tests and documentation.

**Knowledge prerequisite:**
If a student needs to know something to be able to complete the project, be sure to list it.

**Mentor:**
Add your name if you are a developer who is willing to be a primary or secondary mentor for the project.
```

If you cannot submit the project as a pull request, please submit it to:

* The [#gsoc](https://clojurians.slack.com/messages/gsoc/) channel in the [Clojurians slack](http://clojurians.net)
* The [Clojure mailing list](http://groups.google.com/group/clojure) using the subject prefix `[GSoC Idea]`.


## Project ideas

### Clojure

### Clojure Numerics

#### Clojure OpenCL

**Brief explanation:**
We have a growing ecosystem of numerical code in Clojure, based around core.matrix (which will be an oficial Clojure Contrib library in the near future). However we don't yet have a well-integrated library for array computing on the GPU, which is an important capability for high performance numerical computing and deep learning.

The goal of this project is to develop a fully working, optimised core.matrix implementation on the GPU using OpenCL (which will provide compatibility with most modern GPUs). 

There is an initial experimental project (https://github.com/mikera/vectorz-opencl) which could serve as a framework to be developed into a full implementation, although other options could also be considered.

**Expected results:**
The end result should be a fully compatible core.matrix implementation running on the GPU with OpenCL, with optimisations for all of the most common numerical computing operations. This should include at a minimum:

- Matrix/vector/array muliplications
- Elementwise operations (add, muliply, negate, log etc.)
- Functional operations (map, reduce etc.)

As a stretch goal, it could be possible to compile some subsets of Clojure expressions into efficient GPU code.

**Knowledge prerequisite:**
Key knowledge required:

- Clojure
- Java
- Familiarity with array-based numerical programming (e.g. Numpy)
- Some GPU computing experience (needed to write OpenCL kernels)

**Mentor:**
Mike Anderson

### ClojureScript

### Typed Clojure

### Tooling

#### Add cool features to KLIPSE

**Brief explanation:**
[KLIPSE](https://github.com/viebel/klipse) is a clojure[script] web repl and also a javascript tag that transforms static code snippets of an html page into live and interactive snippets. It uses self-host clojurescript for evaluating clojure code inside the browser.

There a plenty of cool features in KLIPSE backlog. Here are a couple of ideas: code completion, source code search, full integration with github gist, literate programming and more...

If you have other ideas, you are welcome to suggest them.

**Expected results:**
Implement several features.
Write blog posts demonstrating the features you have added.

**Knowledge prerequisite:**
Familiarity with clojure.

**Mentor:**
Yehonathan Sharvit as a primary mentor - email: viebel@gmail.com

#### Self-host clojurescript migration

**Brief explanation:**
Make popular clojure[script] libraries self-host compatible.

Self-host clojurescript is the compilation of clojurescript code inside clojurescript. It was introduced in [July 2015](http://swannodette.github.io/2015/07/29/clojurescript-17) but yet not all the popular clojure[script] libraries are self-host compatible. 

When a library is self-host compatible it can be used inside a clojurescipt repl like [planck](https://github.com/mfikes/planck), [lumo](https://github.com/anmonteiro/lumo), [klipse](https://github.com/viebel/klipse) and many more...

Here are some clojure[script] libraries that are not yet self-host compatible: [core.matrix](https://github.com/mikera/core.matrix/), [core.logic](https://github.com/clojure/core.logic), [sablono](https://github.com/r0man/sablono), [rum](https://github.com/tonsky/rum).

**Expected results:**
A pull-request to the github repo of one or more clojure[script] lib that has been made self-host compatible.
A blog post with interactive code snippets demonstrating the usage of the library - using [the klipse plugin](https://github.com/viebel/klipse) like this blog posts about [core.match](http://blog.klipse.tech/clojure/2016/10/25/core-match.html), [clojure.spec](http://blog.klipse.tech/clojure/2016/05/30/spec.html) and [om.next](http://read.klipse.tech/om-next-interactive-tutorial/).

**Knowledge prerequisite:**
Familiarity with clojure macros.

**Mentor:**
Yehonathan Sharvit as a primary mentor - email: viebel@gmail.com.
