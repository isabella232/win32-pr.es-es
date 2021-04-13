---
title: Atributo V-Text-Anchor de VML
description: Atributo V-Text-Anchor de VML
ms.assetid: d6e2f60c-5cc7-4340-a9cd-b6c2b0b5b0be
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 603f118a260c8ce9c271128fa642e9e2ae569806
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104421065"
---
# <a name="vml-v-text-anchor-attribute"></a>Atributo V-Text-Anchor de VML

En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir del 2011 de diciembre, este tema se ha archivado. Como resultado, ya no se mantiene de forma activa. Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).

 

Define la delimitación vertical del texto en un cuadro de texto. Lectura/escritura **Cadena**.

**Se aplica a**

[TextBox](msdn-online-vml-textbox-element.md)

**Sintaxis de etiquetas**

<v: *elemento* v-Text-Anchor = " *expresión* " >

**Comentarios:**

Estos valores incluyen:

-   **Top** (predeterminado)
-   **Apellido**
-   **descendente**
-   **Centro superior**
-   **Centro central**
-   **centro inferior**
-   **línea de base superior**
-   **línea de base inferior**
-   **Centro de la línea de base superior**
-   **línea central inferior**

El texto se delimitará a una posición vertical en el cuadro de texto tal y como se indica en el valor del atributo. La alineación de un delimitador de texto solo es evidente si [MSO-Fit-Text-to-Shape](msdn-online-vml-mso-fit-text-to-shape-attribute.md) es **false**. Este atributo es diferente del atributo de estilo **vertical-align** , que se usa para los Idiomas ideográficos.

Este atributo lo usa Microsoft Office para almacenar datos en documentos web, pero no se representa en Microsoft Internet Explorer 5 o posterior.

*Atributo estándar de VML*

**Ejemplo**

El texto se alinea en la parte inferior del cuadro de texto.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="red"
   style="top:10pt;left:10pt;width:50pt;height:50pt"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:textbox style="v-text-anchor:bottom" id="mytextbox">
   VML
   </v:textbox/>
   </v:shape>
```



 

 