---
title: Configuración de vídeo Secuencias para buscar rendimiento
description: Configuración de vídeo Secuencias para buscar rendimiento
ms.assetid: 2df507f9-60a5-4489-b3db-7fe15604e625
keywords:
- streams,configuring video streams
- códecs, configuración de secuencias de vídeo
- secuencias de vídeo, configurar
- secuencias de vídeo, rendimiento
- rendimiento, secuencias de vídeo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33b4fc68e0b3a91cf135d29dc7123d5af88db84c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127251511"
---
# <a name="configuring-video-streams-for-seeking-performance"></a>Configuración de vídeo Secuencias para buscar rendimiento

Algunas aplicaciones de reproducción realizan muchas búsquedas en secuencias individuales. La búsqueda es un área en la que el rendimiento puede variar considerablemente en función de la configuración de la secuencia. Si sabe que el contenido debe optimizarse para búsquedas rápidas, puede adaptar la configuración de la secuencia para mejorar el rendimiento.

El factor más importante que afecta a la velocidad de búsqueda de operaciones en vídeo es el espaciado de los fotogramas clave. Dado que cada fotograma entre fotogramas clave debe reconstruirse en función de los fotogramas anteriores, los fotogramas clave ampliamente espaciados tienen como resultado tiempos de búsqueda más largos. Por ejemplo, si una secuencia de vídeo con 30 fotogramas por segundo tiene un espaciado máximo entre fotogramas clave de 10 segundos, puede haber 300 fotogramas entre fotogramas clave. Si busca el último marco [*delta,*](wmformat-glossary.md)se deben reconstruir 299 fotogramas para que se descomprima. Si cada reconstrucción de fotogramas tardara 0,01 segundos, la búsqueda tardaría casi 3 segundos. Si desea aumentar la eficacia de la búsqueda, reducir el espaciado entre fotogramas clave puede ayudar. Sin embargo, si establece los fotogramas clave demasiado cerca, puede perder calidad.

Puede establecer el espaciado máximo entre fotogramas clave llamando a [**IWMVideoMediaProps::SetMaxKeyFrameSpacing.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmvideomediaprops-setmaxkeyframespacing) Los valores recomendados, en función de la velocidad de bits de la secuencia, se enumeran en la tabla siguiente. Estos valores proporcionan un buen equilibrio entre el rendimiento y la calidad de la búsqueda. El SDK no aplica ningún límite en el tiempo entre fotogramas clave. En general, los tiempos de más de 30 segundos pueden afectar negativamente a los tiempos de búsqueda tanto cuando el contenido se transmite a través de una red como cuando se reproduce localmente.



| Velocidad de bits             | Espaciado máximo de fotogramas clave sugerido |
|----------------------|-------------------------------------|
| De 22 Kbps a 300 Kbps  | 8 segundos                           |
| De 300 Kbps a 600 Kbps | 6 segundos                           |
| De 600 Kbps a 2 Mbps   | 4 segundos                           |
| 2 Mbps y superiores    | 3 segundos                           |



 

Para obtener más información sobre cómo obtener el mejor rendimiento al buscar archivos de vídeo, vea [Obtener el mejor rendimiento de búsqueda de vídeo.](getting-the-best-video-seeking-performance.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Configuración de Secuencias**](configuring-streams.md)
</dt> </dl>

 

 




