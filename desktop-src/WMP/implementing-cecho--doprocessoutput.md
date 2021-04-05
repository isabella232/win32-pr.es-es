---
title: Implementación de CEcho DoProcessOutput
description: Implementación de CEcho DoProcessOutput
ms.assetid: afd91022-4e2d-46a2-a0f4-cd2b558536d6
keywords:
- Complementos de Media Player de Windows, método echo de ejemplo DoProcessOutput
- complementos, método echo de ejemplo DoProcessOutput
- Complementos de procesamiento de señal digital, ejemplo echo método DoProcessOutput
- Complementos DSP, método echo de ejemplo DoProcessOutput
- Ejemplo de complemento DSP de eco, método DoProcessOutput
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ff40246a6a0ccda2b3f17b12924c44cb79fa4d9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104076356"
---
# <a name="implementing-cechodoprocessoutput"></a><span data-ttu-id="5c018-108">Implementación de CEcho::D oProcessOutput</span><span class="sxs-lookup"><span data-stu-id="5c018-108">Implementing CEcho::DoProcessOutput</span></span>

<span data-ttu-id="5c018-109">El método **DoProcessOutput** realiza el procesamiento de la señal digital.</span><span class="sxs-lookup"><span data-stu-id="5c018-109">The **DoProcessOutput** method performs the digital signal processing.</span></span> <span data-ttu-id="5c018-110">Este es el método que realiza los cambios en los datos proporcionados por Media Player de Windows.</span><span class="sxs-lookup"><span data-stu-id="5c018-110">This is the method that makes the changes to the data provided by Windows Media Player.</span></span> <span data-ttu-id="5c018-111">Los resultados de este método se escuchan como un efecto de eco cuando se completa el complemento de ejemplo echo.</span><span class="sxs-lookup"><span data-stu-id="5c018-111">It is the results of this method that you will hear as an echo effect when your Echo sample plug-in is complete.</span></span>

<span data-ttu-id="5c018-112">En este ejemplo, el complemento solo procesará audio de 8 o 16 bits.</span><span class="sxs-lookup"><span data-stu-id="5c018-112">For this sample, the plug-in will only process 8-bit or 16-bit audio.</span></span> <span data-ttu-id="5c018-113">Tendrá que realizar algunos cambios en el código de ejemplo del Asistente para complementos para quitar las secciones que procesan audio de mayor profundidad de bits.</span><span class="sxs-lookup"><span data-stu-id="5c018-113">You will need to make some changes to the plug-in wizard sample code to remove the sections that process higher bit depth audio.</span></span> <span data-ttu-id="5c018-114">Sin embargo, merece la pena estudiar estas secciones, ya que puede decidir agregar su propia implementación de Eco para esos formatos.</span><span class="sxs-lookup"><span data-stu-id="5c018-114">It is worthwhile to study these sections, however, because you may decide to add your own echo implementation for those formats.</span></span>

<span data-ttu-id="5c018-115">En las secciones siguientes se detallan los cambios que debe realizar en el código:</span><span class="sxs-lookup"><span data-stu-id="5c018-115">The following sections detail the changes you need to make to the code:</span></span>

-   [<span data-ttu-id="5c018-116">Quitar el código para procesar más de 16 bits</span><span class="sxs-lookup"><span data-stu-id="5c018-116">Removing the Code to Process Greater than 16 Bits</span></span>](removing-the-code-to-process-greater-than-16-bits.md)
-   [<span data-ttu-id="5c018-117">Procesamiento de los datos de audio</span><span class="sxs-lookup"><span data-stu-id="5c018-117">Processing the Audio Data</span></span>](processing-the-audio-data.md)
-   [<span data-ttu-id="5c018-118">Variables para realizar el procesamiento</span><span class="sxs-lookup"><span data-stu-id="5c018-118">Variables to Perform Processing</span></span>](variables-to-perform-processing.md)
-   [<span data-ttu-id="5c018-119">Crear el efecto de eco</span><span class="sxs-lookup"><span data-stu-id="5c018-119">Creating the Echo Effect</span></span>](creating-the-echo-effect.md)

## <a name="related-topics"></a><span data-ttu-id="5c018-120">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="5c018-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5c018-121">**El ejemplo echo**</span><span class="sxs-lookup"><span data-stu-id="5c018-121">**The Echo Sample**</span></span>](the-echo-sample.md)
</dt> </dl>

 

 




