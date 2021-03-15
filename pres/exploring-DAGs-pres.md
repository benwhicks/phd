Exploring Causal Models with DAGs
========================================================
author: Ben Hicks
date: 2021-03-16
autosize: true



## Today's menu

### - -  Causal Model review, with toy examples

### - -  Berkeley Admissions Paradox (neat)

### - -  CSU Retention (messy)

Review of DAGs
========================================================
incremental: true

* Represents _causal assumptions_ about the system.
* Structure of the DAG implies _expected association_ in the data.


***


Review of DAGs
========================================================

* Represents _causal assumptions_ about the system.
* Structure of the DAG implies _expected association_ in the data.
  - X -> Y  (open)

***

![plot of chunk unnamed-chunk-2](exploring-DAGs-pres-figure/unnamed-chunk-2-1.png)

Review of DAGs
========================================================

* Represents _causal assumptions_ about the system.
* Structure of the DAG implies _expected association_ in the data.
  - X -> Y  (open)
  - Chain: X -> Y -> Z  (open, __mediator__ Y)

***

![plot of chunk unnamed-chunk-3](exploring-DAGs-pres-figure/unnamed-chunk-3-1.png)![plot of chunk unnamed-chunk-3](exploring-DAGs-pres-figure/unnamed-chunk-3-2.png)

Review of DAGs
========================================================

* Represents _causal assumptions_ about the system.
* Structure of the DAG implies _expected association_ in the data.
  - X -> Y  (open)
  - Chain: X -> Y -> Z  (open, __mediator__ Y)
  - Fork: X <- Y -> Z (open, __common cause__ Y)

***

![plot of chunk unnamed-chunk-4](exploring-DAGs-pres-figure/unnamed-chunk-4-1.png)![plot of chunk unnamed-chunk-4](exploring-DAGs-pres-figure/unnamed-chunk-4-2.png)![plot of chunk unnamed-chunk-4](exploring-DAGs-pres-figure/unnamed-chunk-4-3.png)

Review of DAGs
========================================================

* Represents _causal assumptions_ about the system.
* Structure of the DAG implies _expected association_ in the data.
  - X -> Y  (open)
  - Chain: X -> Y -> Z  (open, __mediator__ Y)
  - Fork: X <- Y -> Z (open, __common cause__ Y)
  - Collider: X -> Y <- Z (closed between X and Z, __collider__ Y)

***

![plot of chunk unnamed-chunk-5](exploring-DAGs-pres-figure/unnamed-chunk-5-1.png)![plot of chunk unnamed-chunk-5](exploring-DAGs-pres-figure/unnamed-chunk-5-2.png)![plot of chunk unnamed-chunk-5](exploring-DAGs-pres-figure/unnamed-chunk-5-3.png)![plot of chunk unnamed-chunk-5](exploring-DAGs-pres-figure/unnamed-chunk-5-4.png)

Conditioning - Toy Examples
========================================================
incremental: true

When we _condition_ on a variable it changes the flow of information (association) through the causal model.

## Chain

Student  Capacity -> Doing Work -> Achievement

![plot of chunk unnamed-chunk-6](exploring-DAGs-pres-figure/unnamed-chunk-6-1.png)

![plot of chunk unnamed-chunk-7](exploring-DAGs-pres-figure/unnamed-chunk-7-1.png)


***

## Fork

Asking Questions <- Motivation -> LMS Activity

![plot of chunk unnamed-chunk-8](exploring-DAGs-pres-figure/unnamed-chunk-8-1.png)


![plot of chunk unnamed-chunk-9](exploring-DAGs-pres-figure/unnamed-chunk-9-1.png)

Conditioning - Toy Examples
========================================================
incremental: true

## Collider

Educational Support -> Attrition <- Extrinsic Factors

![plot of chunk unnamed-chunk-10](exploring-DAGs-pres-figure/unnamed-chunk-10-1.png)

------

![plot of chunk unnamed-chunk-11](exploring-DAGs-pres-figure/unnamed-chunk-11-1.png)





The Berkeley Admissions Paradox
=============================================

In 1973 Eugene Hammel noticed that the men got accepted to the graduate school at Berkeley at a rate of 44% whilst women got accepted at a rate of 35%.

Admission decisions were made at a department level, and in each individual department the acceptance rate favoured women over men.

__Was gender discrimination happening?__

----

![plot of chunk unnamed-chunk-12](exploring-DAGs-pres-figure/unnamed-chunk-12-1.png)

The Berkeley Admissions Paradox
=============================================

In 1973 Eugene Hammel noticed that the men got accepted to the graduate school at Berkeley at a rate of 44% whilst women got accepted at a rate of 35%.

Admission decisions were made at a department level, and in each individual department the acceptance rate favoured women over men.

__Was gender discrimination happening?__

__How would discrimination (not bias) be represented in the DAG?__

__What arrows would you draw (or more strongly, leave out) from the causal diagram?__

----

![plot of chunk unnamed-chunk-13](exploring-DAGs-pres-figure/unnamed-chunk-13-1.png)


Berkeleys Admission Paradox
========================================================


Initial approach?

__What does this model assume?__

__Does this match with the data?__

(Remember, that the results changed when conditioning by department)

-------

![plot of chunk unnamed-chunk-14](exploring-DAGs-pres-figure/unnamed-chunk-14-1.png)

Berkeleys Admission Paradox
========================================================
incremental: true

### Model proposed by Peter Bickel

__Does this imply we should condition on department?__

__What happens when we condition on department?__

-------

![plot of chunk unnamed-chunk-15](exploring-DAGs-pres-figure/unnamed-chunk-15-1.png)

Berkeleys Admission Paradox
========================================================

### Bickel's model, with conditioning


![plot of chunk unnamed-chunk-16](exploring-DAGs-pres-figure/unnamed-chunk-16-1.png)

-----

### Bickel & Hammels conclusions

_The campus as a whole did not engage in discrimination against women applicants_. The total effect of bias against women acceptances is due women applying in greater numbers to departments that are harder to get into.

It is worth noting that discrimination here is the _direct effect_ between __Gender__ and __Outcome__; with all other pathways blocked. Bickel was very careful distinguishing between _bias_ and _discrimination_.

Berkeleys Admission Paradox
========================================================

### Kruskal's alternative



What if there was another variable, such as State of Residence, that influences the Outcome as well?

__What, now, is the consequence of conditioning on Department?__

-----

![plot of chunk unnamed-chunk-18](exploring-DAGs-pres-figure/unnamed-chunk-18-1.png)

Berkeleys Admission Paradox
========================================================

### Kruskal's alternative

What if there was another variable, such as State of Residence, that influences the Outcome as well?

__What do we do now?__

-----

![plot of chunk unnamed-chunk-19](exploring-DAGs-pres-figure/unnamed-chunk-19-1.png)

Berkeleys Admission Paradox
========================================================

### Kruskal's alternative

What if there was another variable, such as State of Residence, that influences the Outcome as well?


-----

![plot of chunk unnamed-chunk-20](exploring-DAGs-pres-figure/unnamed-chunk-20-1.png)


CSU Retention
========================================================

![Retention Causal Model](retention dag.png)


CSU Retention
========================================================

![plot of chunk unnamed-chunk-21](exploring-DAGs-pres-figure/unnamed-chunk-21-1.png)

Nice links
========================================================

