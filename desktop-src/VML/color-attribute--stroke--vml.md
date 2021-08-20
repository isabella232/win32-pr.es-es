---
title: Atributo color (Trazo)(VML)
description: Atributo color (Trazo)(VML)
ms.assetid: 8fa19789-0bd6-4e9f-8af4-566155eafc6a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a17b3dd30d95765c98ec754526349b2bdc274696112043065fa7ddc7d894b582
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118125375"
---
# <a name="color-attribute-strokevml"></a>Atributo color (Trazo)(VML)

En este tema se describe VML, una característica que está en desuso a partir Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML deben migrarse a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir de diciembre de 2011, este tema se archivó. Como resultado, ya no se mantiene activamente. Para obtener más información, vea [Contenido archivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, [vea Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Define el color de un trazo. Lectura/escritura **DvColor**.

**Se aplica a**

[Golpe](msdn-online-vml-stroke-element.md)

**Sintaxis de etiquetas**

<v: *element* color=" *expression* ">

**Sintaxis de script**

*element* .color="*expression*"

*expresión* = *elemento*.color

**Comentarios:**

Invalida el atributo **StrokeColor** de una forma. El valor predeterminado es **negro.**

*Atributo estándar de VML*

**Ejemplo**

La forma tiene un color de trazo **verde,** no **rojo.**


```HTML
   <v:shape id="rect01"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:stroke color="green"/>
   </v:shape>
```



 

 