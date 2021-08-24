---
title: Atributo de ruta de acceso de VML
description: Atributo de ruta de acceso de VML
ms.assetid: ecb64a2f-65f7-4eb9-8d67-d7909bf52d9c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f314956452db5a88011a147fd05302483e50cbce3724cf8188068770ec492db6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119136968"
---
# <a name="vml-path-attribute"></a>Atributo de ruta de acceso de VML

En este tema se describe VML, una característica que está en desuso a partir Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML deben migrarse a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir de diciembre de 2011, este tema se archivó. Como resultado, ya no se mantiene activamente. Para obtener más información, vea [Contenido archivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, [vea Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Especifica la línea que forma los bordes de una forma. Lectura/escritura **Cadena**.

**Se aplica a**

[Forma](shape-element--vml.md)

**Sintaxis de etiquetas**

<v: *element* path=" *expression* ">

**Sintaxis de script**

*element* .path="*expression*"

*expresión* = *elemento*.path

**Comentarios:**

Si una forma contiene el [elemento Path,](msdn-online-vml-path-element.md) los comandos path del elemento Path tienen prioridad sobre el valor del atributo de forma. Consulte el tema **elemento Path** para obtener más información sobre el conjunto de comandos que se usa para las rutas de acceso.

*Atributo estándar de VML*

**Ejemplo**

Se define una ruta de acceso cuadrada cerrada en la cadena del atributo path. Un punto inicial se define con (se usa para el comando moveto) en 1,1 y se dibuja una línea con (la letra "L" usada para la línea de comandos para ) desde la posición inicial (1,1) a los otros tres puntos `m`  `l` (en orden): 1200; 200 200;  200,1. La línea se cierra con `x` (**close**) y termina con `e` (**end**). Tenga en cuenta que las coordenadas se dan en el espacio de coordenadas relativo y que el tamaño real viene determinado por **el ancho y** **alto.**


```HTML
   <v:shape id="rect01"
   fillcolor="red" strokecolor="red"
   coordorigin="0 0" coordsize="200 200"
   style="position:relative;top:1;left:1;width:20;height:20"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   </v:shape>
```



[Ejemplo de atributo path](/previous-versions/bb264089(v=vs.85)). (Requiere Microsoft Internet Explorer 5 o superior).

 

 