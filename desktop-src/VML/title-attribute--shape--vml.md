---
title: Atributo Title (Forma)(VML)
description: Atributo Title (Forma)(VML)
ms.assetid: 08680706-5274-46d4-9199-4fdbf32f884b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55ec2a16df6740bca64357dae039f4222de956300604198b2d199977970c526d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118596513"
---
# <a name="title-attribute-shapevml"></a>Atributo Title (Forma)(VML)

En este tema se describe VML, una característica que está en desuso a partir Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML deben migrarse a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir de diciembre de 2011, este tema se archivó. Como resultado, ya no se mantiene activamente. Para obtener más información, vea [Contenido archivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, [vea Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Define el texto que se muestra cuando el puntero del mouse se mueve sobre la forma. Lectura/escritura **Cadena**.

**Se aplica a**

[Forma](shape-element--vml.md)

**Sintaxis de etiquetas**

<v: *element* title=" *expression* ">

**Sintaxis de script**

*element* .title="*expression*"

*expresión* = *elemento*.title

**Comentarios:**

El **atributo Title** es similar al atributo título HTML estándar.  El comportamiento de un título es similar a una información sobre herramientas Windows Microsoft.

**Atributo estándar de VML**

**Ejemplo**

El título de la forma es "Presentación de información sobre herramientas" y aparecerá cuando el puntero del mouse se mueva sobre la forma.


```HTML
   <v:rect id=myrect fillcolor="red" title="ToolTip display"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



[Ejemplo de atributo title](/previous-versions/bb264097(v=vs.85)). (Requiere Microsoft Internet Explorer 5 o superior).

 

 