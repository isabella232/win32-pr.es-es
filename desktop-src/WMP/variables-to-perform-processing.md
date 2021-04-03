---
title: Variables para realizar el procesamiento
description: Variables para realizar el procesamiento
ms.assetid: 02f194ea-cac0-410f-886f-2894dd6971c8
keywords:
- Complementos de Media Player de Windows, método echo de ejemplo DoProcessOutput
- complementos, método echo de ejemplo DoProcessOutput
- Complementos de procesamiento de señal digital, ejemplo echo método DoProcessOutput
- Complementos DSP, método echo de ejemplo DoProcessOutput
- Ejemplo de complemento DSP de eco, método DoProcessOutput
- Ejemplo de complemento de DSP de eco, variables de procesamiento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e44f044aee6d893fba97cf921360444ec43db871
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103776644"
---
# <a name="variables-to-perform-processing"></a><span data-ttu-id="85ce2-109">Variables para realizar el procesamiento</span><span class="sxs-lookup"><span data-stu-id="85ce2-109">Variables to Perform Processing</span></span>

<span data-ttu-id="85ce2-110">Las variables miembro para controlar el búfer de retraso tratan las cantidades de **bytes** . son punteros de **bytes** y un entero que almacena un recuento de bytes.</span><span class="sxs-lookup"><span data-stu-id="85ce2-110">The member variables for handling the delay buffer deal with **BYTE** quantities; they are **BYTE** pointers and an integer that stores a count of bytes.</span></span> <span data-ttu-id="85ce2-111">Esto es idóneo para procesar audio de 8 bits, ya que una muestra de 8 bits se ajusta perfectamente a un byte de memoria.</span><span class="sxs-lookup"><span data-stu-id="85ce2-111">This is ideal for processing 8-bit audio, since an 8-bit sample fits nicely into one byte of memory.</span></span> <span data-ttu-id="85ce2-112">Sin embargo, cuando se procesa audio de 16 bits, es más conveniente convertirlos en punteros **cortos** , por lo que el procesamiento puede producirse en dos bytes a la vez.</span><span class="sxs-lookup"><span data-stu-id="85ce2-112">When processing 16-bit audio, though, it is more convenient to convert these to **short** pointers, so the processing can occur two bytes at a time.</span></span>

<span data-ttu-id="85ce2-113">En el siguiente código de ejemplo se asignan los nuevos punteros de 16 bits y se agrega una variable de puntero que almacena la dirección del final del búfer de retraso.</span><span class="sxs-lookup"><span data-stu-id="85ce2-113">The following example code allocates the new 16-bit pointers, and adds a pointer variable that stores the address of the end of the delay buffer.</span></span> <span data-ttu-id="85ce2-114">Insértelo en la sección "Case 16" justo antes del punto de entrada del bucle:</span><span class="sxs-lookup"><span data-stu-id="85ce2-114">Insert it in the "case 16" section just before the loop entry point:</span></span>


```C++
// Store local pointers to the delay buffer.
short    *pwDelayPointer = (short *)m_pbDelayPointer;
short    *pwDelayBuffer = (short *) m_pbDelayBuffer;
// Store the address of the last word of the delay buffer.
short    *pwEOFDelayBuffer = (short *)(m_pbDelayBuffer + m_cbDelayBuffer - sizeof(short)); 

```



<span data-ttu-id="85ce2-115">El código para el procesamiento de 8 bits también asigna una variable que almacena la dirección del final del búfer de retraso.</span><span class="sxs-lookup"><span data-stu-id="85ce2-115">The code for 8-bit processing also allocates a variable that stores the address of the end of the delay buffer.</span></span> <span data-ttu-id="85ce2-116">El almacenamiento de este valor facilita la prueba de si el puntero de búfer de retraso móvil ha alcanzado el final del búfer de retraso.</span><span class="sxs-lookup"><span data-stu-id="85ce2-116">Storing this value makes it easy to test whether the movable delay buffer pointer has reached the end of the delay buffer.</span></span> <span data-ttu-id="85ce2-117">En el código de ejemplo siguiente se calcula el valor:</span><span class="sxs-lookup"><span data-stu-id="85ce2-117">The following example code calculates the value:</span></span>


```C++
// Store the address of the end of the delay buffer.
BYTE * pbEOFDelayBuffer = (m_pbDelayBuffer + m_cbDelayBuffer - sizeof(BYTE));

```



## <a name="related-topics"></a><span data-ttu-id="85ce2-118">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="85ce2-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="85ce2-119">**Implementación de CEcho::D oProcessOutput**</span><span class="sxs-lookup"><span data-stu-id="85ce2-119">**Implementing CEcho::DoProcessOutput**</span></span>](implementing-cecho--doprocessoutput.md)
</dt> </dl>

 

 




