o100 sub
  (helical hole milling, load tool and set feed first, then use like so:)
  (o100 call [x pos] [y pos] [safety height] [hole depth] [hole dia] [tool dia])
  (tool dia doesn't have to be specified exactly.)
#4=[0 - #4]
#7=[#6 / 2]  (#7 is depth per circle = half of tool diameter)
#8=[#3 - #7] (#8 is current depth step)
g0 z#3
(start above and right so we make a convex corner for entry to the ccw arcs)
g0 x[#1 + #6] y[#2 + [#5 / 2]] 
g41 g0 x#1 y[#2 + [#5 / 2]]
o101 while [#8 GT #4]
(down toward the specified depth a bit at a time)
g3 x#1 y[#2 + [#5 / 2]] i0 j[0 - [#5 / 2]] z#8
#8=[#8 - #7]
o101 endwhile
(down to the actual depth)
g3 x#1 y[#2 + [#5 / 2]] i0 j[0 - [#5 / 2]] z#4
(full circle at the actual depth)
g3 x#1 y[#2 + [#5 / 2]] i0 j[0 - [#5 / 2]]
g0 z#3
g40
o100 endsub

