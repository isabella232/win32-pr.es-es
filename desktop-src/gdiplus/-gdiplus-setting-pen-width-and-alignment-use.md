---
description: Al crear un objeto Pen, puede proporcionar el ancho del lápiz como uno de los argumentos al constructor. También puede cambiar el ancho del lápiz mediante el método Pen::SetWidth.
ms.assetid: b529ba0b-1786-4925-88bd-1a8369fc368c
title: Establecer el ancho y la alineación del lápiz
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca59895cc73480b054302091342c8f8f4f410b34
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127063415"
---
# <a name="setting-pen-width-and-alignment"></a>Establecer el ancho y la alineación del lápiz

Al crear un objeto [**Pen,**](/windows/desktop/api/gdipluspen/nl-gdipluspen-pen) puede proporcionar el ancho del lápiz como uno de los argumentos al constructor. También puede cambiar el ancho del lápiz mediante el [**método Pen::SetWidth.**](/windows/desktop/api/Gdipluspen/nf-gdipluspen-pen-setwidth)

Una línea teórica tiene un ancho de cero. Al dibujar una línea, los píxeles se centra en la línea teórica. En el ejemplo siguiente se dibuja una línea especificada dos veces: una con un lápiz negro de ancho 1 y otra con un lápiz verde de ancho 10.


```
Pen blackPen(Color(255, 0, 0, 0), 1);
Pen greenPen(Color(255, 0, 255, 0), 10);
stat = greenPen.SetAlignment(PenAlignmentCenter);

// Draw the line with the wide green pen.
stat = graphics.DrawLine(&greenPen, 10, 100, 100, 50);

// Draw the same line with the thin black pen.
stat = graphics.DrawLine(&blackPen, 10, 100, 100, 50);
```



En la ilustración siguiente se muestra la salida del código anterior. Los píxeles verdes y los píxeles negros se centra en la línea teórica.

![ilustración que muestra una línea fina, diagonal y negra rodeada por una línea ancha y verde ](images/pens1a.png)

En el ejemplo siguiente se dibuja un rectángulo especificado dos veces: una vez con un lápiz negro de ancho 1 y una vez con un lápiz verde de ancho 10. El código pasa el valor **PenAlignmentCenter** (un elemento de la enumeración [**PenAlignment)**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-penalignment) al método [**Pen::SetAlignment**](/windows/desktop/api/Gdipluspen/nf-gdipluspen-pen-setalignment) para especificar que los píxeles dibujados con el lápiz verde se centren en el límite del rectángulo.


```
Pen blackPen(Color(255, 0, 0, 0), 1);
Pen greenPen(Color(255, 0, 255, 0), 10);
stat = greenPen.SetAlignment(PenAlignmentCenter);

// Draw the rectangle with the wide green pen.
stat = graphics.DrawRectangle(&greenPen, 10, 100, 50, 50);

// Draw the same rectangle with the thin black pen.
stat = graphics.DrawRectangle(&blackPen, 10, 100, 50, 50);
```



En la ilustración siguiente se muestra la salida del código anterior. Los píxeles verdes se centra en el rectángulo teórico, representado por los píxeles negros.

![ilustración que muestra una línea negra fina en la forma de un rectángulo, rodeado por una línea verde más ancha](images/pens2.png)

Puede cambiar la alineación del lápiz verde modificando la tercera instrucción del ejemplo anterior como se muestra a continuación:


```
stat = greenPen.SetAlignment(PenAlignmentInset);
```



Ahora los píxeles de la línea verde ancha aparecen en el interior del rectángulo, como se muestra en la ilustración siguiente.

![ilustración en la que se muestra una línea negra fina en forma de rectaclo, que incluye una línea verde ancha de la misma forma.](images/pens3.png)

 

 



