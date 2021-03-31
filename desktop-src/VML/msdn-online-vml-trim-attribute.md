---
title: Atributo Trim de VML
description: Atributo Trim de VML
ms.assetid: c8038361-00bd-4787-9759-506a8a47b19a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25f7aa2ce17d5b2b8df772954cee323e3d5ea2db
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103904785"
---
# <a name="vml-trim-attribute"></a>Atributo Trim de VML

En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir del 2011 de diciembre, este tema se ha archivado. Como resultado, ya no se mantiene de forma activa. Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).

 

Determina si el espacio adicional se quita por encima y por debajo del texto. Lectura/escritura **VgTriState**.

**Se aplica a**

[TextPath](msdn-online-vml-textpath-element.md)

**Sintaxis de etiquetas**

<v: *Element* style = "Trim: *Expression* " >

**Sintaxis de script**

*Element* . Style. Trim = "*expresión*"

*expresión* = de *Element*. Style. Trim

**Comentarios:**

Si es **true**, se quita el espacio reservado para ascendentes y descendentes. El valor predeterminado es **False**.

*Atributo estándar de VML*

**Ejemplo**

Se recorta el espacio adicional por encima y debajo de.


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="trim:True;font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 