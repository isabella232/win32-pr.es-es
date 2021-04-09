---
description: La clase de dispositivo de onda/salida consta de dispositivos de audio para la salida de audio de onda de bajo nivel.
ms.assetid: 85894134-e8ad-43e2-8b97-09b80bfd36d5
title: onda/salida
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 975a3308b6f0b29e130ad07534494e1cb1d991a9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913805"
---
# <a name="waveout"></a><span data-ttu-id="1d69f-103">onda/salida</span><span class="sxs-lookup"><span data-stu-id="1d69f-103">wave/out</span></span>

<span data-ttu-id="1d69f-104">La clase de dispositivo de onda/salida consta de dispositivos de audio para la salida de audio de onda de bajo nivel.</span><span class="sxs-lookup"><span data-stu-id="1d69f-104">The wave/out device class consists of audio devices for low-level wave audio output.</span></span> <span data-ttu-id="1d69f-105">Puede acceder a estos dispositivos mediante las funciones de onda, que se describen en el kit de desarrollo de software (SDK) de la plataforma.</span><span class="sxs-lookup"><span data-stu-id="1d69f-105">You access these devices by using the wave functions, which are described in the Platform Software Development Kit (SDK).</span></span> <span data-ttu-id="1d69f-106">Los dispositivos de esta clase están asociados a los dispositivos de línea que admiten el \_ tipo de medio LINEMEDIAMODE AUTOMATEDVOICE, que se especifica en el miembro **dwMediaModes** de la estructura [**LINEDEVCAPS**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps) para el dispositivo de línea.</span><span class="sxs-lookup"><span data-stu-id="1d69f-106">Devices in this class are associated with line devices that support the LINEMEDIAMODE\_AUTOMATEDVOICE media type, which is specified in the **dwMediaModes** member of the [**LINEDEVCAPS**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps) structure for the line device.</span></span>

<span data-ttu-id="1d69f-107">Las funciones [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) y [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) rellenan una estructura [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring) , estableciendo el miembro **dwStringFormat** en el \_ valor binario STRINGFORMAT y anexando este miembro adicional:</span><span class="sxs-lookup"><span data-stu-id="1d69f-107">The [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) and [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) functions fill a [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring) structure, setting the **dwStringFormat** member to the STRINGFORMAT\_BINARY value and appending this additional member:</span></span>

``` syntax
DWORD DeviceId;  // identifier of audio device
```

<span data-ttu-id="1d69f-108">El miembro **DeviceId** es el identificador de un dispositivo de audio cerrado.</span><span class="sxs-lookup"><span data-stu-id="1d69f-108">The **DeviceId** member is the identifier of a closed audio device.</span></span> <span data-ttu-id="1d69f-109">Este identificador se usa en una llamada a la función [**waveOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen) para abrir el dispositivo para la salida.</span><span class="sxs-lookup"><span data-stu-id="1d69f-109">You use this identifier in a call to the [**waveOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen) function to open the device for output.</span></span> <span data-ttu-id="1d69f-110">Puede usar el identificador de dispositivo resultante para reproducir datos de audio digitalizados en el dispositivo de línea o teléfono.</span><span class="sxs-lookup"><span data-stu-id="1d69f-110">You can use the resulting device handle to play digitized audio data at the line or phone device.</span></span>

<span data-ttu-id="1d69f-111">Aunque también existe una clase de dispositivo "Wave" para dispositivos de audio de onda de bajo nivel, siempre debe usar la clase de dispositivo de onda/salida para la salida de onda de bajo nivel.</span><span class="sxs-lookup"><span data-stu-id="1d69f-111">Although a "wave" device class also exists for low-level wave audio devices, you should always use the wave/out device class for low-level wave output.</span></span>

<span data-ttu-id="1d69f-112">Para obtener más información sobre las funciones de onda, consulte [**funciones multimedia**](../multimedia/multimedia-functions.md).</span><span class="sxs-lookup"><span data-stu-id="1d69f-112">For more information about the wave functions, see [**Multimedia Functions**](../multimedia/multimedia-functions.md).</span></span>

 

 
