---
title: Quitar el código para procesar más de 16 bits
description: Quitar el código para procesar más de 16 bits
ms.assetid: 90c165e1-bc77-42a5-878d-056762c62991
keywords:
- Complementos de Media Player de Windows, método echo de ejemplo DoProcessOutput
- complementos, método echo de ejemplo DoProcessOutput
- Complementos de procesamiento de señal digital, ejemplo echo método DoProcessOutput
- Complementos DSP, método echo de ejemplo DoProcessOutput
- Ejemplo de complemento DSP de eco, método DoProcessOutput
- Ejemplo de complemento DSP de eco, procesamiento de más de 16 bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec33332ee332d0ca7b615844ba8ad5cd7b00eb2f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903493"
---
# <a name="removing-the-code-to-process-greater-than-16-bits"></a><span data-ttu-id="6b286-109">Quitar el código para procesar más de 16 bits</span><span class="sxs-lookup"><span data-stu-id="6b286-109">Removing the Code to Process Greater than 16 Bits</span></span>

<span data-ttu-id="6b286-110">Dado que este ejemplo solo procesa audio de 8 o 16 bits, debe modificar el código en **CEcho:: ValidateMediaType** para que devuelva el \_ tipo DMO \_ E \_ no \_ aceptado para tipos de medios mayores de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="6b286-110">Because this sample only processes 8-bit or 16-bit audio, you need to modify the code in **CEcho::ValidateMediaType** to return DMO\_E\_TYPE\_NOT\_ACCEPTED for media types greater than 16 bits.</span></span> <span data-ttu-id="6b286-111">Para ello, debe cambiar el código en el bloque switch que comprueba los formatos de tipo WAVE \_ format \_ extensible.</span><span class="sxs-lookup"><span data-stu-id="6b286-111">To accomplish this, you must change the code in the switch block that tests formats of type WAVE\_FORMAT\_EXTENSIBLE.</span></span> <span data-ttu-id="6b286-112">Reemplace el código del asistente por el siguiente código de ejemplo:</span><span class="sxs-lookup"><span data-stu-id="6b286-112">Replace the wizard code with the following example code:</span></span>


```C++
case WAVE_FORMAT_EXTENSIBLE:
    {
         // Sample size is greater than 16-bit or is multichannel.
        WAVEFORMATEXTENSIBLE *pWaveXT = (WAVEFORMATEXTENSIBLE *) pWave;

        if (KSDATAFORMAT_SUBTYPE_PCM != pWaveXT->SubFormat)
        {
            return DMO_E_TYPE_NOT_ACCEPTED;
        }
    }
    break;

```



<span data-ttu-id="6b286-113">A continuación, elimine o comente las secciones de código de **DoProcessOutput** que controlan el audio de alta resolución de bits.</span><span class="sxs-lookup"><span data-stu-id="6b286-113">Next, delete or comment out the sections of code in **DoProcessOutput** that handle high bit resolution audio.</span></span> <span data-ttu-id="6b286-114">Estas son las secciones que comienzan con el caso 24 y el caso 32.</span><span class="sxs-lookup"><span data-stu-id="6b286-114">These are the sections that begin with case 24 and case 32.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6b286-115">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="6b286-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6b286-116">**Implementación de CEcho::D oProcessOutput**</span><span class="sxs-lookup"><span data-stu-id="6b286-116">**Implementing CEcho::DoProcessOutput**</span></span>](implementing-cecho--doprocessoutput.md)
</dt> </dl>

 

 




