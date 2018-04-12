# <div align = center>gSpan</div>

 **gSpan** is an algorithm for mining frequent subgraphs.

gSpan implemented on Python 2.7. This program supports undirected graphs as well as directed graphs. 

### How to run

This program supports both **Python 2** and **Python 3**.

```
$ python main.py [-s min_support] [-n num_graph] [-l min_num_vertices] [-u max_num_vertices] [-d True/False] [-v True/False] [-p True/False] [-w True/False] [-h] database_file_name 
```

##### example runs

- Read graph data from ./graphdata/graph.data, and mine undirected subgraphs given min support is 5000
```
$ python main.py -s 5000 ./graphdata/graph.data
```

- Read graph data from ./graphdata/graph.data, mine undirected subgraphs given min support is 5000, and visualize these frequent subgraphs(matplotlib and networkx are required)
```
$ python main.py -s 5000 -p True ./graphdata/graph.data
```

- Read graph data from ./graphdata/graph.data, and mine directed subgraphs given min support is 5000
```
$ python main.py -s 5000 -d True ./graphdata/graph.data
```

- Print help info
```
$ python main.py -h
```

The author also wrote [example code](https://github.com/betterenvi/gSpan/blob/master/main.ipynb) using Jupyter Notebook. Mining results and visualizations are presented. For detail, please refer to [main.ipynb](https://github.com/betterenvi/gSpan/blob/master/main.ipynb).

### Running time

- Environment
    + OS: Windows 10
    + Python version: Python 2.7.12
    + Processor: Intel(R) Core(TM) i7-4790 CPU @ 3.60GHz 3.60 GHz
    + Ram: 8.00 GB


- Running time
On the dataset [./graphdata/graph.data](https://github.com/betterenvi/gSpan/blob/master/graphdata/graph.data), running time is listed below:


| Min support | Number of frequent subgraphs | time |
| --- | --- | --- |
| 5000 | 26 | 51.48 s |
| 3000 | 52 | 69.07 s |
| 1000 | 455 | 3 m 49 s |
| 600 | 1235 | 7 m 29 s |
| 400 | 2710 | 12 m 53 s |

### Forked from
- [gSpan](https://github.com/betterenvi/gSpan)

### Reference
- [Paper](http://www.cs.ucsb.edu/~xyan/papers/gSpan-short.pdf)

gSpan: Graph-Based Substructure Pattern Mining, by X. Yan and J. Han. 
Proc. 2002 of Int. Conf. on Data Mining (ICDM'02). 

- [gboost](http://www.nowozin.net/sebastian/gboost/)

One C++ implementation of gSpan.
