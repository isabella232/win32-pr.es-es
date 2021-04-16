---
title: Asistente para complementos de DSP
description: Asistente para complementos de DSP
ms.assetid: 3d1ae5ef-12c4-4db3-815a-2adc73353f20
keywords:
- Complementos de Windows Media Player, Asistente para complementos
- complementos, Asistente para complementos
- Complementos de procesamiento de señal digital, Asistente para complementos
- Complementos DSP, Asistente para complementos
- Asistente para complementos
- Visual Studio, Asistente para complementos de DSP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e9a7228056d821d2c2bca258f5c236fe1dce11d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104532079"
---
# <a name="dsp-plug-in-wizard"></a><span data-ttu-id="789c3-109">Asistente para complementos de DSP</span><span class="sxs-lookup"><span data-stu-id="789c3-109">DSP Plug-in Wizard</span></span>

<span data-ttu-id="789c3-110">El SDK de Windows Media Player proporciona un asistente para complementos que puede Agregar a Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="789c3-110">The Windows Media Player SDK provides a plug-in wizard that you can add to Visual Studio.</span></span> <span data-ttu-id="789c3-111">El asistente puede generar código de ejemplo para una variedad de complementos, incluidos los siguientes tipos de complementos de DSP:</span><span class="sxs-lookup"><span data-stu-id="789c3-111">The wizard can generate sample code for a variety of plug-ins, including the following types of DSP plug-ins:</span></span>

-   <span data-ttu-id="789c3-112">Complemento DSP de audio</span><span class="sxs-lookup"><span data-stu-id="789c3-112">Audio DSP plug-in</span></span>
-   <span data-ttu-id="789c3-113">Complemento DSP de audio (modo dual)</span><span class="sxs-lookup"><span data-stu-id="789c3-113">Audio DSP plug-in (dual mode)</span></span>
-   <span data-ttu-id="789c3-114">Complemento DSP de vídeo</span><span class="sxs-lookup"><span data-stu-id="789c3-114">Video DSP plug-in</span></span>
-   <span data-ttu-id="789c3-115">Complemento DSP de vídeo (modo dual)</span><span class="sxs-lookup"><span data-stu-id="789c3-115">Video DSP plug-in (dual mode)</span></span>

<span data-ttu-id="789c3-116">Cada uno de los dos complementos de ejemplo básicos, DSP de audio y vídeo DSP, funciona como un objeto multimedia de DirectX (DMO).</span><span class="sxs-lookup"><span data-stu-id="789c3-116">Each of the two basic sample plug-ins, Audio DSP and Video DSP, functions as a DirectX Media Object (DMO).</span></span> <span data-ttu-id="789c3-117">Es decir, cada complemento de ejemplo implementa la interfaz **IMediaObject** .</span><span class="sxs-lookup"><span data-stu-id="789c3-117">That is, each sample plug-in implements the **IMediaObject** interface.</span></span> <span data-ttu-id="789c3-118">Cada uno de los dos complementos de ejemplo de doble modo puede funcionar como DMO o como una transformación de Media Foundation (MFT).</span><span class="sxs-lookup"><span data-stu-id="789c3-118">Each of the two dual-mode sample plug-ins can function either as a DMO or as a Media Foundation Transform (MFT).</span></span> <span data-ttu-id="789c3-119">Es decir, cada complemento de ejemplo de dos modos implementa la interfaz **IMediaObject** y la interfaz **IMFTransform** .</span><span class="sxs-lookup"><span data-stu-id="789c3-119">That is, each dual-mode sample plug-in implements both the **IMediaObject** interface and the **IMFTransform** interface.</span></span>

<span data-ttu-id="789c3-120">Puede compilar, vincular, registrar y probar el código del complemento de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="789c3-120">You can compile, link, register, and test the sample plug-in code.</span></span> <span data-ttu-id="789c3-121">Después, puede modificar el código de ejemplo generado para crear su propio complemento DSP.</span><span class="sxs-lookup"><span data-stu-id="789c3-121">Then you can modify the generated sample code to create your own DSP plug-in.</span></span>

## <a name="related-topics"></a><span data-ttu-id="789c3-122">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="789c3-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="789c3-123">**Crear un complemento DSP**</span><span class="sxs-lookup"><span data-stu-id="789c3-123">**Building a DSP Plug-in**</span></span>](building-a-dsp-plug-in.md)
</dt> <dt>

[<span data-ttu-id="789c3-124">**Introducción al desarrollador de complementos de DSP**</span><span class="sxs-lookup"><span data-stu-id="789c3-124">**DSP Plug-in Developer Overview**</span></span>](dsp-plug-in-developer-overview.md)
</dt> <dt>

[<span data-ttu-id="789c3-125">**Actualizaciones del Asistente para complementos de DSP para Windows Media Player 11**</span><span class="sxs-lookup"><span data-stu-id="789c3-125">**Updates to the DSP Plug-in Wizard for Windows Media Player 11**</span></span>](updates-to-the-dsp-plug-in-wizard-for-windows-media-player-11.md)
</dt> </dl>

 

 




