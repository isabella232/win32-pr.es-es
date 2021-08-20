---
title: Atributo VML Offset2
description: Atributo VML Offset2
ms.assetid: a2792992-71a1-4932-8180-82ca38bd6dd2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddc06b68f075b139f6822a38672b8530fc2172071aab35072659968725d9866b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118124228"
---
# <a name="vml-offset2-attribute"></a>Atributo VML Offset2

En este tema se describe VML, una característica que está en desuso a partir Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML deben migrarse a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir de diciembre de 2011, este tema se archivó. Como resultado, ya no se mantiene activamente. Para obtener más información, vea [Contenido archivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, [vea Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Determina un segundo desplazamiento. Lectura/escritura **DvVector2D**.

**Se aplica a**

[Shadow](msdn-online-vml-shadow-element.md)

**Sintaxis de etiquetas**

<v: *element* offset2=" *expression* ">

**Sintaxis de script**

*Element* .offset2="*expression*"

*expresión* = *elemento*.offset2

**Comentarios:**

El valor predeterminado de un segundo desplazamiento para el valor x es 0 y el valor predeterminado para el valor y es 0. Los valores son una medida absoluta o un valor fraccionrio de forma. Si es fraccionista, los valores oscilan entre el 50 % y el -50 %.

Use un segundo desplazamiento para crear efectos de sombra especiales. Vea el [atributo Type](type-attribute--shadow--vml.md) para obtener más información sobre los desplazamientos de segundo.

*Atributo estándar de VML*

**Ejemplo**

Se crea una sombra doble para la forma.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:shadow on="True" color="red" color2="blue"
   offset="50%" offset2="-20%" type="double"/>
   </v:shape>
```



 

 