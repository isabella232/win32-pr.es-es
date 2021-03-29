---
title: Representación de contenido
description: Representación de contenido
ms.assetid: 9a3baa33-dac4-4742-8f80-33b05caada09
keywords:
- SDK de Windows Media Format, representación de contenido
- Advanced Systems Format (ASF), representación de contenido
- ASF (formato de sistemas avanzados), representación de contenido
- Advanced Systems Format (ASF), representación de contenido
- ASF (formato de sistemas avanzados), representación de contenido
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d6a171ce9b404c4cc16862ffd64b53ada5821b0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903826"
---
# <a name="rendering-content"></a>Representación de contenido

El SDK de Windows Media Format no proporciona rutinas para representar el contenido entregado por el objeto lector. Si escribe aplicaciones para reproducir el contenido en archivos ASF, debe implementar sus propias rutinas de representación.

Debe tener cuidado al representar contenido para asegurarse de que los ejemplos se representan en el orden del tiempo de presentación y que los ejemplos de diferentes flujos se sincronizan cuando se representan. El método que se emplea para garantizar la sincronización de la secuencia dependerá de la técnica de representación que se utilice para la aplicación. En general, si tiene secuencias de audio y vídeo, debe sincronizar con la secuencia de audio, ya que la incoherencia en la secuencia de audio es más perceptible que algunos fotogramas descartados en una secuencia de vídeo.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Leer archivos ASF**](reading-asf-files.md)
</dt> <dt>

[**Para recuperar ejemplos de medios con el lector asincrónico**](to-retrieve-media-samples-with-the-asynchronous-reader.md)
</dt> <dt>

[**Para recuperar ejemplos de medios con el lector sincrónico**](to-retrieve-media-samples-with-the-synchronous-reader.md)
</dt> </dl>

 

 




