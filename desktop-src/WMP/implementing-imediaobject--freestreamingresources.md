---
title: Implementación de IMediaObject FreeStreamingResources
description: Implementación de IMediaObject FreeStreamingResources
ms.assetid: 970dd10b-a7a0-4ba0-97e3-725d5c914500
keywords:
- Reproductor de Windows Media complementos, recursos de streaming de ejemplo de eco
- complementos, recursos de streaming de ejemplo de eco
- complementos de procesamiento de señales digitales, recursos de streaming de ejemplo de eco
- Complementos de DSP, recursos de streaming de ejemplo de eco
- Ejemplo de complemento DSP de eco, recursos de streaming
- Ejemplo de complemento DSP de eco, liberación de memoria
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30da5f92ec8420ccc90f74256003aae02664a57a8ffad3470901f672cf37aa73
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119617325"
---
# <a name="implementing-imediaobjectfreestreamingresources"></a>Implementación de IMediaObject::FreeStreamingResources

Es importante que el código libere cualquier memoria asignada antes de que se destruya el objeto de complemento. Reproductor de Windows Media a **FreeStreamingResources** para permitirle hacerlo. Por motivos de seguridad, el ejemplo creado por el asistente para complementos incluye una llamada a **FreeStreamingResources** en el método **FinalRelease** para asegurarse de que se libera la memoria. Debe agregar el código siguiente a **FreeStreamingResources para** el ejemplo de eco:


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

 

 




