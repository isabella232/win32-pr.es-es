---
description: La clase de dispositivo MIDI/in consta de secuenciadores MIDI que se usan para la entrada. Puede acceder a estos dispositivos mediante las funciones MIDI, que se describen en el kit de desarrollo de software (SDK) de la plataforma.
ms.assetid: 8997a391-bf61-4ec9-8ffc-fe3e6b92d63a
title: MIDI/in
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1d8119990af37cb030211b7dcc3a75d5261411f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808305"
---
# <a name="midiin"></a><span data-ttu-id="87e5d-104">MIDI/in</span><span class="sxs-lookup"><span data-stu-id="87e5d-104">midi/in</span></span>

<span data-ttu-id="87e5d-105">La clase de dispositivo MIDI/in consta de secuenciadores MIDI que se usan para la entrada.</span><span class="sxs-lookup"><span data-stu-id="87e5d-105">The midi/in device class consists of MIDI sequencers that are used for input.</span></span> <span data-ttu-id="87e5d-106">Puede acceder a estos dispositivos mediante las funciones MIDI, que se describen en el kit de desarrollo de software (SDK) de la plataforma.</span><span class="sxs-lookup"><span data-stu-id="87e5d-106">You access these devices by using the MIDI functions, which are described in the Platform Software Development Kit (SDK).</span></span>

<span data-ttu-id="87e5d-107">Las funciones [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) y [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) rellenan una estructura [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring) , estableciendo el miembro **dwStringFormat** en el \_ valor binario STRINGFORMAT y anexando este miembro adicional:</span><span class="sxs-lookup"><span data-stu-id="87e5d-107">The [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) and [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) functions fill a [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring) structure, setting the **dwStringFormat** member to the STRINGFORMAT\_BINARY value and appending this additional member:</span></span>

``` syntax
DWORD DeviceId;  // identifier of MIDI device
```

<span data-ttu-id="87e5d-108">El miembro **DeviceId** es el identificador de un dispositivo MIDI cerrado.</span><span class="sxs-lookup"><span data-stu-id="87e5d-108">The **DeviceId** member is the identifier of a closed MIDI device.</span></span> <span data-ttu-id="87e5d-109">Este identificador se usa en una llamada a la función [**midiInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen) para abrir el dispositivo para la entrada.</span><span class="sxs-lookup"><span data-stu-id="87e5d-109">You use this identifier in a call to the [**midiInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen) function to open the device for input.</span></span> <span data-ttu-id="87e5d-110">Puede usar el identificador de dispositivo resultante para grabar datos MIDI desde el dispositivo de línea o teléfono.</span><span class="sxs-lookup"><span data-stu-id="87e5d-110">You can use the resulting device handle to record MIDI data from the line or phone device.</span></span>

<span data-ttu-id="87e5d-111">Para obtener más información acerca de las funciones MIDI, consulte [**funciones multimedia**](../multimedia/multimedia-functions.md).</span><span class="sxs-lookup"><span data-stu-id="87e5d-111">For more information about the MIDI functions, see [**Multimedia Functions**](../multimedia/multimedia-functions.md).</span></span>

 

 
