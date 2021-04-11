---
title: Atributo de trazado VML
description: Atributo de trazado VML
ms.assetid: 3a62a04b-8165-4d83-8b6d-d5e9bbde2796
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9578027f305f9c720b42ae50befe8abd7e18a949
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104149590"
---
# <a name="vml-stroked-attribute"></a>Atributo de trazado VML

En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir del 2011 de diciembre, este tema se ha archivado. Como resultado, ya no se mantiene de forma activa. Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).

 

Define si se va a trazar la ruta de acceso. Lectura/escritura [VgTriState](msdn-online-vml-vgtristate.md) .

**Se aplica a**

[Forma](shape-element--vml.md)

**Sintaxis de etiquetas**

<v: *elemento* stroked = " *expresión* " >

**Sintaxis de script**

*Element* . stroked = "*expresión*"

*expresión* = de *elemento*. stroked

**Comentarios:**

El valor se duplica desde el atributo **on** del elemento [Stroke](msdn-online-vml-stroke-element.md) .

*Atributo estándar de VML*

**Ejemplo**

La ruta de acceso de la forma se traza.


```HTML
   <v:shape id="rect01" stroked="True"
   strokecolor="red" fillcolor="white"
   coordorigin="0 0" coordsize="200 200"
   style="position:relative;top:1;left:1;width:20;height:20"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   </v:shape>
```



[Ejemplo de atributo de trazo](/previous-versions/bb264094(v=vs.85)). (Requiere Microsoft Internet Explorer 5 o posterior).

 

 