---
title: Atributo de fuente VML
description: Atributo de fuente VML
ms.assetid: 5a48fc54-e2dd-4b68-863c-3a83f9386108
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bace73b90cac7519ea6abacb73c80506c655e133
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105695746"
---
# <a name="vml-font-attribute"></a>Atributo de fuente VML

En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir del 2011 de diciembre, este tema se ha archivado. Como resultado, ya no se mantiene de forma activa. Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).

 

Especifica un valor compuesto de atributos de fuente. Lectura/escritura **Cadena**.

**Se aplica a**

[TextPath](msdn-online-vml-textpath-element.md)

**Sintaxis de etiquetas**

<v: *Element* style = "Font: *Expression* " >

**Sintaxis de script**

*Element* . Style. Font = "*expresión*"

*expresión* = de *elemento*. Style. Font

**Comentarios:**

Define los atributos de una fuente, como familia, estilo, peso, tamaño y variante. El orden de las definiciones en la cadena es: tipo de **fuente**, **fuente-variante**, fuente **-peso**, **fuente-tamaño**, **ancho de línea** y **familia de fuentes**. Los valores son los mismos que los atributos de estilo HTML estándar.

*Atributo estándar de VML*

**Ejemplo**

La fuente del texto textpath es cursiva, Versalitas, negrita, 36 punto Arial.


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="font:italic small-caps bold 36pt Arial"/>
   </v:line>
```



 

 