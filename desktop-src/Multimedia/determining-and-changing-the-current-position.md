---
title: Determinar y cambiar la posición actual
description: Determinar y cambiar la posición actual
ms.assetid: 20f78dcd-3259-43c2-8da3-8cfc299252e6
keywords:
- MCIWndGetStart (macro)
- MCIWndGetEnd (macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84a8e7022bdfcede526a730014a07deaf22fe66d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104486862"
---
# <a name="determining-and-changing-the-current-position"></a><span data-ttu-id="a6e2d-105">Determinar y cambiar la posición actual</span><span class="sxs-lookup"><span data-stu-id="a6e2d-105">Determining and Changing the Current Position</span></span>

<span data-ttu-id="a6e2d-106">Cuando un archivo o un dispositivo están asociados a una ventana de MCIWnd, la posición de reproducción se establece inicialmente al principio del contenido, independientemente del tipo de medio.</span><span class="sxs-lookup"><span data-stu-id="a6e2d-106">When a file or device is associated with an MCIWnd window, the playback position is initially set at the start of the content, regardless of the media type.</span></span> <span data-ttu-id="a6e2d-107">Durante la reproducción, la posición de reproducción se mueve linealmente a través del contenido y, si la reproducción no se interrumpe, llega al final del contenido.</span><span class="sxs-lookup"><span data-stu-id="a6e2d-107">During playback, the playback position moves linearly through the content and, if playback is uninterrupted, eventually reaches the end of the content.</span></span> <span data-ttu-id="a6e2d-108">Si se produce una interrupción, la posición de reproducción actual es la ubicación en la que se detuvo o pausó la reproducción.</span><span class="sxs-lookup"><span data-stu-id="a6e2d-108">If an interruption occurs, the current playback position is the location at which playback was stopped or paused.</span></span>

<span data-ttu-id="a6e2d-109">Puede recuperar las ubicaciones para el principio y el final del contenido mediante las macros [**MCIWndGetStart**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetstart) y [**MCIWndGetEnd**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetend) .</span><span class="sxs-lookup"><span data-stu-id="a6e2d-109">You can retrieve the locations for the beginning and end of the content by using the [**MCIWndGetStart**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetstart) and [**MCIWndGetEnd**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetend) macros.</span></span> <span data-ttu-id="a6e2d-110">Puede determinar la longitud del contenido restando el valor devuelto por **MCIWndGetStart** del valor devuelto por **MCIWndGetEnd** o mediante la macro [**MCIWndGetLength**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetlength) .</span><span class="sxs-lookup"><span data-stu-id="a6e2d-110">You can determine the length of the content by subtracting the value returned by **MCIWndGetStart** from the value returned by **MCIWndGetEnd**, or by using the [**MCIWndGetLength**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetlength) macro.</span></span> <span data-ttu-id="a6e2d-111">Puede recuperar la posición de reproducción actual mediante la macro [**MCIWndGetPosition**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetposition) , o puede recuperar la posición de reproducción como una cadena terminada en NULL mediante la macro [**MCIWndGetPositionString**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetpositionstring) .</span><span class="sxs-lookup"><span data-stu-id="a6e2d-111">You can retrieve the current playback position by using the [**MCIWndGetPosition**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetposition) macro, or you can retrieve the playback position as a null-terminated string by using the [**MCIWndGetPositionString**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetpositionstring) macro.</span></span>

<span data-ttu-id="a6e2d-112">Para cambiar la posición de reproducción actual, use las macros [**MCIWndHome**](/windows/desktop/api/Vfw/nf-vfw-mciwndhome), [**MCIWndEnd**](/windows/desktop/api/Vfw/nf-vfw-mciwndend)y [**MCIWndSeek**](/windows/desktop/api/Vfw/nf-vfw-mciwndseek) .</span><span class="sxs-lookup"><span data-stu-id="a6e2d-112">To change the current playback position, use the [**MCIWndHome**](/windows/desktop/api/Vfw/nf-vfw-mciwndhome), [**MCIWndEnd**](/windows/desktop/api/Vfw/nf-vfw-mciwndend), and [**MCIWndSeek**](/windows/desktop/api/Vfw/nf-vfw-mciwndseek) macros.</span></span> <span data-ttu-id="a6e2d-113">Puede mover la posición de reproducción al inicio del contenido mediante **MCIWndHome** o al final del contenido mediante **MCIWndEnd**.</span><span class="sxs-lookup"><span data-stu-id="a6e2d-113">You can move the playback position to the start of the content by using **MCIWndHome** or to the end of the content by using **MCIWndEnd**.</span></span> <span data-ttu-id="a6e2d-114">Use **MCIWndSeek** para mover la posición de reproducción a cualquier ubicación del contenido.</span><span class="sxs-lookup"><span data-stu-id="a6e2d-114">Use **MCIWndSeek** to move the playback position to any location in the content.</span></span>

<span data-ttu-id="a6e2d-115">También puede recorrer el contenido con la macro [**MCIWndStep**](/windows/desktop/api/Vfw/nf-vfw-mciwndstep) .</span><span class="sxs-lookup"><span data-stu-id="a6e2d-115">You can also step through the content by using the [**MCIWndStep**](/windows/desktop/api/Vfw/nf-vfw-mciwndstep) macro.</span></span> <span data-ttu-id="a6e2d-116">A partir de la posición de reproducción actual, esta macro mueve la posición de reproducción hacia delante o hacia atrás por un incremento especificado.</span><span class="sxs-lookup"><span data-stu-id="a6e2d-116">Beginning from the current playback position, this macro moves the playback position forward or backward by a specified increment.</span></span>

> [!Note]  
> <span data-ttu-id="a6e2d-117">Las unidades utilizadas para especificar la posición varían entre los distintos tipos de medios y dispositivos.</span><span class="sxs-lookup"><span data-stu-id="a6e2d-117">The units used to specify position vary among the different media types and devices.</span></span> <span data-ttu-id="a6e2d-118">Por ejemplo, la posición de reproducción para los archivos AVI utilizados por el dispositivo MCIAVI se mide en fotogramas; la posición de reproducción de los archivos de audio de CD, de audio de forma de onda y de MIDI se mide en milisegundos.</span><span class="sxs-lookup"><span data-stu-id="a6e2d-118">For example, the playback position for AVI files used by the MCIAVI device is measured in frames; the playback position for CD audio, waveform-audio, and MIDI files is measured in milliseconds.</span></span>

 

<span data-ttu-id="a6e2d-119">Los dispositivos de otros tipos de medios y dispositivos de terceros pueden usar otras unidades.</span><span class="sxs-lookup"><span data-stu-id="a6e2d-119">Devices for other media types and third-party devices might use other units.</span></span> <span data-ttu-id="a6e2d-120">Para obtener información acerca de cómo determinar estas unidades, consulte [mejoras de reproducción](playback-enhancements.md).</span><span class="sxs-lookup"><span data-stu-id="a6e2d-120">For information about determining these units, see [Playback Enhancements](playback-enhancements.md).</span></span>

 

 




