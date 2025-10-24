<h1>ExpNo 5 : Implement Simple Hill Climbing Algorithm</h1> 
<h3>Name:Hoshini S           </h3>
<h3>Register Number:2305003006            </h3>
<H3>Aim:</H3>
<p>Implement Simple Hill Climbing Algorithm and Generate a String by Mutating a Single Character at each iteration </p>
<h2> Theory: </h2>
<p>Hill climbing is a variant of Generate and test in which feedback from test procedure is used to help the generator decide which direction to move in search space.
Feedback is provided in terms of heuristic function
</p>


<h2>Algorithm:</h2>
<p>
<ol>
 <li> Evaluate the initial state.If it is a goal state then return it and quit. Otherwise, continue with initial state as current state.</li> 
<li>Loop until a solution is found or there are no new operators left to be applied in current state:
<ul><li>Select an operator that has not yet been applied to the current state and apply it to produce a new state</li>
<li>Evaluate the new state:
  <ul>
<li>if it is a goal state, then return it and quit</li>
<li>if it is not a goal state but better than current state then make new state as current state</li>
<li>if it is not better than current state then continue in the loop</li>
    </ul>
</li>
</ul>
</li>
</ol>

</p>
<hr>
<h3> Steps Applied:</h3>
<h3>Step-1</h3>
<p> Generate Random String of the length equal to the given String</p>
<h3>Step-2</h3>
<p>Mutate the randomized string each character at a time</p>
<h3>Step-3</h3>
<p> Evaluate the fitness function or Heuristic Function</p>
<h3>Step-4:</h3>
<p> Lopp Step -2 and Step-3  until we achieve the score to be Zero to achieve Global Minima.</p>

## PROGRAM
```python
import random, string

target = input("Enter target: ")
s = ''.join(random.choice(string.ascii_letters + ' ') for _ in target)

def fit(x): return sum(a == b for a, b in zip(x, target))

while s != target:
    n = list(s)
    n[random.randrange(len(n))] = random.choice(string.ascii_letters + ' ')
    n = ''.join(n)
    if fit(n) >= fit(s):
        s = n
        print(s)

print("🎯 Final:", s)

SimpleHillClimbing()
```

<hr>
<h2>Sample Input and Output</h2>
<h2>Sample String:</h2>Welcome
<h2>Output:</h2>
Enter target: welcome
nwkqUgD
nwkLUgD
nwkLMgD
nwkLMgP
nwkLMMP
nwkLqMP
nwLLqMP
nJLLqMP
nJTLqMP
QJTLqMP
QZTLqMP
QZTLqMM
QZdLqMM
RZdLqMM
RZoLqMM
RZoyqMM
RZoyqMT
RVoyqMT
RVoyqMj
RVoyCMj
OVoyCMj
OVoyCMO
OVoyCMT
OVtyCMT
OVGyCMT
OVGUCMT
OVGUCfT
OVGUFfT
OVGUFfu
OVGUXfu
cVGUXfu
cVGUpfu
cVGUqfu
cVGUqft
cVGUqfh
cVGUqf 
cVGUqP 
cVGUqPk
cVGUqPm
cVqUqPm
cmqUqPm
cOqUqPm
cOeUqPm
cOtUqPm
cOtUqNm
cOtUqNW
cktUqNW
qktUqNW
qktUqHW
qktUqHW
qktUqHQ
qktuqHQ
qktuqHN
qktuqHS
qktuAHS
qktuDHS
oktuDHS
okLuDHS
okLuDdS
okLuYdS
XkLuYdS
NkLuYdS
NkLsYdS
NkLSYdS
NkLSYds
NkLSYws
NkLSYLs
NkLSYLE
mkLSYLE
mkVSYLE
mkVSuLE
mkVSuLq
mkVSuLm
mkVSubm
mkVSfbm
mkVBfbm
mkSBfbm
mkSBfbs
CkSBfbs
CkSBJbs
CkSBrbs
CkYBrbs
CFYBrbs
CFvBrbs
VFvBrbs
VFvBrVs
VFxBrVs
VoxBrVs
VoxBVVs
VoxBVms
SoxBVms
SoZBVms
roZBVms
rUZBVms
JUZBVms
JVZBVms
JjZBVms
JjHBVms
JXHBVms
JpHBVms
JpHFVms
JpHFhms
JpJFhms
JpJAhms
JBJAhms
JBJAhmI
JBJAhmV
JBzAhmV
JDzAhmV
JDzAhmV
JdzAhmV
JdzApmV
JdzJpmV
JdlJpmV
JelJpmV
PelJpmV
PeltpmV
PelhpmV
PelhNmV
PelyNmV
PelyqmV
PelyqmI
JelyqmI
Jelyqms
Jelyqme
Jelyfme
Jelefme
Velefme
Veleome
Velyome
jelyome
jelFome
jelnome
Oelnome
OelHome
selHome
WelHome
XelHome
XelDome
MelDome
lelDome
EelDome
EelDome
XelDome
Xelyome
XelUome
SelUome
velUome
velHome
FelHome
Fel ome
tel ome
gel ome
pel ome
pelqome
zelqome
zelEome
aelEome
JelEome
JelOome
QelOome
Qeljome
aeljome
aelFome
aelqome
aelvome
aelWome
aelQome
aelKome
EelKome
Eeljome
Deljome
Veljome
Velsome
Lelsome
LelOome
Lelnome
LelAome
LelAome
LelWome
Lelmome
Nelmome
yelmome
yeleome
Eeleome
Eelcome
Belcome
jelcome
Celcome
Celcome
welcome
🎯 Final: welcome
​
