---
description: Introducción a DirectShow Editing Services
ms.assetid: 247c4ba9-53c1-46ed-83ef-a454351920e3
title: Introducción a DirectShow Editing Services
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d12470b45e0b39c32c983176f07444a5136b9e97b99cc5be142974d05178f58
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118952554"
---
# <a name="introduction-to-directshow-editing-services"></a>Introducción a DirectShow Editing Services

\[Esta API no se admite y puede modificarse o no estar disponible en el futuro.\]

El núcleo de DirectShow es una arquitectura eficaz para controlar los medios de streaming. Una aplicación puede usarla para reproducir contenido multimedia escrito en una amplia variedad de formatos, sin que el desarrollador tenga que preocuparse por la compresión de archivos y otros detalles tediosos. Antes de [DirectShow Editing Services](directshow-editing-services.md) (DES), sin embargo, DirectShow faltaba la flexibilidad necesaria para la edición no lineal.

Por ejemplo, supongamos que quiere crear una secuencia de vídeo que consta de 4 segundos del origen A, seguido de 10 segundos del origen B y que termina en 5 segundos desde el origen C. Esto se puede lograr con bastante facilidad con solo la API de DirectShow principal.

Pero ¿qué ocurre si decide que el origen C debe ir antes que el origen B, no después; que la secuencia debe usar 8 segundos desde el origen A, no 4; ¿Y que toda la producción necesitaba una pista de audio independiente reproduciendo en segundo plano? Incluso los cambios menores, como estos, podrían ser difíciles de implementar. Pero el escenario que se acaba de describir es un proyecto de edición trivial en DES: puede hacerlo con una serie de llamadas a métodos.

Estas son algunas de las características que DES aporta a DirectShow:

-   Un modelo de escala de tiempo que organiza las pistas de audio y vídeo en capas anidadas, lo que facilita la manipulación de la producción final.
-   La capacidad de obtener una vista previa de un proyecto de vídeo sobre la marcha
-   Project persistencia a través de un formato basado en XML
-   Compatibilidad con efectos de audio y vídeo, así como transiciones entre pistas de vídeo (como atenuaciones y borrados)
-   Más de 100 borrados estándar, tal como se define en la Society of Motion Picture and Tv Engineers (SMPTE)
-   Clave basada en matiz, luminosidad, valor RGB o valor alfa
-   Conversión automática de velocidades de fotogramas y frecuencias de muestreo de audio, lo que permite que una producción use orígenes heterogéneos
-   Redimensionamiento o recorte de vídeo

Limitaciones:

-   DES no admite orígenes de vídeo MPEG-2 o H.264.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[DirectShow Servicios de edición](directshow-editing-services.md)
</dt> </dl>

 

 



