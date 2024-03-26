# ToriBird's Formula library (TBF)

This is ToriBird's Formula Library.
You can use formula with limit, and Case-wise formulas.

# how to use

* Normal Formula -> TBF.Formula("Your formula:str","Args in your formula:str")
* Limit -> TBF.Limit("min:number","value:str",max:number,"n(This means "<") or e(This means "<="):str","n or e")
* Limited Formula -> TBF.LimitedFormula("Your formula:Formula","Formula's Limit:Limit")
* Formulas -> TBF.Formulas("Formula","Formula"........)

# Sample

~~~python:sample.py
f = Formula("x**2 + 4 * x + 4", "x")
print(f.calc(4))
limit1 = Limit(2, "x", 10)
print(limit1.check("x", 1))
g = LimitedFormula(f, Limit(2, "x", 5))
print(g.calc(4))
fs = Formulas(f, g)
print(fs.calc(10))
~~~

~~~
>>>36
>>>False
>>>36
>>>144
~~~
