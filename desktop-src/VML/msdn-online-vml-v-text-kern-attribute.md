---
title: Atributo V-Text-Kern de VML
description: Atributo V-Text-Kern de VML
ms.assetid: cece49c3-8e62-4327-8949-684a1d073293
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e5ca41b66c05af673839ccbc8ba9eb95cf652eb223cd4dd3915799e91ff6c69
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119974635"
---
# <a name="vml-v-text-kern-attribute"></a>Atributo V-Text-Kern de VML

En este tema se describe VML, una característica que está en desuso a partir Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML deben migrarse a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir de diciembre de 2011, este tema se archivó. Como resultado, ya no se mantiene activamente. Para obtener más información, vea [Contenido archivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, [vea Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Determina si el kerning está activado. Lectura/escritura **DvTriState**.

**Se aplica a**

[TextPath](msdn-online-vml-textpath-element.md)

**Sintaxis de etiquetas**

<v: *element* style="v-text-kern: *expression* ">

**Sintaxis de script**

*element* .style.v-text-kern="*expression*"

*expresión* = *elemento*.style.v-text-kern

**Comentarios:**

Si **es True**, el kerning está activado. El valor predeterminado es **False**. El kerning es la eliminación de espacio entre determinados pares de letras para compensar las formas de letra desiguales. Por ejemplo, si el kerning está activado, se quitaría espacio adicional entre una "T" mayúscula y una "i" minúscula.

*Atributo estándar de VML*

**Ejemplo**

Kerning está activado.


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="v-text-kern:True;font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 