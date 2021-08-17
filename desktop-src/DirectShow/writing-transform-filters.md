---
description: Escribir filtros de transformación
ms.assetid: ce84756b-34ee-4710-8f0f-7553733ca10a
title: Escribir filtros de transformación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3fe8329809b6fe93ea33a9842f57733d7539a56e2ac21abfcf304d2ed780e6d2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117816842"
---
# <a name="writing-transform-filters"></a>Escribir filtros de transformación

En esta sección se describe cómo escribir un filtro de transformación, definido como un filtro que tiene exactamente un pin de entrada y un pin de salida. Para ilustrar los pasos, en esta sección se describe un filtro de transformación hipotético que genera vídeo codificado de longitud de ejecución (RLE). No describe el propio algoritmo de codificación RLE, solo las tareas específicas de DirectShow. (DirectShow ya proporciona un códec RLE a través del [filtro Deserción AVI).](avi-compressor-filter.md)

En esta sección se supone que usará la biblioteca de DirectShow base para crear filtros. Aunque puede escribir un filtro sin él, se recomienda encarecidamente la biblioteca de clases base.

> [!Note]  
> Antes de escribir un filtro de transformación, considere si un objeto multimedia directX (DMO) cumpliría sus requisitos. Las DDO pueden hacer muchas de las mismas cosas que los filtros, y el modelo de programación para DDO es más sencillo. Las DDO se hospedan en DirectShow a través del filtro [DMO wrapper,](dmo-wrapper-filter.md) pero también se pueden usar fuera de DirectShow. Las DDO son ahora la solución recomendada para codificadores y descodificadores.

 

Esta sección contiene los siguientes temas:

-   [Paso 1. Elegir una clase base](step-1--choose-a-base-class.md)
-   [Paso 2. Declarar la clase Filter](step-2--declare-the-filter-class.md)
-   [Paso 3. Compatibilidad con la negociación de tipos de medios](step-3--support-media-type-negotiation.md)
-   [Paso 4. Establecer propiedades del asignador](step-4--set-allocator-properties.md)
-   [Paso 5. Transformación de la imagen](step-5--transform-the-image.md)
-   [Paso 6. Agregar compatibilidad con COM](step-6--add-support-for-com.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Creación de DirectShow filtros](building-directshow-filters.md)
</dt> <dt>

[DirectShow Clases base](directshow-base-classes.md)
</dt> <dt>

[Escribir DirectShow filtros](writing-directshow-filters.md)
</dt> </dl>

 

 



