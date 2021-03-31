---
title: Atributo StartArrow de VML
description: Atributo StartArrow de VML
ms.assetid: 484dfcdb-f68d-40f9-9a83-18abb054d1c8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca2c17569750c1e655a5538ca5bf233e49f827e4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103995432"
---
# <a name="vml-startarrow-attribute"></a>Atributo StartArrow de VML

En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir del 2011 de diciembre, este tema se ha archivado. Como resultado, ya no se mantiene de forma activa. Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).

 

Define la punta de flecha para el inicio de una línea. Lectura/escritura **Cadena**.

**Se aplica a**

[Stroke](msdn-online-vml-stroke-element.md)

**Sintaxis de etiquetas**

<v: *Element* startarrow = " *expresión* " >

**Sintaxis de script**

*Element* . startarrow = "*expresión*"

*expresión* = de *elemento*. startarrow

**Comentarios:**

Estos valores incluyen:

-   Ninguna (valor predeterminado)
-   Bloquear
-   Clásico
-   Diamond
-   Elipse
-   Abrir

Atributo estándar de VML

**Ejemplo**

Una línea se dibuja con una punta de flecha clásica en el inicio del trazo.


```HTML
   <v:line strokecolor="red"
   strokeweight="2pt" to="100pt,20pt" from="20pt,20pt">
   <v:stroke StartArrow="classic"/>
   </v:line>
```



 

 