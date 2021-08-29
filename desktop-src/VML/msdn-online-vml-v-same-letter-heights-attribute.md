---
title: Atributo V-Same-Letter-Heights de VML
description: Atributo V-Same-Letter-Heights de VML
ms.assetid: f06c0a50-1de1-47d8-8b94-01fe0599ed59
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 219d9f06e120ccc86bfa41c1cfff69b7feb64d68b1343732d45f57f26d952b21
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119864155"
---
# <a name="vml-v-same-letter-heights-attribute"></a>Atributo V-Same-Letter-Heights de VML

En este tema se describe VML, una característica que está en desuso a partir Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML deben migrarse a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir de diciembre de 2011, este tema se archivó. Como resultado, ya no se mantiene activamente. Para obtener más información, vea [Contenido archivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, [vea Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Determina si todas las letras tendrán el mismo alto, independientemente del caso inicial. Lectura/escritura **DvTriState**.

**Se aplica a**

[TextPath](msdn-online-vml-textpath-element.md)

**Sintaxis de etiquetas**

<v: *element* style="v-same-letter-heights: *expression* ">

**Sintaxis de script**

*element* .style.v-same-letter-heights="*expression*"

*expresión* = *elemento*.style.v-same-letter-heights

**Comentarios:**

Si **es True**, las letras minúsculas se extienden hasta el alto de las letras mayúsculas. El valor predeterminado es **False**.

*Atributo estándar de VML*

**Ejemplo**

Todas las letras tendrán el mismo alto, independientemente de las mayúsculas y minúsculas.


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="v-same-letter-heights:True;font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 