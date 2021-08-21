---
title: Atributo V-Text-Spacing de VML
description: Atributo V-Text-Spacing de VML
ms.assetid: c0d83854-4009-4d1d-aa8a-37f660dd0ef7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc0b699e70cd235bf7d0f7530f75a8fc5eaef52974180cc8d36a10a69c9197f7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119057683"
---
# <a name="vml-v-text-spacing-attribute"></a>Atributo V-Text-Spacing de VML

En este tema se describe VML, una característica que está en desuso a partir Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML deben migrarse a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir de diciembre de 2011, este tema se archivó. Como resultado, ya no se mantiene activamente. Para obtener más información, vea [Contenido archivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, [vea Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Define la cantidad de espaciado para el texto. Lectura/escritura **NumberNumber**.

**Se aplica a**

[TextPath](msdn-online-vml-textpath-element.md)

**Sintaxis de etiquetas**

<v: *element* style="v-text-spacing: *expression* ">

**Sintaxis de script**

*element* .style.v-text-spacing="*expression*"

*expresión* = *elemento*.style.v-text-spacing

**Comentarios:**

El valor predeterminado es 100. Vea el [atributo V-Text-Spacing-Mode](msdn-online-vml-v-text-spacing-mode-attribute.md) para obtener más información sobre el espaciado de texto.

*Atributo estándar de VML*

**Ejemplo**

Las letras que se escriben entre cada letra se estrechan en 200 unidades.


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="v-text-spacing:200;v-text-spacing-mode:tightening;font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 