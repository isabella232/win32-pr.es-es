---
title: Atributo GradientShapeOK de VML
description: Atributo GradientShapeOK de VML
ms.assetid: c26ac4cb-f7f0-4666-b32f-d9fcaf9044a2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53c25620f8ebc05905b83f3abab7b52f7a206b6bafb522b0104f06fd8f46d6bf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118124778"
---
# <a name="vml-gradientshapeok-attribute"></a>Atributo GradientShapeOK de VML

En este tema se describe VML, una característica que está en desuso a partir Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML deben migrarse a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir de diciembre de 2011, este tema se archivó. Como resultado, ya no se mantiene activamente. Para obtener más información, vea [Contenido archivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, [vea Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Determina si un trazado de degradado se consocirá de rutas de acceso concéntricas repetidas. Lectura/escritura **DvTriState**.

**Se aplica a**

[Ruta de acceso](msdn-online-vml-path-element.md)

**Sintaxis de etiquetas**

<v: *element* gradientshapeok=" *expression* ">

**Sintaxis de script**

*element* .gradientshapeok="*expression*"

*expresión* = *elemento*.gradientshapeok

**Comentarios:**

Si **es True,** el trazado se rellenará con un relleno de degradado concéntrica usando el trazado como forma repetida del degradado. El valor predeterminado es **False.**

*Atributo estándar de VML*

**Ejemplo**

El trazado se rellenará con un relleno de degradado concentrico que se formará con rectángulos repetidos.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:path gradientshapeok="True"/>
   </v:shape>
```



 

 