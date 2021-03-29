---
title: Atributo EndArrowWidth de VML
description: Atributo EndArrowWidth de VML
ms.assetid: a68854d2-33f8-44fb-a0be-830d2be3040f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 108d65fc1a06ace3d318d54a6416e0d98c0a4652
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103793767"
---
# <a name="vml-endarrowwidth-attribute"></a>Atributo EndArrowWidth de VML

En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir del 2011 de diciembre, este tema se ha archivado. Como resultado, ya no se mantiene de forma activa. Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).

 

Define un ancho de la punta de flecha para el final de una línea. Lectura/escritura **VgArrowheadWidth**.

**Se aplica a**

[Stroke](msdn-online-vml-stroke-element.md)

**Sintaxis de etiquetas**

<v: *Element* endarrowwidth = " *expresión* " >

**Sintaxis de script**

*Element* . endarrowwidth = "*expresión*"

*expresión* = de *elemento*. endarrowwidth

**Comentarios:**

Estos valores incluyen:

-   Restrictiv
-   Media (valor predeterminado)
-   Ancho

*Atributo estándar de VML*

**Ejemplo**

Una línea se dibuja con una punta de flecha clásica ancha en el extremo del trazo.


```HTML
   <v:line strokecolor="red"
   strokeweight="2pt" to="100pt,20pt" from="20pt,20pt">
   <v:stroke endarrow="classic" endarrowwidth="wide"/>
   </v:line>
```



 

 