---
description: La clase de dispositivo de entrada y salida consta de dispositivos de audio para entradas de audio de onda de bajo nivel.
ms.assetid: b2f32019-088f-4805-af7e-559a8179b1e6
title: onda/en
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3465a575937538c6a4113ec544b1d246fec3a598
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278556"
---
# <a name="wavein"></a><span data-ttu-id="3ffdb-103">onda/en</span><span class="sxs-lookup"><span data-stu-id="3ffdb-103">wave/in</span></span>

<span data-ttu-id="3ffdb-104">La clase de dispositivo de entrada y salida consta de dispositivos de audio para entradas de audio de onda de bajo nivel.</span><span class="sxs-lookup"><span data-stu-id="3ffdb-104">The wave/in device class consists of audio devices for low-level wave audio input.</span></span> <span data-ttu-id="3ffdb-105">Puede acceder a estos dispositivos mediante las funciones de onda, que se describen en el kit de desarrollo de software (SDK) de la plataforma.</span><span class="sxs-lookup"><span data-stu-id="3ffdb-105">You access these devices by using the wave functions, which are described in the Platform Software Development Kit (SDK).</span></span> <span data-ttu-id="3ffdb-106">Los dispositivos de esta clase están asociados a los dispositivos de línea que admiten el \_ tipo de medio LINEMEDIAMODE AUTOMATEDVOICE, que se especifica en el miembro **dwMediaModes** de la estructura [**LINEDEVCAPS**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps) para el dispositivo de línea.</span><span class="sxs-lookup"><span data-stu-id="3ffdb-106">Devices in this class are associated with line devices that support the LINEMEDIAMODE\_AUTOMATEDVOICE media type, which is specified in the **dwMediaModes** member of the [**LINEDEVCAPS**](/windows/desktop/api/Tapi/ns-tapi-linedevcaps) structure for the line device.</span></span>

<span data-ttu-id="3ffdb-107">Las funciones [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) y [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) rellenan una estructura [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring) , estableciendo el miembro **dwStringFormat** en el \_ valor binario STRINGFORMAT y anexando este miembro adicional:</span><span class="sxs-lookup"><span data-stu-id="3ffdb-107">The [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) and [**phoneGetID**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) functions fill a [**VARSTRING**](/windows/desktop/api/Tapi/ns-tapi-varstring) structure, setting the **dwStringFormat** member to the STRINGFORMAT\_BINARY value and appending this additional member:</span></span>

``` syntax
DWORD DeviceId;  // identifier of audio device
```

<span data-ttu-id="3ffdb-108">El miembro **DeviceId** es el identificador de un dispositivo de audio cerrado.</span><span class="sxs-lookup"><span data-stu-id="3ffdb-108">The **DeviceId** member is the identifier of a closed audio device.</span></span> <span data-ttu-id="3ffdb-109">Este identificador se usa en una llamada a la función [**waveInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveinopen) para abrir el dispositivo para la entrada.</span><span class="sxs-lookup"><span data-stu-id="3ffdb-109">You use this identifier in a call to the [**waveInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveinopen) function to open the device for input.</span></span> <span data-ttu-id="3ffdb-110">Puede usar el identificador de dispositivo resultante para grabar datos de audio digitalizados desde el dispositivo de línea o teléfono.</span><span class="sxs-lookup"><span data-stu-id="3ffdb-110">You can use the resulting device handle to record digitized audio data from the line or phone device.</span></span>

<span data-ttu-id="3ffdb-111">Aunque también existe una clase de dispositivo "Wave" para dispositivos de audio de onda de bajo nivel, siempre debe usar la clase de dispositivo de onda/entrada para la entrada de onda de bajo nivel.</span><span class="sxs-lookup"><span data-stu-id="3ffdb-111">Although a "wave" device class also exists for low-level wave audio devices, you should always use the wave/in device class for low-level wave input.</span></span>

<span data-ttu-id="3ffdb-112">Para obtener más información sobre las funciones de onda, consulte [**funciones multimedia**](../multimedia/multimedia-functions.md).</span><span class="sxs-lookup"><span data-stu-id="3ffdb-112">For more information about the wave functions, see [**Multimedia Functions**](../multimedia/multimedia-functions.md).</span></span>

 

 
