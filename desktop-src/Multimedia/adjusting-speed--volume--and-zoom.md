---
title: Ajustar la velocidad, el volumen y el zoom
description: Ajustar la velocidad, el volumen y el zoom
ms.assetid: 16cfbf86-911e-4cf3-9640-69fffc09c1ed
keywords:
- MCIWndSetSpeed (macro)
- MCIWndGetSpeed (macro)
- MCIWndSetVolume (macro)
- MCIWndGetVolume (macro)
- MCIWndSetZoom (macro)
- MCIWndGetZoom (macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f02b1e14a5153e279e3cfdf6989beade31cf6f3e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418743"
---
# <a name="adjusting-speed-volume-and-zoom"></a><span data-ttu-id="cb088-109">Ajustar la velocidad, el volumen y el zoom</span><span class="sxs-lookup"><span data-stu-id="cb088-109">Adjusting Speed, Volume, and Zoom</span></span>

<span data-ttu-id="cb088-110">Las macros de velocidad, volumen y zoom proporcionan la funcionalidad de los comandos **Ver**, **volumen** y **velocidad** del menú MCIWnd.</span><span class="sxs-lookup"><span data-stu-id="cb088-110">The speed, volume, and zoom macros provide the functionality of the **View**, **Volume**, and **Speed** commands on the MCIWnd menu.</span></span> <span data-ttu-id="cb088-111">Las macros que se describen en esta sección se suelen usar con vídeo y otros dispositivos que muestran imágenes durante la reproducción.</span><span class="sxs-lookup"><span data-stu-id="cb088-111">The macros described in this section are generally used with video and other devices that display images during playback.</span></span>

<span data-ttu-id="cb088-112">Algunos dispositivos admiten varios cambios de velocidad de reproducción.</span><span class="sxs-lookup"><span data-stu-id="cb088-112">Some devices support multiple playback speed changes.</span></span> <span data-ttu-id="cb088-113">Puede establecer la velocidad de reproducción de estos dispositivos mediante la macro [**MCIWndSetSpeed**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetspeed) .</span><span class="sxs-lookup"><span data-stu-id="cb088-113">You can set the playback speed for these devices by using the [**MCIWndSetSpeed**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetspeed) macro.</span></span> <span data-ttu-id="cb088-114">Esta macro define la velocidad de reproducción como 1000.</span><span class="sxs-lookup"><span data-stu-id="cb088-114">This macro defines the playback speed as 1000.</span></span> <span data-ttu-id="cb088-115">Los valores más altos indican velocidades más rápidas.</span><span class="sxs-lookup"><span data-stu-id="cb088-115">Higher values indicate faster speeds.</span></span> <span data-ttu-id="cb088-116">Los valores menores indican velocidades más lentas.</span><span class="sxs-lookup"><span data-stu-id="cb088-116">Lower values indicate slower speeds.</span></span>

<span data-ttu-id="cb088-117">Puede recuperar la velocidad de reproducción actual mediante la macro [**MCIWndGetSpeed**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetspeed) .</span><span class="sxs-lookup"><span data-stu-id="cb088-117">You can retrieve the current playback speed by using the [**MCIWndGetSpeed**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetspeed) macro.</span></span> <span data-ttu-id="cb088-118">Esta macro usa los mismos valores e intervalo que los usados por **MCIWndSetSpeed**.</span><span class="sxs-lookup"><span data-stu-id="cb088-118">This macro uses the same values and range as those used by **MCIWndSetSpeed**.</span></span>

<span data-ttu-id="cb088-119">Algunos dispositivos admiten cambios de volumen.</span><span class="sxs-lookup"><span data-stu-id="cb088-119">Some devices support volume changes.</span></span> <span data-ttu-id="cb088-120">Puede ajustar o establecer el volumen mediante la macro [**MCIWndSetVolume**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetvolume) .</span><span class="sxs-lookup"><span data-stu-id="cb088-120">You can adjust or set the volume by using the [**MCIWndSetVolume**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetvolume) macro.</span></span> <span data-ttu-id="cb088-121">Esta macro define el nivel de volumen normal como 1000.</span><span class="sxs-lookup"><span data-stu-id="cb088-121">This macro defines the normal volume level as 1000.</span></span> <span data-ttu-id="cb088-122">Los valores más altos indican volúmenes más altos.</span><span class="sxs-lookup"><span data-stu-id="cb088-122">Higher values indicate louder volumes.</span></span> <span data-ttu-id="cb088-123">Los valores más bajos indican volúmenes más silenciosos.</span><span class="sxs-lookup"><span data-stu-id="cb088-123">Lower values indicate quieter volumes.</span></span>

<span data-ttu-id="cb088-124">Puede recuperar el nivel de volumen actual mediante la macro [**MCIWndGetVolume**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetvolume) .</span><span class="sxs-lookup"><span data-stu-id="cb088-124">You can retrieve the current volume level by using the [**MCIWndGetVolume**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetvolume) macro.</span></span> <span data-ttu-id="cb088-125">Esta macro usa los mismos valores numéricos e intervalo que los usados por **MCIWndSetVolume**.</span><span class="sxs-lookup"><span data-stu-id="cb088-125">This macro uses the same numerical values and range as those used by **MCIWndSetVolume**.</span></span>

<span data-ttu-id="cb088-126">En el caso de los dispositivos que usan una ventana de reproducción, MCIWnd admite una característica de zoom que establece el tamaño de la imagen de reproducción.</span><span class="sxs-lookup"><span data-stu-id="cb088-126">For devices that use a playback window, MCIWnd supports a zoom feature that sets the size of the playback image.</span></span> <span data-ttu-id="cb088-127">Puede establecer el tamaño de la imagen de reproducción mediante la macro [**MCIWndSetZoom**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetzoom) .</span><span class="sxs-lookup"><span data-stu-id="cb088-127">You can set the playback image size by using the [**MCIWndSetZoom**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetzoom) macro.</span></span> <span data-ttu-id="cb088-128">La macro vuelve a definir el tamaño de la imagen de reproducción y mantiene una relación de aspecto constante para la imagen.</span><span class="sxs-lookup"><span data-stu-id="cb088-128">The macro redefines the playback image size while maintaining a constant aspect ratio for the image.</span></span> <span data-ttu-id="cb088-129">El valor de zoom se define como un porcentaje del tamaño de la imagen original.</span><span class="sxs-lookup"><span data-stu-id="cb088-129">The zoom value is defined as a percentage of the original image size.</span></span> <span data-ttu-id="cb088-130">Por lo tanto, 100 representa el tamaño original de la imagen, 50 indica que la imagen que se muestra tiene la mitad del tamaño original y 200 indica que la imagen mostrada tiene el doble del tamaño original.</span><span class="sxs-lookup"><span data-stu-id="cb088-130">Thus, 100 represents the original image size, 50 indicates the image shown is half its original size, and 200 indicates that the image shown is twice its original size.</span></span>

<span data-ttu-id="cb088-131">Puede recuperar el valor de zoom actual mediante la macro [**MCIWndGetZoom**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetzoom) .</span><span class="sxs-lookup"><span data-stu-id="cb088-131">You can retrieve the current zoom value by using the [**MCIWndGetZoom**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetzoom) macro.</span></span> <span data-ttu-id="cb088-132">Esta macro usa los mismos valores e intervalo que los usados por **MCIWndSetZoom**.</span><span class="sxs-lookup"><span data-stu-id="cb088-132">This macro uses the same values and range as those used by **MCIWndSetZoom**.</span></span>

> [!Note]  
> <span data-ttu-id="cb088-133">Los controladores de audio y de onda del CD de MCI estándar no admiten cambios de volumen o de velocidad.</span><span class="sxs-lookup"><span data-stu-id="cb088-133">The standard MCI CD audio and waveform-audio drivers do not support volume or speed changes.</span></span>

 

 

 




