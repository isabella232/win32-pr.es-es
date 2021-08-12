---
title: Atributo LineStyle de VML
description: Atributo LineStyle de VML
ms.assetid: eec5c1f3-5256-4104-b021-ebf799665752
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f90be9c2aceeb3663f55c92e1140eb6a12f66aa23dd8856d0da63f0a306d8cd0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118598288"
---
# <a name="vml-linestyle-attribute"></a>Atributo LineStyle de VML

En este tema se describe VML, una característica que está en desuso a partir Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML deben migrarse a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir de diciembre de 2011, este tema se archivó. Como resultado, ya no se mantiene activamente. Para obtener más información, vea [Contenido archivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, [vea Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Define el estilo de línea del trazo. Lectura/escritura **Cadena**.

**Se aplica a**

[Golpe](msdn-online-vml-stroke-element.md)

**Sintaxis de etiquetas**

<v: *element* linestyle=" *expression* ">

**Sintaxis de script**

*element* .linestyle="*expression*"

*expresión* = *elemento*.linestyle

**Comentarios:**

Estos valores incluyen:

-   Single (valor predeterminado)
-   ThinThin
-   ThinThick
-   ThickThin
-   ThickBetweenThin

*Atributo estándar de VML*

**Ejemplo**

Se dibuja una línea doble con dos trazos finos.


```HTML
   <v:line strokecolor="red"
   strokeweight="2pt" to="100pt,20pt" from="20pt,20pt">
   <v:stroke linestyle="thinthin" />
   </v:line>
```



 

 