---
title: Atributo Position (H) (VML)
description: Atributo Position (H) (VML)
ms.assetid: 0bae708d-5409-4609-a102-7f799f2c1fbb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac310c0fad457beaf3b9aeb04671b7ffbb1dbd8d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105695734"
---
# <a name="position-attribute-hvml"></a>Atributo Position (H) (VML)

En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir del 2011 de diciembre, este tema se ha archivado. Como resultado, ya no se mantiene de forma activa. Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).

 

Especifica los valores TheX e y del identificador. **VgVector2D** de lectura/escritura.

**Se aplica a**

[H](msdn-online-vml-h-element.md) (subelemento de [Handles](msdn-online-vml-handles-element.md))

**Sintaxis de etiquetas**

<v: *elemento* position = " *expresión* " >

**Comentarios:**

los valores x e y pueden ser de uno de los tipos siguientes:

-   constant
-   fórmula (por ejemplo, @2 )
-   ajustar (por ejemplo, \# 3)
-   centro
-   a la izquierda
-   PivotDetailRange

Si se especifica cualquiera de los tipos anteriores, excepto *ADJUST* , la posición del identificador se fija en esa dimensión. Si se especifica un identificador de ajuste, el identificador es libre de mover en esa dimensión y el valor de ajuste viene determinado por la posición del identificador.

Si se especifica un atributo [polar](msdn-online-vml-polar-attribute.md) , el atributo **Position** representa los valores de radio y ángulo del controlador en lugar de x e y.

El valor predeterminado es 0,0.

*Atributo estándar de VML*

 

 