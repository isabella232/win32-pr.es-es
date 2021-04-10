---
title: Variables para administrar el búfer de retraso
description: Variables para administrar el búfer de retraso
ms.assetid: 2c5963a1-04e2-4421-8f56-14c1e059de4e
keywords:
- Complementos de Windows Media Player, echo ejemplo de recursos de streaming
- complementos, echo ejemplo de recursos de streaming
- Complementos de procesamiento de señal digital, echo ejemplo de recursos de streaming
- Complementos DSP, echo ejemplo de recursos de streaming
- Ejemplo de complemento DSP de eco, recursos de streaming
- Ejemplo de complemento DSP de eco, búfer de retraso
- búfer de retraso
- búferes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09d7f9657d16d0805ff2fc85d2238635fbfa6e5e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104268941"
---
# <a name="variables-to-manage-the-delay-buffer"></a><span data-ttu-id="365c7-111">Variables para administrar el búfer de retraso</span><span class="sxs-lookup"><span data-stu-id="365c7-111">Variables to Manage the Delay Buffer</span></span>

<span data-ttu-id="365c7-112">Debe agregar las declaraciones de las variables de miembro que necesita para administrar el búfer de retraso.</span><span class="sxs-lookup"><span data-stu-id="365c7-112">You must add the declarations for the member variables you need to manage the delay buffer.</span></span> <span data-ttu-id="365c7-113">Agregue las declaraciones siguientes a ECHO. h en la sección "privada":</span><span class="sxs-lookup"><span data-stu-id="365c7-113">Add the following declarations to Echo.h in the "private" section:</span></span>


```C++
DWORD  m_cbDelayBuffer;   // Count of bytes in delay buffer size.
BYTE*  m_pbDelayPointer;  // Movable pointer to delay buffer.
BYTE*  m_pbDelayBuffer;   // Pointer to the head of the delay buffer.

```



<span data-ttu-id="365c7-114">Agregue el código siguiente al constructor CEcho para inicializar las variables de búfer de retraso:</span><span class="sxs-lookup"><span data-stu-id="365c7-114">Add the following code to the CEcho constructor to initialize the delay buffer variables:</span></span>


```C++
m_pbDelayBuffer = NULL;
m_pbDelayPointer = NULL;
m_cbDelayBuffer = 0;

```



## <a name="related-topics"></a><span data-ttu-id="365c7-115">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="365c7-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="365c7-116">**Trabajar con recursos de streaming**</span><span class="sxs-lookup"><span data-stu-id="365c7-116">**Working with Streaming Resources**</span></span>](working-with-streaming-resources.md)
</dt> </dl>

 

 




