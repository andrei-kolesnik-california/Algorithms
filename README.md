# 🚀 Algorithms Repository

A collection of efficient algorithm implementations in Python, featuring advanced search and sorting techniques.

[![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)](https://www.python.org/downloads/)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)
[![Status](https://img.shields.io/badge/Status-Active-brightgreen.svg)]()

## 📋 Table of Contents

- [Overview](#overview)
- [Algorithms](#algorithms)
  - [Broken Array Search](#broken-array-search)
  - [In-Place Quick Sort](#in-place-quick-sort)
- [Requirements](#requirements)
- [Usage](#usage)
- [Examples](#examples)
- [Performance](#performance)
- [Contributing](#contributing)

## 🎯 Overview

This repository contains implementations of advanced algorithms designed for competitive programming and real-world applications. Each algorithm is optimized for performance and includes comprehensive documentation.

## 🔍 Algorithms

### Broken Array Search

**File:** `broken_array.py`

A sophisticated binary search algorithm designed to find elements in a "broken" sorted array - an array that was originally sorted but has been rotated/shifted.

#### Problem Description
Alla made an error while copying data from one data structure to another. She stored an array of numbers in a circular buffer. The array was sorted in ascending order and could be searched in logarithmic time. When copying from the circular buffer to a regular array, she shifted the data from the original sorted sequence. Now the array is no longer sorted, but we still need to find elements in O(log n) time.

#### Key Features
- ✅ **Time Complexity:** O(log n)
- ✅ **Space Complexity:** O(1)
- ✅ **Handles rotated sorted arrays**
- ✅ **Works with unique elements only**
- ✅ **Returns -1 if element not found**

#### Input Format
- Array of natural numbers (length ≤ 10,000)
- Target number k (≤ 10,000)
- All elements are unique

#### Output Format
- Returns the index of the target element (0-based indexing)
- Returns -1 if element not found

#### Example
```
Input:
9
5
19 21 100 101 1 4 5 7 12

Output:
5
```

### In-Place Quick Sort

**File:** `quick_sort_effective.py`

An optimized in-place implementation of the Quick Sort algorithm designed for sorting competition participants based on multiple criteria.

#### Problem Description
Timofey organized a competitive programming competition to find talented interns. Each participant has a unique login and two metrics: number of solved problems (Pi) and penalty (Fi). The sorting criteria are:
1. Higher number of solved problems first
2. If equal, lower penalty first
3. If equal, lexicographically earlier login first

#### Key Features
- ✅ **In-place sorting** (O(1) additional memory)
- ✅ **Multi-criteria sorting**
- ✅ **Handles large datasets** (up to 100,000 participants)
- ✅ **Custom comparison logic**

#### Input Format
- Number of participants n (1 ≤ n ≤ 100,000)
- For each participant: login (string ≤ 20 chars), solved problems Pi, penalty Fi
- Pi and Fi are integers from 0 to 10^9

#### Output Format
- Sorted list of participant logins, one per line

#### Example
```
Input:
alla 4 100
gena 6 1000
gosha 2 90
rita 2 90
timofey 4 80

Output:
gena
timofey
alla
gosha
rita
```

## ⚙️ Requirements

### System Requirements
- **Python:** 3.8 or higher
- **Memory:** 64MB (Broken Array), 17MB (Quick Sort)
- **Time Limits:** 1.5s (Broken Array), 0.5s (Quick Sort)

### Dependencies
- No external dependencies required
- Uses only Python standard library

## �� Usage

### Running Broken Array Search
```bash
python broken_array.py
```

### Running In-Place Quick Sort
```bash
python quick_sort_effective.py
```

### Input Methods
Both algorithms support:
- Standard input (stdin)
- File input (`input.txt`)
- Standard output (stdout)
- File output (`output.txt`)

## 📊 Performance

| Algorithm | Time Complexity | Space Complexity | Best Case | Worst Case |
|-----------|----------------|------------------|-----------|------------|
| Broken Array Search | O(log n) | O(1) | O(1) | O(log n) |
| In-Place Quick Sort | O(n log n) | O(1) | O(n log n) | O(n²) |

## 🎨 Algorithm Details

### Broken Array Search Implementation
The algorithm uses a modified binary search that handles the rotation point in the array. It determines which half of the array is sorted and applies binary search accordingly.

### In-Place Quick Sort Implementation
Uses the classic Quick Sort algorithm with in-place partitioning to avoid additional memory usage. The pivot selection uses the middle element for balanced performance.

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- Competitive programming problems from Yandex Academy
- Algorithm optimization techniques
- Python community for best practices

---

**Note:** For detailed information about each algorithm, please refer to the individual README files:
- `README(broken_array).md` - Detailed broken array search documentation
- `README(quick_sort_effective).md` - Detailed quick sort documentation
