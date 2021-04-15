---
title: Atributo de la interseción de VML
description: Atributo de la interseción de VML
ms.assetid: e67d1bae-2f54-4c43-8445-1f5109e4afde
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d4a4027f079ffb284125032570dd2293b1ab69e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105695674"
---
# <a name="vml-arcsize-attribute"></a>Atributo de la interseción de VML

En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir del 2011 de diciembre, este tema se ha archivado. Como resultado, ya no se mantiene de forma activa. Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).

 

Define la cantidad de redondeo de un rectángulo redondeado. Lectura/escritura [VgFraction](msdn-online-vml-vgfraction-data-type.md) .

**Se aplica a**

[RoundRect](msdn-online-vml-roundrect-element.md)

**Sintaxis de etiquetas**

<v: *elemento* -arcos = " *expresión* " >

**Sintaxis de script**

*Element* . arcos = "*expresión*"

*expresión* = de *elemento*. arcos

**Comentarios:**

Define las esquinas redondeadas de un rectángulo redondeado como un porcentaje de la mitad de la dimensión más pequeña de la longitud y el ancho de un rectángulo. 0% tendría esquinas cuadradas y el 100% formaría esquinas circulares. Un cuadrado con un **valor de** un valor de entre valores 1,0 sería un círculo. El valor predeterminado es 0,2 (20%).

*Atributo estándar de VML*

**Ejemplo**

El rectángulo redondeado se dibuja con esquinas estrechas pero redondeadas.


```HTML
   <v:roundrect id=myrr
   style="height:100;left:100;top:100;width:200"
   fillcolor="red"
   arcsize="5%">
   </v:roundrect>
```



 

 