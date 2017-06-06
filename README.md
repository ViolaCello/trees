## Introduction

### Objectives
- Learn how the different components of a tree relate
- Learn about the characteristics of a binary search tree
- Explore how trees are a recursive data structure

### Trees in the world

Trees are a data structure that connects nodes in a parent - child relationship.  Each parent node has a pointer to and therefore knows about its children.  

For example, here is a family tree.

```text
      Grampa (Abe) Simpson
               |      
          Homer Simpson
         |     |       |
      Bart    Lisa    Maggie
```

In the diagram above, Grampa Simpson is a parent of Homer Simpson and Homer Simpson is a parent of Bart, Lisa and Maggie.  Each individual in the Simpson family tree is a node.  The **root node** is the only node in a tree without a parent.  Another example of a tree is an organizational chart.

```text
                                   CEO
       |                            |                                 |
  Chief Ops Officer        Chief Finance Officer             Chief Marketing Officer
    |                            |         |                        |        |
  VP Human Resources    VP Operations      VP Accounting       VP Sales      VP Ads

```

In the above diagram, the CEO has a parent-child relationship with his/her direct reports, the Chief Operating Officer, the Chief Financial Officer and the Chief Marketing Officer.  Each of the C-level officers has a parent-child relationship with each one of his/her direct reports.  

One thing that you may start noticing is that the parent-child relationship is convenient for sorting information.  For example, the tree above represents the organizational hierarchy.  Those who report to the same employee (for example, all of the Vice Presidents) are **siblings**.   

> In a tree, siblings are nodes who share a parent node.

So as we see, trees with parent-child relationships, siblings, and root nodes naturally fit models of social and organizational structures, and thus become an important data structure to explore.

### Trees as a recursive data structure

There is one characteristic to remember about trees as we discuss methods of tree exploration in the sections that follow: they are recursive.  

We have seen recursive data structures before.  Arrays and linked lists are both recursive data structures.  For example, every array is made up of smaller arrays.  It's that characteristic that allows us to say that the sum of the elements in an array is the sum of all of the elements up to the last element, plus the final element.  Turning that into a recursive method relies on an array being made up of smaller arrays.  

Similarly linked lists also consist of linked lists.  If we remove a node from a linked list, what we are left with is another linked list.

Cut off the limbs of a linked list and you get a linked list.  Cut off the limbs of an array and you have an array.

![](https://s3.amazonaws.com/learn-verified/montypython.gif)

Notice that the same thing is true of a tree.

```text
      Grampa (Abe) Simpson
               |      
          Homer Simpson
         |     |       |
      Bart    Lisa    Maggie
```

If we remove Grampa Simpson from the tree, we still have a tree with Homer as our root node.  If we remove Maggie (perish the thought), we still have a tree in tact.  That is, a large tree consists of smaller subtrees.  In later sections we will take advantage of trees being a recursive data structures with the methods we write, just as we did with arrays and linked lists.

### Summary

Trees connect nodes in a parent child relationship.  The node without a parent in any tree is called the root node.  Nodes that share a parent node are called siblings.  Trees are a recursive data structure, meaning that each tree is made up of other trees with parent and child nodes.  
