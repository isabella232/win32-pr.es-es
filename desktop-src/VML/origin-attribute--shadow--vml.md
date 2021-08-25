---
title: Atributo origin (Shadow)(VML)
description: Atributo origin (Shadow)(VML)
ms.assetid: acef5134-dad6-4ba6-9d70-a9f56cd8c5ef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e1776b0d8a857a3247543eae13d280d023585229d27c04a576420003ea53920
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119959185"
---
# <a name="origin-attribute-shadowvml"></a>Atributo origin (Shadow)(VML)

En este tema se describe VML, una característica que está en desuso a partir Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML deben migrarse a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir de diciembre de 2011, este tema se archivó. Como resultado, ya no se mantiene activamente. Para obtener más información, vea [Contenido archivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, [vea Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Define el centro de la sombra. Lectura/escritura **Dvvector2D**.

**Se aplica a**

[Shadow](msdn-online-vml-shadow-element.md)

**Sintaxis de etiquetas**

<v: *element* origin=" *expression* ">

**Sintaxis de script**

*element* .origin="*expression*"

*expresión* = *elemento*.origin

**Comentarios:**

Un par de valores fraccionales de la forma, que oscilan entre el 50 % y el -50 %. El valor predeterminado es 0,0.

*Atributo estándar de VML*

**Ejemplo**

La sombra tiene un origen que está un 20 % hacia abajo y un 20 % a la derecha del origen de la forma.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:shadow on="True" origin="20%,20%"/>
   </v:shape>
```



 

 