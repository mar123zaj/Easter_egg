# What is Easter_egg? #

This is simple python module which contains program for competition from this site: http://golf.coding-dojo-silesia.pl/.<br/>
Organiser: [firemark](https://github.com/firemark/)<br/>
Goal of this contest was to write the code to draw an easter egg using the smallest possible amount of characters.<br/>
There's no requirements needed because module uses only built-in packages.

## How to use it? ##

Open terminal and write `python3 cc.py {command1,arg1:command2,arg1,arg2,…,argN:…:commandN,arg1,...}`.

Command is one of the following functions:
-zigzag with following arguments: character, size
```
zigzag,Q,5
Q         QQ         QQ         QQ         QQ         QQ    
 Q       Q  Q       Q  Q       Q  Q       Q  Q       Q  Q   
  Q     Q    Q     Q    Q     Q    Q     Q    Q     Q    Q  
   Q   Q      Q   Q      Q   Q      Q   Q      Q   Q      Q 
    Q Q        Q Q        Q Q        Q Q        Q Q        Q
```
-maze   with following arguments: character, width, height
```
maze,Q,5,5
Q    QQQQQQ    QQQQQQ    QQQQQQ    QQQQQQ    QQQQQQ    QQQQQ
Q    Q    Q    Q    Q    Q    Q    Q    Q    Q    Q    Q    
Q    Q    Q    Q    Q    Q    Q    Q    Q    Q    Q    Q    
Q    Q    Q    Q    Q    Q    Q    Q    Q    Q    Q    Q    
QQQQQQ    QQQQQQ    QQQQQQ    QQQQQQ    QQQQQQ    QQQQQQ
```
-cross  with following arguments: character, size
```
cross,Q,5
  Q     Q     Q     Q     Q     Q     Q     Q     Q     Q   
  Q     Q     Q     Q     Q     Q     Q     Q     Q     Q   
QQQQQ QQQQQ QQQQQ QQQQQ QQQQQ QQQQQ QQQQQ QQQQQ QQQQQ QQQQQ 
  Q     Q     Q     Q     Q     Q     Q     Q     Q     Q   
  Q     Q     Q     Q     Q     Q     Q     Q     Q     Q  
```
-hstrip with following arguments: character, height, shift(to next line)
```
hstrip,Q,5,5
Q     Q     Q     Q     Q     Q     Q     Q     Q     Q     
Q     Q     Q     Q     Q     Q     Q     Q     Q     Q     
Q     Q     Q     Q     Q     Q     Q     Q     Q     Q     
Q     Q     Q     Q     Q     Q     Q     Q     Q     Q     
Q     Q     Q     Q     Q     Q     Q     Q     Q     Q 

```
-vstrip with following arguments: character
```
vstrip,Q
QQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQ
```
-empty  with following arguments: size(amount of lines)

### Example ###

```
python cc.py zigzag,c,9:cross,V,5:zigzag,I,5:cross,e,7:hstrip,e,1,1:cross,X,3:vstrip,o:zigzag,A,7:
cross,b,7:cross,K,7
```

And we obtain:
```
                      @@@@@@@@@@@@@@@@                      
                   @@@              c @@@                   
                 @@  c             c    c@@                 
               @@     c           c      c @@               
             @@        c         c        c  @@             
            @c          c       c          c   @            
           @c            c     c            c   @           
          @c              c   c              c   @          
         @c                c c                c c @         
        @     V     V     V     V     V     V     V@        
       @V     V     V     V     V     V     V     V @       
      @VVVV VVVVV VVVVV VVVVV VVVVV VVVVV VVVVV VVVVV@      
     @  V     V     V     V     V     V     V     V   @     
    @   V     V     V     V     V     V     V     V    @    
    @     II         II         II         II         I@    
   @     I  I       I  I       I  I       I  I       I  @   
  @     I    I     I    I     I    I     I    I     I    @  
  @I   I      I   I      I   I      I   I      I   I     @  
  @ I I        I I        I I        I I        I I      @  
 @ e       e       e       e       e       e       e      @ 
 @ e       e       e       e       e       e       e      @ 
@  e       e       e       e       e       e       e       @
@eeeeee eeeeeee eeeeeee eeeeeee eeeeeee eeeeeee eeeeeee eee@
@  e       e       e       e       e       e       e       @
@  e       e       e       e       e       e       e       @
@  e       e       e       e       e       e       e       @
@ e e e e e e e e e e e e e e e e e e e e e e e e e e e e e@
@X   X   X   X   X   X   X   X   X   X   X   X   X   X   X @
@XX XXX XXX XXX XXX XXX XXX XXX XXX XXX XXX XXX XXX XXX XXX@
@X   X   X   X   X   X   X   X   X   X   X   X   X   X   X @
@oooooooooooooooooooooooooooooooooooooooooooooooooooooooooo@
@             AA             AA             AA             @
@A           A  A           A  A           A  A           A@
@ A         A    A         A    A         A    A         A @
 @ A       A      A       A      A       A      A       A @ 
  @ A     A        A     A        A     A        A     A @  
  @  A   A          A   A          A   A          A   A  @  
   @@ A A            A A            A A            A A @@   
     @     b       b       b       b       b       b  @     
      @@   b       b       b       b       b       b@@      
        @@ b       b       b       b       b      @@        
          @@bbb bbbbbbb bbbbbbb bbbbbbb bbbbbbb @@          
            @@@    b       b       b       b @@@            
               @@@@b       b       b     @@@@               
                   @@@@@@@@@@@@@@@@@@@@@@             
```