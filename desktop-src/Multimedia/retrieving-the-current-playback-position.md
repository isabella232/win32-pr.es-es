---
title: Recuperar la posición de reproducción actual
description: Recuperar la posición de reproducción actual
ms.assetid: a08fe5da-8945-486f-9413-877c7d13d5de
keywords:
- audio de forma de onda, posición de reproducción actual
- 'forma de onda: interfaz de audio, posición de reproducción actual'
- reproducción de forma de onda-archivos de audio, posición de reproducción actual
- waveOutGetPosition función)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b28737cfc292dc8779b21756f38813642b82e452
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104358820"
---
# <a name="retrieving-the-current-playback-position"></a><span data-ttu-id="d58a4-107">Recuperar la posición de reproducción actual</span><span class="sxs-lookup"><span data-stu-id="d58a4-107">Retrieving the Current Playback Position</span></span>

<span data-ttu-id="d58a4-108">Puede supervisar la posición de reproducción actual dentro del archivo mientras se reproduce el audio de forma de onda mediante la función [**waveOutGetPosition**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetposition) .</span><span class="sxs-lookup"><span data-stu-id="d58a4-108">You can monitor the current playback position within the file while waveform audio is playing by using the [**waveOutGetPosition**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetposition) function.</span></span>

<span data-ttu-id="d58a4-109">En el caso de los dispositivos de audio de forma de onda, los ejemplos son el formato de hora preferido en el que se representa la posición actual.</span><span class="sxs-lookup"><span data-stu-id="d58a4-109">For waveform-audio devices, samples are the preferred time format in which to represent the current position.</span></span> <span data-ttu-id="d58a4-110">Por lo tanto, la posición actual de un dispositivo de audio de forma de onda se especifica como el número de muestras de un canal desde el principio del archivo de audio de forma de onda.</span><span class="sxs-lookup"><span data-stu-id="d58a4-110">Thus, the current position of a waveform-audio device is specified as the number of samples for one channel from the beginning of the waveform-audio file.</span></span> <span data-ttu-id="d58a4-111">Para consultar la posición actual de un dispositivo de audio de forma de onda, establezca el miembro **wType** de la estructura [**MMTIME**](/previous-versions//dd757347(v=vs.85)) en ejemplos de tiempo \_ y pase esta estructura a **waveOutGetPosition**.</span><span class="sxs-lookup"><span data-stu-id="d58a4-111">To query the current position of a waveform-audio device, set the **wType** member of the [**MMTIME**](/previous-versions//dd757347(v=vs.85)) structure to TIME\_SAMPLES and pass this structure to **waveOutGetPosition**.</span></span>

<span data-ttu-id="d58a4-112">La estructura **MMTIME** puede representar el tiempo en uno o varios formatos diferentes, incluidos los milisegundos, ejemplos, SMPTE (sociedad de los ingenieros de cine y televisión) y formatos de puntero de canción MIDI.</span><span class="sxs-lookup"><span data-stu-id="d58a4-112">The **MMTIME** structure can represent time in one or more different formats, including milliseconds, samples, SMPTE (Society of Motion Picture and Television Engineers), and MIDI song pointer formats.</span></span> <span data-ttu-id="d58a4-113">El miembro **wType** especifica el formato que se usa para representar la hora.</span><span class="sxs-lookup"><span data-stu-id="d58a4-113">The **wType** member specifies the format used to represent time.</span></span> <span data-ttu-id="d58a4-114">Antes de llamar a una función que usa la estructura **MMTIME** , debe establecer **wType** para indicar el formato de hora solicitado.</span><span class="sxs-lookup"><span data-stu-id="d58a4-114">Before calling a function that uses the **MMTIME** structure, you must set **wType** to indicate your requested time format.</span></span> <span data-ttu-id="d58a4-115">Asegúrese de comprobar **wType** después de la llamada para ver si se admite el formato de hora solicitado.</span><span class="sxs-lookup"><span data-stu-id="d58a4-115">Be sure to check **wType** after the call to see whether the requested time format is supported.</span></span> <span data-ttu-id="d58a4-116">Si no se admite el formato de hora solicitado, el controlador de dispositivo especifica la hora en un formato de hora alternativo y cambia el miembro de **wType** al formato de hora seleccionado.</span><span class="sxs-lookup"><span data-stu-id="d58a4-116">If the requested time format is not supported, the device driver specifies the time in an alternate time format and changes the **wType** member to the selected time format.</span></span>

<span data-ttu-id="d58a4-117">Para obtener más información sobre la estructura **MMTIME** , vea [temporizadores multimedia](multimedia-timers.md).</span><span class="sxs-lookup"><span data-stu-id="d58a4-117">For more information about the **MMTIME** structure, see [Multimedia Timers](multimedia-timers.md).</span></span>

 

 