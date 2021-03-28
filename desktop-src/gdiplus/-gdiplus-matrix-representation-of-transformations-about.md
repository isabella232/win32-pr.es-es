---
description: Una matriz m&\# 215; n es un conjunto de números organizados en m filas y n columnas. En la ilustración siguiente se muestran varias matrices.
ms.assetid: 62215ae0-b095-42b2-911c-aa7607a8b61a
title: Representación matricial de transformaciones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0577cae38c401e842cff2ff14179594f9118dfd2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809650"
---
# <a name="matrix-representation-of-transformations"></a>Representación matricial de transformaciones

Una matriz *m × n* es un conjunto de números organizados en *m* filas y *n* columnas. En la ilustración siguiente se muestran varias matrices.

![Ilustración que muestra seis matrices de dimensiones variables](images/aboutgdip05-art04.png)

Puede agregar dos matrices del mismo tamaño agregando elementos individuales. En la siguiente ilustración se muestran dos ejemplos de adición de matrices.

![Ilustración que muestra cómo realizar la adición de matrices](images/aboutgdip05-art05.png)

Una matriz *m × n* se puede multiplicar por una matriz *n × p* y el resultado es una matriz *m × p* . El número de columnas de la primera matriz debe ser el mismo que el número de filas de la segunda matriz. Por ejemplo, una matriz de 4 × 2 se puede multiplicar por una matriz de 2 × 3 para generar una matriz de 4 × 3.

Los puntos del plano y las filas y columnas de una matriz pueden considerarse como vectores. Por ejemplo, (2,5) es un vector con dos componentes, y (3, 7, 1) es un vector con tres componentes. El producto de punto de dos vectores se define de la siguiente manera:

(a, b) • (c, d) = AC + BD

(a, b, c) • (d, e, f) = ad + ser + CF

Por ejemplo, el producto DOT de (2, 3) y (5, 4) es (2) (5) + (3) (4) = 22. El producto de punto de (2, 5, 1) y (4, 3, 1) es (2) (4) + (5) (3) + (1) (1) = 24. Tenga en cuenta que el producto de punto de dos vectores es un número, no otro vector. Tenga en cuenta también que puede calcular el producto DOT solo si los dos vectores tienen el mismo número de componentes.

Permita A (i, j) ser la entrada en la matriz A de la **fila i** y **la columna j** . Por ejemplo, A (3, 2) es la entrada de la matriz A en la fila de 3 **Rd** y la columna 2 **ND** . Suponga que A, B y C son matrices y AB = C. Las entradas de C se calculan de la siguiente manera:

C (i, j) = (fila i de A) • (columna j de B)

En la ilustración siguiente se muestran varios ejemplos de multiplicación de matrices.

![Ilustración que muestra cómo realizar la multiplicación de matrices](images/aboutgdip05-art06.png)

Si piensa en un punto del plano como una matriz de 1 × 2, puede transformar ese punto multiplicándolo por una matriz de 2 × 2. En la ilustración siguiente se muestran varias transformaciones aplicadas al punto (2, 1).

![Ilustración que muestra cómo usar la multiplicación de matrices para escalar, girar o reflejar un punto en un plano](images/aboutgdip05-art07.png)

Todas las transformaciones que se muestran en la ilustración anterior son transformaciones lineales. Algunas otras transformaciones, como la traslación, no son lineales y no se pueden expresar como multiplicación por una matriz de 2 × 2. Supongamos que desea empezar con el punto (2, 1), girarlo 90 grados, traducir 3 unidades en la dirección x y traducir 4 unidades en la dirección y. Para ello, puede realizar una multiplicación de matrices seguida de una suma de matriz.

![Ilustración que muestra cómo la multiplicación y la suma de las matrices pueden girar un punto y convertirlo dos veces](images/aboutgdip05-art08.png)

Una transformación lineal (multiplicación por una matriz de 2 × 2) seguida de una traducción (adición de una matriz 1 × 2) se denomina transformación afín. Una alternativa al almacenamiento de una transformación afín en un par de matrices (una para la parte lineal y otra para la traducción) es almacenar toda la transformación en una matriz de 3 × 3. Para realizar este trabajo, un punto del plano debe almacenarse en una matriz de 1 × 3 con una tercera coordenada ficticia. La técnica habitual es hacer que todas las coordenadas de terceras sean iguales a 1. Por ejemplo, el punto (2, 1) se representa mediante la matriz \[ 2 1 1 \] . En la ilustración siguiente se muestra una transformación afín (gire 90 grados; traduzca 3 unidades en la dirección x, 4 unidades en la dirección y) expresadas como multiplicación por una sola matriz de 3 × 3.

