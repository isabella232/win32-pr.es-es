---
title: Uso de la estructura DESATEX
description: Uso de la estructura DESATEX
ms.assetid: 9b668e1e-cb5f-4065-802b-23974925eacf
keywords:
- audio de forma de onda, estructura DESATEX
- audio auxiliar, estructura DESATEX
- STRUCTUREATEX (estructura)
- Datos de audio de PCM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1534cf660c2f2423dc526c3d29f8eca06878fc0c
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124371324"
---
# <a name="using-the-waveformatex-structure"></a>Uso de la estructura DESATEX

En el caso de los datos de audio PCM en no más de dos canales y con muestras de 8 o 16 bits, use la estructura [**DESACTETEX**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) para especificar el formato de datos.

En el ejemplo siguiente se muestra cómo configurar una estructura **DE FORMADEDATEX** para 11,025 kilohercios (kHz) mono de 8 bits y para estéreo de 16 bits de 44,1 kHz. Después de configurar **LAMTEX,** en el ejemplo se llama a la función IsFormatSupported para comprobar que el dispositivo de salida de forma de onda PCM admite el formato. El código fuente de IsFormatSupported se muestra en un ejemplo de Determinar la [compatibilidad con formato no estándar.](determining-nonstandard-format-support.md)


```C++
UINT wReturn; 
WAVEFORMATEX pcmWaveFormat; 
 
// Set up WAVEFORMATEX for 11 kHz 8-bit mono. 
 
pcmWaveFormat.wFormatTag = WAVE_FORMAT_PCM; 
pcmWaveFormat.nChannels = 1; 
pcmWaveFormat.nSamplesPerSec = 11025L; 
pcmWaveFormat.nAvgBytesPerSec = 11025L; 
pcmWaveFormat.nBlockAlign = 1; 
pcmWaveFormat.wBitsPerSample = 8; 
pcmWaveFormat.cbSize = 0;
 
// See if format is supported by any device in system. 
 
wReturn = IsFormatSupported(&pcmWaveFormat, WAVE_MAPPER); 
 
// Report results. 
 
if (wReturn == 0) 
     MessageBox(hMainWnd, "11 kHz 8-bit mono is supported.", 
       "", MB_ICONINFORMATION); 
else if (wReturn == WAVERR_BADFORMAT) 
     MessageBox(hMainWnd, "11 kHz 8-bit mono NOT supported.", 
       "", MB_ICONINFORMATION); 
else 
     MessageBox(hMainWnd, "Error opening waveform device.", 
       "Error", MB_ICONEXCLAMATION); 
 
// Set up WAVEFORMATEX for 44.1 kHz 16-bit stereo. 
 
pcmWaveFormat.wFormatTag = WAVE_FORMAT_PCM; 
pcmWaveFormat.nChannels = 2; 
pcmWaveFormat.nSamplesPerSec = 44100L; 
pcmWaveFormat.nAvgBytesPerSec = 176400L; 
pcmWaveFormat.nBlockAlign = 4; 
pcmWaveFormat.wBitsPerSample = 16; 
pcmWaveFormat.cbSize = 0;
 
// See if format is supported by any device in the system. 
 
wReturn = IsFormatSupported(&pcmWaveFormat, WAVE_MAPPER); 
 
// Report results. 
 
if (wReturn == 0) 
    MessageBox(hMainWnd, "44.1 kHz 16-bit stereo is supported.", 
      "", MB_ICONINFORMATION); 
else if (wReturn == WAVERR_BADFORMAT) 
    MessageBox(hMainWnd, "44.1 kHz 16-bit stereo NOT supported.", 
      "", MB_ICONINFORMATION); 
else 
    MessageBox(hMainWnd, "Error opening waveform device.", 
      "Error", MB_ICONEXCLAMATION); 

```



 

 