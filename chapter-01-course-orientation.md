# Chapter 01: Course Orientation and Learning Foundations

**Course:** Foundations of Computer Science & Artificial Intelligence\
**Module:** Algorithms, Data Structures, and Connectionist AI\
**Audience:** First-year university learners with basic computer
literacy\
**Chapter status:** Drafted - review reported, but a concrete review outcome was not supplied in the available records

## Chapter overview

This chapter introduces the three main strands of the course:
algorithms, data structures, and connectionist artificial intelligence
(AI). It explains what each strand studies, how the strands connect, and
how learners will approach the material throughout the course.

The chapter uses familiar examples---a library catalogue, campus route
planning, and image classification---to show how these ideas appear in
practical situations. It also introduces essential vocabulary and
explains how pseudocode and step-by-step tracing can help learners
understand computational processes.

## Learning objectives

After studying this chapter, you should be able to:

-   Identify the three strands of the course and describe their
    purposes.
-   Explain how data structures, algorithms, and AI models can work
    together.
-   Describe the main skills the course aims to develop.
-   Define input, output, state, operation, data, model, prediction, and
    training.
-   Explain what pseudocode is and why it is useful.
-   Describe the predict--trace--check learning method.

## 1. The three strands of the course

### 1.1 Algorithms

An **algorithm** is a precise sequence of steps for solving a problem or
completing a task. Algorithms specify what should happen and in what
order. They can be described in ordinary language, pseudocode, or a
programming language.

For example, finding a particular book in a catalogue requires a method
for deciding which entries to inspect and when to stop. Different
algorithms can solve the same problem, but they may differ in the
conditions they require and the amount of work they perform.

### 1.2 Data structures

A **data structure** is a way of organizing data so that it can be
stored, accessed, updated, or processed. Different structures support
different operations and use cases.

Examples include:

-   **Arrays:** store elements in an ordered sequence that can be
    accessed by index.
-   **Linked lists:** connect elements through references or links.
-   **Stacks:** support a last-in, first-out pattern.
-   **Queues:** support a first-in, first-out pattern.
-   **Trees:** organize elements in a hierarchical structure.
-   **Graphs:** represent entities and the connections between them.

Choosing a suitable data structure can make an algorithm easier to
implement or more efficient for a particular task.

### 1.3 Connectionist artificial intelligence

**Connectionist AI** refers in this course to learning systems built
from connected artificial neurons. A neural network processes numerical
inputs through connected units and uses adjustable parameters, including
weights and biases, to produce outputs.

During training, a learning procedure adjusts those parameters using
examples. Once trained, the model can produce predictions for new
inputs. A prediction is an output from the model; it is not guaranteed
to be correct.

Not every AI system is a neural network. This course focuses on
connectionist AI as one important approach to machine learning.

## 2. How the three strands work together

Algorithms, data structures, and connectionist AI are distinct topics,
but they often work together in real applications.

A system may store information in an appropriate data structure, use
algorithms to retrieve or process it, and use a trained model when a
prediction is needed. The result can then be checked against the task's
requirements.

Consider a book recommendation system:

1.  Information about books and users is stored as data.
2.  Algorithms retrieve candidate books and process relevant
    information.
3.  A recommendation model may estimate which books a reader is likely
    to prefer.
4.  The system presents recommendations that can be evaluated and
    improved.

Not every task needs AI. A simple, well-defined problem may be solved
entirely with conventional algorithms and data structures. AI is useful
when a task benefits from learning patterns from examples.

## 3. Learning through familiar examples

### 3.1 Finding a book in a library catalogue

A library catalogue may store each book's title, author, and location. A
record groups information about one book, while the catalogue organizes
many records.

A search algorithm is a method for locating a target entry. **Linear
search** checks entries one by one and can work even when the entries
are not sorted. **Binary search** repeatedly narrows the search range by
comparing the target with a middle entry. Ordinary binary search
requires the entries to be sorted according to the ordering used for
comparisons.

This example demonstrates that the organization of data affects which
algorithms can be used effectively. Recommendations are a separate task:
they aim to suggest books that may interest a reader rather than simply
locate a known title.

### 3.2 Planning a route around campus

A campus map can be represented as a **graph**. In this representation:

-   A **vertex** (also called a node) represents a location, such as a
    building.
-   An **edge** represents a connection, such as a walkway between two
    buildings.
-   A **weighted edge** associates a value, such as distance or travel
    cost, with a connection.
-   A **path** is a sequence of connected vertices.

Algorithms can process a graph to explore possible routes. The route
with the fewest connections is not necessarily the route with the
shortest total distance. The best route depends on the objective being
optimized.

This example shows why graphs are useful for representing relationships
and how algorithms operate on those representations.

### 3.3 Classifying an image

An image-classification system might predict whether an image contains a
cat or a dog. In simplified terms, the image is converted into numerical
input, processed by a neural network, and mapped to an output.

Several terms are important:

-   A **feature** is information used as input to a model.
-   A **prediction** is the output produced by the model.
-   A **label** is the correct category assigned to an example in a
    labelled dataset.
-   **Training** is the process of adjusting model parameters using data
    and a learning procedure.
-   **Loss** is a numerical measure of how far a prediction is from a
    target under a chosen rule.

A model can make incorrect predictions. During training, its parameters
may be adjusted to reduce the measured loss, although this does not
guarantee that every future prediction will be correct. The details of
neurons, network layers, prediction, loss, and parameter updates are
developed in later course material.

