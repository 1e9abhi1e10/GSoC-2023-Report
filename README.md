# GSoC-2023-Report

This report provides an overview of my contributions to the project titled **Improving Polynomial GCD** as part of my participation in Google Summer of Code 2023 with SymPy.

## About Me

I'm Abhishek Patidar, a third-year undergraduate student. I am passionate about open-source projects and am eager to contribute to any projects involving scientific or mathematical computations.

## Project Synopsis

The project aims to add new algorithms for computing the greatest common divisor (GCD)
of polynomials in the sparse representation in order to improve the speed of many parts of
SymPy such as matrices, solvers, integration, and simplification functions. Currently, the slow
speed of polynomial GCD impacts many operations in SymPy, leading to heavy performance
penalties and avoiding the use of domain elements in some algorithms. By improving the
speed of polynomial GCD algorithms, many parts of SymPy could become faster, and the use
of GCD could become more widespread. This project could significantly enhance the overall
performance and usability of SymPy.
Here's a list of all the Pull Requests I've opened over the past three months:

- [#25278](https://github.com/sympy/sympy/pull/25278): In this pull request, I've introduced several critical methods to enhance sparse polynomial representation within the `PolyElement` class. These methods, including `coeff_wrt` for precise coefficient calculations with respect to degree and symbol, `prem` for pseudo-remainder computation, `pdiv` for pseudo-division, `pquo` for polynomial pseudo-quotient, and `pexquo` for exact polynomial pseudo-quotient, play a pivotal role in enabling advanced polynomial operations and manipulations. These additions expand the functionality of the `PolyElement` class, making it an indispensable tool for upcoming stages of development and analysis involving multivariate polynomials.

- [#89](https://github.com/sympy/sympy_benchmarks/pull/89): In this pull request, I included benchmarks in the `sympy/sympy_benchmarks` repository for the `pseudo remainder` method mentioned above. These benchmarks illustrate the performance difference between the new method using sparse representation and the old method using dense representation.

- [#25371](https://github.com/sympy/sympy/pull/25371): In this pull request, I've implemented the Subresultant Polynomial Remainder Sequences (PRS) algorithm with sparse representations, enabling the efficient calculation of the greatest common divisor (GCD) between two polynomials, `f` and `g`. This method significantly improves computational efficiency by avoiding expensive polynomial divisions, making it a valuable addition for the next stages of development.

- [#94](https://github.com/sympy/sympy_benchmarks/pull/94): In this pull request, I've added benchmarks to the `sympy/sympy_benchmarks` repository for the `subresultant PRS` method mentioned earlier. These benchmarks explore various cases of polynomials to assess performance.

- [#25442](https://github.com/sympy/sympy/pull/25442): In this pull request, I've implemented improvements to the GCD (Greatest Common Divisor) functions by integrating them with the existing GCD methods. I've utilized the PolyElement methods mentioned earlier for enhanced integration. This implementation includes a function to simplify the polynomials and introduces quick exit strategies to expedite GCD calculations. To address the slow performance of the `dmp_inner_gcd` method using dense representation, I've replaced it with the `_gcd_prs` method that utilizes sparse representation, significantly boosting efficiency. While integrating the GCD algorithms with the older methods, I've also addressed and resolved some numerical errors. Additionally, I've focused on optimizing the code further to enhance overall performance.

- [#95](https://github.com/sympy/sympy_benchmarks/pull/95): In this pull request, I've contributed benchmarks to the `sympy/sympy_benchmarks` repository, specifically targeting the previously mentioned `gcd` method. These benchmarks cover a range of polynomial scenarios, providing a comprehensive performance evaluation.

- [#97](https://github.com/sympy/sympy_benchmarks/pull/97):  In this pull request, I've contributed benchmarks to the `sympy/sympy_benchmarks` repository. These benchmarks encompass a diverse set of polynomial scenarios, including cases involving specialized domains such as `ZZ_I` and `ZZ.algebraic_field(sqrt(2))`. This comprehensive testing approach ensures thorough performance assessment across various mathematical domains and scenarios.

## Future Work

Future work possibilities related to polynomial GCD (Greatest Common Divisor) optimization include exploring and benchmarking different algorithms and implementations to determine their speed advantages and subsequently developing logic for employing various strategies. Additionally, there's potential to implement modular GCD algorithms and investigate algorithms that excel in sparse representations, such as Zippel or sparse modular GCD algorithms. These enhancements aim to enhance the efficiency and versatility of polynomial GCD computations, opening doors for further improvements in the field.

## Conclusion 

My participation in GSoC 2023 has exceeded my expectations, providing me with an exceptional experience during my time with SymPy this past summer. Beyond enhancing my coding skills, I gained valuable insights into documentation and testing-driven software development practices, which will undoubtedly benefit me as I transition into the industry in the near future.

Throughout this journey, I acquired knowledge in various areas, including benchmarking, debugging, profiling, and the art of writing clean code. I owe immense gratitude to SymPy for granting me this invaluable experience. Special thanks go to my mentors, [Oscar Benjamin](https://github.com/oscarbenjamin) and [Kalevi Suominen](https://github.com/jksuom), who provided unwavering support and guidance whenever I encountered challenges. I'd also like to extend my appreciation to the organization members and administrators for their continuous availability and contributions to code reviews.

Looking ahead, I am committed to continuing my contributions to SymPy by completing the proposed work outlined in the Future Work section and addressing any issues identified in the Work in Progress section.

Link of Wiki Page on SymPy :- https://github.com/sympy/sympy/wiki/GSoC-2023-Report-Abhishek-Patidar-:-Improving-Polynomial-GCD
