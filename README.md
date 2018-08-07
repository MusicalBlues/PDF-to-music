#!/usr/bin/env python3
# -*- coding: utf-8 -*-
"""
Created on Mon Aug  6 11:43:18 2018

@author: Dimihollo ./p2mp /Users/Dimihollo/Desktop/"Bach BWV609.pdf" -format XML -pathdest /Users/Dimihollo/Desktop/
"""
import sys
import os
import glob
import subprocess

exe = '/Users/Dimihollo/Applications/p2mp'

def convert(score, dest):
    cmd = [exe, f'{score}', '-format', 'XML', '-pathdest', f'{dest}']
    print(score)
    print(cmd[0:])
    subprocess.check_output(cmd)
    subprocess.run(cmd[0:])
    
#./p2mp /Users/Dimihollo/Desktop/"Bill Evans - New Jazz Conceptions - I Got It Bad (And That Aint Good).pdf" -format XML -pathdest /Users/Dimihollo/Desktop    

if __name__ == '__main__':
    src_dir = sys.argv[1]
    target_dir = sys.argv[2]
    
    os.chdir(src_dir)
    for score in glob.glob('*.pdf'):
        convert(score, target_dir)
