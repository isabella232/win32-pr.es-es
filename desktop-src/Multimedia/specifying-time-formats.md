---
title: Especificar formatos de hora
description: Especificar formatos de hora
ms.assetid: 11d28d63-ed3e-4137-b9d8-1681bf0e33ff
keywords:
- MCIWndGetTimeFormat (macro)
- MCIWndSetTimeFormat (macro)
- MCIWndUseTime (macro)
- MCIWndUseFrames (macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e390e811bde4d797572c19f372923906f6b738b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357118"
---
# <a name="specifying-time-formats"></a><span data-ttu-id="50044-107">Especificar formatos de hora</span><span class="sxs-lookup"><span data-stu-id="50044-107">Specifying Time Formats</span></span>

<span data-ttu-id="50044-108">Normalmente, los tipos de datos multimedia pueden usar el tiempo para identificar posiciones significativas dentro de su contenido.</span><span class="sxs-lookup"><span data-stu-id="50044-108">Multimedia data types typically can use time to identify significant positions within their content.</span></span> <span data-ttu-id="50044-109">Los formatos de hora comunes son milisegundos, pistas y fotogramas; también existen otros formatos de hora menos comunes, como SMPTE (sociedad de la imagen de movimiento y ingenieros de televisión) 24.</span><span class="sxs-lookup"><span data-stu-id="50044-109">Common time formats are milliseconds, tracks, and frames; other less common time formats, such as SMPTE (Society of Motion Picture and Television Engineers) 24, also exist.</span></span> <span data-ttu-id="50044-110">La hora es el sistema de formato y de referencia para los datos de audio de forma de onda, MIDI y CD.</span><span class="sxs-lookup"><span data-stu-id="50044-110">Time is the format and reference system for waveform-audio, MIDI, and CD audio data.</span></span> <span data-ttu-id="50044-111">El vídeo admite el tiempo aunque se grabe como una secuencia de fotogramas (secuencia) que normalmente se reproduce a una velocidad específica.</span><span class="sxs-lookup"><span data-stu-id="50044-111">Video supports time even though it is recorded as a sequence of frames (stream) that is typically played at a specific speed.</span></span> <span data-ttu-id="50044-112">Hay varias macros disponibles para designar el formato de hora.</span><span class="sxs-lookup"><span data-stu-id="50044-112">Several macros are available for designating time format.</span></span>

<span data-ttu-id="50044-113">Puede recuperar el formato de hora actual para un archivo o dispositivo mediante la macro [**MCIWndGetTimeFormat**](/windows/desktop/api/Vfw/nf-vfw-mciwndgettimeformat) .</span><span class="sxs-lookup"><span data-stu-id="50044-113">You can retrieve the current time format for a file or device by using the [**MCIWndGetTimeFormat**](/windows/desktop/api/Vfw/nf-vfw-mciwndgettimeformat) macro.</span></span> <span data-ttu-id="50044-114">Puede cambiar el formato de hora actual a cualquier otro formato de hora compatible con un dispositivo mediante la macro [**MCIWndSetTimeFormat**](/windows/desktop/api/Vfw/nf-vfw-mciwndsettimeformat) .</span><span class="sxs-lookup"><span data-stu-id="50044-114">You can change the current time format to any other time format supported by a device by using the [**MCIWndSetTimeFormat**](/windows/desktop/api/Vfw/nf-vfw-mciwndsettimeformat) macro.</span></span> <span data-ttu-id="50044-115">O bien, puede establecer el formato de hora en milisegundos o en marcos mediante el uso de las macros [**MCIWndUseTime**](/windows/desktop/api/Vfw/nf-vfw-mciwndusetime) o [**MCIWndUseFrames**](/windows/desktop/api/Vfw/nf-vfw-mciwnduseframes) .</span><span class="sxs-lookup"><span data-stu-id="50044-115">Or you can the set the time format to milliseconds or frames by using the [**MCIWndUseTime**](/windows/desktop/api/Vfw/nf-vfw-mciwndusetime) or [**MCIWndUseFrames**](/windows/desktop/api/Vfw/nf-vfw-mciwnduseframes) macros.</span></span>

> [!Note]  
> <span data-ttu-id="50044-116">Los formatos no continuos, como las pistas y SMPTE, pueden hacer que la barra de herramientas se comporte de forma errática.</span><span class="sxs-lookup"><span data-stu-id="50044-116">Noncontinuous formats, such as tracks and SMPTE, can cause the toolbar to behave erratically.</span></span> <span data-ttu-id="50044-117">Para estos formatos de hora, puede que desee desactivar la barra de herramientas especificando el estilo de ventana de MCIWNDF \_ NOPLAYBAR al crear una ventana de MCIWnd.</span><span class="sxs-lookup"><span data-stu-id="50044-117">For these time formats, you might want to turn off the toolbar by specifying the MCIWNDF\_NOPLAYBAR window style when creating an MCIWnd window.</span></span>

 

 

 




