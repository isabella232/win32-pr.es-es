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
# <a name="determining-nonstandard-format-support"></a>Determinar la compatibilidad con formatos no estándar

Para ver si un dispositivo admite un formato determinado (estándar o no estándar), puede llamar a la función [**waveOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen) con la marca de consulta de formato de onda \_ \_ . En el ejemplo siguiente se usa esta técnica para determinar si un dispositivo de audio de forma de onda admite un formato especificado.


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



Esta técnica para determinar la compatibilidad con el formato no estándar también se aplica a los dispositivos de entrada de audio de forma de onda. La única diferencia es que la función [**waveInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveinopen) se usa en lugar de [**waveOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen) para consultar la compatibilidad con el formato.

Para determinar si un formato de datos de forma de onda determinado es compatible con cualquiera de los dispositivos de audio de forma de onda de un sistema, use la técnica que se ilustra en el ejemplo anterior, pero especifique la \_ constante del asignador de ondas para el parámetro *uDeviceID* .

 

 