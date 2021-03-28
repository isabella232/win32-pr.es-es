---
description: Un objeto de matriz único puede almacenar una transformación única o una secuencia de transformaciones.
ms.assetid: 1dc68ff8-6b17-4934-82da-ab2fc612aafa
title: Importancia del orden de transformación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a7350d63456902ff47183faa08170b3b2fef481
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984423"
---
# <a name="why-transformation-order-is-significant"></a>Importancia del orden de transformación

Un objeto de [**matriz**](/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) único puede almacenar una transformación única o una secuencia de transformaciones. Esto último se denomina transformación *compuesta*.   La matriz de una transformación compuesta se obtiene multiplicando las matrices de las transformaciones individuales.

En una transformación compuesta, el orden de las transformaciones individuales es importante. Por ejemplo, si primero se gira, después se realiza la escala y después se traduce, se obtiene un resultado diferente que si primero se traslada, después se gira y luego se escala. En GDI+ de Windows, las transformaciones compuestas se crean de izquierda a derecha. Si S, R y T son matrices de escala, rotación y traducción, respectivamente, el producto SRT (en ese orden) es la matriz de la transformación compuesta que se escala primero, luego gira y luego se convierte. La matriz generada por el producto SRT es diferente de la que genera el producto de la.

Un orden de razón es importante es que las transformaciones como la rotación y el escalado se realizan con respecto al origen del sistema de coordenadas. El escalado de un objeto que está centrado en el origen genera un resultado diferente que el escalado de un objeto que se ha quitado del origen. Del mismo modo, la rotación de un objeto que está centrado en el origen genera un resultado diferente que la rotación de un objeto que se ha quitado del origen.

En el ejemplo siguiente se combina el escalado, la rotación y la traslación (en ese orden) para formar una transformación compuesta. El argumento [* * * * MatrixOrderAppend * *](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-matrixorder) * * que se pasa al método [**Graphics:: RotateTransform**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-rotatetransform) especifica que el giro seguirá el escalado. Del mismo modo, el argumento * * * * [MatrixOrderAppend * *](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-matrixorder) * * que se pasa al método [**Graphics:: TranslateTransform**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-translatetransform) especifica que la conversión seguirá a la rotación.


```
Rect rect(0, 0, 50, 50);
Pen pen(Color(255, 255, 0, 0), 0);
graphics.ScaleTransform(1.75f, 0.5f);
graphics.RotateTransform(28.0f, MatrixOrderAppend);
graphics.TranslateTransform(150.0f, 150.0f, MatrixOrderAppend);
graphics.DrawRectangle(&pen, rect);
```



En el ejemplo siguiente se realizan las mismas llamadas al método que en el ejemplo anterior, pero se invierte el orden de las llamadas. El orden resultante de las operaciones se traduce primero, después se gira y luego se escala, lo que genera un resultado muy diferente de la primera escala, y luego gira y, a continuación, traduce:


```
Rect rect(0, 0, 50, 50);
Pen pen(Color(255, 255, 0, 0), 0);
graphics.TranslateTransform(150.0f, 150.0f);
graphics.RotateTransform(28.0f, MatrixOrderAppend);
graphics.ScaleTransform(1.75f, 0.5f, MatrixOrderAppend);
graphics.DrawRectangle(&pen, rect);
```



Una manera de invertir el orden de las transformaciones individuales en una transformación compuesta es invertir el orden de una secuencia de llamadas a métodos. Una segunda manera de controlar el orden de las operaciones es cambiar el argumento de orden de la matriz. El ejemplo siguiente es el mismo que el anterior, salvo que [* * * * MatrixOrderAppend * *](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-matrixorder) * * se ha cambiado a [* * * * MatrixOrderPrepend * *](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-matrixorder)* *. La multiplicación de matrices se realiza en el orden SRT, donde S, R y T son las matrices para la escala, la rotación y la traslación, respectivamente. En primer lugar, el orden de la transformación compuesta es la primera escala, la rotación y la traslación.


```
Rect rect(0, 0, 50, 50);
Pen pen(Color(255, 255, 0, 0), 0);
graphics.TranslateTransform(150.0f, 150.0f,MatrixOrderPrepend);
graphics.RotateTransform(28.0f, MatrixOrderPrepend);
graphics.ScaleTransform(1.75f, 0.5f, MatrixOrderPrepend);
graphics.DrawRectangle(&pen, rect);
```



El resultado del ejemplo anterior es el mismo resultado que hemos logrado en el primer ejemplo de esta sección. Esto se debe a que se invirtió el orden de las llamadas al método y el orden de la multiplicación de la matriz.

 

 



