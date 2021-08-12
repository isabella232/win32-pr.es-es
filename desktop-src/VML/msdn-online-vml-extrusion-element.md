---
title: Elemento de extrusión de VML
description: Elemento de extrusión de VML
ms.assetid: d26b2451-383a-4ded-a46d-5ecca05ddb7f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9ee19db9d933f0b6b749c3165281614d1be87b0e0828f43849f8a36a5b37067
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118601345"
---
# <a name="vml-extrusion-element"></a>Elemento de extrusión de VML

En este tema se describe VML, una característica que está en desuso a partir Windows Internet Explorer 9. Las páginas web y las aplicaciones que se basan en VML deben migrarse a SVG u otros estándares ampliamente admitidos.

> [!Note]  
> A partir de diciembre de 2011, este tema se archivó. Como resultado, ya no se mantiene activamente. Para obtener más información, vea [Contenido archivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obtener información, recomendaciones e instrucciones sobre la versión actual de Windows Internet Explorer, [vea Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Define una extrusión para una forma.

Los atributos siguientes modifican una extrusión.



| Atributo                                                              | Descripción                                                                                             |
|------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| [AutoRotationCenter](msdn-online-vml-autorotationcenter-attribute.md) | Determina si el centro de rotación será el centro geométrico de la extrusión.                |
| [BackDepth](msdn-online-vml-backdepth-attribute.md)                   | Define la cantidad de extrusión hacia atrás.                                                               |
| [Luminosidad](msdn-online-vml-brightness-attribute.md)                 | Especifica la cantidad de brillo de una escena.                                                          |
| [Color](color-attribute--extrusion--vml.md)                           | Define el color de las caras de la extrusión.                                                               |
| [ColorMode](msdn-online-vml-colormode-attribute.md)                   | Determina el modo de color de extrusión.                                                                 |
| [Diffusity](msdn-online-vml-diffusity-attribute.md)                   | Define la cantidad de luz reflejada a partir de una forma extruida.                              |
| [Edge](msdn-online-vml-edge-attribute.md)                             | Define el bisel aparente de los bordes de la extrusión.                                                      |
| [Ext](ext-attribute--extrusion--vml.md)                               | Define el comportamiento predeterminado de la extrusión para los editores gráficos.                                           |
| [Faceta](msdn-online-vml-facet-attribute.md)                           | Define el número de facetas usadas para describir las superficies curvas de una extrusión.                          |
| [ForeDepth](msdn-online-vml-foredepth-attribute.md)                   | Define la cantidad de extrusión hacia delante.                                                                |
| [LightFace](msdn-online-vml-lightface-attribute.md)                   | Determina si la cara frontal de la extrusión responderá a los cambios en la iluminación.             |
| [LightHarsh](msdn-online-vml-lightharsh-attribute.md)                 | Determina si la fuente de luz principal será dura.                                              |
| [LightHarsh2](msdn-online-vml-lightharsh2-attribute.md)               | Determina si la fuente de luz secundaria será dura.                                            |
| [LightLevel](msdn-online-vml-lightlevel-attribute.md)                 | Define la intensidad de la fuente de luz principal para la escena.                                        |
| [LightLevel2](msdn-online-vml-lightlevel2-attribute.md)               | Define la intensidad de la fuente de luz secundaria para la escena.                                      |
| [LightPosition](msdn-online-vml-lightposition-attribute.md)           | Especifica la posición de la luz principal en una escena.                                                 |
| [LightPosition2](msdn-online-vml-lightposition2-attribute.md)         | Especifica la posición de la luz secundaria en una escena.                                               |
| [LockRotationCenter](msdn-online-vml-lockrotationcenter-attribute.md) | Determina si el atributo **RotationAngle** especifica la rotación del objeto extruido. |
| [Metal](msdn-online-vml-metal-attribute.md)                           | Determina si la superficie de la forma extruida se parecerá al metal.                               |
| [Activado](on-attribute--extrusion--vml.md)                                 | Determina si se mostrará una extrusión.                                                      |
| [Orientación](msdn-online-vml-orientation-attribute.md)               | Especifica el vector alrededor del cual se girará una forma.                                              |
| [OrientationAngle](msdn-online-vml-orientationangle-attribute.md)     | Define el ángulo en el que una extrusión gira alrededor de la orientación.                                     |
| [Avión](msdn-online-vml-plane-attribute.md)                           | Especifica el plano que está en ángulos derecho para la extrusión.                                           |
| [Representar](msdn-online-vml-render-attribute.md)                         | Define el modo de representación de la extrusión.                                                            |
| [RotationAngle](msdn-online-vml-rotationangle-attribute.md)           | Especifica la rotación del objeto sobre los ejes x e y.                                           |
| [RotationCenter](msdn-online-vml-rotationcenter-attribute.md)         | Especifica el centro de rotación de una forma.                                                           |
| [Brillo](msdn-online-vml-shininess-attribute.md)                   | Define la concentración de luz reflejada de una superficie de extrusión.                                   |
| [SkewAmt](msdn-online-vml-skewamt-attribute.md)                       | Define la cantidad de sesgo de una extrusión.                                                             |
| [SkewAngle](msdn-online-vml-skewangle-attribute.md)                   | Define el ángulo de sesgo de una extrusión.                                                              |
| [Especularidad](msdn-online-vml-specularity-attribute.md)               | Define la especulación de una forma extruida.                                                           |
| [Type](type-attribute--extrusion--vml.md)                             | Define la forma en que se extruye la forma.                                                             |
| [Mirador](msdn-online-vml-viewpoint-attribute.md)                   | Define el punto de vista del observador.                                                                  |
| [ViewpointOrigin](msdn-online-vml-viewpointorigin-attribute.md)       | Define el origen del punto de vista dentro del cuadro de límite de la forma.                               |



 

**Comentarios:**

Este elemento debe definirse dentro de un [elemento Shape.](shape-element--vml.md)

Además, el [atributo On](on-attribute--extrusion--vml.md) debe establecerse en **True.**

A continuación se muestra el código mínimo necesario para generar una extrusión.


```HTML
   <v:rect style="width:50px;height:50px">
   <v:extrusion on="True"/>
   </v:rect>
```



**Ejemplos**

-   [Extrusión de forma simple](/previous-versions/bb229656(v=vs.85))
-   [Extrusión de formas dinámicas](/previous-versions/bb229657(v=vs.85))

 

 