---
title: Atributo de modo de espaciado-texto (V) de VML
description: Atributo de modo de espaciado-texto (V) de VML
ms.assetid: 2c20e9d7-cb6a-4da7-af7a-9a7b1baa8e1f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a288f89a1405412ba8c582a5c52c7bfe56809c38
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104488247"
---
# <a name="vml-v-text-spacing-mode-attribute"></a>Atributo de modo de espaciado-texto (V) de VML

En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir del 2011 de diciembre, este tema se ha archivado. Como resultado, ya no se mantiene de forma activa. Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).

 

Define el modo de espaciado entre letras. Lectura/escritura **Cadena**.

**Se aplica a**

[TextPath](msdn-online-vml-textpath-element.md)

**Sintaxis de etiquetas**

<v: *Element* style = "v-Text-spacing-Mode: *expresión* " >

**Sintaxis de script**

*Element* . Style. v-Text-spacing-Mode = "*expresión*"

*expresión* = de *Element*. Style. v: modo de espaciado de texto

**Comentarios:**

Los valores incluyen

-   **apretar** (valor predeterminado)
-   **llevar**

Este atributo determina si se quitará el espacio entre cada letra (apriete) o se agregará entre cada letra (seguimiento). La cantidad de cambio de letterSpacing se define mediante el atributo [de espaciado de texto V](msdn-online-vml-v-text-spacing-attribute.md) .

*Atributo estándar de VML*

**Ejemplo**

El espaciado entre letras se incrementa en 200 unidades.


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="v-text-spacing:200;v-text-spacing-mode:tracking;font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 