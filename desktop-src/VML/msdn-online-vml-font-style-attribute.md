---
title: Atributo de Font-Style VML
description: Atributo de Font-Style VML
ms.assetid: 3dfea8d0-d03b-46c0-b972-a529bc12b62c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4571f9805b3a12f1c3c7b340780d0f3d9f6ce8644c2ec501e8c93aa58d378de6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119057863"
---
# <a name="vml-font-style-attribute"></a>Atributo de Font-Style VML

En este tema se describe VML, una característica que está en desuso a partir Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML deben migrarse a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir de diciembre de 2011, este tema se archivó. Como resultado, ya no se mantiene activamente. Para obtener más información, vea [Contenido archivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, [vea Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Define la cantidad de slant para una fuente. Lectura/escritura **Cadena**.

**Se aplica a**

[TextPath](msdn-online-vml-textpath-element.md)

**Sintaxis de etiquetas**

<v: *element* style="font-style: *expression* ">

**Sintaxis de script**

*element* .style.fontstyle="*expression*"

*expresión* = *elemento*.style.fontstyle

**Comentarios:**

Los valores son:

-   normal (valor predeterminado)
-   Oblicua
-   cursiva

La mayoría de los exploradores se representan como oblicuos en cursiva. Los valores son los mismos que los atributos de estilo HTML estándar.

*Atributo estándar de VML*

**Ejemplo**

La fuente está en cursiva (inclinada).


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="font:italic normal normal 36pt Arial"/>
   </v:line>
```



 

 