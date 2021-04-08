---
title: VML V-Same-Letter-alto atributo
description: VML V-Same-Letter-alto atributo
ms.assetid: f06c0a50-1de1-47d8-8b94-01fe0599ed59
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6d155c3c72eb67718edd33ae601d22f8e5d074a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103791973"
---
# <a name="vml-v-same-letter-heights-attribute"></a>VML V-Same-Letter-alto atributo

En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir del 2011 de diciembre, este tema se ha archivado. Como resultado, ya no se mantiene de forma activa. Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).

 

Determina si todas las letras serán el mismo alto independientemente del caso inicial. Lectura/escritura **VgTriState**.

**Se aplica a**

[TextPath](msdn-online-vml-textpath-element.md)

**Sintaxis de etiquetas**

<v: *Element* style = "v-Same-Letter-alturas: *expresión* " >

**Sintaxis de script**

*Element* . Style. v-Same-Letter-alto = "*expresión*"

*expresión* = de *Element*. Style. v-Same-Letter-alto

**Comentarios:**

Si **es true**, las letras minúsculas se ajustan al alto de las letras mayúsculas. El valor predeterminado es **False**.

*Atributo estándar de VML*

**Ejemplo**

Todas las letras tendrán el mismo alto, independientemente del uso de mayúsculas o minúsculas.


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="v-same-letter-heights:True;font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 