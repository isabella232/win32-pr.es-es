---
title: Atributo de clip VML
description: Atributo de clip VML
ms.assetid: 8839c10e-96dd-4419-9f02-80033a4633e9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2702355ea93d8e87d173ee4c23406b12557dce4a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105695672"
---
# <a name="vml-clip-attribute"></a>Atributo de clip VML

En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir del 2011 de diciembre, este tema se ha archivado. Como resultado, ya no se mantiene de forma activa. Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).

 

Determina si el recorte está activado. Lectura/escritura **VgTriState**.

**Se aplica a**

[VMLFrame](msdn-online-vml-vmlframe-element.md)

**Sintaxis de etiquetas**

<v: *elemento* clip = " *expresión* " >

**Sintaxis de script**

*Element* . clip = "*expresión*"

*expresión* = de *elemento*. clip

**Comentarios:**

Si **clip** es **false**, la forma se escalará para ajustarse al marco. Si **es true**, no se mostrarán las partes de la forma que estén fuera del marco.

Tenga en cuenta que el [origen](origin-attribute--vmlframe--vml.md) y [el tamaño](size-attribute--vmlframe.md) no se usarán a menos que el **recorte** sea **true**.

*Atributo estándar de VML*

**Ejemplo**

Se recortará la imagen definida en el archivo externo.


```HTML
   <v:vmlframe id="frame01" clip="True"
   origin="100pt,100pt" size="50pt,50pt"
   src="external.vml#shape01"
   style='top:160pt; left:100pt; width:50pt; height:50pt'>
   </v:vmlframe>
```



 

 