---
description: La transformación universal es una propiedad de la clase Graphics.
ms.assetid: 22f43b29-ea7b-4faf-9795-2242bf704ed3
title: Utilizar la transformación de coordenadas universales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2138df1bbd2be6d3329695fc6898da49da93b3b4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275372"
---
# <a name="using-the-world-transformation"></a>Utilizar la transformación de coordenadas universales

La transformación universal es una propiedad de la clase [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) . Los números que especifican la transformación universal se almacenan en un objeto de [**matriz**](/windows/desktop/api/gdiplusmatrix/nl-gdiplusmatrix-matrix) , que representa una matriz de 3 × 3. Las clases **Matrix** y **Graphics** tienen varios métodos para establecer los números en la matriz de transformación universal. En los ejemplos de esta sección se manipulan los rectángulos porque los rectángulos son fáciles de dibujar y resulta sencillo ver los efectos de las transformaciones en los rectángulos.

Comenzaremos creando un rectángulo de 50 por 50 y buscándolo en el origen (0,0). El origen se encuentra en la esquina superior izquierda del área cliente.


```
Rect rect(0, 0, 50, 50);
Pen pen(Color(255, 255, 0, 0), 0);
graphics.DrawRectangle(&pen, rect);
```



En el código siguiente se aplica una transformación de escala que expande el rectángulo por un factor de 1,75 en la dirección x y reduce el rectángulo entre un factor de 0,5 en la dirección y:


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



 

 



