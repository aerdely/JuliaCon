# Visualizando dependencia probabilística con Pluto.jl

La función *cópula* 
$C_{X,Y}$
de un vector aleatorio $(X,Y)$ es la relación funcional entre la función de distribución conjunta de probabilidades $F_{X,Y}$ de dicho vector aleatorio y las respectivas funciones de distribución de probabilidad marginales $F_X$ y $F_Y$ de las variables aleatorias de dicho vector aleatorio, esto es:

$\mathbb{P}(X\leq x, Y\leq y)=F_{X,Y}(x,y)=C_{X,Y}(F_X(x),F_Y(y))$

Esto significa que toda la información sobre la dependencia entre las variables $(X,Y)$ 
está en la cópula subyacente 
$C_{X,Y}$ que es una función $[0,1]\times[0,1]\rightarrow[0,1]$ que puede deducirse mediante:

$C_{X,Y}(u,v)=F_{X,Y}(F_X^{-1}(u), F_Y^{-1}(v))$

Las distribuciones marginales individuales
$F_X$ y $F_Y$ 
nada aportan sobre la dependencia, y sí estorban para su análisis, por lo que es necesario eliminar su efecto para analizar los datos de la cópula subyacente, que puede obtenerse de la siguiente forma: Si 
$(x_1,y_1),\ldots,(x_n,y_n)$
son datos observados del vector aleatorio
$(X,Y)$ 
basta definir 
$u_k=F_X(x_k)$ y $v_k=F_Y(y_k)$
para $k\in\{1,\ldots,n\}$ y así los pares de valores
$(u_1,v_1),\ldots,(u_n,v_n)$ son los valores observados de la cópula subyacente, ya sin la distorsión de la distribuciones marginales.
