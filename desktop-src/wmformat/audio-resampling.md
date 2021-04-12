---
title: Remuestreo de audio
description: Remuestreo de audio
ms.assetid: ec6ad6b2-1d35-4ac4-9a1e-3fc9c053000c
keywords:
- SDK de Windows Media Format, remuestreo de audio
- SDK de Windows Media Format, volver a muestrear audio
- Advanced Systems Format (ASF), remuestreo de audio
- ASF (formato de sistemas avanzados), remuestreo de audio
- Advanced Systems Format (ASF), volver a muestrear audio
- ASF (formato de sistemas avanzados), volver a muestrear audio
- remuestreo de audio
- volver a muestrear audio, acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 608272a7e531d7380991a705d391e6226a6758d1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357076"
---
# <a name="audio-resampling"></a><span data-ttu-id="1432e-111">Remuestreo de audio</span><span class="sxs-lookup"><span data-stu-id="1432e-111">Audio Resampling</span></span>

<span data-ttu-id="1432e-112">Cada formato comprimido de un códec de audio tiene una frecuencia de muestreo y un tamaño de muestra concretos.</span><span class="sxs-lookup"><span data-stu-id="1432e-112">Every compressed format of an audio codec has a specific sample rate and sample size.</span></span> <span data-ttu-id="1432e-113">No es necesario que coincidan con la configuración del formato de entrada o de salida.</span><span class="sxs-lookup"><span data-stu-id="1432e-113">These do not need to match the settings of the input format or output format.</span></span> <span data-ttu-id="1432e-114">Si un formato de entrada tiene una configuración diferente a la del formato comprimido descrito en el perfil, el escritor volverá a muestrear el audio, durante el proceso de codificación, para que coincida con el formato comprimido.</span><span class="sxs-lookup"><span data-stu-id="1432e-114">If an input format has different settings than the compressed format described in the profile, the writer will resample the audio, during the encoding process, to match the compressed format.</span></span> <span data-ttu-id="1432e-115">El escritor solo acepta determinados formatos como entrada.</span><span class="sxs-lookup"><span data-stu-id="1432e-115">Only certain formats are accepted by the writer as input.</span></span> <span data-ttu-id="1432e-116">Al enumerar los formatos de entrada de una secuencia de audio comprimida, se pueden volver a muestrear todos los formatos recuperados para que coincidan con el formato del perfil.</span><span class="sxs-lookup"><span data-stu-id="1432e-116">When you enumerate the input formats for a compressed audio stream, all of the formats retrieved can be resampled to match the format in the profile.</span></span>

<span data-ttu-id="1432e-117">Al leer audio comprimido, el lector volverá a muestrear el contenido para que coincida con el formato de salida.</span><span class="sxs-lookup"><span data-stu-id="1432e-117">When reading compressed audio, the reader will resample the content to match the output format.</span></span> <span data-ttu-id="1432e-118">Debe usar uno de los formatos de salida enumerados por el lector, por lo que se garantiza que el audio se puede volver a muestrear en la configuración del formato de salida.</span><span class="sxs-lookup"><span data-stu-id="1432e-118">You must use one of the output formats enumerated by the reader, so you are guaranteed that the audio can be resampled to the output format settings.</span></span>

<span data-ttu-id="1432e-119">Cada remuestreo puede afectar a la calidad del audio.</span><span class="sxs-lookup"><span data-stu-id="1432e-119">Each resampling potentially affects the quality of the audio.</span></span> <span data-ttu-id="1432e-120">Cuando sea posible, debe usar los formatos de entrada y salida con valores que coincidan con el formato comprimido.</span><span class="sxs-lookup"><span data-stu-id="1432e-120">When possible, you should use input and output formats with settings that match the compressed format.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1432e-121">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="1432e-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1432e-122">**Características de escritura de archivos**</span><span class="sxs-lookup"><span data-stu-id="1432e-122">**File Writing Features**</span></span>](file-writing-features.md)
</dt> <dt>

[<span data-ttu-id="1432e-123">**Trabajar con entradas**</span><span class="sxs-lookup"><span data-stu-id="1432e-123">**Working with Inputs**</span></span>](working-with-inputs.md)
</dt> <dt>

[<span data-ttu-id="1432e-124">**Trabajar con salidas**</span><span class="sxs-lookup"><span data-stu-id="1432e-124">**Working with Outputs**</span></span>](working-with-outputs.md)
</dt> </dl>

 

 




