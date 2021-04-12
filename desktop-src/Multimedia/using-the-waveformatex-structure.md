---
title: Usar la estructura WAVEFORMATEX
description: Usar la estructura WAVEFORMATEX
ms.assetid: 9b668e1e-cb5f-4065-802b-23974925eacf
keywords:
- onda audio, WAVEFORMATEX (estructura)
- audio auxiliar, WAVEFORMATEX (estructura)
- WAVEFORMATEX (estructura)
- Datos de audio PCM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1534cf660c2f2423dc526c3d29f8eca06878fc0c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104487606"
---
# <a name="using-the-waveformatex-structure"></a><span data-ttu-id="6bce3-107">Usar la estructura WAVEFORMATEX</span><span class="sxs-lookup"><span data-stu-id="6bce3-107">Using the WAVEFORMATEX Structure</span></span>

<span data-ttu-id="6bce3-108">En el caso de los datos de audio PCM en un máximo de dos canales y con ejemplos de 8 o 16 bits, use la estructura [**WAVEFORMATEX**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) para especificar el formato de los datos.</span><span class="sxs-lookup"><span data-stu-id="6bce3-108">For PCM audio data on no more than two channels and with 8-bit or 16-bit samples, use the [**WAVEFORMATEX**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) structure to specify the data format.</span></span>

<span data-ttu-id="6bce3-109">En el ejemplo siguiente se muestra cómo configurar una estructura **WAVEFORMATEX** para mono 11,025 kilohercios (kHz) de 8 bits y para estéreo de 16 bits de 44,1 kHz.</span><span class="sxs-lookup"><span data-stu-id="6bce3-109">The following example shows how to set up a **WAVEFORMATEX** structure for 11.025 kilohertz (kHz) 8-bit mono and for 44.1 kHz 16-bit stereo.</span></span> <span data-ttu-id="6bce3-110">Después de configurar **WAVEFORMATEX**, el ejemplo llama a la función IsFormatSupported para comprobar que el dispositivo de salida de forma de onda PCM admite el formato.</span><span class="sxs-lookup"><span data-stu-id="6bce3-110">After setting up **WAVEFORMATEX**, the example calls the IsFormatSupported function to verify that the PCM waveform output device supports the format.</span></span> <span data-ttu-id="6bce3-111">El código fuente de IsFormatSupported se muestra en un ejemplo para [determinar la compatibilidad con el formato no estándar](determining-nonstandard-format-support.md).</span><span class="sxs-lookup"><span data-stu-id="6bce3-111">The source code for IsFormatSupported is shown in an example in [Determining Nonstandard Format Support](determining-nonstandard-format-support.md).</span></span>


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



 

 