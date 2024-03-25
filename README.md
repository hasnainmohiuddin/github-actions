# OOASP

OOASP Object Oriented Answer Set Programming

## Getting started

To run the examples, it is recommend to use clingo.
See [https://potassco.org/clingo/] for installation instructions.

## Description

Given is an encoding (ooasp.lp) which, given a description of an OOASP configuration
model (config-model.lp), and a partial instantiation (partial-instantiation.lp), generates a complete instantiation of the model,
using the output format of the instantiation predicates in Table 2 from the above paper.

In case the partial instantiation cannot be extended to a complete one, clingo gives UNSAT. A suite of test cases are also defined to test different constraints.

## Modules example

This example is taken from the paper "OOASP: Connecting Object-Oriented and Logic Programming".

[./config-model.lp](./config-model.lp) contains the knowledge base of the Modules example

[./partial-instantiation.lp](./partial-instantiation.lp) contains a partial configuration.

## CONSTRAINT AND TEST SUITE COMMANDS

**Minimum Cardinality Constraint**

Ensures that the minimum cardinality of associations between instantiated objects is maintained.

The Command to run the test case for this constraint is:
```
clingo ooasp.lp constraints.lp test-cases/min-card/config-model.lp test-cases/min-card/partial-instantiation.lp
```

**Maximum Cardinality Constraint** 

Ensures that the maximum cardinality of associations between instantiated objects is maintained.

The Command to run the test case for this constraint is:
```
clingo ooasp.lp constraints.lp test-cases/max-card/config-model.lp test-cases/max-card/partial-instantiation.lp
```

**Association b/w Instantiated Objects**

Ensures that associations only occur between instantiated objects.

The Command to run the test case for this constraint is:
```
clingo ooasp.lp constraints.lp test-cases/assoc-bw-ins-obj/config-model.lp test-cases/assoc-bw-ins-obj/partial-instantiation.lp
```
**Id is an instance of one class**

Ensures that an object is not an instance of two different classes.

The Command to run the test case for this constraint is:
```
clingo ooasp.lp constraints.lp test-cases/id-instance-of-one-class/config-model.lp test-cases/id-instance-of-one-class/partial-instantiation.lp
```
**Every Attribute Value must belong to an instance**

Ensures that attribute values are associated with instantiated objects.

The Command to run the test case for this constraint is:
```
clingo ooasp.lp constraints.lp test-cases/attr-value-to-ins/config-model.lp test-cases/attr-value-to-ins/partial-instantiation.lp
```
**Integer Value Below range**

Ensures that integer attribute values are not below the minimum inclusive value specified for them.

The Command to run the test case for this constraint is:
```
clingo ooasp.lp constraints.lp test-cases/int-value-below-range/config-model.lp test-cases/int-value-below-range/partial-instantiation.lp
```
**Integer Value Above range**

Ensures that integer attribute values are not above the maximum inclusive value specified for them.

The Command to run the test case for this constraint is:
```
clingo ooasp.lp constraints.lp test-cases/int-value-above-range/config-model.lp test-cases/int-value-above-range/partial-instantiation.lp
```
