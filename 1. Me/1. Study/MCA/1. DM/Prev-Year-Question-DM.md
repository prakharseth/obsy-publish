# Previous Year Question Paper Solutions - Discrete Mathematics

## SECTION-A (Very Short Answer Type Questions)

### Q.1.a) Differentiate between Equal set and Equivalent set? (CO1)
**Reference**: [[Unit 1 - Set Theory and Relations/1. Set Theory]]

Equal Sets and Equivalent Sets are two different concepts:
- **Equal Sets**: Two sets that have exactly the same elements
  - Example: A = {1,2,3} and B = {1,2,3} are equal sets
  - Notation: A = B

- **Equivalent Sets**: Sets having same number of elements (cardinality)
  - Example: A = {1,2,3} and B = {a,b,c} are equivalent
  - Notation: A ~ B

### Q.1.b) Which relations are partial orderings? (CO2)
**Reference**: [[Unit 1 - Set Theory and Relations/10. Partial Ordered Sets]]

For a relation to be a partial ordering, it must be:
- Reflexive (aRa)
- Antisymmetric (if aRb and bRa, then a=b)
- Transitive (if aRb and bRc, then aRc)

Analysis:
i) {(0,0), (1,1), (2,2), (3,3)}
   - ✅ Is a partial ordering
   - Satisfies all three properties
   
ii) {(0,0), (1,1), (2,0), (2,2), (2,3), (3,2), (3,3)}
   - ❌ Not a partial ordering
   - Fails antisymmetry: (2,3) and (3,2) exist but 2≠3
   
iii) {(0,0), (1,1), (1,2), (2,2), (3,3)}
   - ✅ Is a partial ordering
   - Satisfies all three properties

### Q.1.c) Is the negation of a conditional statement also a conditional statement? (CO3)
**Reference**: [[Unit 3 - Propositional Logic/Conditional Statements]]

- The negation of p → q is NOT a conditional statement
- It is equivalent to: p ∧ ¬q
- Example:
  - Statement: "If it rains, then the ground is wet" (p → q)
  - Negation: "It rains and the ground is not wet" (p ∧ ¬q)

### Q.1.d) Every subgroup of an abelian group is normal. (CO4)
**Reference**: [[Unit 4 - Algebraic Structures/Abelian Groups]]

- ✅ This statement is TRUE
- Proof outline:
  1. In an abelian group G, all elements commute: ab = ba for all a,b ∈ G
  2. For any subgroup H of G and element g ∈ G
  3. gH = Hg (due to commutativity)
  4. Therefore, H is normal in G

### Q.1.e) Differentiate between strong induction and induction with non zero base. (CO5)
**Reference**: [[Unit 5 - Number Theory and Combinatorics/37. Mathematical Induction]]

- **Strong Induction**:
  - Assumes P(k) is true for all k ≤ n to prove P(n+1)
  - Uses all previous cases as inductive hypothesis
  - Example: Proving properties of prime factorization

- **Induction with Non-Zero Base**:
  - Starts proof from a base case k > 0 (instead of n = 1)
  - Only uses P(n) to prove P(n+1)
  - Example: Proving properties that hold for n ≥ 4

### Q.1.f) Define principle of mathematical Induction. (CO5)
**Reference**: [[Unit 5 - Number Theory and Combinatorics/37. Mathematical Induction]]

Mathematical Induction has three steps:
1. **Base Step**: Prove P(1) or P(k) for initial value
2. **Inductive Hypothesis**: Assume P(n) is true
3. **Inductive Step**: Prove P(n) → P(n+1)

If all steps are satisfied, then P(n) is true for all n ≥ 1 (or k)

### Q.1.g) Find a counter example for universally quantified statements over integers. (CO3)
**Reference**: [[Unit 3 - Propositional Logic/Universal Quantifiers]]

Statement: "For all integers n, n² ≥ n"
Counter example: 
- Let n = 0: 0² = 0 = 0 (true)
- Let n = 1: 1² = 1 = 1 (true)
- Let n = -2: (-2)² = 4 > -2 (true)
- Let n = 0.5: (0.5)² = 0.25 < 0.5 (false)
Therefore, statement is false for some real numbers between 0 and 1

