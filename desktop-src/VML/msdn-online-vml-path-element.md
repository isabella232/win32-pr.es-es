---
title: Elemento de trazado VML
description: Elemento de trazado VML
ms.assetid: c5b9f9e3-edee-45fa-9387-8f15e09983ee
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1de9440761479d6b3dc6cb10c96b00ea48626247
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105676395"
---
# <a name="vml-path-element"></a>Elemento de trazado VML

En este tema se describe VML, una característica que está desusada en Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML se deben migrar a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir del 2011 de diciembre, este tema se ha archivado. Como resultado, ya no se mantiene de forma activa. Para obtener más información, vea [contenido archivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, consulte [Centro para desarrolladores de Internet Explorer](https://msdn.microsoft.com/ie/).

 

Define una ruta de acceso para una forma.

Los atributos siguientes modifican una sombra.



| Atributo                                                        | Descripción                                                                     |
|------------------------------------------------------------------|---------------------------------------------------------------------------------|
| [Arrowok](msdn-online-vml-arrowok-attribute.md)                 | Determina si se mostrarán las puntas de flecha.                                |
| [ConnectAngles](msdn-online-vml-connectangles-attribute.md)     | Especifica cómo se conectará una curva a un punto de conexión.                       |
| [ConnectLocs](msdn-online-vml-connectlocs-attribute.md)         | Define la ubicación de los puntos de conexión en una ruta de acceso.                            |
| [ConnectType](msdn-online-vml-connecttype-attribute.md)         | Define el tipo de punto de conexión utilizado para adjuntar formas a otras formas. |
| [ExtrusionOK](msdn-online-vml-extrusionok-attribute.md)         | Determina si se mostrará una extrusión.                              |
| [FillOK](msdn-online-vml-fillok-attribute.md)                   | Determina si se mostrará un relleno.                                    |
| [GradientShapeOK](msdn-online-vml-gradientshapeok-attribute.md) | Determina si se mostrará una forma de degradado.                          |
| [Id](id-attribute--path--vml.md)                                | Define un identificador único para una ruta de acceso.                                         |
| [Limo](msdn-online-vml-limo-attribute.md)                       | Define un punto de estiramiento en la ruta de acceso.                                            |
| [ShadowOK](msdn-online-vml-shadowok-attribute.md)               | Determina si se mostrará una sombra.                                  |
| [StrokeOK](msdn-online-vml-strokeok-attribute.md)               | Determina si se mostrará un trazo.                                  |
| [TextBoxRect](msdn-online-vml-textboxrect-attribute.md)         | Define uno o varios cuadros de texto dentro de una forma.                                   |
| [TextPathOK](msdn-online-vml-textpathok-attribute.md)           | Determina si se va a mostrar un textpath.                                |
| [V](msdn-online-vml-v-attribute.md)                             | Define los comandos que componen una ruta de acceso.                                       |



 

**Comentarios:**

Este elemento debe definirse dentro de un elemento de [forma](shape-element--vml.md) .

En el código siguiente se muestra cómo definir una forma con una ruta de acceso.


```HTML
   <v:shape strokecolor="red"
   coordorigin="0 0" coordsize="200 200"
   style="top:1;left:1;width:50;height:50">
   <v:path v="m 1,1 l 1,200, 200,200, 200,1 x e"/>
   </v:shape>
```



Tenga en cuenta que el atributo [V](msdn-online-vml-v-attribute.md) de **path** reemplaza el atributo [path](msdn-online-vml-path-attribute.md) de [Shape](shape-element--vml.md).

**Ejemplos**

-   [Ejemplo de elemento secundario path simple](/previous-versions/bb229545(v=vs.85))
-   [Ejemplo de elemento secundario path dinámico](https://samples.msdn.microsoft.com/workshop/samples/vml/shape/path/x_path.md)

 

 