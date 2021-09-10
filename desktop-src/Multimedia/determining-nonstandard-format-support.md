---
title: Determinar la compatibilidad con formato no estándar
description: Determinar la compatibilidad con formato no estándar
ms.assetid: a795aa7d-704b-4f03-9815-7a298907bd3d
keywords:
- audio de forma de onda, compatibilidad con formato no estándar
- audio auxiliar, compatibilidad con formato no estándar
- audio de forma de onda, compatibilidad con formato estándar
- audio auxiliar, compatibilidad con formato estándar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d0933a82ca8da53c89e1cb8b7d32b40dc89ae0c
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124371312"
---
# <a name="determining-nonstandard-format-support"></a>Determinar la compatibilidad con formato no estándar

Para ver si un dispositivo admite un formato determinado (estándar o no estándar), puede llamar a la [**función waveOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen) con la marca WAVE \_ FORMAT \_ QUERY. En el ejemplo siguiente se usa esta técnica para determinar si un dispositivo de audio de forma de onda admite un formato especificado.


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



Esta técnica para determinar la compatibilidad con formato no estándar también se aplica a los dispositivos de entrada de audio de forma de onda. La única diferencia es que la [**función waveInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveinopen) se usa en lugar de [**waveOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen) para consultar la compatibilidad con formato.

Para determinar si un formato de datos de audio de forma de onda determinado es compatible con cualquiera de los dispositivos de audio de forma de onda de un sistema, use la técnica que se muestra en el ejemplo anterior, pero especifique la constante WAVE MAPPER para el parámetro \_ *uDeviceID.*

 

 