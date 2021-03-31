---
title: Atributo oculto VML
description: Atributo oculto VML
ms.assetid: b8cdb066-e4fc-4dd6-a55a-7c2488f89e61
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3e383061d3210c9c52dc8c89322bd617257555e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104077956"
---
# <a name="vml-obscured-attribute"></a>Atributo oculto VML

En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir del 2011 de diciembre, este tema se ha archivado. Como resultado, ya no se mantiene de forma activa. Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).

 

Determina si una sombra es transparente. Lectura/escritura **VgTriState**.

**Se aplica a**

[Shadow](msdn-online-vml-shadow-element.md)

**Sintaxis de etiquetas**

<v: *elemento* oculto = " *expresión* " >

**Sintaxis de script**

*Element* . Obscured = "*expresión*"

*expresión* = de *Element*. Obscured

**Comentarios:**

Si es **true**, le permite ver a través de la sombra si no hay ningún relleno en la forma. El valor predeterminado es **false**.

*Atributo estándar de VML*

**Ejemplo**

El fondo se muestra a través de la sombra.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m1,1 l 1,200,200,200, 200,1 x e">
   <v:shadow on="True" obscured="True"/>
   </v:shape>
```



 

 