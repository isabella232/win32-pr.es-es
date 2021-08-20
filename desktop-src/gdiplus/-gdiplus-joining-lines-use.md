---
description: Una combinación de línea es el área común formada por dos líneas cuyos extremos se encuentran o se superponen.
ms.assetid: 4ec3e76a-2531-4869-a5b0-c595198e8345
title: Unir líneas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2aa93eac405bd77f6d87b2a8b86edc8a4043a57de3e4c4d5f31fb45acecc955
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118066979"
---
# <a name="joining-lines"></a>Unir líneas

Una combinación de línea es el área común formada por dos líneas cuyos extremos se encuentran o se superponen. Windows GDI+ proporciona cuatro estilos de combinación de línea: bisel, bisel, redondeo y recortado. El estilo de combinación de línea es una propiedad de la [**clase Pen.**](/windows/desktop/api/gdipluspen/nl-gdipluspen-pen) Cuando se especifica un estilo de combinación de línea para un lápiz y, a continuación, se usa ese lápiz para dibujar un trazado, el estilo de combinación especificado se aplica a todas las líneas conectadas en la ruta de acceso.

Puede especificar el estilo de combinación de línea mediante el [**método Pen::SetLineJoin**](/windows/desktop/api/Gdipluspen/nf-gdipluspen-pen-setlinejoin) de la [**clase Pen.**](/windows/desktop/api/gdipluspen/nl-gdipluspen-pen) En el ejemplo siguiente se muestra una combinación de línea biselada entre una línea horizontal y una línea vertical:


```
GraphicsPath path;
Pen penJoin(Color(255, 0, 0, 255), 8);

path.StartFigure();
path.AddLine(Point(50, 200), Point(100, 200));
path.AddLine(Point(100, 200), Point(100, 250));

penJoin.SetLineJoin(LineJoinBevel);
graphics.DrawPath(&penJoin, &path);
```



En la ilustración siguiente se muestra la combinación de línea biselada resultante.

![ilustración que muestra dos líneas que se reúnen en un ángulo derecho, con una combinación biselada](images/pens5.png)

En el ejemplo anterior, el valor (**LineJoinBevel**) pasado al [**método Pen::SetLineJoin**](/windows/desktop/api/Gdipluspen/nf-gdipluspen-pen-setlinejoin) es un elemento de la [**enumeración LineJoin.**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-linejoin)

 

 



