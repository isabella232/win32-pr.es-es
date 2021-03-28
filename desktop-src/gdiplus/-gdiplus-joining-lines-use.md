---
description: Una combinación de líneas es el área común formada por dos líneas cuyos extremos coinciden o superponen.
ms.assetid: 4ec3e76a-2531-4869-a5b0-c595198e8345
title: Combinar líneas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b2ab0bc53239b9a0d9327a26e25eed1c93c685b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104551054"
---
# <a name="joining-lines"></a>Combinar líneas

Una combinación de líneas es el área común formada por dos líneas cuyos extremos coinciden o superponen. GDI+ de Windows proporciona cuatro estilos de combinación de líneas: angular, bisel, redondo y angular. El estilo de combinación de líneas es una propiedad de la clase [**Pen**](/windows/desktop/api/gdipluspen/nl-gdipluspen-pen) . Cuando se especifica un estilo de combinación de líneas para un lápiz y, a continuación, se usa ese lápiz para dibujar un trazado, el estilo de combinación especificado se aplica a todas las líneas conectadas en la ruta de acceso.

Puede especificar el estilo de unión de línea mediante el método [**Pen:: SetLineJoin**](/windows/desktop/api/Gdipluspen/nf-gdipluspen-pen-setlinejoin) de la clase [**Pen**](/windows/desktop/api/gdipluspen/nl-gdipluspen-pen) . En el ejemplo siguiente se muestra una combinación de líneas biseladas entre una línea horizontal y una línea vertical:


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

![Ilustración que muestra dos líneas que se comparan en un ángulo recto, con una combinación biselada](images/pens5.png)

En el ejemplo anterior, el valor (**LineJoinBevel**) que se pasa al método [**Pen:: SetLineJoin**](/windows/desktop/api/Gdipluspen/nf-gdipluspen-pen-setlinejoin) es un elemento de la enumeración [**LineJoin**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-linejoin) .

 

 



