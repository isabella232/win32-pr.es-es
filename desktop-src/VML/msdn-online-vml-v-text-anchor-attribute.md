---
title: Atributo V-Text-Anchor de VML
description: Atributo V-Text-Anchor de VML
ms.assetid: d6e2f60c-5cc7-4340-a9cd-b6c2b0b5b0be
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7c4b355aa4e56e3b0320200a092a66aa1f504b16be02f697e1335cd295627c6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119057703"
---
# <a name="vml-v-text-anchor-attribute"></a>Atributo V-Text-Anchor de VML

En este tema se describe VML, una característica que está en desuso a partir Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML deben migrarse a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir de diciembre de 2011, este tema se archivó. Como resultado, ya no se mantiene activamente. Para obtener más información, vea [Contenido archivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, [vea Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Define el delimitador vertical del texto en un cuadro de texto. Lectura/escritura **Cadena**.

**Se aplica a**

[TextBox](msdn-online-vml-textbox-element.md)

**Sintaxis de etiquetas**

<v: *elemento* v-text-anchor=" *expresión* ">

**Comentarios:**

Estos valores incluyen:

-   **top** (valor predeterminado)
-   **Medio**
-   **Parte inferior**
-   **centro superior**
-   **centro intermedio**
-   **centro inferior**
-   **línea de base superior**
-   **línea de base inferior**
-   **top-center-baseline**
-   **bottom-center-baseline**

El texto se delimitará a una posición vertical en el cuadro de texto como indica el valor del atributo . La alineación de un delimitador de texto solo es evidente si [MSO-Fit-Text-To-Shape](msdn-online-vml-mso-fit-text-to-shape-attribute.md) es **False.** Este atributo es diferente del atributo **Estilo de alineación vertical,** que se usa para lenguajes ideográficos.

Este atributo lo usa Microsoft Office almacenar datos en documentos web, pero no se representa en Microsoft Internet Explorer 5 o superior.

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



 

 