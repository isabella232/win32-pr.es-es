---
title: Atributo Color2 (Trazo)(VML)
description: Atributo Color2 (Trazo)(VML)
ms.assetid: 60b8035e-9477-4f8b-817b-dd6c41bdfa79
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 108c767f7337f486f8b7df5a4506b3b3d487dabf146656890def0c5e1ad32a88
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119867435"
---
# <a name="color2-attribute-strokevml"></a>Atributo Color2 (Trazo)(VML)

En este tema se describe VML, una característica que está en desuso a partir Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML deben migrarse a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir de diciembre de 2011, este tema se archivó. Como resultado, ya no se mantiene activamente. Para obtener más información, vea [Contenido archivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, [vea Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Define un segundo color para los trazos. Lectura/escritura **Cadena**.

**Se aplica a**

[Golpe](msdn-online-vml-stroke-element.md)

**Sintaxis de etiquetas**

<v: *element* color2=" *expression* ">

Sintaxis de script

*element* .color2="*expression*"

*expresión* = *elemento*.color2

**Comentarios:**

Se usa un segundo color cuando el tipo de relleno de un trazo es un patrón.

*Atributo estándar de VML*

**Ejemplo**

El trazo de la forma es un relleno de patrón donde la imagen de origen define el relleno, pero el fondo transparente se define mediante el segundo color.


```HTML
   <v:shape id="rect01"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:stroke filltype="pattern" width="5pt" src="cylinder.gif" color2="green"/>
   </v:shape>
```



 

 