### Q.1.h) Let A be the set {1, 2, 3, 4}. Which ordered pairs are in the relation R = {(a,b) | a divides b}? (CO1)
**Reference**: [[Unit 1 - Set Theory and Relations/Relations]]

Let's check all possible divisibility pairs in A = {1,2,3,4}:
- 1 divides: (1,1), (1,2), (1,3), (1,4)
- 2 divides: (2,2), (2,4)
- 3 divides: (3,3)
- 4 divides: (4,4)

Therefore, R = {(1,1), (1,2), (1,3), (1,4), (2,2), (2,4), (3,3), (4,4)}

## SECTION-B (Short Answer Type Questions)

### Q.2.a) What is the Cartesian product A × B × C, where A = {0, 1}, B = {1, 2}, and C = {0, 1, 2}? (CO1)
**Reference**: [[Unit 1 - Set Theory and Relations/2. Set Operations]]

A × B × C = {(a,b,c) | a ∈ A, b ∈ B, c ∈ C}

The result will be:
{(0,1,0), (0,1,1), (0,1,2), (0,2,0), (0,2,1), (0,2,2),
 (1,1,0), (1,1,1), (1,1,2), (1,2,0), (1,2,1), (1,2,2)}

Total elements = |A| × |B| × |C| = 2 × 2 × 3 = 12 ordered triples

### Q.2.b) Which of these are posets? (CO2)
**Reference**: [[Unit 2 - Lattices and Boolean Algebra/12. Introduction to Lattices]]

For each relation on R (real numbers):

i) (R, =)
- ✅ Reflexive: a = a
- ✅ Antisymmetric: if a = b and b = a, then a = b
- ✅ Transitive: if a = b and b = c, then a = c
Result: Is a poset

ii) (R, <)
- ❌ Not reflexive: a < a is false
- ✅ Antisymmetric: if a < b, then b < a cannot be true
- ✅ Transitive: if a < b and b < c, then a < c
Result: Not a poset (fails reflexivity)

iii) (R, ≤)
- ✅ Reflexive: a ≤ a
- ✅ Antisymmetric: if a ≤ b and b ≤ a, then a = b
- ✅ Transitive: if a ≤ b and b ≤ c, then a ≤ c
Result: Is a poset

iv) (R, # =)
- ❌ Not reflexive: a # a is false
- ❌ Not antisymmetric
- ❌ Not transitive
Result: Not a poset

### Q.2.c) Show that p → (q → r) is logically equivalent to (p ∧ q) → r. (CO3)
**Reference**: [[Unit 3 - Propositional Logic/Conditional Statements]]

Proof using truth table:

| p | q | r | q → r | p → (q → r) | p ∧ q | (p ∧ q) → r |
|---|---|---|--------|-------------|--------|-------------|
| T | T | T |   T    |     T       |   T    |     T       |
| T | T | F |   F    |     F       |   T    |     F       |
| T | F | T |   T    |     T       |   F    |     T       |
| T | F | F |   T    |     T       |   F    |     T       |
| F | T | T |   T    |     T       |   F    |     T       |
| F | T | F |   F    |     T       |   F    |     T       |
| F | F | T |   T    |     T       |   F    |     T       |
| F | F | F |   T    |     T       |   F    |     T       |

Since both expressions have identical truth values in all cases, they are logically equivalent.

### Q.2.d) Prove that intersection of any two normal subgroups of a group (G, *) is a normal subgroup of a group (G, *). (CO4)
**Reference**: [[Unit 4 - Algebraic Structures/34. Cosets]]

Proof:
1. Let H and K be normal subgroups of G
2. Let N = H ∩ K

To prove N is normal, we need to show:
1. N is a subgroup
   - Closure: For h ∈ H, k ∈ K: h * k ∈ H and h * k ∈ K, so h * k ∈ N
   - Identity: e ∈ H and e ∈ K, so e ∈ N
   - Inverse: If n ∈ N, then n⁻¹ ∈ H and n⁻¹ ∈ K, so n⁻¹ ∈ N

2. N is normal
   - For any g ∈ G and n ∈ N:
   - gng⁻¹ ∈ H (since H is normal)
   - gng⁻¹ ∈ K (since K is normal)
   - Therefore, gng⁻¹ ∈ H ∩ K = N

Thus, N is a normal subgroup of G.

### Q.2.e) A factory makes custom sports cars at an interesting rate. (CO5)
**Reference**: [[Unit 5 - Number Theory and Combinatorics/39. Simple Recurrence Relations]]

i) Recurrence relation for cars produced in first n months:
- Let a(n) be the number of cars in nth month
- a(n) = n (given in problem)
- Total cars in n months = T(n) = 1 + 2 + 3 + ... + n
- T(n) = n(n+1)/2 (sum of arithmetic sequence)

