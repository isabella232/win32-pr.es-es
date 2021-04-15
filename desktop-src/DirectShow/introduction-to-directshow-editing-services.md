---
description: Introducción a los servicios de edición de DirectShow
ms.assetid: 247c4ba9-53c1-46ed-83ef-a454351920e3
title: Introducción a los servicios de edición de DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c75d9cf22eba81ebb9794310f63983b991bcf22
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104494963"
---
# <a name="introduction-to-directshow-editing-services"></a>Introducción a los servicios de edición de DirectShow

\[Esta API no se admite y puede modificarse o no estar disponible en el futuro.\]

El núcleo de DirectShow es una arquitectura eficaz para administrar los medios de streaming. Una aplicación puede utilizarla para reproducir contenido multimedia creado en una amplia variedad de formatos, sin que el desarrollador tenga que preocuparse por la compresión de archivos y otros detalles tediosos. Sin embargo, antes de los [servicios de edición de DirectShow](directshow-editing-services.md) (des), DirectShow carecía de la flexibilidad necesaria para la edición no lineal.

Por ejemplo, supongamos que desea crear una secuencia de vídeo compuesta por 4 segundos desde el origen A, seguido de 10 segundos del origen B y de que termina con 5 segundos a partir del código fuente C. Podría hacerlo con bastante facilidad con solo la API de DirectShow básica.

Pero, ¿qué ocurre si decidió que el origen C debe aparecer antes que el origen B, no después de; que la secuencia debe usar 8 segundos del origen A, no 4; y que todo el entorno de producción necesitaba una pista de audio independiente jugando en segundo plano. Incluso los cambios menores como estos podrían ser difíciles de implementar. Pero el escenario que se acaba de describir es un proyecto de edición trivial en DES: puede hacerlo con una serie de llamadas a métodos.

Estas son algunas de las características que DES aporta a DirectShow:

-   Modelo de escala de tiempo que organiza las pistas de audio y vídeo en capas anidadas, lo que facilita la manipulación de la producción final.
-   La capacidad de obtener una vista previa de un proyecto de vídeo sobre la marcha
-   Persistencia del proyecto a través de un formato basado en XML
-   Compatibilidad con efectos de audio y vídeo, así como transiciones entre pistas de vídeo (como transiciones y barridos)
-   Más de 100 barridos estándar, tal y como se define en la sociedad de los ingenieros de películas y TV (SMPTE)
-   Incrustación basada en matiz, luminancia, valor RGB o valor alfa
-   Conversión automática de velocidades de fotogramas y tasas de muestreo de audio, lo que permite a una producción usar orígenes heterogéneos
-   Cambiar el tamaño o recortar el vídeo

Limitaciones:

-   DES no es compatible con orígenes de vídeo MPEG-2 o H. 264.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Servicios de edición de DirectShow](directshow-editing-services.md)
</dt> </dl>

 

 



