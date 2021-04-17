---
title: Trabajar con recursos de streaming
description: Trabajar con recursos de streaming
ms.assetid: 0258ad24-f1b9-4cb3-921c-068072fd2dbb
keywords:
- Complementos de Windows Media Player, echo ejemplo de recursos de streaming
- complementos, echo ejemplo de recursos de streaming
- Complementos de procesamiento de señal digital, echo ejemplo de recursos de streaming
- Complementos DSP, echo ejemplo de recursos de streaming
- Ejemplo de complemento DSP de eco, recursos de streaming
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a1df8cc221f3d75c8333b3ffd41a144d28bed7a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105704793"
---
# <a name="working-with-streaming-resources"></a>Trabajar con recursos de streaming

El proyecto de complemento DSP de audio de ejemplo generado por el Asistente para complementos de Windows Media Player no requiere que el complemento asigne recursos de streaming. Sin embargo, el ejemplo echo requiere un búfer independiente para almacenar los datos de audio durante un período de tiempo para crear el efecto de retraso. El búfer se administra mediante dos métodos: **IMediaObject:: AllocateStreamingResources**, que crea el búfer y **IMediaObject:: FreeStreamingResources**, que libera el búfer. Los métodos de **IMediaObject** se implementan en echo. cpp.

En las secciones siguientes se proporciona más información acerca de la administración de los búferes:

-   [Variables para administrar el búfer de retraso](variables-to-manage-the-delay-buffer.md)
-   [Implementación de IMediaObject:: AllocateStreamingResources](implementing-imediaobject--allocatestreamingresources.md)
-   [Implementación de IMediaObject:: FreeStreamingResources](implementing-imediaobject--freestreamingresources.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**El ejemplo echo**](the-echo-sample.md)
</dt> </dl>

 

 




