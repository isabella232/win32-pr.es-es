---
title: Atributo de ruta de acceso VML
description: Atributo de ruta de acceso VML
ms.assetid: ecb64a2f-65f7-4eb9-8d67-d7909bf52d9c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e43e453e982327549475de4643cc0ad21bc0b4db
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103904805"
---
# <a name="vml-path-attribute"></a>Atributo de ruta de acceso VML

En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir del 2011 de diciembre, este tema se ha archivado. Como resultado, ya no se mantiene de forma activa. Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).

 

Especifica la línea que constituye los bordes de una forma. Lectura/escritura **Cadena**.

**Se aplica a**

[Forma](shape-element--vml.md)

**Sintaxis de etiquetas**

<v: *elemento* path = " *expresión* " >

**Sintaxis de script**

*Element* . Path = "*expresión*"

*expresión* = de *Element*. Path

**Comentarios:**

Si una forma contiene el elemento [path](msdn-online-vml-path-element.md) , los comandos path del elemento path tienen prioridad sobre el valor del atributo Shape. Vea el tema del elemento path para obtener más información sobre el conjunto de comandos que se usa para las rutas de **acceso** .

*Atributo estándar de VML*

**Ejemplo**

Una ruta de acceso cuadrada cerrada se define en la cadena del atributo path. Un punto inicial se define con `m` (se usa para el comando **moveTo** ) en 1, 1 y se dibuja una línea con `l` (la letra "L" usada para la **línea** de comandos) desde la posición inicial (1,1) hasta los otros tres puntos (en orden): 1.200; 200.200; 200, 1. La línea se cierra con `x` (**Close**) y termina con `e` (**End**). Tenga en cuenta que las coordenadas se proporcionan en el espacio de coordenadas relativo y que el **ancho** y el **alto** determinan el tamaño real.


```HTML
   <v:shape id="rect01"
   fillcolor="red" strokecolor="red"
   coordorigin="0 0" coordsize="200 200"
   style="position:relative;top:1;left:1;width:20;height:20"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   </v:shape>
```



[Ejemplo de atributo de ruta de acceso](/previous-versions/bb264089(v=vs.85)). (Requiere Microsoft Internet Explorer 5 o posterior).

 

 