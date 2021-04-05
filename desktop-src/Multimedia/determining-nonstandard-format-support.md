---
title: Determinar la compatibilidad con formatos no estándar
description: Determinar la compatibilidad con formatos no estándar
ms.assetid: a795aa7d-704b-4f03-9815-7a298907bd3d
keywords:
- audio de forma de onda, compatibilidad con formato no estándar
- audio auxiliar, compatibilidad con formato no estándar
- audio de forma de onda, compatibilidad con formato estándar
- audio auxiliar, compatibilidad con formato estándar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d0933a82ca8da53c89e1cb8b7d32b40dc89ae0c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104077664"
---
# <a name="determining-nonstandard-format-support"></a><span data-ttu-id="c7d81-107">Determinar la compatibilidad con formatos no estándar</span><span class="sxs-lookup"><span data-stu-id="c7d81-107">Determining Nonstandard Format Support</span></span>

<span data-ttu-id="c7d81-108">Para ver si un dispositivo admite un formato determinado (estándar o no estándar), puede llamar a la función [**waveOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen) con la marca de consulta de formato de onda \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="c7d81-108">To see whether a device supports a particular format (standard or nonstandard), you can call the [**waveOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen) function with the WAVE\_FORMAT\_QUERY flag.</span></span> <span data-ttu-id="c7d81-109">En el ejemplo siguiente se usa esta técnica para determinar si un dispositivo de audio de forma de onda admite un formato especificado.</span><span class="sxs-lookup"><span data-stu-id="c7d81-109">The following example uses this technique to determine whether a waveform-audio device supports a specified format.</span></span>


```C++
// Determines whether the specified waveform-audio output device 
// supports a specified waveform-audio format. Returns 
// MMSYSERR_NOERROR if the format is supported, WAVEERR_BADFORMAT if 
// the format is not supported, and one of the other MMSYSERR_ error 
// codes if there are other errors encountered in opening the 
// specified waveform-audio device. 
 
MMRESULT IsFormatSupported(LPWAVEFORMATEX pwfx, UINT uDeviceID) 
{ 
    return (waveOutOpen( 
        NULL,                 // ptr can be NULL for query 
        uDeviceID,            // the device identifier 
        pwfx,                 // defines requested format 
        NULL,                 // no callback 
        NULL,                 // no instance data 
        WAVE_FORMAT_QUERY));  // query only, do not open device 
} 
```



<span data-ttu-id="c7d81-110">Esta técnica para determinar la compatibilidad con el formato no estándar también se aplica a los dispositivos de entrada de audio de forma de onda.</span><span class="sxs-lookup"><span data-stu-id="c7d81-110">This technique for determining nonstandard format support also applies to waveform-audio input devices.</span></span> <span data-ttu-id="c7d81-111">La única diferencia es que la función [**waveInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveinopen) se usa en lugar de [**waveOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen) para consultar la compatibilidad con el formato.</span><span class="sxs-lookup"><span data-stu-id="c7d81-111">The only difference is that the [**waveInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveinopen) function is used in place of [**waveOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen) to query for format support.</span></span>

<span data-ttu-id="c7d81-112">Para determinar si un formato de datos de forma de onda determinado es compatible con cualquiera de los dispositivos de audio de forma de onda de un sistema, use la técnica que se ilustra en el ejemplo anterior, pero especifique la \_ constante del asignador de ondas para el parámetro *uDeviceID* .</span><span class="sxs-lookup"><span data-stu-id="c7d81-112">To determine whether a particular waveform-audio data format is supported by any of the waveform-audio devices in a system, use the technique illustrated in the previous example, but specify the WAVE\_MAPPER constant for the *uDeviceID* parameter.</span></span>

 

 