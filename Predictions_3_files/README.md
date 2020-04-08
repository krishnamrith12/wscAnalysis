### For calculating statistical significance :

Requirements include : `scipy numpy`

1. Run the python file `save_stats.py` to save the sentence level UAS and LAS.
```
python save_stats.py BiAFF/Test.conll DCST/Test.conll
```

- This should generate files named `results1_las.txt  results1_uas.txt  results2_las.txt  results2_uas.txt` where 1 refers to BiAFF and 2 refers to DCST.


2. Run significance test for UAS results:
```
python test_significance.py results1_uas.txt results2_uas.txt 0.05
```

- This should prompt user for the type of test. For t-test, type `t-test`
- Program should print the p-value of the test
- Similarly run for LAS

`test_significance.py` has been used from [this repo](https://github.com/rtmdrr/testSignificanceNLP) with some changes to adapt the code for Python3. 
