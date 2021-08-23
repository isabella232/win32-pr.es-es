---
description: Elija una clase base como parte de la escritura de un filtro de transformación. Obtenga información sobre qué clases son adecuadas para los filtros de transformación.
ms.assetid: 4b2d3add-0430-480b-ad5f-bb1aa19fef21
title: Paso 1. Elegir una clase base
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c140beba3df02ace21d99779c152a79632fe0b4a1a916c4412c467b0f4ac5627
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119315885"
---
# <a name="step-1-choose-a-base-class"></a>Paso 1. Elegir una clase base

Este es el paso 1 del tutorial Escribir [filtros de transformación](writing-transform-filters.md).

Suponiendo que decide escribir un filtro y no un DMO, el primer paso es elegir qué clase base usar. Las siguientes clases son adecuadas para los filtros de transformación:

-   [**CTransformFilter está**](ctransformfilter.md) diseñado para transformar filtros que usan búferes de entrada y salida independientes. Este tipo de filtro a veces se denomina filtro copy-transform. Cuando un filtro de transformación de copia recibe un ejemplo de entrada, escribe datos nuevos en un ejemplo de salida y entrega el ejemplo de salida al filtro siguiente.
-   [**CTransInPlaceFilter está**](ctransinplacefilter.md) diseñado para filtros que modifican datos en el búfer original, también denominados filtros trans-in-place. Cuando un filtro trans-in-place recibe una muestra, cambia los datos dentro de esa muestra y entrega el mismo ejemplo de bajada. El pin de entrada y el pin de salida del filtro siempre se conectan con los tipos de medios correspondientes.
-   [**CVideoTransformFilter está**](cvideotransformfilter.md) diseñado principalmente para descodificadores de vídeo. Se deriva de **CTransformFilter, pero** incluye funcionalidad para quitar fotogramas si el representador de bajada se queda atrás.
-   [**CBaseFilter es**](cbasefilter.md) una clase de filtro genérica. Todas las demás clases de esta lista derivan de **CBaseFilter.** Si ninguno de ellos es adecuado, puede volver a usar esta clase. Sin embargo, esta clase también requiere el máximo trabajo por su parte.
-   \[! Importante\]  
    > Las transformaciones de vídeo locales pueden tener un impacto grave en el rendimiento de la representación. Las transformaciones locales requieren operaciones de lectura,modificación y escritura en el búfer. Si la memoria reside en una tarjeta gráfica, las operaciones de lectura son significativamente más lentas. Además, incluso una transformación de copia puede provocar operaciones de lectura no deseadas si no se implementa cuidadosamente. Por lo tanto, siempre debe realizar pruebas de rendimiento si escribe una transformación de vídeo.

     

Para el codificador RLE de ejemplo, la mejor opción es **CTransformFilter** o **CVideoTransformFilter.** De hecho, las diferencias entre ellas son en gran medida internas, por lo que es fácil convertir de una a otra. Dado que los tipos de medios deben ser diferentes en los dos pines, la **clase CTransInPlaceFilter** no es adecuada para este filtro. En este ejemplo se **usará CTransformFilter.**

Siguiente: [Paso 2. Declare la clase Filter](step-2--declare-the-filter-class.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Escribir DirectShow filtros](writing-directshow-filters.md)
</dt> </dl>

 

 



