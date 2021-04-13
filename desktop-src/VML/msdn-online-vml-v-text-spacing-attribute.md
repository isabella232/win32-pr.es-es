---
title: Atributo de espaciado de texto V de VML
description: Atributo de espaciado de texto V de VML
ms.assetid: c0d83854-4009-4d1d-aa8a-37f660dd0ef7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab31d1f0b0b1d41b7e99451c422028fe54498483
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104421064"
---
# <a name="vml-v-text-spacing-attribute"></a>Atributo de espaciado de texto V de VML

En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir del 2011 de diciembre, este tema se ha archivado. Como resultado, ya no se mantiene de forma activa. Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).

 

Define la cantidad de espaciado del texto. Lectura/escritura **VgNumber**.

**Se aplica a**

[TextPath](msdn-online-vml-textpath-element.md)

**Sintaxis de etiquetas**

<v: *Element* style = "v-Text-spacing: *Expression* " >

**Sintaxis de script**

*Element* . Style. v-Text-spacing = "*expresión*"

*expresión* = de *Element*. Style. v: espaciado de texto

**Comentarios:**

El valor predeterminado es 100. Vea el atributo de [modo de espaciado de texto V](msdn-online-vml-v-text-spacing-mode-attribute.md) para obtener más información sobre el espaciado de texto.

*Atributo estándar de VML*

**Ejemplo**

El espaciado entre letras se ajusta en 200 unidades.


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="v-text-spacing:200;v-text-spacing-mode:tightening;font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 