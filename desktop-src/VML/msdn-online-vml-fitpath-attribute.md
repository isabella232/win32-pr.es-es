---
title: Atributo FitPath de VML
description: Atributo FitPath de VML
ms.assetid: f15775ed-f7b7-45d9-83ed-e307daf7451b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8863fb4d8a382ac9ccddaf7cc55fe5e8ceeff221dc1f816e340fa0a78cf9d7b2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118124788"
---
# <a name="vml-fitpath-attribute"></a>Atributo FitPath de VML

En este tema se describe VML, una característica que está en desuso a partir Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML deben migrarse a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir de diciembre de 2011, este tema se archivó. Como resultado, ya no se mantiene activamente. Para obtener más información, vea [Contenido archivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, [vea Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Define si el texto se ajusta al trazado de una forma. Lectura/escritura **DvTriState**.

**Se aplica a**

[TextPath](msdn-online-vml-textpath-element.md)

**Sintaxis de etiquetas**

<v: *element* fitpath=" *expression* ">

**Sintaxis de script**

*element* .fitpath="*expression*"

*expresión* = *elemento*.fitpath

**Comentarios:**

Si **es True**, el tamaño del texto para rellenar la ruta de acceso en la que se encuentra. El valor predeterminado es **False**.

*Atributo estándar de VML*

**Ejemplo**

El texto se ajustará a la ruta de acceso.


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text" fitpath="True"
   style="font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 