---
title: Atributo VML V-Text-align
description: Atributo VML V-Text-align
ms.assetid: ca2cbbf6-ddbb-4f2b-942c-3fe0033bd649
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6efb96bde980a4831f400ada7032f9ee37f1d976
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103995374"
---
# <a name="vml-v-text-align-attribute"></a>Atributo VML V-Text-align

En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir del 2011 de diciembre, este tema se ha archivado. Como resultado, ya no se mantiene de forma activa. Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).

 

Define la alineación del texto. Lectura/escritura **Cadena**.

**Se aplica a**

[TextPath](msdn-online-vml-textpath-element.md)

**Sintaxis de etiquetas**

<v: *Element* style = "v-Text-align: *Expression* " >

**Sintaxis de script**

*Element* . Style. v-Text-align = "*expresión*"

*expresión* = de *Element*. Style. v-Text-align

**Comentarios:**

Estos valores incluyen:

-   **left** (valor predeterminado)
-   **correcta**
-   **Centro**
-   **ante**
-   **Carta-justificación**
-   **Stretch: justificación**

*Atributo estándar de VML*

**Ejemplo**

El texto se ajustará para ajustarse a la ruta de acceso, pero el espacio adicional se colocará entre cada letra.


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="v-text-align:letter-justify;font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 