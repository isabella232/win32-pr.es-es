---
title: Atributo de recorte de VML
description: Atributo de recorte de VML
ms.assetid: c8038361-00bd-4787-9759-506a8a47b19a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a05f7463465c10abb4f4f01267a7ebeac878cbf36c41f1effde6ec218bad1088
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119974620"
---
# <a name="vml-trim-attribute"></a>Atributo de recorte de VML

En este tema se describe VML, una característica que está en desuso a partir Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML deben migrarse a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir de diciembre de 2011, este tema se archivó. Como resultado, ya no se mantiene activamente. Para obtener más información, vea [Contenido archivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, [vea Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Determina si se quita espacio adicional encima y debajo del texto. Lectura/escritura **DvTriState**.

**Se aplica a**

[TextPath](msdn-online-vml-textpath-element.md)

**Sintaxis de etiquetas**

<v: *element* style="trim: *expression* ">

**Sintaxis de script**

*element* .style.trim="*expression*"

*expresión* = *elemento*.style.trim

**Comentarios:**

Si **es True,** se quita el espacio reservado para ascendentes y descendientes. El valor predeterminado es **False**.

*Atributo estándar de VML*

**Ejemplo**

Se recorta el espacio adicional por encima y por debajo.


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="trim:True;font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 