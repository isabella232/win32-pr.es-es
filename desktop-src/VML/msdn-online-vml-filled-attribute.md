---
title: Atributo rellenado de VML
description: Atributo rellenado de VML
ms.assetid: c5a71a8d-5310-4e58-9153-c5cc64b0a5e0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 232d8b36b6d272c3a1ee8c17f3ddeca023ab4708
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104488255"
---
# <a name="vml-filled-attribute"></a>Atributo rellenado de VML

En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir del 2011 de diciembre, este tema se ha archivado. Como resultado, ya no se mantiene de forma activa. Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).

 

Determina si la ruta de acceso cerrada se rellenará. Lectura/escritura **VgTriState**.

**Se aplica a**

[Forma](shape-element--vml.md)

**Sintaxis de etiquetas**

<v: *elemento* filled = " *expresión* " >

**Sintaxis de script**

*Element* . filled = "*expresión*"

*expresión* = de *elemento*. filled

**Comentarios:**

El valor se duplica desde el atributo **on** del elemento [Fill](msdn-online-vml-fill-element.md) .

*Atributo estándar de VML*

**Ejemplo**

Se rellena la ruta de acceso de la forma.


```HTML
   <v:shape id="rect01" filled="True"
   strokecolor="red" fillcolor="white"
   coordorigin="0 0" coordsize="200 200"
   style="position:relative;top:1;left:1;width:20;height:20"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   </v:shape>
```



[Ejemplo de atributo rellenado](/previous-versions/bb229669(v=vs.85)). (Requiere Microsoft Internet Explorer 5 o posterior).

 

 