---
title: Configuración de secuencias de vídeo para buscar rendimiento
description: Configuración de secuencias de vídeo para buscar rendimiento
ms.assetid: 2df507f9-60a5-4489-b3db-7fe15604e625
keywords:
- flujos, configurar secuencias de vídeo
- códecs, configurar secuencias de vídeo
- secuencias de vídeo, configurar
- secuencias de vídeo, rendimiento
- rendimiento, secuencias de vídeo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33b4fc68e0b3a91cf135d29dc7123d5af88db84c
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "103788716"
---
# <a name="configuring-video-streams-for-seeking-performance"></a>Configuración de secuencias de vídeo para buscar rendimiento

Algunas aplicaciones de reproducción realizan muchas búsquedas en flujos individuales. La búsqueda es un área en la que el rendimiento puede variar considerablemente en función de la configuración de la secuencia. Si sabe que el contenido debe optimizarse para una búsqueda rápida, puede adaptar la configuración del flujo para mejorar el rendimiento.

El mayor factor que afecta a la velocidad de las operaciones de búsqueda en vídeo es el espaciado de los fotogramas clave. Dado que cada fotograma entre fotogramas clave debe reconstruirse en función de los fotogramas anteriores, los fotogramas clave muy espaciados resultan en tiempos de búsqueda más largos. Por ejemplo, si una secuencia de vídeo con 30 fotogramas por segundo tiene un espaciado de fotogramas de clave máximo de 10 segundos, habrá fotogramas potencialmente 300 entre fotogramas clave. Si busca en el último [*fotograma Delta*](wmformat-glossary.md), se deben reconstruir 299 fotogramas para que el fotograma se descomprime. Si cada reconstrucción del fotograma tardó .01 segundo, la búsqueda tardaría casi 3 segundos. Si desea aumentar la eficacia de la búsqueda, puede ser útil reducir el espaciado de fotogramas clave. Sin embargo, si establece los fotogramas clave demasiado próximos, puede perder calidad.

Puede establecer el espaciado máximo de fotogramas clave mediante una llamada a [**IWMVideoMediaProps:: SetMaxKeyFrameSpacing**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmvideomediaprops-setmaxkeyframespacing). En la tabla siguiente se enumeran los valores recomendados, en función de la velocidad de bits de la secuencia. Estos valores proporcionan un buen equilibrio de búsqueda de rendimiento y calidad. El SDK no impone ningún límite en el tiempo entre fotogramas clave. En general, los tiempos de más de 30 segundos pueden afectar negativamente a los tiempos de búsqueda cuando el contenido se transmite por secuencias a través de una red y cuando se reproduce de forma local.



| Velocidad de bits             | Espaciado máximo sugerido de fotogramas clave |
|----------------------|-------------------------------------|
| 22 Kbps a 300 kbps  | 8 segundos                           |
| 300 kbps a 600 Kbps | 6 segundos                           |
| 600 Kbps a 2 Mbps   | 4 segundos                           |
| 2 Mbps y superior    | 3 segundos                           |



 

Para obtener más información sobre cómo obtener el mejor rendimiento al buscar archivos de vídeo, consulte [obtención del mejor rendimiento de búsqueda de vídeo](getting-the-best-video-seeking-performance.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Configuración de secuencias**](configuring-streams.md)
</dt> </dl>

 

 




