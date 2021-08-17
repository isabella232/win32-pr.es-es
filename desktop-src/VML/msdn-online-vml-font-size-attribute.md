---
title: Atributo de Font-Size VML
description: Atributo de Font-Size VML
ms.assetid: 49394cd5-3009-424a-97d3-28c85d874bc4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 401d66668b0a86b92e453ac2e4a8a9adb96411131cc90f7bf14bd22be67e6775
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118346582"
---
# <a name="vml-font-size-attribute"></a>Atributo de Font-Size VML

En este tema se describe VML, una característica que está en desuso a partir Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML deben migrarse a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir de diciembre de 2011, este tema se archivó. Como resultado, ya no se mantiene activamente. Para obtener más información, vea [Contenido archivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, [vea Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Define el tamaño de la fuente. Lectura/escritura **Cadena**.

**Se aplica a**

[TextPath](msdn-online-vml-textpath-element.md)

**Sintaxis de etiquetas**

<v: *element* style="font-size: *expression* ">

**Sintaxis de script**

*element* .style.fontsize="*expression*"

*expresión* = *elemento*.style.fontsize

**Comentarios:**

El tamaño de fuente se define en puntos. Los valores son los mismos que los atributos de estilo HTML estándar.

*Atributo estándar de VML*

**Ejemplo**

El tamaño de fuente es de 36 puntos.


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 