![Ilustración que muestra cómo la multiplicación de matrices puede realizar una transformación afín](images/aboutgdip05-art09.png)

En el ejemplo anterior, el punto (2, 1) se asigna al punto (2, 6). Tenga en cuenta que la tercera columna de la matriz 3 × 3 contiene los números 0, 0, 1. Siempre será el caso de la matriz 3 × 3 de una transformación afín. Los números importantes son los seis números en las columnas 1 y 2. La parte superior izquierda 2 × 2 de la matriz representa la parte lineal de la transformación y las dos primeras entradas de la tercera fila representan la traducción.

![Ilustración que muestra que las dos primeras columnas son más importantes para una matriz de 3x3 de una transformación afín](images/aboutgdip05-art10.png)

En GDI+ de Windows, puede almacenar una transformación afín en un objeto de [**matriz**](/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) . Dado que la tercera columna de una matriz que representa una transformación afín siempre es (0, 0, 1), solo se especifican los seis números de las dos primeras columnas al construir un objeto de **matriz** . La instrucción `Matrix myMatrix(0.0f, 1.0f, -1.0f, 0.0f, 3.0f, 4.0f);` crea la matriz mostrada en la ilustración anterior.

## <a name="composite-transformations"></a>Transformaciones compuestas

Una transformación compuesta es una secuencia de transformaciones, una seguida de la otra. Tenga en cuenta las matrices y las transformaciones en la lista siguiente:

-   Matriz A gira 90 grados
-   Escala de la matriz B en un factor de 2 en la dirección x
-   La matriz C traduce 3 unidades en la dirección y

Si empieza con el punto (2, 1) (representado por la matriz \[ 2 1 1) \] y multiplica por a, entonces B y después a C, el punto (2, 1) se someterá a las tres transformaciones en el orden mostrado.

\[2 1 1 \] ABC = \[ – 2 5 1\]

En lugar de almacenar las tres partes de la transformación compuesta en tres matrices independientes, puede multiplicar A, B y C a la vez para obtener una sola matriz de 3 × 3 que almacena toda la transformación compuesta. Supongamos que es ABC = D. Después, un punto multiplicado por D proporciona el mismo resultado que un punto multiplicado por a, a continuación, B y después a C.

\[2 1 1 \] D = \[ – 2 5 1\]

En la ilustración siguiente se muestran las matrices A, B, C y D.

![Ilustración que muestra cómo realizar varias transformaciones multiplicando las matrices constituyentes](images/aboutgdip05-art12.png)

El hecho de que se pueda formar la matriz de una transformación compuesta multiplicando las matrices de transformación individuales significa que cualquier secuencia de transformaciones afines puede almacenarse en un objeto de [**matriz**](/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) único.

> [!Note]  
> El orden de una transformación compuesta es importante. En general, gire, después escale y, a continuación, translate no es lo mismo que Scale, después Rotate y, después, translate. Del mismo modo, es importante el orden de multiplicación de la matriz. En general, ABC no es lo mismo que CPF.

 

La clase [**Matrix**](/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) proporciona varios métodos para crear una transformación compuesta: [**Matrix:: Multiply**](/windows/desktop/api/Gdiplusmatrix/nf-gdiplusmatrix-matrix-multiply), [**Matrix:: Rotate**](/windows/desktop/api/Gdiplusmatrix/nf-gdiplusmatrix-matrix-rotate), [**Matrix:: RotateAt**](/windows/desktop/api/Gdiplusmatrix/nf-gdiplusmatrix-matrix-rotateat), [**Matrix:: scale**](/windows/desktop/api/Gdiplusmatrix/nf-gdiplusmatrix-matrix-scale), [**Matrix:: cizalla**](/windows/desktop/api/Gdiplusmatrix/nf-gdiplusmatrix-matrix-shear)y [**Matrix:: translate**](/windows/desktop/api/Gdiplusmatrix/nf-gdiplusmatrix-matrix-translate). En el ejemplo siguiente se crea la matriz de una transformación compuesta que primero gira 30 grados, después se escala por un factor de 2 en la dirección y y, a continuación, convierte 5 unidades en la dirección x.


```
Matrix myMatrix;
myMatrix.Rotate(30.0f);
myMatrix.Scale(1.0f, 2.0f, MatrixOrderAppend);
myMatrix.Translate(5.0f, 0.0f, MatrixOrderAppend);
```



En la ilustración siguiente se muestra la matriz.

![Ilustración en la que se muestra una matriz con valores expresados como funciones trigonométricas y una matriz con valores aproximados de esas funciones.](images/aboutgdip05-art13.png)

 

 



