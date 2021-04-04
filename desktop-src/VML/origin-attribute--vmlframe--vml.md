---
title: Atributo Origin (VMLFrame) (VML)
description: Atributo Origin (VMLFrame) (VML)
ms.assetid: 317c027e-5054-4543-ad98-2c21d1cf7154
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae9341eecea9ec1eae8aaf1d7b1ad729986a8249
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103793642"
---
# <a name="origin-attribute-vmlframevml"></a>Atributo Origin (VMLFrame) (VML)

En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir del 2011 de diciembre, este tema se ha archivado. Como resultado, ya no se mantiene de forma activa. Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).

 

Define el origen de la región de recorte del marco. Lectura/escritura **VgVector2D**.

**Se aplica a**

[VMLFrame](msdn-online-vml-vmlframe-element.md)

**Sintaxis de etiquetas**

<v: *elemento* Origin = " *expresión* " >

**Sintaxis de script**

*Element* . Origin = "*expresión*"

*expresión* = de *elemento*. Origin

**Comentarios:**

El valor predeterminado es 0,0. Tenga en cuenta que **Origin** solo funciona si [clip](msdn-online-vml-clip-attribute.md) es **true**. En este atributo, el origen se define como la esquina superior izquierda del marco.

*Atributo estándar de VML*

**Ejemplo**

El origen de la región de recorte es 100pt, 100pt.


```HTML
   <v:vmlframe id="frame01" clip="True"
   origin="100pt,100pt" size="50pt,50pt"
   src="external.vml#shape01"
   style='top:160pt; left:100pt; width:50pt; height:50pt'
   </v:vmlframe>
```



 

 