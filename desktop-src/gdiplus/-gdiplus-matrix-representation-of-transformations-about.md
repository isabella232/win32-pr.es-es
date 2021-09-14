---
description: Una matriz m&215;n es un conjunto de \# números organizados en m filas y n columnas. En la ilustración siguiente se muestran varias matrices.
ms.assetid: 62215ae0-b095-42b2-911c-aa7607a8b61a
title: Representación matricial de transformaciones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0577cae38c401e842cff2ff14179594f9118dfd2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127072421"
---
# <a name="matrix-representation-of-transformations"></a>Representación matricial de transformaciones

Una *matriz m×n* es un conjunto de números organizados en *m* filas y *n* columnas. En la ilustración siguiente se muestran varias matrices.

![ilustración en la que se muestran seis matrices de dimensiones variables](images/aboutgdip05-art04.png)

Puede agregar dos matrices del mismo tamaño agregando elementos individuales. En la ilustración siguiente se muestran dos ejemplos de adición de matrices.

![ilustración que muestra cómo realizar la adición de matrices](images/aboutgdip05-art05.png)

Una *matriz m×n* se puede multiplicar por una matriz *n×p* y el resultado es una matriz *m×p.* El número de columnas de la primera matriz debe ser el mismo que el número de filas de la segunda matriz. Por ejemplo, una matriz de 4 ×2 se puede multiplicar por una matriz de 2 ×3 para generar una matriz de 4 ×3.

Los puntos del plano y las filas y columnas de una matriz se pueden pensar como vectores. Por ejemplo, (2, 5) es un vector con dos componentes y (3, 7, 1) es un vector con tres componentes. El producto de punto de dos vectores se define de la siguiente manera:

(a, b) • (c, d) = ac + bd

(a, b, c) • (d, e, f) = ad + be + cf

Por ejemplo, el producto de puntos de (2, 3) y (5, 4) es (2)(5) + (3)(4) = 22. El producto de puntos de (2, 5, 1) y (4, 3, 1) es (2)(4) + (5)(3) + (1)(1) = 24. Tenga en cuenta que el producto de puntos de dos vectores es un número, no otro vector. Tenga en cuenta también que solo puede calcular el producto de puntos si los dos vectores tienen el mismo número de componentes.

Deje que A(i, j) sea la entrada de la matriz A en **la** fila i y la **columna** j. Por ejemplo, A(3, 2) es la entrada de la matriz A en la fila 3 **rd** y la segunda **columna.** Supongamos que A, B y C son matrices y AB = C. Las entradas de C se calculan de la manera siguiente:

C(i, j) = (fila i de A) • (columna j de B)

En la ilustración siguiente se muestran varios ejemplos de multiplicación de matrices.

![ilustración en la que se muestra cómo realizar la multiplicación de matrices](images/aboutgdip05-art06.png)

Si piensa en un punto del plano como una matriz de 1 × 2, puede transformar ese punto multiplicándose por una matriz de 2 × 2. En la ilustración siguiente se muestran varias transformaciones aplicadas al punto (2, 1).

![ilustración que muestra cómo usar la multiplicación de matrices para escalar, girar o reflejar un punto en un plano](images/aboutgdip05-art07.png)

Todas las transformaciones que se muestran en la ilustración anterior son transformaciones lineales. Algunas otras transformaciones, como la traducción, no son lineales y no se pueden expresar como multiplicación mediante una matriz de 2 × 2. Imagine que quiere empezar con el punto (2, 1), girarlo 90 grados, traducirlo 3 unidades en la dirección x y traducirlo 4 unidades en la dirección y. Para ello, realice una multiplicación de matrices seguida de una adición de matriz.

![ilustración que muestra cómo la multiplicación y la suma de la matriz pueden girar un punto y traducirlo dos veces](images/aboutgdip05-art08.png)

Una transformación lineal (multiplicación por una matriz de 2 × 2) seguida de una traducción (adición de una matriz de 1 × 2) se denomina transformación afín. Una alternativa al almacenamiento de una transformación afín en un par de matrices (una para la parte lineal y otra para la traducción) es almacenar toda la transformación en una matriz de 3 × 3. Para que esto funcione, un punto del plano debe almacenarse en una matriz de 1 × 3 con una tercera coordenada ficticia. La técnica habitual es hacer que todas las terceras coordenadas sea igual a 1. Por ejemplo, el punto (2, 1) se representa mediante la \[ matriz 2 1 1 \] . En la ilustración siguiente se muestra una transformación afín (girar 90 grados; traducir 3 unidades en la dirección x, 4 unidades en la dirección y) expresada como multiplicación por una sola matriz de 3 × 3.

