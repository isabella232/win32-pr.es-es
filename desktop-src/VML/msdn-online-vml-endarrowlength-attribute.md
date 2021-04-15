---
title: Atributo EndArrowLength de VML
description: Atributo EndArrowLength de VML
ms.assetid: aab898b6-4c59-4471-81fd-621f79610d63
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43d9d8bfbd24a6a1b79208d50d4d2aef956a5bc5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105695614"
---
# <a name="vml-endarrowlength-attribute"></a>Atributo EndArrowLength de VML

En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir del 2011 de diciembre, este tema se ha archivado. Como resultado, ya no se mantiene de forma activa. Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).

 

Define una longitud de la punta de flecha para el final de una línea. Lectura/escritura **VgArrowheadLength**.

**Se aplica a**

[Stroke](msdn-online-vml-stroke-element.md)

**Sintaxis de etiquetas**

<v: *Element* endarrowlength = " *expresión* " >

**Sintaxis de script**

*Element* . endarrowlength = "*expresión*"

*expresión* = de *elemento*. endarrowlength

**Comentarios:**

Estos valores incluyen:

-   Short
-   Media (valor predeterminado)
-   long

*Atributo estándar de VML*

**Ejemplo**

Una línea se dibuja con una punta de flecha clásica corta en el final del trazo.


```HTML
   <v:line strokecolor="red"
   strokeweight="2pt" to="100pt,20pt" from="20pt,20pt">
   <v:stroke endarrow="classic" endarrowlength="short"/>
   </v:line>
```



 

 