---
title: Atributo Offset (Shadow)(VML)
description: Atributo Offset (Shadow)(VML)
ms.assetid: bb5810cd-bd9a-4888-a0ce-8de732215c80
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0683e9536e10bed141ecca56b4335d6221c5ced7e3d26220908aa388b453843
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118596910"
---
# <a name="offset-attribute-shadowvml"></a>Atributo Offset (Shadow)(VML)

En este tema se describe VML, una característica que está en desuso a partir Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML deben migrarse a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir de diciembre de 2011, este tema se archivó. Como resultado, ya no se mantiene activamente. Para obtener más información, vea [Contenido archivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, [vea Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Define hasta qué punto se extiende la sombra más allá de la forma. Lectura/escritura **DvVector2D**.

**Se aplica a**

[Shadow](msdn-online-vml-shadow-element.md)

**Sintaxis de etiquetas**

<v: *element* offset=" *expression* ">

**Sintaxis de script**

*element* .offset="*expression*"

*expresión* = *elemento*.offset

**Comentarios:**

El desplazamiento predeterminado para el valor x es 2pt y el valor predeterminado para el valor y es 2pt. Los valores son una medida absoluta o un valor fraccionrio de forma. Si son fraccionales, oscilan entre el 50 % y el -50 %.

*Atributo estándar de VML*

**Ejemplo**

La forma tiene una sombra con un desplazamiento de 5 puntos hacia abajo y 10 puntos a la derecha.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:shadow on="True" offset="10pt,5pt"/>
   </v:shape>
```



 

 