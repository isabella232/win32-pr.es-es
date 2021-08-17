---
title: Formato de audio
description: Formato de audio
ms.assetid: a65dbd3f-1539-4f02-8573-c527c4e3c58d
keywords:
- WM_CAP_GET_AUDIOFORMAT mensaje
- CapGetAudioFormat macro
- CapGetAudioFormatSize macro
- WM_CAP_SET_AUDIOFORMAT mensaje
- CapSetAudioFormat macro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5891e8c244487895c51d68dd92fc4935f8981a36cf67d81437ff45f58950527b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118375704"
---
# <a name="audio-format"></a>Formato de audio

Puede recuperar el formato de captura actual de los datos de audio o el tamaño de la estructura de formato de audio mediante el envío del mensaje [**\_ GET \_ \_ AUDIOFORMAT**](wm-cap-get-audioformat.md) de WM CAP (o las macros [**capGetAudioFormat**](/windows/desktop/api/Vfw/nf-vfw-capgetaudioformat) y [**capGetAudioFormatSize)**](/windows/desktop/api/Vfw/nf-vfw-capgetaudioformatsize) a una ventana de captura. El formato de captura de audio predeterminado es mono, PCM de 8 bits y 11 kHz (pulse Code Sides). Al recuperar el formato mediante WM \_ CAP \_ GET \_ AUDIOFORMAT, use siempre la [**estructura DEFORMATEX.**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex)

Puede establecer el formato de captura de los datos de audio mediante el envío del mensaje [**WM \_ CAP SET \_ \_ AUDIOFORMAT**](wm-cap-set-audioformat.md) (o la macro [**capSetAudioFormat)**](/windows/desktop/api/Vfw/nf-vfw-capsetaudioformat) a una ventana de captura. Al establecer el formato de audio, puede pasar un puntero a una estructura [**WAVEFORMAT,**](/windows/win32/api/mmreg/ns-mmreg-waveformat) **WAVEFORMAT** o [**PCMWAVEFORMAT,**](/windows/win32/api/mmreg/ns-mmreg-pcmwaveformat) según el formato de audio especificado.

 

 