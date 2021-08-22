---
title: Atributo Src (Stroke)(VML)
description: Atributo Src (Stroke)(VML)
ms.assetid: dac6b5b7-2038-4534-97e9-a1340102777e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57bc71d7a36ee944a2352cde6bfa1ef33f0b5c480d78c7aada751ea67db9ca7f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118596631"
---
# <a name="src-attribute-strokevml"></a>Atributo Src (Stroke)(VML)

En este tema se describe VML, una característica que está en desuso a partir Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML deben migrarse a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir de diciembre de 2011, este tema se archivó. Como resultado, ya no se mantiene activamente. Para obtener más información, vea [Contenido archivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, [vea Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Define la imagen de origen que se cargará para un relleno de trazo. Lectura/escritura **Cadena**.

**Se aplica a**

[Golpe](msdn-online-vml-stroke-element.md)

**Sintaxis de etiquetas**

<v: *element* src=" *expression* ">

**Sintaxis de script**

*element* .src="*expression*"

*expresión* = *elemento*.src

**Comentarios:**

Dirección URL de una imagen que se cargará para rellenos de imagen y patrón. Este atributo siempre debe estar presente y apuntar a datos de imagen válidos para que aparezca una imagen. Si este atributo aparece solo, es decir, sin **HRef** ni **Title**, la imagen se vincula.

*Atributo estándar de VML*

**Ejemplo**

El trazo se crea con la imagen especificada por el cylinder.gif archivo.


```HTML
   <v:shape id="rect01"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:stroke src="cylinder.gif" filltype="tile" width="10pt"/>
   </v:shape>
```





 

 