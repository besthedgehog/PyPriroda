# PyPriroda

'PyPriroda' is a Python package for quantum chemical program 'PRIRODA', which can be used to create hessian "input" files from optimization "out" files, or optimization "input" files from hessian "out" files.

## Installation

```
pip install PyPriroda
```
## Usage

**Here are the main functions that PyPriroda offers:**

__create_optim__(_name_of_out_hess_file = 'name'_)

This  function creates an optimization file from the hess file. The name of out file will be "optim_name_of_out_hess_file.in".

_Parameters:_
name_of_hess_file : string, default= 'name'. The name of the hessian file, where the coordinates and the energies come from. 
If 'name', the function takes the name of the hessian file from keybord.

__create_hess__(name_of_out_optimization_file='name')

Function creates hessian from an optimization file. The name of out file will be "HESS_name_of_out_optimization_file.in".

_Parameters:_
name_of_out_optimization_file : string, default= 'name'. 
The name of the optimization file, where the coordinates and the energies come from.
If 'name', the function takes the name of the optimization file from keybord.

## Examples

```
import PyPriroda.CreateFiles as pp

pp.create_optim('HESS_H2O2.out)
#or
pp.create_optim() #We can use keyboard to write a name of the hess file


pp.create_hess('optim_H2O2.out')
#or 
pp.create_hess() #We can use keyboard to write a name of the optimization file
```

## Testing library
Simply download files "optim_H2O2.out" and "HESS_H2O2.out" from this repository to test this library

# License (MIT License)
2023 Copyright (c) Alexey Polukhin, Olga Lavrukhina

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, ITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
