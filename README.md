#!/usr/bin/env python
#coding:utf-8
from heapq import merge
def merge_sort(seq):
  if len(seq)<=1:
    return seq
  else:
    middle=len(seq)/2
    left=merge_sort(seq[:middle])
    right=merge_sort(seq[middle:])
    return list(merge(left,right))
if __name__=="__main__":
  seq=[1,3,7,5,9,8]
  print merge_sort(seq)
