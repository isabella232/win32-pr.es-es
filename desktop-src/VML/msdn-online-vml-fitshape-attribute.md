---
title: Atributo FitShape de VML
description: Atributo FitShape de VML
ms.assetid: a6e5a198-1478-4256-a4f2-b9ae6db6d7fb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0adbb6fd92f296156cf2f95cf2b714cfacd2f193f8e1e1b912e6637b9e8d5cd6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120099255"
---
# <a name="vml-fitshape-attribute"></a>Atributo FitShape de VML

En este tema se describe VML, una característica que está en desuso a partir Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML deben migrarse a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir de diciembre de 2011, este tema se archivó. Como resultado, ya no se mantiene activamente. Para obtener más información, vea [Contenido archivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, [vea Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Define si el texto se ajusta al rectángulo delimitador de una forma. Lectura/escritura **DvTriState**.

**Se aplica a**

[TextPath](msdn-online-vml-textpath-element.md)

**Sintaxis de etiquetas**

<v: *element* fitshape=" *expression* ">

**Sintaxis de script**

*element* .fitshape="*expression*"

*expresión* = *elemento*.fitshape

**Comentarios:**

Si **es True**, extiende el texto hasta los bordes del cuadro que define toda la forma. El valor predeterminado es **False**.

*Atributo estándar de VML*

**Ejemplo**

El texto se ajustará para ajustarse a la forma.


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text" fitshape="True"
   style="font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 