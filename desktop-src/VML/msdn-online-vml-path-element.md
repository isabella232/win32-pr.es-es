---
title: Elemento PATH de VML
description: Elemento PATH de VML
ms.assetid: c5b9f9e3-edee-45fa-9387-8f15e09983ee
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb46ce43d2dc9ad80aeb21340dceacde80feba99d9debdf66920b662eeaf3a9b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119308185"
---
# <a name="vml-path-element"></a>Elemento PATH de VML

En este tema se describe VML, una característica que está en desuso a partir Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML deben migrarse a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir de diciembre de 2011, este tema se archivó. Como resultado, ya no se mantiene activamente. Para obtener más información, vea [Contenido archivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, [vea Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Define un trazado para una forma.

Los atributos siguientes modifican una sombra.



| Atributo                                                        | Descripción                                                                     |
|------------------------------------------------------------------|---------------------------------------------------------------------------------|
| [Arrowok](msdn-online-vml-arrowok-attribute.md)                 | Determina si se mostrarán las puntas de flecha.                                |
| [ConnectAngles](msdn-online-vml-connectangles-attribute.md)     | Especifica cómo se conectará una curva a un punto de conexión.                       |
| [ConnectLocs](msdn-online-vml-connectlocs-attribute.md)         | Define la ubicación de los puntos de conexión en una ruta de acceso.                            |
| [ConnectType](msdn-online-vml-connecttype-attribute.md)         | Define el tipo de punto de conexión utilizado para adjuntar formas a otras formas. |
| [ExtrusiónAok](msdn-online-vml-extrusionok-attribute.md)         | Determina si se mostrará una extrusión.                              |
| [FillOK](msdn-online-vml-fillok-attribute.md)                   | Determina si se mostrará un relleno.                                    |
| [GradientShapeOK](msdn-online-vml-gradientshapeok-attribute.md) | Determina si se mostrará una forma de degradado.                          |
| [Id](id-attribute--path--vml.md)                                | Define un identificador único para una ruta de acceso.                                         |
| [Limusina](msdn-online-vml-limo-attribute.md)                       | Define un punto de extensión en la ruta de acceso.                                            |
| [ShadowOK](msdn-online-vml-shadowok-attribute.md)               | Determina si se mostrará una sombra.                                  |
| [StrokeOK](msdn-online-vml-strokeok-attribute.md)               | Determina si se mostrará un trazo.                                  |
| [TextBoxRect](msdn-online-vml-textboxrect-attribute.md)         | Define uno o varios cuadros de texto dentro de una forma.                                   |
| [TextPathOK](msdn-online-vml-textpathok-attribute.md)           | Determina si se mostrará una ruta de texto.                                |
| [V](msdn-online-vml-v-attribute.md)                             | Define los comandos que son una ruta de acceso.                                       |



 

**Comentarios:**

Este elemento debe definirse dentro de un [elemento Shape.](shape-element--vml.md)

El código siguiente muestra cómo definir una forma con un trazado.


```HTML
   <v:shape strokecolor="red"
   coordorigin="0 0" coordsize="200 200"
   style="top:1;left:1;width:50;height:50">
   <v:path v="m 1,1 l 1,200, 200,200, 200,1 x e"/>
   </v:shape>
```



Tenga en cuenta que [el atributo V](msdn-online-vml-v-attribute.md) de **Path** reemplaza el [atributo Path](msdn-online-vml-path-attribute.md) de [Shape](shape-element--vml.md).

**Ejemplos**

-   [Ejemplo de elemento secundario De ruta de acceso simple](/previous-versions/bb229545(v=vs.85))
-   [Ejemplo de elemento secundario Dynamic Path](https://samples.msdn.microsoft.com/workshop/samples/vml/shape/path/x_path.md)

 

 