---
description: Puede dibujar el inicio o el final de una línea en una de varias formas llamadas extremos de línea. GDI+ de Windows admite varios extremos de línea, como Round, Square, Diamond y punta de flecha.
ms.assetid: c9d90114-3913-486c-a808-b08dd473d9a1
title: Dibujar una línea con extremos de línea
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50ee4dd12a3068fe5200e0f1ae786765170ccba7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104987804"
---
# <a name="drawing-a-line-with-line-caps"></a>Dibujar una línea con extremos de línea

Puede dibujar el inicio o el final de una línea en una de varias formas llamadas extremos de línea. GDI+ de Windows admite varios extremos de línea, como Round, Square, Diamond y punta de flecha.

Puede especificar los extremos de línea para el inicio de una línea (extremo inicial), el final de una línea (extremo final) o los guiones de una línea discontinua (extremo de guion).

En el ejemplo siguiente se dibuja una línea con una punta de flecha en un extremo y un extremo redondeado en el otro extremo:


```
Pen pen(Color(255, 0, 0, 255), 8);
stat = pen.SetStartCap(LineCapArrowAnchor);
stat = pen.SetEndCap(LineCapRoundAnchor);
stat = graphics.DrawLine(&pen, 20, 175, 300, 175);
```



En la ilustración siguiente se muestra la línea resultante.

![Ilustración en la que se muestra una línea horizontal con una flecha en el extremo izquierdo y un círculo en el extremo derecho](images/pens4.png)

**LineCapArrowAnchor** y **LineCapRoundAnchor** son elementos de la enumeración [**LineCap**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-linecap) .

 

 



