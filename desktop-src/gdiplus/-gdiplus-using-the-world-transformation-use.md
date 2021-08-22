---
description: La transformación del mundo es una propiedad de la clase Graphics.
ms.assetid: 22f43b29-ea7b-4faf-9795-2242bf704ed3
title: Utilizar la transformación de coordenadas universales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6288b5640e330a827e96b632541dac44e9463b87c566c16a94797810c4c92c0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118977245"
---
# <a name="using-the-world-transformation"></a>Utilizar la transformación de coordenadas universales

La transformación del mundo es una propiedad de la [**clase Graphics.**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) Los números que especifican la transformación del mundo se almacenan en un [**objeto Matrix,**](/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) que representa una matriz de 3 ×3. Las **clases Matrix** y **Graphics** tienen varios métodos para establecer los números en la matriz de transformación del mundo. Los ejemplos de esta sección manipulan rectángulos porque los rectángulos son fáciles de dibujar y es fácil ver los efectos de las transformaciones en los rectángulos.

Comenzamos creando un rectángulo de 50 por 50 y ubicándose en el origen (0, 0). El origen está en la esquina superior izquierda del área de cliente.


```
Rect rect(0, 0, 50, 50);
Pen pen(Color(255, 255, 0, 0), 0);
graphics.DrawRectangle(&pen, rect);
```



El código siguiente aplica una transformación de escalado que expande el rectángulo por un factor de 1,75 en la dirección x y reduce el rectángulo en un factor de 0,5 en la dirección y:


```
Rect rect(0, 0, 50, 50);
Pen pen(Color(255, 255, 0, 0), 0);
graphics.ScaleTransform(1.75f, 0.5f);
graphics.DrawRectangle(&pen, rect);
```



El resultado es un rectángulo que es más largo en la dirección x y más corto en la dirección y que el original.

Para girar el rectángulo en lugar de escalarlo, use el código siguiente en lugar del código anterior:


```
Rect rect(0, 0, 50, 50);
Pen pen(Color(255, 255, 0, 0), 0);
graphics.RotateTransform(28.0f);
graphics.DrawRectangle(&pen, rect);
```



Para traducir el rectángulo, use el código siguiente:


```
Rect rect(0, 0, 50, 50);
Pen pen(Color(255, 255, 0, 0), 0);
graphics.TranslateTransform(150.0f, 150.0f);
graphics.DrawRectangle(&pen, rect);
```



 

 



