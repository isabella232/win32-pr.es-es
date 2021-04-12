---
title: Convertir datos de un formato a otro
description: Convertir datos de un formato a otro
ms.assetid: df995b7d-ac45-4964-a1b0-efd079c0c010
keywords:
- Administrador de compresión de audio (ACM), convertir datos
- ACM (Administrador de compresión de audio), convertir datos
- Ejemplos de ACM, convertir datos
- convertir datos
- acmStreamOpen función)
- acmStreamSize función)
- acmStreamPrepareHeader función)
- acmStreamConvert función)
- acmStreamUnprepareHeader función)
- acmStreamClose función)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9645342aa9f19b2c31de77dc9d1031122ed0b2ac
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357042"
---
# <a name="converting-data-from-one-format-to-another"></a><span data-ttu-id="0922c-113">Convertir datos de un formato a otro</span><span class="sxs-lookup"><span data-stu-id="0922c-113">Converting Data from One Format to Another</span></span>

<span data-ttu-id="0922c-114">ACM usa funciones de secuencia para admitir la conversión de formato de datos.</span><span class="sxs-lookup"><span data-stu-id="0922c-114">The ACM uses stream functions to support data format conversion.</span></span> <span data-ttu-id="0922c-115">Los convertidores en ACM cambian el formato, pero no el tipo de datos.</span><span class="sxs-lookup"><span data-stu-id="0922c-115">Converters in the ACM change the format, but not the data type.</span></span> <span data-ttu-id="0922c-116">Por ejemplo, un módulo de convertidor puede cambiar los datos de 44 kHz de 16 bits 44 a los datos de 8 bits y de 8 kHz.</span><span class="sxs-lookup"><span data-stu-id="0922c-116">For example, a converter module can change 44-kHz, 16-bit data to 44-kHz, 8-bit data.</span></span>

<span data-ttu-id="0922c-117">Las siguientes funciones ACM admiten la conversión de formato de datos.</span><span class="sxs-lookup"><span data-stu-id="0922c-117">The following ACM functions support data format conversion.</span></span> <span data-ttu-id="0922c-118">Aparecen en el orden en el que normalmente los usaría.</span><span class="sxs-lookup"><span data-stu-id="0922c-118">They are listed in the order in which you would typically use them.</span></span>

-   <span data-ttu-id="0922c-119">La función [**acmStreamOpen**](/windows/desktop/api/Msacm/nf-msacm-acmstreamopen) abre un flujo de conversión.</span><span class="sxs-lookup"><span data-stu-id="0922c-119">The [**acmStreamOpen**](/windows/desktop/api/Msacm/nf-msacm-acmstreamopen) function opens a conversion stream.</span></span>
-   <span data-ttu-id="0922c-120">La función [**acmStreamSize**](/windows/desktop/api/Msacm/nf-msacm-acmstreamsize) calcula el tamaño adecuado del búfer de origen o de destino.</span><span class="sxs-lookup"><span data-stu-id="0922c-120">The [**acmStreamSize**](/windows/desktop/api/Msacm/nf-msacm-acmstreamsize) function calculates the appropriate size of the source or destination buffer.</span></span>
-   <span data-ttu-id="0922c-121">La función [**acmStreamPrepareHeader**](/windows/desktop/api/Msacm/nf-msacm-acmstreamprepareheader) prepara los búferes de origen y de destino que se van a usar en una conversión.</span><span class="sxs-lookup"><span data-stu-id="0922c-121">The [**acmStreamPrepareHeader**](/windows/desktop/api/Msacm/nf-msacm-acmstreamprepareheader) function prepares source and destination buffers to be used in a conversion.</span></span>
-   <span data-ttu-id="0922c-122">La función [**acmStreamConvert**](/windows/desktop/api/Msacm/nf-msacm-acmstreamconvert) convierte los datos de un búfer de origen en el formato de destino, escribiendo los datos convertidos en el búfer de destino.</span><span class="sxs-lookup"><span data-stu-id="0922c-122">The [**acmStreamConvert**](/windows/desktop/api/Msacm/nf-msacm-acmstreamconvert) function converts data in a source buffer into the destination format, writing the converted data into the destination buffer.</span></span>
-   <span data-ttu-id="0922c-123">La función [**acmStreamUnprepareHeader**](/windows/desktop/api/Msacm/nf-msacm-acmstreamunprepareheader) limpia los búferes de origen y de destino preparados por **acmStreamPrepareHeader**.</span><span class="sxs-lookup"><span data-stu-id="0922c-123">The [**acmStreamUnprepareHeader**](/windows/desktop/api/Msacm/nf-msacm-acmstreamunprepareheader) function cleans up the source and destination buffers prepared by **acmStreamPrepareHeader**.</span></span> <span data-ttu-id="0922c-124">Debe llamar a esta función antes de liberar los búferes de origen y de destino.</span><span class="sxs-lookup"><span data-stu-id="0922c-124">You must call this function before freeing the source and destination buffers.</span></span>
-   <span data-ttu-id="0922c-125">La función [**acmStreamClose**](/windows/desktop/api/Msacm/nf-msacm-acmstreamclose) cierra una secuencia de conversión.</span><span class="sxs-lookup"><span data-stu-id="0922c-125">The [**acmStreamClose**](/windows/desktop/api/Msacm/nf-msacm-acmstreamclose) function closes a conversion stream.</span></span>

