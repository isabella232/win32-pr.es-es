---
title: Atributo de fuente VML
description: Atributo de fuente VML
ms.assetid: 5a48fc54-e2dd-4b68-863c-3a83f9386108
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 074aa0672002dcbbac55d21ed27383d5a3fd6e3b9ccfe9125ad89c2c43ac71ba
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119986665"
---
# <a name="vml-font-attribute"></a>Atributo de fuente VML

En este tema se describe VML, una característica que está en desuso a partir Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML deben migrarse a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir de diciembre de 2011, este tema se archivó. Como resultado, ya no se mantiene activamente. Para obtener más información, vea [Contenido archivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, [vea Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Especifica un valor compuesto de atributos de fuente. Lectura/escritura **Cadena**.

**Se aplica a**

[TextPath](msdn-online-vml-textpath-element.md)

**Sintaxis de etiquetas**

<v: *element* style="font: *expression* ">

**Sintaxis de script**

*element* .style.font="*expression*"

*expresión* = *elemento*.style.font

**Comentarios:**

Define los atributos de una fuente, incluida la familia, el estilo, el peso, el tamaño y la variante. El orden de las definiciones de la cadena es: **font-style**, **font-variant , font-weight**, **font-size**, **line-height** y **font-family**.  Los valores son los mismos que los atributos de estilo HTML estándar.

*Atributo estándar de VML*

**Ejemplo**

La fuente del texto textpath es cursiva, con mayúsculas pequeñas, negrita, Arial de 36 puntos.


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="font:italic small-caps bold 36pt Arial"/>
   </v:line>
```



 

 