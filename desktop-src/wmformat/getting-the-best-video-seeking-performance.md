---
title: Obtención del mejor rendimiento de búsqueda de vídeo
description: Obtención del mejor rendimiento de búsqueda de vídeo
ms.assetid: 21269f0c-fc3a-46fc-88b4-f71828b5d5a7
keywords:
- Windows Media Format SDK, mejor rendimiento de búsqueda de vídeo
- Advanced Systems Format (ASF), mejor rendimiento de búsqueda de vídeo
- ASF (formato de sistemas avanzados), mejor rendimiento de búsqueda de vídeo
- Advanced Systems Format (ASF), vídeo que busca rendimiento
- ASF (formato de sistemas avanzados), rendimiento de búsqueda de vídeo
- Advanced Systems Format (ASF), performance
- ASF (formato de sistemas avanzados), rendimiento
- búsqueda en vídeo
- rendimiento, búsqueda de vídeo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c95feb9158bbab09ce28024100f3ebbffb56ad9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105695382"
---
# <a name="getting-the-best-video-seeking-performance"></a>Obtención del mejor rendimiento de búsqueda de vídeo

La búsqueda de contenido en un archivo es una operación muy común que puede suponer un problema de rendimiento. El vídeo codificado con el códec de Windows Media Video 9 se compone principalmente de fotogramas Delta, que solo registran los cambios en relación con el fotograma anterior. Reconstruir fotogramas Delta lleva tiempo, especialmente si los fotogramas clave están alejados. Para obtener más información sobre cómo configurar fotogramas clave para una búsqueda eficaz, consulte [configuración de secuencias de vídeo para buscar el rendimiento](configuring-video-streams-for-seeking-performance.md).

Además de la configuración adecuada, puede mejorar el rendimiento de búsqueda mediante la indexación de fotogramas para la secuencia de vídeo. La búsqueda de un número de marco suele ser más rápida que la búsqueda en el momento de la presentación.

Si busca en un archivo con varias secuencias, debe seleccionar solo los flujos que sean necesarios. Cada flujo configurado para lectura afectará al rendimiento de la búsqueda, ya que todas las secuencias seleccionadas se sincronizan cuando se busca un punto en un archivo.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Leer archivos ASF**](reading-asf-files.md)
</dt> <dt>

[**Para buscar por número de marco mediante el lector asincrónico**](to-seek-by-frame-number-using-the-asynchronous-reader.md)
</dt> <dt>

[**Para buscar por número de marco mediante el lector sincrónico**](to-seek-by-frame-number-using-the-synchronous-reader.md)
</dt> <dt>

[**Para buscar por tiempo mediante el lector asincrónico**](to-seek-by-time-using-the-asynchronous-reader.md)
</dt> <dt>

[**Para buscar por tiempo mediante el lector sincrónico**](to-seek-by-time-using-the-synchronous-reader.md)
</dt> </dl>

 

 




