---
title: Atributo EndCap de VML
description: Atributo EndCap de VML
ms.assetid: d8669a34-0fec-461e-90de-d9d5f7749a15
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 726d2bba2128ebb1897f306ae608f4bebb48d63f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104359401"
---
# <a name="vml-endcap-attribute"></a>Atributo EndCap de VML

En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir del 2011 de diciembre, este tema se ha archivado. Como resultado, ya no se mantiene de forma activa. Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).

 

Define el estilo de extremo para el final de un trazo. Lectura/escritura **VgLineEndCapStyle**.

**Se aplica a**

[Stroke](msdn-online-vml-stroke-element.md)

**Sintaxis de etiquetas**

<v: *Element* Endcap = " *expresión* " >

**Sintaxis de script**

*Element* . Endcap = "*expresión*"

*expresión* = de *elemento*. Endcap

**Comentarios:**

Estos valores incluyen:

-   Plano (valor predeterminado)
-   Square
-   Round

*Atributo estándar de VML*

**Ejemplo**

Una línea se dibuja con una punta plana al final del trazo.


```HTML
   <v:line strokecolor="red"
   strokeweight="2pt" to="100pt,20pt" from="20pt,20pt">
   <v:stroke endcap="flat"/>
   </v:line>
```



 

 