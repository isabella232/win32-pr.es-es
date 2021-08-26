---
title: Contenido de representación
description: Contenido de representación
ms.assetid: 9a3baa33-dac4-4742-8f80-33b05caada09
keywords:
- Windows SDK de formato multimedia, contenido de representación
- Formato de sistemas avanzados (ASF), contenido de representación
- ASF (formato de sistemas avanzados), contenido de representación
- Formato de sistemas avanzados (ASF), representación de contenido
- ASF (formato de sistemas avanzados), representación de contenido
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7add8d31f1fd025327325256e56c9f38faa4c97fd7e2aa206cedfebcc84c1302
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119929665"
---
# <a name="rendering-content"></a>Contenido de representación

El SDK Windows Media Format no proporciona ninguna rutina para representar el contenido entregado por el objeto de lector. Si escribe aplicaciones para reproducir el contenido en archivos ASF, debe implementar sus propias rutinas de representación.

Debe tener cuidado al representar contenido para asegurarse de que las muestras se representan en orden de tiempo de presentación y que las muestras de diferentes secuencias se sincronizan al representarse. El método que emplea para asegurarse de que la sincronización de flujos dependerá de la técnica de representación que use para la aplicación. En general, si tiene secuencias de audio y vídeo, debe sincronizarse con la secuencia de audio, ya que la incoherencia en la secuencia de audio es más evidente que algunos fotogramas descartados en una secuencia de vídeo.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Lectura de archivos ASF**](reading-asf-files.md)
</dt> <dt>

[**Para recuperar ejemplos de medios con el lector asincrónico**](to-retrieve-media-samples-with-the-asynchronous-reader.md)
</dt> <dt>

[**Para recuperar ejemplos de medios con el lector sincrónico**](to-retrieve-media-samples-with-the-synchronous-reader.md)
</dt> </dl>

 

 