ii) Cars produced in first year:
- n = 12 months
- T(12) = 12(12+1)/2
- T(12) = 12 × 13/2
- T(12) = 78 cars

### Q.2.f) Find the value of 10!/8! (CO5)
**Reference**: [[Unit 5 - Number Theory and Combinatorics/Factorial Functions]]
s
Solution:
10!/8! = 10 × 9 × 8!
         ___________
             8!

       = 10 × 9
       = 90

### Q.2.g) Express the compound propositions p→(q∨r), p∧(~q) in words. (CO3)
**Reference**: [[Unit 3 - Propositional Logic/Conditional Statements]]

Given:
- p: A circle is a conic
- q: 5 is a real number
- r: Exponential series is convergent

Expressing in words:
1. p→(q∨r): 
   "If a circle is a conic, then either 5 is a real number or exponential series is convergent"

2. p∧(~q):
   "A circle is a conic and 5 is not a real number"

### Q.2.h) Let U be the set of positive integers not exceeding 1000. Find |S| where S is the set of integers not divisible by 3, 5 or 7? (CO5)
**Reference**: [[Unit 5 - Number Theory and Combinatorics/Inclusion-Exclusion Principle]]

Using Inclusion-Exclusion Principle:
|S| = |U| - |D₃| - |D₅| - |D₇| + |D₃∩D₅| + |D₃∩D₇| + |D₅∩D₇| - |D₃∩D₅∩D₇|

Where:
- |U| = 1000
- |D₃| = ⌊1000/3⌋ = 333
- |D₅| = ⌊1000/5⌋ = 200
- |D₇| = ⌊1000/7⌋ = 142
- |D₃∩D₅| = ⌊1000/15⌋ = 66
- |D₃∩D₇| = ⌊1000/21⌋ = 47
- |D₅∩D₇| = ⌊1000/35⌋ = 28
- |D₃∩D₅∩D₇| = ⌊1000/105⌋ = 9

|S| = 1000 - 333 - 200 - 142 + 66 + 47 + 28 - 9 = 457

## SECTION-C (Descriptive Answer Type Questions)

### Q.3.a) Let A be the set of English words that contain the letter x, and let B be the set of English words that contain the letter q. Express each of these sets as a combination of A and B. (CO1)
**Reference**: [[Unit 1 - Set Theory and Relations/2. Set Operations]]

i) The set of English words that do not contain the letter x
   - Answer: A' (complement of A)
   - Example: "dog", "cat", "queen"

ii) The set of English words that contain both x and q
   - Answer: A ∩ B
   - Example: "exquisite"

iii) The set of English words that contain an x but not a q
   - Answer: A ∩ B'
   - Example: "box", "extra"

iv) The set of English words that do not contain either an x or a q
   - Answer: A' ∩ B'
   - Example: "dog", "cat"

v) The set of English words that contain an x or a q, but not both
   - Answer: A ⊕ B (symmetric difference) = (A ∪ B) - (A ∩ B)
   - Example: "box", "queen"

### Q.3.b) Draw the Hasse diagram for inclusion on the set P(S), where S = {a, b, c, d}. (CO2)
**Reference**: [[Unit 2 - Lattices and Boolean Algebra/12. Introduction to Lattices]]

