---
title: Atributo StartArrowWidth de VML
description: Atributo StartArrowWidth de VML
ms.assetid: 47b55330-7165-4368-ad01-5b7b38a6e5b2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01ba4f5adddc328d1791fa2beb570f59da826f83
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103792555"
---
# <a name="vml-startarrowwidth-attribute"></a>Atributo StartArrowWidth de VML

En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir del 2011 de diciembre, este tema se ha archivado. Como resultado, ya no se mantiene de forma activa. Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).

 

Define el ancho de la punta de flecha para el inicio de una línea. Lectura/escritura **VgArrowheadWidth**.

**Se aplica a**

[Stroke](msdn-online-vml-stroke-element.md)

**Sintaxis de etiquetas**

<v: *Element* startarrowwidth = " *expresión* " >

**Sintaxis de script**

*Element* . startarrowwidth = "*expresión*"

*expresión* = de *elemento*. startarrowwidth

**Comentarios:**

Estos valores incluyen:

-   Restrictiv
-   Media (valor predeterminado)
-   Ancho

Atributo estándar de VML

**Ejemplo**

Una línea se dibuja con una punta de flecha clásica ancha en el inicio del trazo.


```HTML
   <v:line strokecolor="red"
   strokeweight="2pt" to="100pt,20pt" from="20pt,20pt">
   <v:stroke startarrow="classic" startarrowwidth="wide"/>
   </v:line>
```



 

 