---
title: Valores devueltos de MCIERR
description: Valores devueltos de MCIERR
ms.assetid: 61f7b128-b4f7-4385-9daf-e2bc9fb36e24
keywords:
- Windows multimedia, valores devueltos de MCIERR
- multimedia, valores devueltos de MCIERR
- referencia multimedia, valores devueltos de MCIERR
- referencia para multimedia, valores devueltos de MCIERR
- Valores devueltos de MCIERR, acerca de
- mciSendCommand función)
- mciSendString función)
- Windows multimedia, errores
- multimedia, errores
- referencia multimedia, errores
- referencia de multimedia, errores
- Media control Interface (MCI), valores devueltos de MCIERR
- MCI (media control Interface), valores devueltos de MCIERR
- referencia de MCI, valores devueltos de MCIERR
- Referencia de MCI, valores devueltos de MCIERR
- Media control Interface (MCI), errores
- MCI (interfaz de control multimedia), errores
- referencia de MCI, errores
- Referencia de MCI, errores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8912284b98b2aacb60905e3fef4dc32705a5656
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "105676365"
---
# <a name="mcierr-return-values"></a><span data-ttu-id="28658-122">Valores devueltos de MCIERR</span><span class="sxs-lookup"><span data-stu-id="28658-122">MCIERR Return Values</span></span>

<span data-ttu-id="28658-123">Las funciones [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) y [**mciSendString**](/previous-versions//dd757161(v=vs.85)) devuelven cero si son correctas; de lo contrario, devuelven un valor **DWORD** que contiene uno de los siguientes valores de error en la palabra baja.</span><span class="sxs-lookup"><span data-stu-id="28658-123">The [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) and [**mciSendString**](/previous-versions//dd757161(v=vs.85)) functions return zero if they are successful; otherwise, they return a **DWORD** value that contains one of the following error values in the low word.</span></span>

-   [<span data-ttu-id="28658-124">Errores generales de MCI</span><span class="sxs-lookup"><span data-stu-id="28658-124">General MCI Errors</span></span>](general-mci-errors.md)
-   [<span data-ttu-id="28658-125">Errores de mciSendString</span><span class="sxs-lookup"><span data-stu-id="28658-125">mciSendString Errors</span></span>](mcisendstring-errors.md)
-   [<span data-ttu-id="28658-126">Errores de vídeo digital</span><span class="sxs-lookup"><span data-stu-id="28658-126">Digital-Video Errors</span></span>](digital-video-errors.md)
-   [<span data-ttu-id="28658-127">Errores del secuenciador</span><span class="sxs-lookup"><span data-stu-id="28658-127">Sequencer Errors</span></span>](sequencer-errors.md)
-   [<span data-ttu-id="28658-128">Onda-errores de audio</span><span class="sxs-lookup"><span data-stu-id="28658-128">Waveform-Audio Errors</span></span>](waveform-audio-errors.md)

<span data-ttu-id="28658-129">Puede obtener una descripción de los valores devueltos individuales pasando los valores devueltos a la función [**mciGetErrorString**](/previous-versions//dd757158(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="28658-129">You can obtain a description of individual return values by passing the return values to the [**mciGetErrorString**](/previous-versions//dd757158(v=vs.85)) function.</span></span>

 

 