---
title: Atributo size (VMLFrame)
description: Atributo size (VMLFrame)
ms.assetid: 95d953fa-cbe2-4ebc-9b23-408347232fee
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 779b0401c414a3536e22bdb7328b2b08b2fbcf45
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104077816"
---
# <a name="size-attribute-vmlframe"></a>Atributo size (VMLFrame)

En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir del 2011 de diciembre, este tema se ha archivado. Como resultado, ya no se mantiene de forma activa. Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).

 

Define el tamaño de la región de recorte del marco. Lectura/escritura **VgVector2D**.

**Se aplica a**

[VMLFrame](msdn-online-vml-vmlframe-element.md)

**Sintaxis de etiquetas**

<v: *elemento* size = " *expresión* " >

**Sintaxis de script**

*Element* . size = "*expresión*"

*expresión* = de *elemento*. Size

**Comentarios:**

El valor predeterminado es 0,0. Tenga en cuenta que **el tamaño** solo funciona si [clip](msdn-online-vml-clip-attribute.md) es **true**. En este atributo, el tamaño se define como el ancho y el alto del marco.

*Atributo estándar de VML*

**Ejemplo**

El tamaño de la región de recorte será 50pt, 50pt.


```HTML
   <v:vmlframe id="frame01" clip="True"
   origin="100pt,100pt" size="50pt,50pt"
   src="external.vml#shape01"
   style='top:160pt; left:100pt; width:50pt; height:50pt'>
   </v:vmlframe>
```



 

 