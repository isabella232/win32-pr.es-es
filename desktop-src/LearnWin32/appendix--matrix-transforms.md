---
title: 'Apéndice: Transformaciones de matriz'
description: En este tema se proporciona información general matemática de las transformaciones de matriz para gráficos 2D.
ms.assetid: 8cc01f45-dd84-4f3e-a5f2-26edc5cbdfa1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12d02976446824bba07829173bb326338a55732b39c640c93319630a209096b7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118389335"
---
# <a name="appendix-matrix-transforms"></a>Apéndice: Transformaciones de matriz

En este tema se proporciona información general matemática de las transformaciones de matriz para gráficos 2D. Sin embargo, no es necesario conocer las matemáticas de matriz para poder usar transformaciones en Direct2D. Lea este tema si está interesado en las matemáticas; De lo contrario, no dude en omitir este tema.

-   [Introducción a matrices](#introduction-to-matrices)
    -   [Operaciones de matriz](#matrix-operations)
-   [Transformaciones afín](#affine-transforms)
    -   [Transformación de traducción](#translation-transform)
    -   [Transformación de escalado](#scaling-transform)
    -   [Rotación alrededor del origen](#rotation-around-the-origin)
    -   [Rotación alrededor de un punto arbitrario](#rotation-around-an-arbitrary-point)
    -   [Transformación de asimetría](#skew-transform)
-   [Representación de transformaciones en Direct2D](#representing-transforms-in-direct2d)
-   [Siguiente](#next)

## <a name="introduction-to-matrices"></a>Introducción a matrices

Una matriz es una matriz rectangular de números reales. El *orden* de la matriz es el número de filas y columnas. Por ejemplo, si la matriz tiene 3 filas y 2 columnas, el orden es 3 × 2. Normalmente, las matrices se muestran con los elementos de matriz entre corchetes:

![Matriz de 3 x 2.](images/matrix01.png)

Notación: una matriz se designa mediante una letra mayúscula. Los elementos se designan con letras minúsculas. Los subíndices indican el número de fila y columna de un elemento. Por ejemplo, un *ij* es el elemento de la fila i'th y la columna j'th de la matriz A.

El diagrama siguiente muestra una matriz i × j, con los elementos individuales de cada celda de la matriz.

![una matriz con filas i y columnas j.](images/matrix15.png)

### <a name="matrix-operations"></a>Operaciones de matriz

En esta sección se describen las operaciones básicas definidas en matrices.

*Adición* de . La suma A + B de dos matrices se obtiene agregando los elementos correspondientes de A y B:

<dl> A + B = \[ a *ij* \]  +  \[ b *ij* \]  =  \[ a *ij* + b *ij*\]
</dl>

*Multiplicación escalar.* Esta operación multiplica una matriz por un número real. Dado un número real *k*, el producto escalar kA se obtiene multiplicando cada elemento de A por *k*.

<dl> kA = k \[ a *ij* \]  =  \[ k × a *ij*\]
</dl>

*Multiplicación de matriz.* Dadas dos matrices A y B con order (m × n) y (n × p), el producto C = A × B es una matriz con order (m × p), definida de la siguiente manera:

![Muestra una fórmula para la multiplicación de matrices.](images/matrix02.png)

o, de forma equivalente:

<dl> c *ij* = a *i* 1 x b1 *j* + a *i* 2 x b2 *j* + ... + a *in* +*bck*  
</dl>

Es decir, para calcular cada elemento c *ij*, haga lo siguiente:

1.  Tome la fila i'th de A y la columna j'th de B.
2.  Multiplique cada par de elementos de la fila y columna: la primera entrada de fila por la primera entrada de columna, la segunda entrada de fila por la segunda entrada de columna, etc.
3.  Sumar el resultado.

Este es un ejemplo de multiplicación de una matriz (2 × 2) por una matriz (2 × 3).

![multiplicación de matriz.](images/matrix03.png)

La multiplicación de matrices no es conmutativa. Es decir, A × B ≠ B × A. Además, a partir de la definición se sigue que no se pueden multiplicar todos los pares de matrices. El número de columnas de la matriz de la izquierda debe ser igual al número de filas de la matriz de la derecha. De lo contrario, × operador no está definido.

*Identifique la matriz*. Una matriz de identidad, designada I, es una matriz cuadrada definida de la siguiente manera:

<dl> I *ij* = 1 si *i*  =  *j* o 0 en caso contrario.  
</dl>

En otras palabras, una matriz de identidad contiene 1 para cada elemento donde el número de fila es igual al número de columna y cero para todos los demás elementos. Por ejemplo, esta es la matriz de identidades 3 × 3.

![matriz de identidad.](images/matrix04.png)

Las siguientes igualdades se mantienen para cualquier matriz M.

<dl> M x I = M  
I x M = M  
</dl>

## <a name="affine-transforms"></a>Transformaciones afín

Una *transformación afín es* una operación matemática que asigna un espacio de coordenadas a otra. En otras palabras, asigna un conjunto de puntos a otro conjunto de puntos. Las transformaciones afín tienen algunas características que las hacen útiles en los gráficos del equipo.

-   Las transformaciones afín conservan *la colisión.* Si tres o más puntos se quedan en una línea, siguen formando una línea después de la transformación. Las líneas rectas permanecen rectas.
-   La composición de dos transformaciones afín es una transformación afín.

Las transformaciones afín para el espacio 2D tienen el formato siguiente.

![Muestra una transformación afín para el espacio 2D.](images/matrix05.png)

Si aplica la definición de multiplicación de matriz que se ha dado anteriormente, puede mostrar que el producto de dos transformaciones afín es otra transformación afín. Para transformar un punto 2D mediante una transformación afín, el punto se representa como una matriz 1 × 3.

<dl> P = \| x y 1 \|  
</dl>

Los dos primeros elementos contienen las coordenadas x e y del punto. El 1 se coloca en el tercer elemento para que las matemáticas funcionen correctamente. Para aplicar la transformación, multiplique las dos matrices como se muestra a continuación.

<dl> P' = P × M  
</dl>

Esto se expande a lo siguiente.

![transformación de affine.](images/matrix06.png)

where

<dl> x' = ax + cy + e  
y' = bx + dy + f  
</dl>

Para obtener el punto transformado, tome los dos primeros elementos de la matriz P'.

<dl> p = (x', y') = (ax + cy + e, bx + dy + f)  
</dl>

> [!Note]  
> Una matriz × *n se* denomina vector *de fila*. Tanto Direct2D como Direct3D usan vectores de fila para representar puntos en espacio 2D o 3D. Puede obtener un resultado equivalente mediante un vector de columna *(n* × 1) y la matriz de transformación. La mayoría de los textos gráficos usan el formato de vector de columna. En este tema se presenta el formato de vector de fila para mantener la coherencia con Direct2D y Direct3D.

 

Las siguientes secciones derivan las transformaciones básicas.

### <a name="translation-transform"></a>Transformación de traducción

La matriz de transformación de traducción tiene el formato siguiente.

![transformación de traducción.](images/matrix07.png)

La conexión de un *punto P* a esta ecuación produce:

<dl> P' = (*x*  +  *dx*, *y*  +  *dy*)
</dl>

que corresponde al punto (x, y) traducido por *dx* en el eje X y *dy* en el eje Y.

![diagrama que muestra la traducción de dos puntos.](images/graphics22.png)

### <a name="scaling-transform"></a>Transformación de escalado

La matriz de transformación de escalado tiene el formato siguiente.

![transformación de escalado.](images/matrix09.png)

La conexión de un *punto P* a esta ecuación produce:

<dl> P' = (*x* ( *dx*, *y* *)*
</dl>

que corresponde al punto (x,y) escalado por *dx* y *dy*.

![diagrama que muestra el escalado de dos puntos.](images/graphics23.png)

### <a name="rotation-around-the-origin"></a>Rotación alrededor del origen

La matriz para girar un punto alrededor del origen tiene el formato siguiente.

![Muestra una fórmula para una transformación de rotación.](images/matrix11.png)

El punto transformado es:

<dl> P' = (*x* cosΘ – ysinA, *x* sinN + *y* cos):
</dl>

Prueba. Para mostrar que P' representa una rotación, considere el diagrama siguiente.

![diagrama que muestra la rotación alrededor del origen.](images/graphics24.png)

Con estas premisas:

<dl> <dt>

<span id="P____x_y_"></span><span id="p____x_y_"></span><span id="P____X_Y_"></span>P = (x,y)
</dt> <dd>

Punto original que se debe transformar.

</dd> <dt>

Φ
</dt> <dd>

Ángulo formado por la línea (0,0) a P.

</dd> <dt>

Θ
</dt> <dd>

Ángulo por el que se va a girar (x,y) sobre el origen.

</dd> <dt>

<span id="P_____x__y__"></span><span id="p_____x__y__"></span><span id="P_____X__Y__"></span>P' = (x', y')
</dt> <dd>

Punto transformado.

</dd> <dt>

<span id="R"></span><span id="r"></span>R
</dt> <dd>

Longitud de la línea (0,0) a P. También el radio del círculo de rotación.

</dd> </dl>

> [!Note]  
> En este diagrama se usa el sistema de coordenadas estándar que se usa en la geometría, donde el eje Y positivo apunta hacia arriba. Direct2D usa el Windows coordenadas, donde el eje Y positivo apunta hacia abajo.

 

El ángulo entre el eje X y la línea (0,0) a P' es А + Θ. Las siguientes identidades se mantienen:

<dl> x = R cos  
y = R sin Y  
x' = R cos(Θ + Θ)  
y' = R sin(Θ+ Θ)  
</dl>

Ahora, resuelva x' e y' en términos de Θ. Por las fórmulas de adición trigonométricas:

<dl> x' = R(cos YcosA – sinАsin): Rcos YcosA – IosNSinS  
y' = R(sinАcos + cosАsin): Iosn Ycos Y + Rcos YSinS  
</dl>

Sustituyendo, se obtiene lo siguiente:

<dl> x' = xcos – ysinΘ  
y' = xsin( + ycos)  
</dl>

que corresponde al punto transformado P' mostrado anteriormente.

### <a name="rotation-around-an-arbitrary-point"></a>Rotación alrededor de un punto arbitrario

Para girar alrededor de un punto (x,y) distinto del origen, se usa la siguiente matriz.

![transformación de rotación.](images/matrix13.png)

Puede derivar esta matriz tomando el punto (x,y) como origen.

![diagrama que muestra la rotación alrededor de un punto.](images/graphics25.png)

Deje que (x1, y1) sea el punto que resulta de girar el punto (x0, y0) alrededor del punto (x,y). Podemos derivar x1 como se muestra a continuación.

<dl> x1 = (x0 – x)cosΘ– (y0 – y)sinΘ + x  
x1 = x0cosΘ – y0sinΘ + \[ (1 – cosΘ) + ysin): \]  
</dl>

Ahora vuelva a conectar esta ecuación a la matriz de transformación con la fórmula x1 = ax0 + cy0 + e anterior. Use el mismo procedimiento para derivar y1.

### <a name="skew-transform"></a>Transformación de sesgo

La transformación de sesgo se define mediante cuatro parámetros:

-   ): la cantidad que se sesga a lo largo del eje X, medida como un ángulo desde el eje Y.
-   ): la cantidad que se sesga a lo largo del eje Y, medida como un ángulo desde el eje X.
-   (*px*, *py*): las coordenadas x e y del punto sobre el que se realiza la asimetría.

La transformación de sesgo usa la siguiente matriz.

![transformación de sesgo.](images/matrix14.png)

El punto transformado es:

<dl> P' = (*x*  +  *y* tan – *py* tanA, *y*  +  *x* tanA) – *py* tanA
</dl>

o de forma equivalente:

<dl> P' = (*x* + (*y* – *py*)tan, *y* + (*x* – *px*)tanA)
</dl>

Para ver cómo funciona esta transformación, considere cada componente individualmente. El parámetro Θ mueve cada punto de la dirección x en una cantidad igual a tan/. En el diagrama siguiente se muestra la relación entre Θ y el sesgo del eje X.

![Diagrama que muestra la asimetría a lo largo del eje X.](images/graphics26.png)

Este es el mismo sesgo aplicado a un rectángulo:

![Diagrama que muestra la asimetría a lo largo del eje X cuando se aplica a un rectángulo.](images/graphics27.png)

El parámetro Ö tiene el mismo efecto, pero a lo largo del eje Y:

![Diagrama que muestra la asimetría a lo largo del eje Y.](images/graphics28.png)

En el diagrama siguiente se muestra la asimetría del eje Y aplicada a un rectángulo.

![Diagrama que muestra la asimetría a lo largo del eje Y cuando se aplica a un rectángulo.](images/graphics29.png)

Por último, los parámetros *px* *y py* desplazan el punto central de la asimetría a lo largo de los ejes X e Y.

## <a name="representing-transforms-in-direct2d"></a>Representación de transformaciones en Direct2D

Todas las transformaciones de Direct2D son transformaciones afín. Direct2D no admite transformaciones no afín. Las transformaciones se representan mediante la [**estructura D2D1 \_ MATRIX \_ 3X2 \_ F.**](/windows/desktop/Direct2D/d2d1-matrix-3x2-f) Esta estructura define una matriz de 3 × 2. Dado que la tercera columna de una transformación afín es siempre la misma (0, 0, 1 ) y porque Direct2D no admite transformaciones no afín, no es necesario especificar toda la \[ \] matriz de 3 × 3. Internamente, Direct2D usa 3 × 3 matrices para calcular las transformaciones.

Los miembros de [**D2D1 \_ MATRIX \_ 3X2 \_ F**](/windows/desktop/Direct2D/d2d1-matrix-3x2-f) se denominan según su posición de índice: **\_ el miembro 11** es elemento (1,1), el **\_ miembro 12** es elemento (1,2), etc. Aunque puede inicializar los miembros de la estructura directamente, se recomienda usar la [**clase D2D1::Matrix3x2F.**](/windows/desktop/api/d2d1helper/nl-d2d1helper-matrix3x2f) Esta clase hereda **D2D1 \_ MATRIX \_ 3X2 \_ F** y proporciona métodos auxiliares para crear cualquiera de las transformaciones afín básicas. La clase también define [**el \* operador ()**](/windows/desktop/api/d2d1helper/nf-d2d1helper-matrix3x2f-operator-mult) para componer dos o más transformaciones, como se describe en Aplicar transformaciones [en Direct2D.](applying-transforms-in-direct2d.md)

## <a name="next"></a>Siguientes

[Módulo 4. Entrada del usuario](module-4--user-input.md)

 

 