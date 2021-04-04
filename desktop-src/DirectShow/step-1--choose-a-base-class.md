---
description: Paso 1.
ms.assetid: 4b2d3add-0430-480b-ad5f-bb1aa19fef21
title: Paso 1. Elegir una clase base
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4679873e78e75b350335b5294db63579fd41f36
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911094"
---
# <a name="step-1-choose-a-base-class"></a>Paso 1. Elegir una clase base

Este es el paso 1 del tutorial de [escritura de filtros de transformación](writing-transform-filters.md).

Suponiendo que decida escribir un filtro y no un DMO, el primer paso es elegir la clase base que se va a usar. Las siguientes clases son adecuadas para los filtros de transformación:

-   [**CTransformFilter**](ctransformfilter.md) está diseñado para filtros de transformación que utilizan búferes de entrada y salida independientes. Este tipo de filtro a veces se denomina filtro de copiar y transformar. Cuando un filtro de copia y transformación recibe un ejemplo de entrada, escribe datos nuevos en un ejemplo de salida y entrega el ejemplo de salida al siguiente filtro.
-   [**CTransInPlaceFilter**](ctransinplacefilter.md) está diseñado para los filtros que modifican los datos en el búfer original, también denominados filtros de transacciones en contexto. Cuando un filtro de transferencia en contexto recibe un ejemplo, cambia los datos dentro de ese ejemplo y entrega el mismo ejemplo de nivel inferior. El PIN de entrada y la salida del filtro siempre se conectan con tipos de medios coincidentes.
-   [**CVideoTransformFilter**](cvideotransformfilter.md) está diseñado principalmente para descodificadores de vídeo. Se deriva de **CTransformFilter**, pero incluye funcionalidad para quitar fotogramas si el representador de nivel inferior cae por detrás.
-   [**CBaseFilter**](cbasefilter.md) es una clase de filtro genérico. Todas las demás clases de esta lista se derivan de **CBaseFilter**. Si ninguno de ellos es adecuado, puede revertir a esta clase. Sin embargo, esta clase también requiere el mayor trabajo de su parte.
-   \[! Aún\]  
    > Las transformaciones de vídeo en contexto pueden tener un impacto serio en el rendimiento de la representación. Las transformaciones en contexto requieren operaciones de lectura-modificación-escritura en el búfer. Si la memoria reside en una tarjeta gráfica, las operaciones de lectura son significativamente más lentas. Además, incluso una transformación de copia puede producir operaciones de lectura imprevistas si no se implementa con cuidado. Por lo tanto, siempre debe realizar pruebas de rendimiento si escribe una transformación de vídeo.

     

Para el codificador RLE de ejemplo, la mejor opción es **CTransformFilter** o **CVideoTransformFilter**. De hecho, las diferencias entre ellos son principalmente internas, por lo que es fácil convertir de uno a otro. Dado que los tipos de medios deben ser diferentes en los dos PIN, la clase **CTransInPlaceFilter** no es adecuada para este filtro. En este ejemplo se usará **CTransformFilter**.

Siguiente: [paso 2. Declare la clase de filtro](step-2--declare-the-filter-class.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Escribir filtros de DirectShow](writing-directshow-filters.md)
</dt> </dl>

 

 



