---
title: Atributo ArcSize de VML
description: Atributo ArcSize de VML
ms.assetid: e67d1bae-2f54-4c43-8445-1f5109e4afde
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8715440f56625d16ed5b4386120dbf50588ce861c1ba59772e3ec8f35a077dd6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117755129"
---
# <a name="vml-arcsize-attribute"></a>Atributo ArcSize de VML

En este tema se describe VML, una característica que está en desuso a partir Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML deben migrarse a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir de diciembre de 2011, este tema se archivó. Como resultado, ya no se mantiene activamente. Para obtener más información, vea [Contenido archivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, [vea Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Define la cantidad de redondeo de un rectángulo redondeado. Lectura/escritura [Accionario](msdn-online-vml-vgfraction-data-type.md) .

**Se aplica a**

[RoundRect](msdn-online-vml-roundrect-element.md)

**Sintaxis de etiquetas**

<v: *element* arcsize=" *expression* ">

**Sintaxis de script**

*element* .arcSize="*expression*"

*expresión* = *elemento*.arcSize

**Comentarios:**

Define las esquinas redondeadas de un rectángulo redondeado como un porcentaje de la mitad de la dimensión más pequeña de la longitud y el ancho de un rectángulo. El 0 % tendría esquinas cuadradas y el 100 % formaría esquinas circulares. Un cuadrado con un **valor de ArcSize** de 1,0 sería un círculo. El valor predeterminado es 0,2 (20 %).

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



 

 