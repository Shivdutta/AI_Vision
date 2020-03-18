# EVA
# EVA_Assignment-1B

# What are Channels and Kernels (according to EVA)?
   ## Channels: 
      Channels are the containers of specific features. They do contain the information about the location of the specific feature and
      the score for that specific feature present. We have differnt channels containing different features ranging  from basic features
      to the most complex features of a given Image. The relation between the number of kernels in a layer is  number of kernels used in
      that layer  =  number of channels obtained from that layer.Also we do maxpooling from  those channels which contains meaningful
      edges & gradients, textures, Patterns, Parts of objects and objects. We do normalize the  values present in channels before doing
      further convolutions.
   ## Kernels:
      Kernels are also called feature extractors. They have the ability to extract features which might be simple or complex 
      features.Its better to have specific filters to do specific feature extractions. Having said that if we give too many than 
      required kernels, we can prune the unwanted kernels. Also if we give less kernels than needed, kernel has the ability to                 learn complex feature extractions. after doing a series of convolutions,kernels at specific receptive field as depends 
      on the domainn has the capability to extract meaningful features such as edges and gradients,textures, patterns, parts 
      of objects  and objects. In the initial layers Kernels extract low level features then middle level features and finally 
      the high  level features. Generally we use 3*3 sized kernels as feature extractors.
                
# Why should we only (well mostly) use 3x3 Kernels?
       a) A 3*3 Kernel which is a odd kernel has a line of symmetry so that it can see into left and right parts of image with
       equal priority.
       b) Since most people started using 3*3 kernels Nvidea has optimized its usage to be fast. then many people started using it
       and it became a cycle.
       c) All the other  kernels such as 5*5,7*7,11*11 etc can be simulated to get the exact result and the advantage by using 3*3
       kernels over other kernels is that we have very less parameters to learn for the CNN.
# How many times do we need to perform 3x3 convolution operation to reach 1x1 from 199x199 (show calculations)?
                
         199*199 ---3*3convolution---> 197*197 ---3*3convolution---> 195*195 ---3*3convolution---> 193*193 ---3*3convolution---> 191*191
         191*191 ---3*3convolution---> 189*189 ---3*3convolution---> 187*187 ---3*3convolution---> 185*185 ---3*3convolution--->183*183
         183*183 ---3*3convolution---> 181*181 ---3*3convolution---> 179*179 ---3*3convolution---> 177*177 ---3*3convolution---> 175*175
         175*175 ---3*3convolution---> 173*173 ---3*3convolution---> 171*171 ---3*3convolution---> 169*169 ---3*3convolution---> 167*167
         167*167 ---3*3convolution---> 165*165 ---3*3convolution---> 163*163 ---3*3convolution---> 161*161 ---3*3convolution---> 159*159
         159*159 ---3*3convolution---> 157*157 ---3*3convolution---> 155*155 ---3*3convolution---> 153*153 ---3*3convolution---> 151*151
         151*151 ---3*3convolution---> 149*149 ---3*3convolution---> 147*147 ---3*3convolution---> 145*145 ---3*3convolution---> 143*143
         143*143 ---3*3convolution---> 141*141 ---3*3convolution---> 139*139 ---3*3convolution---> 137*137 ---3*3convolution---> 135*135
         135*135 ---3*3convolution---> 133*133 ---3*3convolution---> 131*131 ---3*3convolution---> 129*129 ---3*3convolution---> 127*127
         127*127 ---3*3convolution---> 125*125 ---3*3convolution---> 123*123 ---3*3convolution---> 121*121 ---3*3convolution---> 119*119
         119*119 ---3*3convolution---> 117*117 ---3*3convolution---> 115*115 ---3*3convolution---> 113*113 ---3*3convolution---> 111*111
         111*111 ---3*3convolution---> 109*109 ---3*3convolution---> 107*107 ---3*3convolution---> 105*105 ---3*3convolution---> 103*103
         103*103 ---3*3convolution---> 101*101 ---3*3convolution---> 99*99   ---3*3convolution---> 97*97 ---3*3convolution ---> 95*95
         95*95 --3*3convolution---> 93*93 ---3*3convolution---> 91*91   ---3*3convolution---> 89*89 ---3*3convolution ---> 87*87
         87*87 --3*3convolution---> 85*85 ---3*3convolution---> 83*83   ---3*3convolution---> 81*81 ---3*3convolution ---> 79*79
         79*79 --3*3convolution---> 77*77 ---3*3convolution---> 75*75   ---3*3convolution---> 73*73 ---3*3convolution ---> 71*71
         71*71 --3*3convolution---> 69*69 ---3*3convolution---> 67*67   ---3*3convolution---> 65*65 ---3*3convolution ---> 63*63
         63*63 --3*3convolution---> 61*61 ---3*3convolution---> 59*59   ---3*3convolution---> 57*57 ---3*3convolution ---> 55*55
         55*55 --3*3convolution---> 53*53 ---3*3convolution---> 51*51   ---3*3convolution---> 49*49 ---3*3convolution ---> 47*47
         47*47 --3*3convolution---> 45*45 ---3*3convolution---> 43*43   ---3*3convolution---> 41*41 ---3*3convolution ---> 39*39
         39*39 --3*3convolution---> 37*37 ---3*3convolution---> 35*35   ---3*3convolution---> 33*33 ---3*3convolution ---> 31*31
         31*31 --3*3convolution---> 29*29 ---3*3convolution---> 27*27   ---3*3convolution---> 25*25 ---3*3convolution ---> 23*23
         23*23 --3*3convolution---> 21*21 ---3*3convolution---> 19*19   ---3*3convolution---> 17*17 ---3*3convolution ---> 15*15
         15*15 --3*3convolution---> 13*13 ---3*3convolution---> 11*11   ---3*3convolution---> 9*9 ---3*3convolution ---> 7*7        
         7*7 --3*3convolution---> 5*5 ---3*3convolution---> 3*3   ---3*3convolution---> 1*1
         
         
         
        

