---
description: Un único objeto Matrix puede almacenar una sola transformación o una secuencia de transformaciones.
ms.assetid: 1dc68ff8-6b17-4934-82da-ab2fc612aafa
title: Importancia del orden de transformación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a7350d63456902ff47183faa08170b3b2fef481
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127474282"
---
# <a name="why-transformation-order-is-significant"></a>Importancia del orden de transformación

Un único [**objeto Matrix**](/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) puede almacenar una sola transformación o una secuencia de transformaciones. El último se denomina *transformación**compuesta.*   La matriz de una transformación compuesta se obtiene multiplicando las matrices de las transformaciones individuales.

En una transformación compuesta, el orden de las transformaciones individuales es importante. Por ejemplo, si gira primero, escala y, a continuación, traduce, obtiene un resultado diferente que si primero traduce, gira y, a continuación, escala. En Windows GDI+, las transformaciones compuestas se construyen de izquierda a derecha. Si S, R y T son matrices de escala, rotación y traducción respectivamente, el producto SRT (en ese orden) es la matriz de la transformación compuesta que primero escala, gira y, a continuación, se traduce. La matriz producida por el producto SRT es diferente de la matriz producida por el producto TRS.

Un orden de razón es significativo es que las transformaciones como la rotación y el escalado se realizan con respecto al origen del sistema de coordenadas. El escalado de un objeto centrado en el origen produce un resultado diferente al de un objeto que se ha alejado del origen. De forma similar, la rotación de un objeto centrado en el origen produce un resultado diferente al de girar un objeto que se ha alejado del origen.

En el ejemplo siguiente se combina el escalado, la rotación y la traducción (en ese orden) para formar una transformación compuesta. El argumento [*:MatrixOrderAppend*'](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-matrixorder) pasado al método [**Graphics::RotateTransform**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-rotatetransform) especifica que la rotación seguirá el escalado. Del mismo modo, el argumento [*:MatrixOrderAppend**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-matrixorder) pasado al método [**Graphics::TranslateTransform**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-translatetransform) especifica que la traducción seguirá la rotación.


```
Rect rect(0, 0, 50, 50);
Pen pen(Color(255, 255, 0, 0), 0);
graphics.ScaleTransform(1.75f, 0.5f);
graphics.RotateTransform(28.0f, MatrixOrderAppend);
graphics.TranslateTransform(150.0f, 150.0f, MatrixOrderAppend);
graphics.DrawRectangle(&pen, rect);
```



En el ejemplo siguiente se realiza la misma llamada de método que en el ejemplo anterior, pero se invierte el orden de las llamadas. El orden resultante de las operaciones es, en primer lugar, traducir, girar, luego escalar, lo que genera un resultado muy diferente al de la primera escala, girar y, a continuación, traducir:


```
Rect rect(0, 0, 50, 50);
Pen pen(Color(255, 255, 0, 0), 0);
graphics.TranslateTransform(150.0f, 150.0f);
graphics.RotateTransform(28.0f, MatrixOrderAppend);
graphics.ScaleTransform(1.75f, 0.5f, MatrixOrderAppend);
graphics.DrawRectangle(&pen, rect);
```



Una manera de invertir el orden de las transformaciones individuales en una transformación compuesta es invertir el orden de una secuencia de llamadas a métodos. Una segunda manera de controlar el orden de las operaciones es cambiar el argumento de orden de matriz. El ejemplo siguiente es el mismo que el ejemplo anterior, salvo que se ha cambiado [*:MatrixOrderAppend**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-matrixorder) a [*:MatrixOrderPrepend**..](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-matrixorder) La multiplicación de matriz se realiza en el orden SRT, donde S, R y T son las matrices de escala, rotación y traducción, respectivamente. El orden de la transformación compuesta es escalar primero, girar y, a continuación, traducir.


```
Rect rect(0, 0, 50, 50);
Pen pen(Color(255, 255, 0, 0), 0);
graphics.TranslateTransform(150.0f, 150.0f,MatrixOrderPrepend);
graphics.RotateTransform(28.0f, MatrixOrderPrepend);
graphics.ScaleTransform(1.75f, 0.5f, MatrixOrderPrepend);
graphics.DrawRectangle(&pen, rect);
```



El resultado del ejemplo anterior es el mismo resultado que logramos en el primer ejemplo de esta sección. Esto se debe a que hemos invertido el orden de las llamadas al método y el orden de la multiplicación de la matriz.

 

 



