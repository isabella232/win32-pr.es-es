---
title: Escribir secuencias de velocidad de bits variable
description: Escribir secuencias de velocidad de bits variable
ms.assetid: 9eccde59-8342-44ad-90e6-032db022d7c5
keywords:
- Advanced Systems Format (ASF), escribir secuencias VBR
- ASF (formato de sistemas avanzados), escritura de secuencias VBR
- velocidad de bits variable (VBR), escribir secuencias
- VBR (velocidad de bits variable), escribir secuencias
- secuencias, escribir VBR
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6981cbae04085c4bf4f771d9dd29e30752427cdc
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "103788685"
---
# <a name="writing-variable-bit-rate-streams"></a><span data-ttu-id="e0a68-108">Escribir secuencias de velocidad de bits variable</span><span class="sxs-lookup"><span data-stu-id="e0a68-108">Writing Variable Bit Rate Streams</span></span>

<span data-ttu-id="e0a68-109">Las secuencias de velocidad de bits variable (VBR) se escriben de la misma forma que las secuencias de velocidad de bits constante (CBR).</span><span class="sxs-lookup"><span data-stu-id="e0a68-109">Variable bit rate (VBR) streams are written the same way as constant bit rate (CBR) streams.</span></span> <span data-ttu-id="e0a68-110">La única diferencia es el procesamiento que realiza internamente el escritor y los códecs.</span><span class="sxs-lookup"><span data-stu-id="e0a68-110">The only difference is in the processing performed internally by the writer and the codecs.</span></span> <span data-ttu-id="e0a68-111">Sin embargo, la VBR basada en la velocidad de bits (tanto restringida como sin restricciones) requiere un paso de preprocesamiento en el escritor.</span><span class="sxs-lookup"><span data-stu-id="e0a68-111">However, bit rate based VBR (both constrained and unconstrained) requires a preprocessing pass in the writer.</span></span>

<span data-ttu-id="e0a68-112">Debe comprobar el valor devuelto por la primera llamada que realice a [**IWMWriter:: WriteSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-writesample) para cada secuencia.</span><span class="sxs-lookup"><span data-stu-id="e0a68-112">You should check the return value for the first call you make to [**IWMWriter::WriteSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-writesample) for each stream.</span></span> <span data-ttu-id="e0a68-113">Si el código de error devuelto es NS \_ E \_ no válidos \_ \_ , la secuencia requiere un paso de preprocesamiento.</span><span class="sxs-lookup"><span data-stu-id="e0a68-113">If the error code returned is NS\_E\_INVALID\_NUM\_PASSES, the stream requires a preprocessing pass.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e0a68-114">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e0a68-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e0a68-115">**Uso de la codificación de Two-Pass**</span><span class="sxs-lookup"><span data-stu-id="e0a68-115">**Using Two-Pass Encoding**</span></span>](using-two-pass-encoding.md)
</dt> <dt>

[<span data-ttu-id="e0a68-116">**Escribir archivos ASF**</span><span class="sxs-lookup"><span data-stu-id="e0a68-116">**Writing ASF Files**</span></span>](writing-asf-files.md)
</dt> </dl>

 

 




