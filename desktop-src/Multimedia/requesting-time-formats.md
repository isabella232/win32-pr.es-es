---
title: Solicitar formatos de hora
description: Solicitar formatos de hora
ms.assetid: 3492dfe3-ed54-405a-aa4f-b17abbd1e07f
keywords:
- Interfaz digital de instrumentos musicales (MIDI), formatos de hora
- MIDI (interfaz digital de instrumentos musicales), formatos de hora
- Servicios MIDI, formatos de hora
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf191c857c45896c916ace4656d33bd3dd558f04
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103789754"
---
# <a name="requesting-time-formats"></a><span data-ttu-id="dc819-106">Solicitar formatos de hora</span><span class="sxs-lookup"><span data-stu-id="dc819-106">Requesting Time Formats</span></span>

<span data-ttu-id="dc819-107">Windows usa la estructura [**MMTIME**](/previous-versions//dd757347(v=vs.85)) para representar la hora en uno o varios formatos diferentes, incluidos los formatos de puntero de milisegundos, ejemplos, SMPTE y MIDI Song.</span><span class="sxs-lookup"><span data-stu-id="dc819-107">Windows uses the [**MMTIME**](/previous-versions//dd757347(v=vs.85)) structure to represent time in one or more different formats, including milliseconds, samples, SMPTE, and MIDI song pointer formats.</span></span> <span data-ttu-id="dc819-108">El miembro **wType** especifica el formato de hora.</span><span class="sxs-lookup"><span data-stu-id="dc819-108">The **wType** member specifies the time format.</span></span>

<span data-ttu-id="dc819-109">La función [**midiStreamPosition**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamposition) utiliza la estructura **MMTIME** .</span><span class="sxs-lookup"><span data-stu-id="dc819-109">The [**midiStreamPosition**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamposition) function uses the **MMTIME** structure.</span></span> <span data-ttu-id="dc819-110">Antes de llamar a esta función, debe establecer el miembro **wType** para indicar el formato de hora solicitado.</span><span class="sxs-lookup"><span data-stu-id="dc819-110">Before calling this function, you must set the **wType** member to indicate your requested time format.</span></span> <span data-ttu-id="dc819-111">Para ver si se admite el formato de hora solicitado, compruebe **wType** después de la llamada.</span><span class="sxs-lookup"><span data-stu-id="dc819-111">To see if the requested time format is supported, check **wType** after the call.</span></span> <span data-ttu-id="dc819-112">Si no se admite el formato de hora solicitado, la hora se especifica en un formato de hora alternativo seleccionado por el controlador de dispositivo y el miembro **wType** se cambia para indicar el formato de hora seleccionado.</span><span class="sxs-lookup"><span data-stu-id="dc819-112">If the requested time format is not supported, the time is specified in an alternate time format selected by the device driver and the **wType** member is changed to indicate the selected time format.</span></span>

<span data-ttu-id="dc819-113">Para obtener más información sobre la estructura **MMTIME** , vea [temporizadores multimedia](multimedia-timers.md).</span><span class="sxs-lookup"><span data-stu-id="dc819-113">For more information about the **MMTIME** structure, see [Multimedia Timers](multimedia-timers.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="dc819-114">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="dc819-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dc819-115">Servicios MIDI</span><span class="sxs-lookup"><span data-stu-id="dc819-115">MIDI Services</span></span>](midi-services.md)
</dt> </dl>

 

 