## 4. Essential vocabulary

  -----------------------------------------------------------------------
  Term                    Definition              Example
  ----------------------- ----------------------- -----------------------
  **Input**               Information supplied to A target value to
                          a process or model.     search for.

  **Output**              The result produced by  A message saying a book
                          a process or model.     was found.

  **State**               The current values or   The current values of
                          situation during        variables in an
                          execution.              algorithm.

  **Operation**           An action performed by  Comparing two values.
                          a process or program.   

  **Data**                Information that can be Book titles, distances,
                          stored or processed.    or image values.

  **Model**               A representation or     A neural network for
                          system that maps inputs image classification.
                          to outputs; in machine  
                          learning, it may be     
                          learned from examples.  

  **Prediction**          An output estimating a  A model's estimate that
                          value or category for   an image contains a
                          an input.               cat.

  **Training**            Adjusting model         Updating weights using
                          parameters using data   examples and a loss
                          and a learning          measure.
                          procedure.              
  -----------------------------------------------------------------------

The meaning of a term can depend slightly on context. In an algorithm
trace, *state* often refers to current variable or data values. In
machine learning, *training* refers to adjusting a model using examples.

## 5. Reading pseudocode

**Pseudocode** describes an algorithm in a structured,
language-independent form. It allows readers to focus on the logic
without needing to know the exact syntax of a particular programming
language.

Pseudocode conventions differ across textbooks and teams. The important
thing is to define a convention and use it consistently. In this course,
examples may use conventions such as:

-   `INPUT` to receive information.
-   `OUTPUT` to display or return a result.
-   `SET name ← value` to assign a value to a variable.
-   `IF ... THEN ... ELSE ... END IF` to represent a decision.
-   `FOR` and `WHILE` to represent repetition.

For example:

``` text
INPUT target
SET found ← false

IF target = 7 THEN
    SET found ← true
END IF

OUTPUT found
```

If `target` is `7`, the condition is true and the output is `true`. If
`target` is another value, the condition is false and `found` remains
`false`.

The arrow `←` means assignment in this example. It is different from the
equality check `target = 7`: assignment changes a variable's value,
while the equality check asks whether two values are equal.

## 6. Predict, trace, and check

A useful way to learn algorithms is to follow a repeatable cycle:

1.  **Predict:** decide what you think will happen.
2.  **Trace:** follow the instructions one step at a time and record the
    current state.
3.  **Check:** compare the trace with the expected result.
4.  **Explain:** describe why the result follows from the steps.
5.  **Practise:** try a new input or a slightly different case.

A prediction is an expectation. A trace is a step-by-step record of what
an algorithm does under its stated rules. Tracing helps make reasoning
visible and can reveal exactly where a misunderstanding occurs.

Consider the following pseudocode:

``` text
SET total ← 2
SET total ← total + 3
OUTPUT total
```

The first instruction sets `total` to `2`. The second instruction adds
`3` to its current value and stores the result, `5`, back in `total`.
The final instruction outputs `5`.

    Step Instruction                 Value of `total`
  ------ ------------------------- ------------------
       1 `SET total ← 2`                            2
       2 `SET total ← total + 3`                    5
       3 `OUTPUT total`                             5

The goal is not merely to guess the final answer. It is to explain how
each instruction changes the state and to verify that the final output
follows from the procedure.

## 7. What you should be able to do after this chapter

Use the following questions to check your understanding:

1.  What are the three strands of this course?
2.  What is one difference between an algorithm and a data structure?
3.  Why does ordinary binary search require sorted input?
4.  In a campus route graph, what do vertices and edges represent?
5.  What is the difference between a model's prediction and a dataset
    label?
6.  What is pseudocode used for?
7.  What value is output by the `total` example in Section 6?

### Suggested answers

1.  Algorithms, data structures, and connectionist AI.
2.  An algorithm describes steps; a data structure organizes data.
3.  Sorting allows binary search to discard a portion of the search
    range safely after a comparison.
4.  Vertices represent locations; edges represent connections between
    locations.
5.  A prediction is the model's output; a label is the target category
    assigned to an example.
6.  Pseudocode describes algorithm logic without relying on one
    programming language's exact syntax.
7.  `5`.

## Chapter summary

Algorithms describe steps for solving problems. Data structures organize
information so that it can be stored and processed. Connectionist AI
uses connected artificial neurons and adjustable parameters to produce
predictions from inputs.

These strands can support the same application, but they serve different
purposes. A library catalogue demonstrates searching and data
organization; route planning motivates graphs and graph algorithms;
image classification introduces model inputs, predictions, labels, and
training.

Pseudocode and tracing provide a way to reason carefully about
computational procedures. The predict--trace--check method encourages
learners to test their expectations, follow each step, and explain the
result.

## Learner application activity

Trace a linear search for the value `7` in the sequence `[4, 2, 9, 7, 1]`. Record each value checked and stop when the target is found.

### Expected outcome

The search checks `4`, then `2`, then `9`, then `7`. The target is found on the fourth check, so the search stops before checking `1`. This demonstrates the one-by-one process described for linear search.

## References and review status

**Project source:** the team-provided Stage 1 materials and content-development record.

**External references:** No verified external reference list was supplied in the files used to prepare this snapshot. The assignment requires identifiable sources, so this remains an explicit Stage 1 gap rather than being filled with unverified or invented citations.

**Review status:** The team records state that Mahmud (Quality Lead) checked the first Markdown chapter. However, the supplied records do not state a concrete finding and correction/confirmation. Therefore this snapshot does not invent a review outcome and does not mark the chapter as fully checked.
