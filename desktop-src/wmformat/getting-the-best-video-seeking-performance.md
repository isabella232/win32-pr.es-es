---
title: Obtener el mejor rendimiento de búsqueda de vídeo
description: Obtener el mejor rendimiento de búsqueda de vídeo
ms.assetid: 21269f0c-fc3a-46fc-88b4-f71828b5d5a7
keywords:
- Windows SDK de formato multimedia, mejor rendimiento de búsqueda de vídeo
- Formato de sistemas avanzados (ASF), mejor rendimiento de búsqueda de vídeo
- ASF (formato de sistemas avanzados), mejor rendimiento de búsqueda de vídeo
- Formato de sistemas avanzados (ASF), vídeo que busca rendimiento
- ASF (formato de sistemas avanzados), vídeo que busca el rendimiento
- Formato de sistemas avanzados (ASF), rendimiento
- ASF (formato de sistemas avanzados), rendimiento
- búsqueda de vídeo
- rendimiento, búsqueda de vídeo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c95feb9158bbab09ce28024100f3ebbffb56ad9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127359572"
---
# <a name="getting-the-best-video-seeking-performance"></a>Obtener el mejor rendimiento de búsqueda de vídeo

La búsqueda de contenido en un archivo es una operación muy común que puede ser un problema de rendimiento. El vídeo codificado con el códec Windows Media Video 9 se basa principalmente en fotogramas delta, que solo registran los cambios en relación con el fotograma anterior. La reconstrucción de fotogramas delta lleva tiempo, especialmente si los fotogramas clave están separados. Para obtener más información sobre cómo configurar fotogramas clave para búsquedas eficaces, vea [Configuring Video Secuencias for Seeking Performance](configuring-video-streams-for-seeking-performance.md).

Además de la configuración adecuada, puede mejorar el rendimiento de búsqueda mediante el uso de la indexación de fotogramas para la secuencia de vídeo. Buscar un número de fotograma suele ser más rápido que buscar un tiempo de presentación.

Si busca en un archivo con varias secuencias, debe seleccionar solo las secuencias necesarias. Cada secuencia configurada para lectura afectará al rendimiento de las búsquedas, ya que todas las secuencias seleccionadas se sincronizan cuando se busca un punto en un archivo.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Lectura de archivos ASF**](reading-asf-files.md)
</dt> <dt>

[**Para buscar por número de fotograma mediante el lector asincrónico**](to-seek-by-frame-number-using-the-asynchronous-reader.md)
</dt> <dt>

[**Para buscar por número de fotograma mediante el lector sincrónico**](to-seek-by-frame-number-using-the-synchronous-reader.md)
</dt> <dt>

[**Para buscar por tiempo mediante el lector asincrónico**](to-seek-by-time-using-the-asynchronous-reader.md)
</dt> <dt>

[**Para buscar por tiempo mediante el lector sincrónico**](to-seek-by-time-using-the-synchronous-reader.md)
</dt> </dl>

 

 




