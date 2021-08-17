---
description: Puede dibujar el inicio o el final de una línea en una de varias formas denominadas límites de línea. Windows GDI+ admite varios límites de línea, como redondeo, cuadrado, rombo y punta de flecha.
ms.assetid: c9d90114-3913-486c-a808-b08dd473d9a1
title: Dibujar una línea con límites de línea
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33e72e4e1c9c36a7233688378852dfda73196cd7e7131cf7def587ad29a70e82
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117696167"
---
# <a name="drawing-a-line-with-line-caps"></a>Dibujar una línea con límites de línea

Puede dibujar el inicio o el final de una línea en una de varias formas denominadas límites de línea. Windows GDI+ admite varios límites de línea, como redondeo, cuadrado, rombo y punta de flecha.

Puede especificar los límites de línea para el inicio de una línea (extremo inicial), el final de una línea (extremo final) o los guiones de una línea discontinua (extremo de guión).

En el ejemplo siguiente se dibuja una línea con una punta de flecha en un extremo y un extremo redondeado en el otro extremo:


```
Pen pen(Color(255, 0, 0, 255), 8);
stat = pen.SetStartCap(LineCapArrowAnchor);
stat = pen.SetEndCap(LineCapRoundAnchor);
stat = graphics.DrawLine(&pen, 20, 175, 300, 175);
```



En la ilustración siguiente se muestra la línea resultante.

![ilustración que muestra una línea horizontal con una flecha en el extremo izquierdo y un círculo en el extremo derecho](images/pens4.png)

**LineCapArrowAnchor y** **LineCapRoundAnchor** son elementos de la [**enumeración LineCap.**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-linecap)

 

 



