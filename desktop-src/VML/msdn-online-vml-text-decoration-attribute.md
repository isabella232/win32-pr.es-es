---
title: Atributo de Text-Decoration VML
description: Atributo de Text-Decoration VML
ms.assetid: a64985bd-d025-4e9c-bb4b-bf0450d5143a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 474d76b9e37cb363a8b2a28b84c30be77f857159767cc4db221fd7a684b4951e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119796035"
---
# <a name="vml-text-decoration-attribute"></a>Atributo de Text-Decoration VML

En este tema se describe VML, una característica que está en desuso a partir Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML deben migrarse a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir de diciembre de 2011, este tema se archivó. Como resultado, ya no se mantiene activamente. Para obtener más información, vea [Contenido archivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, [vea Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Define el estilo de la decoración de texto. Lectura/escritura **Cadena**.

**Se aplica a**

[TextPath](msdn-online-vml-textpath-element.md)

**Sintaxis de etiquetas**

<v: *element* style="text-decoration: *expression* ">

**Sintaxis de script**

*element* .style.textdecoration="*expression*"

*expresión* = *elemento*.style.textdecoration

**Comentarios:**

Estos valores incluyen:

-   none (valor predeterminado)
-   subrayado
-   línea alta
-   línea a través
-   blink

*Atributo estándar de VML*

**Ejemplo**

El texto se subraya.


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="text-decoration:underline;font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 