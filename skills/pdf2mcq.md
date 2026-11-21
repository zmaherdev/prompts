Convert ALL multiple-choice questions (MCQ) inside the PDFs I'll send into the specific output structure shown in the example below:

### Example Input:

```Text
1. Ozone Depleting Substances (ODS) are the substances such as chlorofluorocarbons, halons, hydrofluorocarbons, etc. that are responsible for the depletion of the ozone layer.

a. Carbon dioxide 
b. Carbon tetrachloride
c. Sulfur oxide
d. Nitrogen oxide


2. Furuncle is/has:
A. An abscess of sweet glands
B. Common in scrotum, check, and in chest
C. Common in immune-compromised people
D. Treated as an abscess
```

### Example Output:

```Typst
#mcq(
  1, [Ozone Depleting Substances (ODS) are the substances such as chlorofluorocarbons, halons, hydrofluorocarbons, etc. that are responsible for the depletion of the ozone layer.],
  (    
    ([Carbon dioxide], 0),    
    ([Carbon tetrachloride], 0),    
    ([Sulfur oxide], 0),    
    ([Nitrogen oxide], 0),  
  ),
)


#mcq(
  2, [Furuncle is/has:],
  (    
    ([An abscess of sweet glands], 0),    
    ([Common in scrotum, check, and in chest], 0),    
    ([Common in immune-compromised people], 0),    
    ([Treated as an abscess], 0),  
  ),
)
```

Bear in mind:
1. Insert `#pagebreak()` every 4 mcqs.
2. Never add [cite: NUMBER] or any kind of citations in the result.
3. If there are many dots next to each other in a question, assume they are 9 dots `.........`
4. If you see an underlined word/text you can use #u[] like this `#u[text]`.
5. DO NOT USE LATEX MATH or any kind of math. Superscripts are done using #super[] and subscripts are #sub[]
6. If the user didn't say answers were correct, assume there are no answers and use 0 next to each choice, otherwise use 1 if the user said answers were correct
