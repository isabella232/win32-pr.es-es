---
title: En atributo (Stroke) (VML)
description: En atributo (Stroke) (VML)
ms.assetid: 8a966dc2-826b-4202-9c5c-c6afb00cd501
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1e418857db22ee1ac12a35e9b81840b89e06c00
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105695695"
---
# <a name="on-attribute-strokevml"></a>En atributo (Stroke) (VML)

En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir del 2011 de diciembre, este tema se ha archivado. Como resultado, ya no se mantiene de forma activa. Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).

 

Determina si se mostrará el trazo. Lectura/escritura **VgTriState**.

**Se aplica a**

[Stroke](msdn-online-vml-stroke-element.md)

**Sintaxis de etiquetas**

<v: *Element* on = " *expresión* " >

**Sintaxis de script**

*Element* . on = "*expresión*"

*expresión* = de *elemento*. on

**Comentarios:**

Si es **false**, no se muestra el trazo. El valor predeterminado es **True**.

*Atributo estándar de VML*

**Ejemplo**

No se mostrará el trazo.


```HTML
   <v:shape id="rect01"
   strokecolor="red" fillcolor="blue"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:stroke on="False"/>
   </v:shape>
```



 

 