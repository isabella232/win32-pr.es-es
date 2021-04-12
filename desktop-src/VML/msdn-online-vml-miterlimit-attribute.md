---
title: Atributo MiterLimit de VML
description: Atributo MiterLimit de VML
ms.assetid: 74744b8a-df73-4a2e-8df7-07fd0e423a47
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f1b2d5b0a186ca416bb6af25df38c4f29964efe
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104487878"
---
# <a name="vml-miterlimit-attribute"></a>Atributo MiterLimit de VML

En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir del 2011 de diciembre, este tema se ha archivado. Como resultado, ya no se mantiene de forma activa. Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).

 

Define la suavidad de la unión angular. Lectura/escritura **VgNumber**.

**Se aplica a**

[Stroke](msdn-online-vml-stroke-element.md)

**Sintaxis de etiquetas**

<v: *Element* miterLimit = " *expresión* " >

**Sintaxis de script**

*Element* . miterLimit = "*expresión*"

*expresión* = de *elemento*. miterLimit

**Comentarios:**

Distancia máxima entre el punto interno y el punto exterior de una Unión. Este número es un múltiplo del grosor de la línea.

El valor predeterminado es 8.

*Atributo estándar de VML*

**Ejemplo**

Las uniones en la polilínea están en ángulo con un límite de 10, es decir, 5 veces 2 puntos.


```HTML
   <v:polyline
   strokecolor="red" strokeweight="2pt"
   points="18pt,54pt,90pt,-9pt,180pt,63pt,261pt,27pt">
   <v:stroke miterlimit="5" joinstyle="miter"/>
   </v:polyline>
```



 

 