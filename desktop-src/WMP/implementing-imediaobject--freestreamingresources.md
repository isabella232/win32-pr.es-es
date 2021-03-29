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
# <a name="implementing-imediaobjectfreestreamingresources"></a><span data-ttu-id="6fd4f-109">Implementación de IMediaObject:: FreeStreamingResources</span><span class="sxs-lookup"><span data-stu-id="6fd4f-109">Implementing IMediaObject::FreeStreamingResources</span></span>

<span data-ttu-id="6fd4f-110">Es importante que el código libere cualquier memoria asignada antes de que se destruya el objeto de complemento.</span><span class="sxs-lookup"><span data-stu-id="6fd4f-110">It is important that your code releases any allocated memory before the plug-in object is destroyed.</span></span> <span data-ttu-id="6fd4f-111">Windows Media Player llama a **FreeStreamingResources** para que pueda hacerlo.</span><span class="sxs-lookup"><span data-stu-id="6fd4f-111">Windows Media Player calls **FreeStreamingResources** to allow you to do this.</span></span> <span data-ttu-id="6fd4f-112">Por motivos de seguridad, el ejemplo creado por el Asistente para complementos incluye una llamada a **FreeStreamingResources** en el método **FinalRelease** para asegurarse de que se libera la memoria.</span><span class="sxs-lookup"><span data-stu-id="6fd4f-112">For safety, the sample created by the plug-in wizard includes a call to **FreeStreamingResources** in the **FinalRelease** method to ensure that the memory is freed.</span></span> <span data-ttu-id="6fd4f-113">Debe agregar el código siguiente a **FreeStreamingResources** para el ejemplo echo:</span><span class="sxs-lookup"><span data-stu-id="6fd4f-113">You must add the following code to **FreeStreamingResources** for the Echo sample:</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="6fd4f-114">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="6fd4f-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6fd4f-115">**Trabajar con recursos de streaming**</span><span class="sxs-lookup"><span data-stu-id="6fd4f-115">**Working with Streaming Resources**</span></span>](working-with-streaming-resources.md)
</dt> </dl>

 

 




