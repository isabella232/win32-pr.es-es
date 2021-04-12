---
title: Compatibilidad con SVG
description: A partir de la actualización de aniversario de Windows 10, Direct2D admite la representación de fuentes de color que contienen contornos de glifos SVG, como se describe en la especificación OpenType (vea la tabla ' SVG ').
ms.assetid: 5cb4cb7c-9b96-e110-bff9-d75ad1980010
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 678c5d9ef42a53c854bb2f175fac63816345c519
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104420760"
---
# <a name="svg-support"></a>Compatibilidad con SVG

A partir de la actualización de aniversario de Windows 10, Direct2D admite la representación de [fuentes de color](../directwrite/color-fonts.md) que contienen contornos de glifos SVG, como se describe en la [especificación OpenType](/typography/opentype/spec/) (vea [la tabla SVG](/typography/opentype/spec/svg)). A partir de Windows 10 Creators Update, Direct2D también admite la representación de imágenes SVG independientes. Sin embargo, algunas características de SVG no se permiten en las fuentes SVG de OpenType y las características de SVG no se admiten actualmente en Direct2D.  

En este tema se identifica el conjunto de características de [SVG 1,1](https://www.w3.org/TR/SVG11/) compatibles con Direct2D en la actualización de aniversario de Windows 10 y versiones más recientes. Este documento se aplica a SVG en fuentes OpenType, así como imágenes SVG independientes.

## <a name="supported-svg-elements-and-attributes"></a>Atributos y elementos SVG admitidos

Direct2D admite la representación de los siguientes elementos SVG y de los atributos asociados para cada elemento. Se omiten otros elementos y atributos normales.



| Elemento                                                                                  | Atributos regulares admitidos                                                             |
|------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| [círculo](https://www.w3.org/TR/SVG11/shapes.mdl#circleelement)                           | identificador, estilo, transformación, CX, CY, r                                                          |
| [clipPath](https://www.w3.org/TR/SVG11/masking.mdl#clippathelement)                      | identificador, estilo, transformación, clipPathUnits                                                      |
| [fichero](https://www.w3.org/TR/SVG11/struct.mdl#defselement)                               | identificador, estilo, transformación                                                                     |
| [multilínea](https://www.w3.org/TR/SVG11/struct.mdl#descriptionandtitleelements)<sup>\*</sup>  | id                                                                                       |
| [puntos](https://www.w3.org/TR/SVG11/shapes.mdl#ellipseelement)                         | ID, Style, Transform, CX, CY, RX, Ry                                                     |
| [g](https://www.w3.org/TR/SVG11/struct.mdl#gelement)                                     | identificador, estilo, transformación                                                                     |
| [image](https://www.w3.org/TR/SVG11/struct.mdl#imageelement)                             | identificador, estilo, transformación, x, y, ancho, alto, preserveAspectRatio, XLink: href               |
| [Ondula](https://www.w3.org/TR/SVG11/shapes.mdl#lineelement)                               | identificador, estilo, transformación, x1, Y1, x2, Y2                                                     |
| [linearGradient](https://www.w3.org/TR/SVG11/pservers.mdl#lineargradientelement)         | ID, Style, x1, Y1, x2, Y2, gradientUnits, gradientTransform, spreadMethod, XLink: href    |
| [path](https://www.w3.org/TR/SVG11/paths.mdl#pathelement)                                | identificador, estilo, transformación, d                                                                  |
| [Polígono](https://www.w3.org/TR/SVG11/shapes.mdl#polygonelement)                         | identificador, estilo, transformación, puntos                                                             |
| [Polyline](https://www.w3.org/TR/SVG11/shapes.mdl#polylineelement)                       | identificador, estilo, transformación, puntos                                                             |
| [radialGradient](https://www.w3.org/TR/SVG11/pservers.mdl#radialgradientelement)         | ID, Style, CX, CY, r, FX, AF, gradientUnits, gradientTransform, spreadMethod, XLink: href |
| [Rect](https://www.w3.org/TR/SVG11/shapes.mdl#rectelement)                               | identificador, estilo, transformación, x, y, ancho, alto, RX, Ry                                        |
| [stop](https://www.w3.org/TR/SVG11/pservers.mdl#stopelement)                             | identificador, estilo, desplazamiento                                                                        |
| [Import](https://www.w3.org/TR/SVG11/struct.mdl#svgelement)                                 | ID, Style, x, y, width, height, viewBox, preserveAspectRatio                             |
| [Titulo](https://www.w3.org/TR/SVG11/struct.mdl#descriptionandtitleelements)<sup>\*</sup> | id                                                                                       |
| [use](https://www.w3.org/TR/SVG11/struct.mdl#useelement)                                 | identificador, estilo, transformación, x, y, ancho, alto, XLink: href                                    |



 

<sup>\*</sup> Solo se admite en Windows 10 Creators Update y versiones más recientes

## <a name="supported-svg-presentation-attributes"></a>Atributos de presentación SVG admitidos

Direct2D también admite los siguientes atributos de presentación. Se pueden especificar en cualquier elemento SVG, pero solo afectan a la apariencia de determinados elementos, tal y como se describe en la especificación SVG (vea [atributos de presentación](https://www.w3.org/TR/SVG11/attindex.mdl#presentationattributes)).

-   clip-ruta de acceso
-   clip-regla
-   color
-   muestra<sup>\*</sup>
-   fill
-   relleno-opacidad
-   regla de relleno
-   opacidad
-   desbordamiento
-   color de detención
-   detener: opacidad
-   stroke
-   Stroke-dasharray
-   Stroke-dashoffset
-   Stroke-LineCap
-   Stroke-LineJoin
-   Stroke-miterLimit
-   trazo: opacidad
-   ancho de trazo
-   visibilidad<sup>\*</sup>

<sup>\*</sup> Solo se admite en Windows 10 Creators Update y versiones más recientes

## <a name="unsupported-svg-features"></a>Características de SVG no admitidas

### <a name="unsupported-elements-and-attributes"></a>Elementos y atributos no admitidos

Los elementos o atributos no incluidos en las listas anteriores se consideran no compatibles con Direct2D. Al analizar el contenido SVG que contiene un elemento o atributo no admitido, se omite la entidad no admitida. El resto del contenido se representa tan fielmente como sea posible.

### <a name="unsupported-length-units"></a>Unidades de longitud no admitidas

A partir de la actualización de aniversario de Windows 10, Direct2D solo admite valores de longitud de espacio de usuario y valores de longitud porcentual. No se admiten las longitudes con sufijos de unidad, como "mm" o "em".

A partir de Windows 10 Fall Creators Update, Direct2D también admite identificadores de unidad absoluta: PX, PT, PC, cm, mm y en. No se admiten los identificadores de unidad relativos (EM, ex).

### <a name="unsupported-image-sources"></a>Orígenes de imagen no admitidos

El elemento de imagen solo se admite si su atributo XLink: href está establecido en una imagen con codificación Base64. No se admiten referencias remotas.

 

 