The Hasse diagram should be drawn with:
1. Bottom level: ∅
2. First level: {a}, {b}, {c}, {d}
3. Second level: {a,b}, {a,c}, {a,d}, {b,c}, {b,d}, {c,d}
4. Third level: {a,b,c}, {a,b,d}, {a,c,d}, {b,c,d}
5. Top level: {a,b,c,d}

Connect elements with lines where one set is a proper subset of another.

### Q.3.c) Show that the following hypotheses are inconsistent. (CO3)
**Reference**: [[Unit 3 - Propositional Logic/Conditional Statements]]

Given statements:
i) If Jack misses many classes through illness, then he fails high school.
ii) If Jack fails high school, then he is uneducated
iii) If Jack reads a lot of books, then he is not uneducated.
iv) Jack misses many classes through illness and reads a lot of books

Let's prove inconsistency:
1. Let p: Jack misses many classes
   q: Jack fails high school
   r: Jack is uneducated
   s: Jack reads a lot of books

2. Given statements in symbolic form:
   - p → q
   - q → r
   - s → ¬r
   - p ∧ s

3. From p ∧ s:
   - p is true (by conjunction)
   - s is true (by conjunction)

4. From p and (p → q):
   - q is true (by modus ponens)

5. From q and (q → r):
   - r is true (by modus ponens)

6. From s and (s → ¬r):
   - ¬r is true (by modus ponens)

7. We have both r and ¬r, which is a contradiction.
Therefore, the hypotheses are inconsistent.

### Q.3.d) Prove that G = {0,1,2,3,4} is an abelian group of order 5 with respect to addition modulo 5. (CO4)
**Reference**: [[Unit 4 - Algebraic Structures/Abelian Groups]]

To prove G is an abelian group under addition modulo 5, we need to verify:

1. **Closure**:
   - For any a,b ∈ G, (a + b) mod 5 ∈ G
   - Example: (3 + 4) mod 5 = 2 ∈ G

2. **Associativity**:
   - (a + b) + c ≡ a + (b + c) (mod 5)
   - Example: (2 + 3) + 4 ≡ 2 + (3 + 4) (mod 5)

3. **Identity Element**:
   - 0 is the identity element
   - For any a ∈ G: (a + 0) mod 5 = a

4. **Inverse Elements**:
   - For each element a, there exists -a such that (a + (-a)) mod 5 = 0
   - 0 + 0 ≡ 0 (mod 5)
   - 1 + 4 ≡ 0 (mod 5)
   - 2 + 3 ≡ 0 (mod 5)
   - 3 + 2 ≡ 0 (mod 5)
   - 4 + 1 ≡ 0 (mod 5)

5. **Commutativity** (Abelian property):
   - For any a,b ∈ G: (a + b) mod 5 = (b + a) mod 5
   - Example: (2 + 3) mod 5 = (3 + 2) mod 5

Since all properties are satisfied, G is an abelian group under addition modulo 5.

### Q.3.e) Solve the recurrence relation a r = ar-1 + ar-2 using generating function. (CO5)
**Reference**: [[Unit 5 - Number Theory and Combinatorics/38. Generating Functions Introduction]]

Let's solve using generating function method:

1. Let G(x) be the generating function:
   G(x) = Σ ar xʳ

2. Given recurrence relation:
   ar = ar-1 + ar-2 for r ≥ 2
   with initial conditions a₀ = 0, a₁ = 1

3. Multiply recurrence by xʳ and sum:
   Σ ar xʳ = Σ ar-1 xʳ + Σ ar-2 xʳ

4. This gives:
   G(x) - a₁x - a₀ = x(G(x) - a₀) + x²G(x)

5. Substitute initial conditions:
   G(x) - x = x(G(x)) + x²G(x)

6. Solve for G(x):
   G(x) - x = xG(x) + x²G(x)
   G(x) - xG(x) - x²G(x) = x
   G(x)(1 - x - x²) = x

7. Therefore:
   G(x) = x/(1 - x - x²)

8. This is the generating function for the Fibonacci sequence
   Therefore, ar is the rth Fibonacci number

The solution sequence is the Fibonacci sequence: 0, 1, 1, 2, 3, 5, 8, 13, ...