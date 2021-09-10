---
title: Formato de audio
description: Formato de audio
ms.assetid: a65dbd3f-1539-4f02-8573-c527c4e3c58d
keywords:
- WM_CAP_GET_AUDIOFORMAT mensaje
- CapGetAudioFormat macro
- CapGetAudioFormatSize macro
- WM_CAP_SET_AUDIOFORMAT mensaje
- CapSetAudioFormat (macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e362abd393097ae8763b44b3ee3474685ffd5c2
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124371972"
---
# <a name="audio-format"></a>Formato de audio

Puede recuperar el formato de captura actual para los datos de audio o el tamaño de la estructura de formato de audio mediante el envío del mensaje [**\_ GET \_ \_ AUDIOFORMAT**](wm-cap-get-audioformat.md) de WM CAP (o las macros [**capGetAudioFormat**](/windows/desktop/api/Vfw/nf-vfw-capgetaudioformat) y [**capGetAudioFormatSize)**](/windows/desktop/api/Vfw/nf-vfw-capgetaudioformatsize) a una ventana de captura. El formato de captura de audio predeterminado es UNM de 11 kHz (PCM de 8 bits y 11 kHz) de forma mono. Cuando se recupera el formato mediante WM \_ CAP \_ GET \_ AUDIOFORMAT, use siempre la [**estructura DEFORMATEX.**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex)

Puede establecer el formato de captura de los datos de audio enviando el mensaje [**\_ WM CAP SET \_ \_ AUDIOFORMAT**](wm-cap-set-audioformat.md) (o la macro [**capSetAudioFormat)**](/windows/desktop/api/Vfw/nf-vfw-capsetaudioformat) a una ventana de captura. Al establecer el formato de audio, puede pasar un puntero a una estructura [**WAVEFORMAT, WAVEFORMAT,**](/windows/win32/api/mmreg/ns-mmreg-waveformat) **WAVEATEX** o [**PCMWAVEFORMAT,**](/windows/win32/api/mmreg/ns-mmreg-pcmwaveformat) en función del formato de audio especificado.

 

 