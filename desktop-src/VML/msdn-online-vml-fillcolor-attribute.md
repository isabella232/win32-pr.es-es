---
title: Atributo FillColor de VML
description: Atributo FillColor de VML
ms.assetid: c18302e1-86a5-4046-811f-576a746ea398
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fbacd688d25745222b5dcaf62691bff8546dad1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105695748"
---
# <a name="vml-fillcolor-attribute"></a>Atributo FillColor de VML

En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir del 2011 de diciembre, este tema se ha archivado. Como resultado, ya no se mantiene de forma activa. Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).

 

Define el color del pincel que rellena la ruta de acceso cerrada de una forma. Lectura/escritura [IVgColor](msdn-online-vml-ivgcolor.md) .

**Se aplica a**

[Forma](shape-element--vml.md)

**Sintaxis de etiquetas**

<v: *elemento* fillColor = " *expresión* " >

**Sintaxis de script**

*Element* . fillColor = "*expresión*"

*expresión* = de *elemento*. colorderelleno

**Comentarios:**

El valor de **fillColor** se duplica desde el atributo **color** del elemento **Fill** .

*Atributo estándar de VML*

**Vea también**

[Shape](shape-element--vml.md), [Fill](msdn-online-vml-fill-element.md), [IVgColor](msdn-online-vml-ivgcolor.md)

**Ejemplo**

El color de relleno del rectángulo es rojo.


```HTML
   <v:rect id=myrect fillcolor="red"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



[Ejemplo del atributo fillColor](/previous-versions/bb229668(v=vs.85)). (Requiere Microsoft Internet Explorer 5 o posterior).

 

 