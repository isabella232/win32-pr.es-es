---
title: 'Apéndice: Transformaciones de matriz'
description: En este tema se proporciona una introducción matemática de transformaciones de matriz para gráficos 2D.
ms.assetid: 8cc01f45-dd84-4f3e-a5f2-26edc5cbdfa1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a5a9b09f75b17e4baf8afe5e7fde8643c06982f
ms.sourcegitcommit: ee06501cc29132927ade9813e0888aaa4decc487
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/28/2021
ms.locfileid: "104555992"
---
# <a name="appendix-matrix-transforms"></a>Apéndice: transformaciones de matriz

En este tema se proporciona una introducción matemática de transformaciones de matriz para gráficos 2D. Sin embargo, no es necesario conocer la aritmética de matrices para usar transformaciones en Direct2D. Lea este tema si está interesado en las matemáticas; de lo contrario, no dude en omitir este tema.

-   [Introducción a las matrices](#introduction-to-matrices)
    -   [Operaciones de matriz](#matrix-operations)
-   [Transformaciones afines](#affine-transforms)
    -   [Transformación de traslación](#translation-transform)
    -   [Transformación de escala](#scaling-transform)
    -   [Giro alrededor del origen](#rotation-around-the-origin)
    -   [Giro alrededor de un punto arbitrario](#rotation-around-an-arbitrary-point)
    -   [Sesgar transformación](#skew-transform)
-   [Representar transformaciones en Direct2D](#representing-transforms-in-direct2d)
-   [Siguiente](#next)

## <a name="introduction-to-matrices"></a>Introducción a las matrices

Una matriz es una matriz rectangular de números reales. El *orden* de la matriz es el número de filas y columnas. Por ejemplo, si la matriz tiene 3 filas y dos columnas, el orden es 3 × 2. Las matrices se suelen mostrar con los elementos de la matriz entre corchetes:

![matriz 3 x 2.](images/matrix01.png)

Notación: una matriz se designa con una letra mayúscula. Los elementos se designan con letras minúsculas. Los subíndices indican el número de fila y columna de un elemento. Por ejemplo, un *ij* es el elemento de la fila i i y la columna j'th de la matriz a.

En el diagrama siguiente se muestra una matriz i × j, con los elementos individuales en cada celda de la matriz.

![matriz con i filas y j columnas.](images/matrix15.png)

### <a name="matrix-operations"></a>Operaciones de matriz

En esta sección se describen las operaciones básicas definidas en las matrices.

*Adición*. La suma A + B de dos matrices se obtiene agregando los elementos correspondientes de A y B:

<dl> A + b = \[ a *ij* \]  +  \[ B *ij* \]  =  \[ a *ij* + b *ij*\]
</dl>

*Multiplicación escalar*. Esta operación multiplica una matriz por un número real. Dado un número *k* real, el producto escalar Ka se obtiene multiplicando todos los elementos de a por *k*.

<dl> Ka = k \[ a *ij* \]  =  \[ k × a *ij*\]
</dl>

*Multiplicación de matrices*. Dadas dos matrices A y B con Order (m × n) y (n × p), el producto C = A × B es una matriz con Order (m × p), definida de la manera siguiente:

![Muestra una fórmula para la multiplicación de matrices.](images/matrix02.png)

o, de forma equivalente:

<dl> c *ij* = a *i* 1 x B1 *j* + a *i* 2 x B2 *j* +... + a *in* + b *NJ*  
</dl>

Es decir, para calcular cada elemento c *ij*, haga lo siguiente:

1.  Tome la fila i i de y la columna j'th de B.
2.  Multiplica cada par de elementos de la fila y la columna: la primera entrada de la primera columna, la segunda entrada de la fila en la segunda entrada de la columna, etc.
3.  Suma el resultado.

Este es un ejemplo de la multiplicación de una matriz (2 × 2) por una matriz (2 × 3).

![multiplicación de matrices.](images/matrix03.png)

La multiplicación de matrices no es conmutativa. Es decir, A × B ≠ B × A. Además, a partir de la definición se sigue que no todos los pares de matrices se pueden multiplicar. El número de columnas de la matriz de la izquierda debe ser igual al número de filas de la matriz de la derecha. De lo contrario, no se define el operador ×.

*Identifique la matriz*. Una matriz de identidad, designada como I, es una matriz cuadrada definida de la siguiente manera:

<dl> I *ij* = 1 si *i*  =  *j* o 0 en caso contrario.  
</dl>

En otras palabras, una matriz de identidad contiene 1 para cada elemento donde el número de fila es igual al número de columna y cero para todos los demás elementos. Por ejemplo, esta es la matriz de identidad 3 × 3.

![matriz de identidad.](images/matrix04.png)

La siguiente es la igualdad de la matriz M.

<dl> M x I = M  
I x M = M  
</dl>

## <a name="affine-transforms"></a>Transformaciones afines

Una *transformación afín* es una operación matemática que asigna un espacio de coordenadas a otro. En otras palabras, asigna un conjunto de puntos a otro conjunto de puntos. Las transformaciones afines tienen algunas características que las hacen útiles en los gráficos de los equipos.

-   Las transformaciones afines conservan la *colinealidad*. Si tres o más puntos se encuentran en una línea, seguirán formando una línea después de la transformación. Las líneas rectas permanecen rectas.
-   La composición de dos transformaciones afines es una transformación afín.

Las transformaciones afines para el espacio 2D tienen el formato siguiente.

![Muestra una transformación afín para el espacio 2D.](images/matrix05.png)

Si aplica la definición de la multiplicación de matrices proporcionada anteriormente, puede mostrar que el producto de dos transformaciones afines es otra transformación afín. Para transformar un punto 2D mediante una transformación afín, el punto se representa como una matriz de 1 × 3.

<dl> P = \| x y 1 \|  
</dl>

Los dos primeros elementos contienen las coordenadas x e y del punto. El 1 se coloca en el tercer elemento para que las operaciones matemáticas funcionen correctamente. Para aplicar la transformación, multiplique las dos matrices como se indica a continuación.

<dl> P ' = P × M  
</dl>

Se expande a lo siguiente.

![transformación afín.](images/matrix06.png)

where

<dl> x ' = AX + CY + e  
y ' = BX + DY + f  
</dl>

Para obtener el punto transformado, tome los dos primeros elementos de la matriz P '.

<dl> p = (x ', y ') = (AX + CY + e, BX + DY + f)  
</dl>

> [!Note]  
> Una matriz de 1 × *n* se denomina *Vector de fila*. Tanto Direct2D como Direct3D usan vectores de filas para representar puntos en el espacio 2D o 3D. Puede obtener un resultado equivalente mediante el uso de un vector de columna (*n* × 1) y transponer la matriz de transformación. La mayoría de los textos gráficos usan el formato de vector de columna. En este tema se presenta el formato de vector de fila para mantener la coherencia con Direct2D y Direct3D.

 

En las siguientes secciones se derivan las transformaciones básicas.

### <a name="translation-transform"></a>Transformación de traslación

La matriz de transformación de traslación tiene el formato siguiente.

![transformación de traslación.](images/matrix07.png)

La conexión de un punto *P* a esta ecuación produce:

<dl> P ' = (*x*  +  *DX*, *y*  +  *DY*)
</dl>

que corresponde al punto (x, y) traducido por *DX* en el eje x y *DY* en el eje y.

![diagrama que muestra la conversión de dos puntos.](images/graphics22.png)

### <a name="scaling-transform"></a>Transformación de escala

La matriz de transformación de escala tiene el formato siguiente.

![transformación de escalado.](images/matrix09.png)

La conexión de un punto *P* a esta ecuación produce:

<dl> P ' = (*x* enviada *DX*, *y* enviada *DY*)
</dl>

que corresponde al punto (x, y) escalado por *DX* y *DY*.

![diagrama que muestra el escalado de dos puntos.](images/graphics23.png)

### <a name="rotation-around-the-origin"></a>Giro alrededor del origen

La matriz para girar un punto alrededor del origen tiene el formato siguiente.

![Muestra una fórmula para una transformación de giro.](images/matrix11.png)

El punto transformado es:

<dl> P ' = (*x* CosΘ – ysinΘ, *x* sinΘ + *y* cosΘ)
</dl>

Justificar. Para mostrar que P ' representa una rotación, considere el siguiente diagrama.

![diagrama que muestra el giro alrededor del origen.](images/graphics24.png)

Con estas premisas:

<dl> <dt>

<span id="P____x_y_"></span><span id="p____x_y_"></span><span id="P____X_Y_"></span>P = (x, y)
</dt> <dd>

Punto original que se va a transformar.

</dd> <dt>

Φ
</dt> <dd>

El ángulo formado por la línea (0,0) a P.

</dd> <dt>

Θ
</dt> <dd>

Ángulo por el que se va a girar (x, y) el origen.

</dd> <dt>

<span id="P_____x__y__"></span><span id="p_____x__y__"></span><span id="P_____X__Y__"></span>P ' = (x ', y ')
</dt> <dd>

Punto transformado.

</dd> <dt>

<span id="R"></span><span id="r"></span>C
</dt> <dd>

Longitud de la línea (0,0) a P. También es el radio del círculo de rotación.

</dd> </dl>

> [!Note]  
> En este diagrama se usa el sistema de coordenadas estándar que se usa en Geometry, donde el eje y positivo apunta hacia arriba. Direct2D usa el sistema de coordenadas de Windows, donde el eje y positivo apunta hacia abajo.

 

El ángulo entre el eje x y la línea (0,0) a P ' es Φ + Θ. Las siguientes identidades contienen:

<dl> x = R cosΦ  
y = R sinΦ  
x ' = R cos (Φ + Θ)  
y ' = R sin (Φ + Θ)  
</dl>

Ahora se resuelve para x ' e y ' en términos de Θ. Por las fórmulas de suma trigonométrica:

<dl> x ' = R (cosΦcosΘ – sinΦsinΘ) = RcosΦcosΘ – RsinΦsinΘ  
y ' = R (sinΦcosΘ + cosΦsinΘ) = RsinΦcosΘ + RcosΦsinΘ  
</dl>

Sustituyendo:

<dl> x ' = xcosΘ – ysinΘ  
y ' = xsinΘ + ycosΘ  
</dl>

que corresponde al punto P ' transformado que se mostró anteriormente.

### <a name="rotation-around-an-arbitrary-point"></a>Giro alrededor de un punto arbitrario

Para girar alrededor de un punto (x, y) que no sea el origen, se usa la matriz siguiente.

![transformación de giro.](images/matrix13.png)

Puede derivar esta matriz tomando el punto (x, y) como el origen.

![diagrama que muestra la rotación alrededor de un punto.](images/graphics25.png)

Let (x1, Y1) es el punto que es el resultado de girar el punto (x0, Y0) alrededor del punto (x, y). Se puede derivar x1 como se indica a continuación.

<dl> x1 = (x0 – x) cosΘ – (Y0 – y) sinΘ + x  
x1 = x0cosΘ – y0sinΘ + \[ (1 – cosΘ) + ysinΘ \]  
</dl>

A continuación, vuelva a conectar esta ecuación a la matriz de transformación con la fórmula x1 = aX0 + cy0 + e anterior. Use el mismo procedimiento para derivar Y1.

### <a name="skew-transform"></a>Sesgar transformación

La transformación de sesgo se define mediante cuatro parámetros:

-   Θ: la cantidad que se va a sesgar a lo largo del eje x, medida como un ángulo desde el eje y.
-   Φ: la cantidad que se va a sesgar a lo largo del eje y, medida como un ángulo del eje x.
-   (*PX*, *py*): las coordenadas x e y del punto sobre el que se realiza el sesgo.

La transformación de sesgo utiliza la matriz siguiente.

![transformación de sesgo.](images/matrix14.png)

El punto transformado es:

<dl> P ' = (*x*  +  *y* tanΘ – *py* tanΘ, *y*  +  *x* tanΦ) – *py* tanΦ
</dl>

o equivalente:

<dl> P ' = (*x* + (*y* – *py*) tanΘ, *y* + (*x* – *PX*) tanΦ)
</dl>

Para ver cómo funciona esta transformación, considere cada componente individualmente. El parámetro Θ mueve cada punto en la dirección x en una cantidad igual a tanΘ. En el diagrama siguiente se muestra la relación entre Θ y el sesgo del eje x.

![Diagrama que muestra el sesgo a lo largo del eje x.](images/graphics26.png)

Este es el mismo sesgo aplicado a un rectángulo:

![Diagrama que muestra el sesgo a lo largo del eje x cuando se aplica a un rectángulo.](images/graphics27.png)

El parámetro Φ tiene el mismo efecto, pero a lo largo del eje y:

![Diagrama que muestra el sesgo a lo largo del eje y.](images/graphics28.png)

En el siguiente diagrama se muestra el sesgo del eje y aplicado a un rectángulo.

![Diagrama que muestra el sesgo a lo largo del eje y cuando se aplica a un rectángulo.](images/graphics29.png)

Por último, los parámetros *PX* y *py* desplazan el punto central para el sesgo a lo largo de los ejes x e y.

## <a name="representing-transforms-in-direct2d"></a>Representar transformaciones en Direct2D

Todas las transformaciones de Direct2D son transformaciones afines. Direct2D no admite transformaciones no afines. Las transformaciones se representan mediante la estructura D2D1 de la [**\_ matriz de \_ 3x2 \_ F**](/windows/desktop/Direct2D/d2d1-matrix-3x2-f) . Esta estructura define una matriz de 3 × 2. Dado que la tercera columna de una transformación afín siempre es la misma ( \[ 0, 0, 1 \] ) y dado que Direct2D no admite transformaciones no afines, no es necesario especificar toda la matriz de 3 × 3. Internamente, Direct2D usa 3 × 3 matrices para calcular las transformaciones.

A los miembros de [**la \_ matriz D2D1 \_ 3x2 \_ F**](/windows/desktop/Direct2D/d2d1-matrix-3x2-f) se les asigna un nombre según su posición de índice: el miembro **\_ 11** es Element (1,1), el miembro **\_ 12** es Element (1, 2), etc. Aunque puede inicializar los miembros de la estructura directamente, se recomienda usar la clase [**D2D1:: Matrix3x2F**](/windows/desktop/api/d2d1helper/nl-d2d1helper-matrix3x2f) . Esta clase hereda **D2D1 \_ Matrix \_ 3x2 \_ F** y proporciona métodos auxiliares para crear cualquiera de las transformaciones afines básicas. La clase también define [**Operator \* ()**](/windows/desktop/api/d2d1helper/nf-d2d1helper-matrix3x2f-operator-mult) para crear dos o más transformaciones, como se describe en [aplicar transformaciones en Direct2D](applying-transforms-in-direct2d.md).

## <a name="next"></a>Siguientes

[Módulo 4. Datos proporcionados por el usuario](module-4--user-input.md)

 

 