![ilustración que muestra cómo la multiplicación de matrices puede realizar una transformación afín](images/aboutgdip05-art09.png)

En el ejemplo anterior, el punto (2, 1) se asigna al punto (2, 6). Tenga en cuenta que la tercera columna de la matriz 3 × 3 contiene los números 0, 0, 1. Este siempre será el caso de la matriz 3 × 3 de una transformación afín. Los números importantes son los seis números de las columnas 1 y 2. La parte superior izquierda 2 × 2 de la matriz representa la parte lineal de la transformación y las dos primeras entradas de la tercera fila representan la traducción.

![ilustración que muestra que las dos primeras columnas son más significativas para una matriz 3x3 de una transformación afín](images/aboutgdip05-art10.png)

En Windows GDI+ puede almacenar una transformación afín en un [**objeto Matrix.**](/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) Dado que la tercera columna de una matriz que representa una transformación afín siempre es (0, 0, 1), solo se especifican los seis números de las dos primeras columnas al construir un objeto **Matrix.** La instrucción `Matrix myMatrix(0.0f, 1.0f, -1.0f, 0.0f, 3.0f, 4.0f);` construye la matriz que se muestra en la ilustración anterior.

## <a name="composite-transformations"></a>Transformaciones compuestas

Una transformación compuesta es una secuencia de transformaciones, una seguida de la otra. Tenga en cuenta las matrices y transformaciones de la lista siguiente:

-   Matriz A Girar 90° grados
-   Matriz B Escala por un factor de 2 en la dirección x
-   Matriz C Traducir 3 unidades en la dirección y

Si empieza con el punto (2, 1), representado por la matriz 2 1 1, y multiplica por A, después B y, a continuación, C, el punto \[ (2,1) se someterá a las tres transformaciones en \] el orden indicado.

\[2 1 1 \] ABC = \[ –2 5 1\]

En lugar de almacenar las tres partes de la transformación compuesta en tres matrices independientes, puede multiplicar A, B y C para obtener una única matriz de 3 × 3 que almacena toda la transformación compuesta. Supongamos QUE ABC = D. A continuación, un punto multiplicado por D proporciona el mismo resultado que un punto multiplicado por A, después B y, a continuación, C.

\[2 1 1 \] D = \[ –2 5 1\]

En la ilustración siguiente se muestran las matrices A, B, C y D.

![ilustración en la que se muestra cómo realizar varias transformaciones multiplicando las matrices constituyentes](images/aboutgdip05-art12.png)

El hecho de que la matriz de una transformación compuesta se pueda formar multiplicando las matrices de transformación individuales significa que cualquier secuencia de transformaciones afín se puede almacenar en un único objeto [**Matrix.**](/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix)

> [!Note]  
> El orden de una transformación compuesta es importante. En general, rote y, a continuación, escale, la traducción no es la misma que la escala, luego rote y, a continuación, traduzca. Del mismo modo, el orden de multiplicación de la matriz es importante. En general, ABC no es lo mismo que BAC.

 

La [**clase Matrix**](/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) proporciona varios métodos para crear una transformación compuesta: [**Matrix::Multiply**](/windows/desktop/api/Gdiplusmatrix/nf-gdiplusmatrix-matrix-multiply), [**Matrix::Rotate**](/windows/desktop/api/Gdiplusmatrix/nf-gdiplusmatrix-matrix-rotate), [**Matrix::RotateAt**](/windows/desktop/api/Gdiplusmatrix/nf-gdiplusmatrix-matrix-rotateat), [**Matrix::Scale**](/windows/desktop/api/Gdiplusmatrix/nf-gdiplusmatrix-matrix-scale), [**Matrix::Shear**](/windows/desktop/api/Gdiplusmatrix/nf-gdiplusmatrix-matrix-shear)y [**Matrix::Translate**](/windows/desktop/api/Gdiplusmatrix/nf-gdiplusmatrix-matrix-translate). En el ejemplo siguiente se crea la matriz de una transformación compuesta que gira primero 30 grados, luego se escala por un factor de 2 en la dirección y y, a continuación, convierte 5 unidades en la dirección x.


```
Matrix myMatrix;
myMatrix.Rotate(30.0f);
myMatrix.Scale(1.0f, 2.0f, MatrixOrderAppend);
myMatrix.Translate(5.0f, 0.0f, MatrixOrderAppend);
```



En la ilustración siguiente se muestra la matriz.

![ilustración que muestra una matriz con valores expresados como funciones trigonométricas y una matriz con valores aproximados de esas funciones](images/aboutgdip05-art13.png)

 

 



