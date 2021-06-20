---
description: Elija una clase base como parte de la escritura de un filtro de transformación. Obtenga información sobre qué clases son adecuadas para los filtros de transformación.
ms.assetid: 4b2d3add-0430-480b-ad5f-bb1aa19fef21
title: Paso 1. Elegir una clase base
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1a2bbf704bb2247034bc2ba3a6f35812f46aaaa
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406468"
---
# <a name="step-1-choose-a-base-class"></a>Paso 1. Elegir una clase base

Este es el paso 1 del tutorial Escribir [filtros de transformación](writing-transform-filters.md).

Suponiendo que decide escribir un filtro y no un DMO, el primer paso es elegir qué clase base usar. Las clases siguientes son adecuadas para los filtros de transformación:

-   [**CTransformFilter está**](ctransformfilter.md) diseñado para filtros de transformación que usan búferes de entrada y salida independientes. Este tipo de filtro a veces se denomina filtro de copia y transformación. Cuando un filtro de copia y transformación recibe un ejemplo de entrada, escribe nuevos datos en un ejemplo de salida y entrega el ejemplo de salida al filtro siguiente.
-   [**CTransInPlaceFilter está**](ctransinplacefilter.md) diseñado para filtros que modifican datos en el búfer original, también denominados filtros trans-in-place. Cuando un filtro trans-in-place recibe una muestra, cambia los datos dentro de esa muestra y entrega la misma muestra de bajada. El pin de entrada y el pin de salida del filtro siempre se conectan con los tipos de medios correspondientes.
-   [**CVideoTransformFilter está**](cvideotransformfilter.md) diseñado principalmente para descodificadores de vídeo. Deriva de **CTransformFilter,** pero incluye funcionalidad para quitar fotogramas si el representador de bajada se queda atrás.
-   [**CBaseFilter es**](cbasefilter.md) una clase de filtro genérica. Todas las demás clases de esta lista se derivan **de CBaseFilter.** Si ninguno de ellos es adecuado, puede volver a usar esta clase. Sin embargo, esta clase también requiere el mayor trabajo por su parte.
-   \[! Importante\]  
    > Las transformaciones de vídeo en su lugar pueden tener un impacto grave en el rendimiento de la representación. Las transformaciones locales requieren operaciones de lectura, modificación y escritura en el búfer. Si la memoria reside en una tarjeta gráfica, las operaciones de lectura son significativamente más lentas. Además, incluso una transformación de copia puede provocar operaciones de lectura no deseadas si no la implementa cuidadosamente. Por lo tanto, siempre debe realizar pruebas de rendimiento si escribe una transformación de vídeo.

     

Para el codificador RLE de ejemplo, la mejor opción es **CTransformFilter** o **CVideoTransformFilter.** De hecho, las diferencias entre ellas son en gran medida internas, por lo que es fácil convertir de una a otra. Dado que los tipos de medios deben ser diferentes en los dos pines, la **clase CTransInPlaceFilter** no es adecuada para este filtro. En este ejemplo se **usará CTransformFilter**.

Siguiente: [Paso 2. Declare la clase Filter](step-2--declare-the-filter-class.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Escribir filtros de DirectShow](writing-directshow-filters.md)
</dt> </dl>

 

 



