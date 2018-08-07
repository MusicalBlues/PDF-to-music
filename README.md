# PDF-to-music

#!/usr/bin/env python3
# -*- coding: utf-8 -*-
"""
Created on Mon Aug  6 11:43:18 2018

@author: Dimihollo ./p2mp /Users/Dimihollo/Desktop/"Bach BWV609.pdf" -format XML -pathdest /Users/Dimihollo/Desktop/
"""
import sys, os
import subprocess

path = ('/Users/Dimihollo/Applications')

path1 = ('/Users/Dimihollo/Desktop/' + sys.argv[1])
path2=('/Users/Dimihollo/Desktop/')


#subprocess.run('pwd')

#os.chdir(path1)
os.chdir(path)

for scores in os.listdir(path1):
     
    PDF_to_music = "./p2mp path1 -format XML -pathdest path2".split()
    
    os.chdir(path)
    
    subprocess.run([path[0:],PDF_to_music[0],path1[0:],scores,PDF_to_music[2],PDF_to_music[3],PDF_to_music[4],path2])
    
#subprocess.check_output and .run
#./p2mp /Users/Dimihollo/Desktop/"Bill Evans - New Jazz Conceptions - I Got It Bad (And That Aint Good).pdf" -format XML -pathdest /Users/Dimihollo/Desktop    

