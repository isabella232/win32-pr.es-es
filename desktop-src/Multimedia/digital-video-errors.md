---
title: Errores de Digital-Video
description: Errores de Digital-Video
ms.assetid: 177436fc-543f-4692-8281-1555c1fa21b0
keywords:
- Valores devueltos de MCIERR, errores de vídeo digital
- referencia multimedia, errores de vídeo digital
- referencia de errores de vídeo digital y multimedia
- Media control Interface (MCI), errores de vídeo digital
- MCI (media control Interface), errores de vídeo digital
- referencia de los errores de MCI y vídeo digital
- Referencia de MCI, errores de vídeo digital
- Media control Interface (MCI), errores
- MCI (interfaz de control multimedia), errores
- referencia de MCI, errores
- Referencia de MCI, errores
- errores de vídeo digital
- Errores de vídeo digital de MCI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6938330d15777ed867bf7d151a9d626e60b28646
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103778762"
---
# <a name="digital-video-errors"></a><span data-ttu-id="28b71-116">Errores de Digital-Video</span><span class="sxs-lookup"><span data-stu-id="28b71-116">Digital-Video Errors</span></span>

<span data-ttu-id="28b71-117">Los siguientes valores devueltos adicionales se definen para dispositivos de vídeo digital:</span><span class="sxs-lookup"><span data-stu-id="28b71-117">The following additional return values are defined for digital-video devices:</span></span>



| <span data-ttu-id="28b71-118">Value</span><span class="sxs-lookup"><span data-stu-id="28b71-118">Value</span></span>                           | <span data-ttu-id="28b71-119">Significado</span><span class="sxs-lookup"><span data-stu-id="28b71-119">Meaning</span></span>                                                         |
|---------------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="28b71-120">MCIAVI \_ NombreProducto</span><span class="sxs-lookup"><span data-stu-id="28b71-120">MCIAVI\_PRODUCTNAME</span></span>             | <span data-ttu-id="28b71-121">Vídeo</span><span class="sxs-lookup"><span data-stu-id="28b71-121">Video</span></span>                                                           |
| <span data-ttu-id="28b71-122">\_AUDIOERROR AVI \_ MCIERR</span><span class="sxs-lookup"><span data-stu-id="28b71-122">MCIERR\_AVI\_AUDIOERROR</span></span>         | <span data-ttu-id="28b71-123">Error desconocido al intentar reproducir audio.</span><span class="sxs-lookup"><span data-stu-id="28b71-123">Unknown error while attempting to play audio.</span></span>                   |
| <span data-ttu-id="28b71-124">\_BADPALETTE AVI \_ MCIERR</span><span class="sxs-lookup"><span data-stu-id="28b71-124">MCIERR\_AVI\_BADPALETTE</span></span>         | <span data-ttu-id="28b71-125">No se puede cambiar a la nueva paleta.</span><span class="sxs-lookup"><span data-stu-id="28b71-125">Unable to switch to new palette.</span></span>                                |
| <span data-ttu-id="28b71-126">\_CANTPLAYFULLSCREEN AVI \_ MCIERR</span><span class="sxs-lookup"><span data-stu-id="28b71-126">MCIERR\_AVI\_CANTPLAYFULLSCREEN</span></span> | <span data-ttu-id="28b71-127">Este archivo AVI no se puede reproducir en modo de pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="28b71-127">This AVI file cannot be played in full screen mode.</span></span>             |
| <span data-ttu-id="28b71-128">\_DISPLAYERROR AVI \_ MCIERR</span><span class="sxs-lookup"><span data-stu-id="28b71-128">MCIERR\_AVI\_DISPLAYERROR</span></span>       | <span data-ttu-id="28b71-129">Error desconocido al intentar mostrar el vídeo.</span><span class="sxs-lookup"><span data-stu-id="28b71-129">Unknown error while attempting to display video.</span></span>                |
| <span data-ttu-id="28b71-130">MCIERR \_ AVI \_ nocompresor</span><span class="sxs-lookup"><span data-stu-id="28b71-130">MCIERR\_AVI\_NOCOMPRESSOR</span></span>       | <span data-ttu-id="28b71-131">No se puede encontrar el compresor instalable necesario para reproducir este archivo.</span><span class="sxs-lookup"><span data-stu-id="28b71-131">Can't locate installable compressor needed to play this file.</span></span>   |
| <span data-ttu-id="28b71-132">\_NODISPDIB AVI \_ MCIERR</span><span class="sxs-lookup"><span data-stu-id="28b71-132">MCIERR\_AVI\_NODISPDIB</span></span>          | <span data-ttu-id="28b71-133">256 modo VGA de color no disponible.</span><span class="sxs-lookup"><span data-stu-id="28b71-133">256 color VGA mode not available.</span></span>                               |
| <span data-ttu-id="28b71-134">\_NOTINTERLEAVED AVI \_ MCIERR</span><span class="sxs-lookup"><span data-stu-id="28b71-134">MCIERR\_AVI\_NOTINTERLEAVED</span></span>     | <span data-ttu-id="28b71-135">Este archivo AVI no está intercalado.</span><span class="sxs-lookup"><span data-stu-id="28b71-135">This AVI file is not interleaved.</span></span>                               |
| <span data-ttu-id="28b71-136">\_OLDAVIFORMAT AVI \_ MCIERR</span><span class="sxs-lookup"><span data-stu-id="28b71-136">MCIERR\_AVI\_OLDAVIFORMAT</span></span>       | <span data-ttu-id="28b71-137">Este archivo AVI tiene un formato obsoleto.</span><span class="sxs-lookup"><span data-stu-id="28b71-137">This AVI file is of an obsolete format.</span></span>                         |
| <span data-ttu-id="28b71-138">\_TOOBIGFORVGA AVI \_ MCIERR</span><span class="sxs-lookup"><span data-stu-id="28b71-138">MCIERR\_AVI\_TOOBIGFORVGA</span></span>       | <span data-ttu-id="28b71-139">Este archivo AVI es demasiado grande para reproducirse en el modo VGA seleccionado.</span><span class="sxs-lookup"><span data-stu-id="28b71-139">This AVI file is too big to be played in the selected VGA mode.</span></span> |



 

 

 




