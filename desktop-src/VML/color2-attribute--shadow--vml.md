---
title: Atributo Color2 (Shadow)(VML)
description: Atributo Color2 (Shadow)(VML)
ms.assetid: 265d189a-1a11-4f57-9299-1bc1efd13595
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 241c7e0a620b6b5f2f54a8849779dcc905d027781fe38a5121ca74b6acbeac4f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119655705"
---
# <a name="color2-attribute-shadowvml"></a>Atributo Color2 (Shadow)(VML)

En este tema se describe VML, una característica que está en desuso a partir Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML deben migrarse a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir de diciembre de 2011, este tema se archivó. Como resultado, ya no se mantiene activamente. Para obtener más información, vea [Contenido archivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, [vea Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Define el segundo color de una sombra. Lectura/escritura **DvColor**.

**Se aplica a**

[Shadow](msdn-online-vml-shadow-element.md)

**Sintaxis de etiquetas**

<v: *element* color2=" *expression* ">

**Sintaxis de script**

*element* .color2="*expression*"

*expresión* = *elemento*.color2

**Comentarios:**

Use un segundo color para crear efectos de sombra especiales. Vea el [atributo Type](type-attribute--shadow--vml.md) para obtener más información sobre los segundos colores.

*Atributo estándar de VML*

**Ejemplo**

La sombra tiene un color azul para un segundo color.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:shadow on="True" color="green" color2="blue"/>
   </v:shape>
```



 

 