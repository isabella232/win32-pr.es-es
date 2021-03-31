---
title: Atributo VML V-Text-Kern
description: Atributo VML V-Text-Kern
ms.assetid: cece49c3-8e62-4327-8949-684a1d073293
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b20eab11cc24cd7580b68de8acf86468fb1d16a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103995464"
---
# <a name="vml-v-text-kern-attribute"></a>Atributo VML V-Text-Kern

En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir del 2011 de diciembre, este tema se ha archivado. Como resultado, ya no se mantiene de forma activa. Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).

 

Determina si el kerning está activado. Lectura/escritura **VgTriState**.

**Se aplica a**

[TextPath](msdn-online-vml-textpath-element.md)

**Sintaxis de etiquetas**

<v: *Element* style = "v-Text-Kern: *Expression* " >

**Sintaxis de script**

*Element* . Style. v-Text-kerning = "*Expression*"

*expresión* = de *elemento*. Style. v-texto-kerning

**Comentarios:**

Si es **true**, el kerning está activado. El valor predeterminado es **False**. El interletraje es la eliminación de espacio entre determinados pares de letras para compensar una letterforms desigual. Por ejemplo, si está activado el interletraje, se quitará el espacio adicional entre una "T" mayúscula y una "i" minúscula.

*Atributo estándar de VML*

**Ejemplo**

El kerning está activado.


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="v-text-kern:True;font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 