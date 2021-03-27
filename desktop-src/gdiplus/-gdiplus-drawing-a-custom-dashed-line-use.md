---
description: Windows GDI+ proporciona varios estilos de guión que se enumeran en la enumeración DashStyle. Si esos estilos de guiones estándar no se adaptan a sus necesidades, puede crear un patrón de guiones personalizado.
ms.assetid: 0e75de3b-1006-4c8f-875c-eeb0782f24b0
title: Dibujar una línea discontinua personalizada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e108dcd6b32a47befcdd99d1f23e90c33d08446
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104988205"
---
# <a name="drawing-a-custom-dashed-line"></a>Dibujar una línea discontinua personalizada

Windows GDI+ proporciona varios estilos de guión que se enumeran en la enumeración [**DashStyle**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-dashstyle) . Si esos estilos de guiones estándar no se adaptan a sus necesidades, puede crear un patrón de guiones personalizado.

Para dibujar una línea discontinua personalizada, coloque las longitudes de los guiones y espacios en una matriz y pase la dirección de la matriz como argumento al método [**Pen:: SetDashPattern**](/windows/desktop/api/Gdipluspen/nf-gdipluspen-pen-setdashpattern) de un objeto [**Pen**](/windows/desktop/api/gdipluspen/nl-gdipluspen-pen) . En el ejemplo siguiente se dibuja una línea discontinua personalizada basada en la matriz {5, 2, 15, 4}. Si multiplica los elementos de la matriz por el ancho del lápiz de 5, obtendrá {25, 10, 75, 20}. Los guiones mostrados alternan la longitud entre 25 y 75, y los espacios alternan entre 10 y 20.


```
REAL dashValues[4] = {5, 2, 15, 4};
Pen blackPen(Color(255, 0, 0, 0), 5);
blackPen.SetDashPattern(dashValues, 4);
stat = graphics.DrawLine(&blackPen, Point(5, 5), Point(405, 5));
```



En la ilustración siguiente se muestra la línea discontinua resultante. Tenga en cuenta que el guión final tiene que tener menos de 25 unidades para que la línea pueda acabar en (405).

![Ilustración que muestra una línea discontinua; cada segmento es una línea corta seguida de una larga](images/pens6.png)

 

 



