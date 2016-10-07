# TP-Shell
TP Shell - LP CSID

QUESTIONS : 

1 - lister les fichiers *.java
find -name '*.java'


2 - compter


3 - lister les fichiers et leur nombre de ligne de code
find . -name \*.java | wc -l


4 - lister les 10 plus gros fichiers
(find . -name \*.java -exec wc -l {} \;) | sort -n | tail -10



5 - compter le nombre total de ligne de code java

total = 0
for f in $(find -name \*.java)
do
count = $cat $f | grep -v '^( \t)*$' | wc -l)
total=$(($total + $count))
done
echo $total
