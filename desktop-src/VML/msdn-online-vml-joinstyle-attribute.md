---
title: Atributo JoinStyle de VML
description: Atributo JoinStyle de VML
ms.assetid: d947d115-2064-446a-8c12-e8063fe10953
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 657d3c815d6165cecd853f394780237ad0b89f0d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105695668"
---
# <a name="vml-joinstyle-attribute"></a>Atributo JoinStyle de VML

En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir del 2011 de diciembre, este tema se ha archivado. Como resultado, ya no se mantiene de forma activa. Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).

 

Define el estilo de combinación de una polilínea. Lectura/escritura String.

**Se aplica a**

[Stroke](msdn-online-vml-stroke-element.md)

**Sintaxis de etiquetas**

<v: *Element* joinstyle = " *expresión* " >

**Sintaxis de script**

*Element* . joinstyle = "*expresión*"

*expresión* = de *elemento*. joinstyle

**Comentarios:**

Estos valores incluyen:

-   Round (valor predeterminado)
-   parezca
-   ángulo

*Atributo estándar de VML*

**Ejemplo**

Los empalmes de la polilínea están biselados.


```HTML
   <v:polyline
   strokecolor="red" strokeweight="2pt"
   points="18pt,54pt,90pt,-9pt,180pt,63pt,261pt,27pt">
   <v:stroke joinstyle="bevel"/>
   </v:polyline>
```



 

 