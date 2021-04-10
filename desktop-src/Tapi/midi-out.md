---
description: La clase de dispositivo MIDI/Out consta de secuenciadores MIDI que se utilizan para la salida. Puede acceder a estos dispositivos mediante las funciones MIDI, que se describen en el kit de desarrollo de software (SDK) de la plataforma.
ms.assetid: 398119ec-2d08-4c37-a993-a9b5ce52bcc8
title: MIDI/salida
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d6ae6a3daba8fa0520fca666e6c43a8b3db86c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275175"
---
# <a name="midiout"></a><span data-ttu-id="32562-104">MIDI/salida</span><span class="sxs-lookup"><span data-stu-id="32562-104">midi/out</span></span>

<span data-ttu-id="32562-105">La clase de dispositivo MIDI/Out consta de secuenciadores MIDI que se utilizan para la salida.</span><span class="sxs-lookup"><span data-stu-id="32562-105">The midi/out device class consists of MIDI sequencers that are used for output.</span></span> <span data-ttu-id="32562-106">Puede acceder a estos dispositivos mediante las funciones MIDI, que se describen en el kit de desarrollo de software (SDK) de la plataforma.</span><span class="sxs-lookup"><span data-stu-id="32562-106">You access these devices by using the MIDI functions, which are described in the Platform Software Development Kit (SDK).</span></span>

<span data-ttu-id="32562-107">Las funciones [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) y [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) rellenan una estructura [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring) , estableciendo el miembro **dwStringFormat** en el \_ valor binario STRINGFORMAT y anexando este miembro adicional:</span><span class="sxs-lookup"><span data-stu-id="32562-107">The [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) and [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) functions fill a [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring) structure, setting the **dwStringFormat** member to the STRINGFORMAT\_BINARY value and appending this additional member:</span></span>

``` syntax
DWORD DeviceId;  // identifier of MIDI device
```

<span data-ttu-id="32562-108">El miembro **DeviceId** es el identificador de un dispositivo MIDI cerrado.</span><span class="sxs-lookup"><span data-stu-id="32562-108">The **DeviceId** member is the identifier of a closed MIDI device.</span></span> <span data-ttu-id="32562-109">Este identificador se usa en una llamada a la función [**midiOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midioutopen) para abrir el dispositivo para la salida.</span><span class="sxs-lookup"><span data-stu-id="32562-109">You use this identifier in a call to the [**midiOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midioutopen) function to open the device for output.</span></span> <span data-ttu-id="32562-110">Puede usar el identificador de dispositivo resultante para reproducir datos MIDI en el dispositivo de línea o teléfono.</span><span class="sxs-lookup"><span data-stu-id="32562-110">You can use the resulting device handle to play MIDI data at the line or phone device.</span></span>

<span data-ttu-id="32562-111">Para obtener más información acerca de las funciones MIDI, consulte [**funciones multimedia**](../multimedia/multimedia-functions.md).</span><span class="sxs-lookup"><span data-stu-id="32562-111">For more information about the MIDI functions, see [**Multimedia Functions**](../multimedia/multimedia-functions.md).</span></span>

 

 
