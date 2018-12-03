Program up_case;
Uses crt;
Const n =10; k1=10; k2=2*k1+1;
Type vec=array[1..n] of integer;
Var a,b :vec;
k,i,f,r :integer;
ch :char;
l :Boolean;
Begin
Repeat
ClrScr;
Randomize;
Write("Вихідний масив a[i]=");
For i:=1 to n do
Begin
f:=Random(k2);
a[i]:=k1-f;
Write(a[i]:3);
End;
Writeln;
b:=a;
Repeat
l:=true;
for i:=1 to n-1 do
If b[i]>b[i+1] then
Begin
r:=b[i];b[i]:=b[i+1]; b[i+1]:=r; l:=false;
End;
Until l;
("WriteУпорядкований масив b[i]=");
For i:=1 to n do Write(b[i]:3);
Readln;
ch:=ReadKey;
Until ch=#27;
End.