<span data-ttu-id="0922c-126">Al convertir datos, identifique primero el formato de origen y, a continuación, elija el formato de destino.</span><span class="sxs-lookup"><span data-stu-id="0922c-126">When converting data, first identify the source format, then choose the destination format.</span></span> <span data-ttu-id="0922c-127">La forma más fácil de hacerlo es mediante la función [**acmFormatChoose**](/windows/desktop/api/Msacm/nf-msacm-acmformatchoose) , que muestra un cuadro de diálogo de selección de formato y devuelve la opción de formato del usuario.</span><span class="sxs-lookup"><span data-stu-id="0922c-127">The easiest way to do this is by using the [**acmFormatChoose**](/windows/desktop/api/Msacm/nf-msacm-acmformatchoose) function, which displays a format-selection dialog box and returns the user's format choice.</span></span>

<span data-ttu-id="0922c-128">Cuando conozca los formatos de origen y de destino, puede usar [**acmStreamOpen**](/windows/desktop/api/Msacm/nf-msacm-acmstreamopen) para abrir una secuencia de conversión.</span><span class="sxs-lookup"><span data-stu-id="0922c-128">When you know the source and destination formats, you can use [**acmStreamOpen**](/windows/desktop/api/Msacm/nf-msacm-acmstreamopen) to open a conversion stream.</span></span> <span data-ttu-id="0922c-129">A continuación, puede usar la función [**acmStreamSize**](/windows/desktop/api/Msacm/nf-msacm-acmstreamsize) para determinar los tamaños de búfer adecuados.</span><span class="sxs-lookup"><span data-stu-id="0922c-129">Then you can use the [**acmStreamSize**](/windows/desktop/api/Msacm/nf-msacm-acmstreamsize) function to determine the appropriate buffer sizes.</span></span>

<span data-ttu-id="0922c-130">El siguiente paso es preparar los búferes que se van a usar en la conversión mediante [**acmStreamPrepareHeader**](/windows/desktop/api/Msacm/nf-msacm-acmstreamprepareheader).</span><span class="sxs-lookup"><span data-stu-id="0922c-130">The next step is to prepare the buffers to be used in the conversion by using [**acmStreamPrepareHeader**](/windows/desktop/api/Msacm/nf-msacm-acmstreamprepareheader).</span></span>

<span data-ttu-id="0922c-131">Para realizar la conversión, use [**acmStreamConvert**](/windows/desktop/api/Msacm/nf-msacm-acmstreamconvert) hasta que se hayan procesado todos los búferes.</span><span class="sxs-lookup"><span data-stu-id="0922c-131">To perform the conversion, use [**acmStreamConvert**](/windows/desktop/api/Msacm/nf-msacm-acmstreamconvert) until all the buffers have been processed.</span></span> <span data-ttu-id="0922c-132">Una vez finalizada la conversión, use [**acmStreamUnprepareHeader**](/windows/desktop/api/Msacm/nf-msacm-acmstreamunprepareheader) para limpiar los búferes y, a continuación, use [**acmStreamClose**](/windows/desktop/api/Msacm/nf-msacm-acmstreamclose) para cerrar la secuencia de conversión.</span><span class="sxs-lookup"><span data-stu-id="0922c-132">When the conversion is complete, use [**acmStreamUnprepareHeader**](/windows/desktop/api/Msacm/nf-msacm-acmstreamunprepareheader) to clean up the buffers and then use [**acmStreamClose**](/windows/desktop/api/Msacm/nf-msacm-acmstreamclose) to close the conversion stream.</span></span>

 

 




