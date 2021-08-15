---
title: Atributo de Font-Family VML
description: Atributo de Font-Family VML
ms.assetid: 10586ae0-1480-4ffe-a690-ce8464e9bf41
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1254be6f7264e0d8f77d5881a11b9c2ec5085a931a0cad713813c059c60e5e62
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117754747"
---
# <a name="vml-font-family-attribute"></a>Atributo de Font-Family VML

En este tema se describe VML, una característica que está en desuso a partir Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML deben migrarse a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir de diciembre de 2011, este tema se archivó. Como resultado, ya no se mantiene activamente. Para obtener más información, vea [Contenido archivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, [vea Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Define la familia de la fuente textpath. Lectura/escritura **Cadena**.

**Se aplica a**

[TextPath](msdn-online-vml-textpath-element.md)

**Sintaxis de etiquetas**

<v: *element* style="font-family: *expression* ">

**Sintaxis de script**

*element* .style.fontfamily="*expression*"

*expresión* = *elemento*.style.fontfamily

**Comentarios:**

Define el nombre de fuente. Se pueden usar nombres específicos, como Arial, o tipos genéricos, como serif, sans-serif, cursive, pornográfica o monospace. Los valores son los mismos que los atributos de estilo HTML estándar.

*Atributo estándar de VML*

**Ejemplo**

La familia de fuentes del texto es Arial.


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 