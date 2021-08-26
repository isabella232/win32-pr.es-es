---
title: Compatibilidad con SVG
description: A partir Windows 10 actualización de aniversario, Direct2D admite la representación de fuentes de color que contienen contornos de glifo SVG, como se describe en la especificación OpenType (vea la tabla "SVG").
ms.assetid: 5cb4cb7c-9b96-e110-bff9-d75ad1980010
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c8c5f34531264f95c3617d1324079895b6444cbdbc776d5468fe51fc9890992
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119917105"
---
# <a name="svg-support"></a>Compatibilidad con SVG

A partir de Windows 10 de aniversario, Direct2D admite la representación de fuentes de [color](../directwrite/color-fonts.md) que contienen contornos de glifo SVG, como se describe en la especificación [OpenType](/typography/opentype/spec/) (consulte [la tabla SVG](/typography/opentype/spec/svg)). A partir Windows 10 Creators Update, Direct2D también admite la representación de imágenes SVG independientes. Sin embargo, algunas características SVG no se admiten dentro de las fuentes SVG openType y direct2D no admite actualmente determinadas características SVG.  

En este tema se identifica el conjunto de características [SVG 1.1](https://www.w3.org/TR/SVG11/) compatibles con Direct2D en Windows 10 de aniversario y versiones más recientes. Este documento se aplica a SVG en fuentes OpenType, así como a imágenes SVG independientes.

## <a name="supported-svg-elements-and-attributes"></a>Atributos y elementos SVG admitidos

Direct2D admite la representación de los siguientes elementos SVG y los atributos asociados para cada elemento. Se omiten otros elementos y atributos normales.



| Elemento                                                                                  | Atributos normales admitidos                                                             |
|------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| [circunferencia](https://www.w3.org/TR/SVG11/shapes.mdl#circleelement)                           | id, style, transform, cx, cy, r                                                          |
| [clipPath](https://www.w3.org/TR/SVG11/masking.mdl#clippathelement)                      | id, style, transform, clipPathUnits                                                      |
| [defs](https://www.w3.org/TR/SVG11/struct.mdl#defselement)                               | id, style, transform                                                                     |
| [Desc](https://www.w3.org/TR/SVG11/struct.mdl#descriptionandtitleelements)<sup>\*</sup>  | id                                                                                       |
| [ellipse](https://www.w3.org/TR/SVG11/shapes.mdl#ellipseelement)                         | id, style, transform, cx, cy, rx, ry                                                     |
| [g](https://www.w3.org/TR/SVG11/struct.mdl#gelement)                                     | id, style, transform                                                                     |
| [image](https://www.w3.org/TR/SVG11/struct.mdl#imageelement)                             | id, style, transform, x, y, width, height, preserveAspectRatio, xlink:href               |
| [Línea](https://www.w3.org/TR/SVG11/shapes.mdl#lineelement)                               | id, style, transform, x1, y1, x2, y2                                                     |
| [linearGradient](https://www.w3.org/TR/SVG11/pservers.mdl#lineargradientelement)         | id, style, x1, y1, x2, y2, gradientUnits, gradientTransform, spreadMethod, xlink:href    |
| [path](https://www.w3.org/TR/SVG11/paths.mdl#pathelement)                                | id, style, transform, d                                                                  |
| [Polígono](https://www.w3.org/TR/SVG11/shapes.mdl#polygonelement)                         | id, style, transform, points                                                             |
| [Polilínea](https://www.w3.org/TR/SVG11/shapes.mdl#polylineelement)                       | id, style, transform, points                                                             |
| [radialGradient](https://www.w3.org/TR/SVG11/pservers.mdl#radialgradientelement)         | id, style, cx, cy, r, fx, fy, gradientUnits, gradientTransform, spreadMethod, xlink:href |
| [Rect](https://www.w3.org/TR/SVG11/shapes.mdl#rectelement)                               | id, style, transform, x, y, width, height, rx, ry                                        |
| [stop](https://www.w3.org/TR/SVG11/pservers.mdl#stopelement)                             | id, style, offset                                                                        |
| [Svg](https://www.w3.org/TR/SVG11/struct.mdl#svgelement)                                 | id, style, x, y, width, height, viewBox, preserveAspectRatio                             |
| [Título](https://www.w3.org/TR/SVG11/struct.mdl#descriptionandtitleelements)<sup>\*</sup> | id                                                                                       |
| [use](https://www.w3.org/TR/SVG11/struct.mdl#useelement)                                 | id, style, transform, x, y, width, height, xlink:href                                    |



 

<sup>\*</sup>Solo se admite en Windows 10 Creators Update y versiones más recientes

## <a name="supported-svg-presentation-attributes"></a>Atributos de presentación SVG admitidos

Direct2D también admite los siguientes atributos de presentación. Se pueden especificar en cualquier elemento SVG, pero solo afectan a la apariencia de determinados elementos, como se describe en la especificación SVG (vea [Atributos de presentación](https://www.w3.org/TR/SVG11/attindex.mdl#presentationattributes)).

-   clip-path
-   clip-rule
-   color
-   Monitor<sup>\*</sup>
-   fill
-   fill-opacity
-   fill-rule
-   opacidad
-   desbordamiento
-   stop-color
-   stop-opacity
-   stroke
-   stroke-dasharray
-   stroke-dashoffset
-   stroke-linecap
-   stroke-linejoin
-   stroke-miterlimit
-   opacidad del trazo
-   ancho de trazo
-   Visibilidad<sup>\*</sup>

<sup>\*</sup>Solo se admite en Windows 10 Creators Update y versiones más recientes

## <a name="unsupported-svg-features"></a>Características SVG no admitidas

### <a name="unsupported-elements-and-attributes"></a>Atributos y elementos no admitidos

Direct2D considera que cualquier elemento o atributo no incluido en las listas anteriores no es compatible. Al analizar contenido SVG que contiene un elemento o atributo no admitidos, se omite la entidad no admitida. El resto del contenido se representa de la manera más adecuada posible.

### <a name="unsupported-length-units"></a>Unidades de longitud no admitidas

A Windows 10 de aniversario, Direct2D solo admite valores de longitud de espacio de usuario y valores de longitud porcentual. No se admiten las longitudes con sufijos de unidad, como "mm" o "em".

A partir Windows 10 Fall Creators Update, Direct2D también admite identificadores de unidad absolutos: px, pt, pc, cm, mm y in. No se admiten los identificadores de unidad relativa (em, p. ej.).

### <a name="unsupported-image-sources"></a>Orígenes de imágenes no admitidos

El elemento image solo se admite si su atributo xlink:href está establecido en una imagen codificada en base64. No se admiten referencias remotas.

 

 