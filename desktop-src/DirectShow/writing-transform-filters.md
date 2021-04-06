---
description: Escribir filtros de transformación
ms.assetid: ce84756b-34ee-4710-8f0f-7553733ca10a
title: Escribir filtros de transformación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3d007181e437ef5691f532fec00923aa2b8012f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002151"
---
# <a name="writing-transform-filters"></a>Escribir filtros de transformación

En esta sección se describe cómo escribir un filtro de transformación, definido como un filtro que tiene exactamente un PIN de entrada y un PIN de salida. Para ilustrar los pasos, en esta sección se describe un filtro de transformación hipotético que genera el vídeo de la longitud de ejecución codificada (RLE). No describe el algoritmo de codificación RLE en sí, solo las tareas específicas de DirectShow. (DirectShow ya proporciona un códec RLE a través del filtro del [compresor AVI](avi-compressor-filter.md) ).

En esta sección se da por supuesto que utilizará la biblioteca de clases base de DirectShow para crear filtros. Aunque puede escribir un filtro sin él, se recomienda encarecidamente la biblioteca de clases base.

> [!Note]  
> Antes de escribir un filtro de transformación, tenga en cuenta si un objeto multimedia de DirectX (DMO) cumplirá sus requisitos. DMOs puede hacer muchas de las mismas cosas que los filtros, y el modelo de programación para DMOs es más sencillo. Los DMOs se hospedan en DirectShow mediante el filtro de [contenedor de DMO](dmo-wrapper-filter.md) , pero también se pueden usar fuera de DirectShow. DMOs es ahora la solución recomendada para codificadores y descodificadores.

 

Esta sección contiene los siguientes temas:

-   [Paso 1. Elegir una clase base](step-1--choose-a-base-class.md)
-   [Paso 2. Declarar la clase de filtro](step-2--declare-the-filter-class.md)
-   [Paso 3. Compatibilidad con la negociación de tipos de medios](step-3--support-media-type-negotiation.md)
-   [Paso 4. Establecer propiedades de asignador](step-4--set-allocator-properties.md)
-   [Paso 5. Transformar la imagen](step-5--transform-the-image.md)
-   [Paso 6. Agregar compatibilidad con COM](step-6--add-support-for-com.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Compilar filtros de DirectShow](building-directshow-filters.md)
</dt> <dt>

[Clases base de DirectShow](directshow-base-classes.md)
</dt> <dt>

[Escribir filtros de DirectShow](writing-directshow-filters.md)
</dt> </dl>

 

 



