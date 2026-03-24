# ODE-WeBWorK

A collection of [WeBWorK](https://webwork.maa.org/) online homework problems for an **Ordinary Differential Equations (ODE)** course at Kennesaw State University (KSU).

## About WeBWorK

[WeBWorK](https://webwork.maa.org/) is an open-source online homework system for math and sciences courses. It is supported by the [Mathematical Association of America (MAA)](https://www.maa.org/) and the [National Science Foundation (NSF)](https://www.nsf.gov/).

- **WeBWorK Project:** https://webwork.maa.org/
- **WeBWorK Open Problem Library (OPL):** https://github.com/openwebwork/webwork-open-problem-library
- **WeBWorK2 Source:** https://github.com/openwebwork/webwork2
- **PG Problem Authoring Guide:** https://webwork.maa.org/wiki/Problem_Authoring_Guide

## Repository Structure

```
ODE-WeBWorK/
├── setDefs/                  # WeBWorK set definition (.def) files
├── problems/
│   ├── 01_intro_ODEs/        # Introduction to ODEs
│   ├── 02_first_order/       # First-order differential equations
│   ├── 03_second_order/      # Second-order linear differential equations
│   ├── 04_systems/           # Systems of differential equations
│   ├── 05_laplace/           # Laplace transforms
│   └── 06_series_solutions/  # Series solutions
└── README.md
```

## Problem File Format

WeBWorK problems are written in **PG (Problem Generator)** language, with the `.pg` file extension. Each file defines a self-contained homework problem with randomized parameters and automated grading.

## Usage

1. Copy the `.pg` problem files into your WeBWorK course's `templates` directory (or a subdirectory thereof).
2. Use the `.def` set definition files in `setDefs/` to create homework sets that reference these problems.
3. Import the set definitions via the WeBWorK instructor interface under **Hmwk Sets Editor → Import**.

## Contributing

Pull requests are welcome. Please follow standard WeBWorK PG coding conventions when adding or editing problem files.

## License

Problem files in this repository are released under the same license as the [WeBWorK Open Problem Library](https://github.com/openwebwork/webwork-open-problem-library): [Creative Commons Attribution-NonCommercial-ShareAlike 3.0 Unported (CC BY-NC-SA 3.0)](https://creativecommons.org/licenses/by-nc-sa/3.0/).
