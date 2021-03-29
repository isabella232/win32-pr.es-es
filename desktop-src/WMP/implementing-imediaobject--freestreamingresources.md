---
title: Implementación de IMediaObject FreeStreamingResources
description: Implementación de IMediaObject FreeStreamingResources
ms.assetid: 970dd10b-a7a0-4ba0-97e3-725d5c914500
keywords:
- Complementos de Windows Media Player, echo ejemplo de recursos de streaming
- complementos, echo ejemplo de recursos de streaming
- Complementos de procesamiento de señal digital, echo ejemplo de recursos de streaming
- Complementos DSP, echo ejemplo de recursos de streaming
- Ejemplo de complemento DSP de eco, recursos de streaming
- Ejemplo de complemento de DSP de eco, liberar memoria
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a31a293cfc68caf43496d031426de2441c9c1d05
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903303"
---
# <a name="implementing-imediaobjectfreestreamingresources"></a>Implementación de IMediaObject:: FreeStreamingResources

Es importante que el código libere cualquier memoria asignada antes de que se destruya el objeto de complemento. Windows Media Player llama a **FreeStreamingResources** para que pueda hacerlo. Por motivos de seguridad, el ejemplo creado por el Asistente para complementos incluye una llamada a **FreeStreamingResources** en el método **FinalRelease** para asegurarse de que se libera la memoria. Debe agregar el código siguiente a **FreeStreamingResources** para el ejemplo echo:


```
// Test whether a buffer exists.
if (m_pbDelayBuffer)
{
    delete m_pbDelayBuffer;
    m_pbDelayBuffer = NULL;
    m_pbDelayPointer = NULL;
    m_cbDelayBuffer = 0;
}
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Trabajar con recursos de streaming**](working-with-streaming-resources.md)
</dt> </dl>

 

 




