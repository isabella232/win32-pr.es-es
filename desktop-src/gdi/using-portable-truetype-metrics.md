---
description: Las aplicaciones que usan las métricas de texto TrueType pueden lograr un alto grado de portabilidad de impresoras y documentos; pueden utilizar métricas TrueType incluso si deben mantener la compatibilidad con las primeras versiones de 16 bits de Windows.
ms.assetid: 29b54315-7c4e-4b8c-ad79-0b85c7386860
title: Uso de métricas TrueType portátiles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83360b620bde11e20726b0ee4124d35bf6cf00b2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104997649"
---
# <a name="using-portable-truetype-metrics"></a>Uso de métricas TrueType portátiles

Las aplicaciones que usan las métricas de texto TrueType pueden lograr un alto grado de portabilidad de impresoras y documentos; pueden utilizar métricas TrueType incluso si deben mantener la compatibilidad con las primeras versiones de 16 bits de Windows.

Los anchos de diseño superan la mayoría de los problemas de texto dependiente del dispositivo introducidos por dispositivos físicos. Los anchos de diseño son un tipo de ancho lógico. Independientemente de cualquier problema de rasterización o transformaciones de escalado, cada glifo tiene un ancho y un alto lógicos. Compuesto en una página lógica, cada carácter de una cadena tiene un lugar independiente de los anchos de dispositivo físico. Aunque un ancho lógico implica que los anchos se pueden escalar linealmente en todos los tamaños de punto, esto no es necesariamente así para las fuentes no portable o la mayoría de las fuentes TrueType. En tamaños de punto más pequeños, algunos glifos se hacen más amplios en relación con su alto para mejorar la legibilidad.

Los caracteres de las fuentes TrueType Core están diseñados para una cuadrícula 2048 de 2048. El ancho del diseño es el ancho de un carácter en estas unidades de la cuadrícula. (TrueType admite cualquier tamaño de cuadrícula entero hasta 16.384 por 16.384; los tamaños de cuadrícula que son potencias enteras de 2 escalas más rápido que otros tamaños de cuadrícula).

El contorno de fuente está diseñado en unidades teóricas. El cuadrado em es la cuadrícula teórica en la que se ajusta el contorno de la fuente. (Puede usar el miembro **otmEMSquare** de [OUTLINETEXTMETRIC](/windows/desktop/api/Wingdi/ns-wingdi-outlinetextmetrica) y el miembro **ntmSizeEM** de [NEWTEXTMETRIC](/windows/win32/api/wingdi/ns-wingdi-newtextmetrica) para recuperar el tamaño del cuadrado EM en unidades teóricas). Cuando se crea una fuente que tiene un tamaño de punto (en unidades de dispositivo) igual al tamaño de su cuadrado em, los anchos ABC para esta fuente son los anchos de diseño deseados. Por ejemplo, supongamos que el tamaño de un cuadrado em es 1000 y el ancho ABC de un carácter de la fuente es 150, 400 y 150. Un carácter de esta fuente de 10 unidades de dispositivo alto tendría anchos ABC de 1,5, 4 y 1,5, respectivamente. Dado que el \_ modo de asignación de texto mm se usa normalmente con fuentes (y el \_ texto mm es equivalente a las unidades de dispositivo), se trata de un cálculo sencillo.

Debido a la alta resolución de los anchos de diseño de TrueType, las aplicaciones que los usan deben tener en cuenta los valores numéricos grandes que se pueden crear. Para obtener más información, vea los temas siguientes:

-   [Dispositivo frente a unidades de diseño](device-vs--design-units.md)
-   [Métricas para documentos portátiles](metrics-for-portable-documents.md)

 

 



