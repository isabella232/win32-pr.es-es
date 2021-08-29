---
description: Las aplicaciones que usan las métricas de texto TrueType pueden lograr un alto grado de portabilidad de impresoras y documentos. pueden usar métricas TrueType incluso si deben mantener la compatibilidad con las primeras versiones de 16 bits de Windows.
ms.assetid: 29b54315-7c4e-4b8c-ad79-0b85c7386860
title: Uso de métricas trueType portátiles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9fb56eaa3111dad8592b1e1f6edbab2a64ced6e2a6c9b6e1a94baf8a5acc7120
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119849005"
---
# <a name="using-portable-truetype-metrics"></a>Uso de métricas trueType portátiles

Las aplicaciones que usan las métricas de texto TrueType pueden lograr un alto grado de portabilidad de impresoras y documentos. pueden usar métricas TrueType incluso si deben mantener la compatibilidad con las primeras versiones de 16 bits de Windows.

Los anchos de diseño superan la mayoría de los problemas de texto dependiente del dispositivo introducidos por los dispositivos físicos. Los anchos de diseño son un tipo de ancho lógico. Independientemente de los problemas de rasterización o las transformaciones de escalado, cada glifo tiene un ancho y alto lógicos. Compuesto por una página lógica, cada carácter de una cadena tiene un lugar que es independiente de los anchos del dispositivo físico. Aunque un ancho lógico implica que los anchos se pueden escalar linealmente en todos los tamaños de punto, esto no es necesariamente cierto para las fuentes TrueType o noportables. En tamaños de punto más pequeños, algunos glifos se hacen más anchos en relación con su altura para mejorar la legibilidad.

Los caracteres de las fuentes principales TrueType están diseñados en una cuadrícula de 2048 a 2048. El ancho de diseño es el ancho de un carácter en estas unidades de cuadrícula. (TrueType admite cualquier tamaño de cuadrícula de enteros de hasta 16 384 por 16 384; tamaños de cuadrícula que son potencias enteras de 2 escalas más rápidas que otros tamaños de cuadrícula).

El contorno de fuente está diseñado en unidades nocionales. El cuadrado em es la cuadrícula notional en la que se ha ajustado el contorno de fuente. (Puede usar el miembro **otmEMSquare** de [OUTLINETEXTMETRIC](/windows/desktop/api/Wingdi/ns-wingdi-outlinetextmetrica) y el miembro **ntmSizeEM** de [NEWTEXTMETRIC](/windows/win32/api/wingdi/ns-wingdi-newtextmetrica) para recuperar el tamaño del cuadrado em en unidades notionales). Cuando se crea una fuente que tiene un tamaño de punto (en unidades de dispositivo) igual al tamaño de su cuadrado em, los anchos abc de esta fuente son los anchos de diseño deseados. Por ejemplo, suponga que el tamaño de un cuadrado em es 1000 y los anchos ABC de un carácter en la fuente son 150, 400 y 150. Un carácter de esta fuente con una altura de 10 unidades de dispositivo tendría anchos ABC de 1,5, 4 y 1,5, respectivamente. Dado que el modo de asignación MM TEXT se usa normalmente con fuentes (y MM TEXT es equivalente a unidades de dispositivo), se trata \_ de un cálculo \_ sencillo.

Debido a la alta resolución de los anchos de diseño trueType, las aplicaciones que los usan deben tener en cuenta los valores numéricos grandes que se pueden crear. Para obtener más información, vea los temas siguientes:

-   [Dispositivo frente a unidades de diseño](device-vs--design-units.md)
-   [Métricas para documentos portátiles](metrics-for-portable-documents.md)

 

 



