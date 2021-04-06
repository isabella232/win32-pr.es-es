---
title: Formato de audio
description: Formato de audio
ms.assetid: a65dbd3f-1539-4f02-8573-c527c4e3c58d
keywords:
- Mensaje WM_CAP_GET_AUDIOFORMAT
- capGetAudioFormat (macro)
- capGetAudioFormatSize (macro)
- Mensaje WM_CAP_SET_AUDIOFORMAT
- capSetAudioFormat (macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e362abd393097ae8763b44b3ee3474685ffd5c2
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103904531"
---
# <a name="audio-format"></a>Formato de audio

Puede recuperar el formato de captura actual para los datos de audio o el tamaño de la estructura de formato de audio enviando el mensaje [**Cap de WM \_ \_ Get \_ AUDIOFORMAT**](wm-cap-get-audioformat.md) (o las macros [**capGetAudioFormat**](/windows/desktop/api/Vfw/nf-vfw-capgetaudioformat) y [**capGetAudioFormatSize**](/windows/desktop/api/Vfw/nf-vfw-capgetaudioformatsize) ) a una ventana de captura. El formato de captura de audio predeterminado es mono, 8 bits, PCM de 11 kHz (modulación de código Pulse). Cuando recupere el formato mediante el uso de \_ Cap Cap \_ Get \_ AUDIOFORMAT, use siempre la estructura [**WAVEFORMATEX**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) .

Puede establecer el formato de captura de los datos de audio mediante el envío del mensaje [**AUDIOFORMAT del conjunto de límites de WM \_ \_ \_**](wm-cap-set-audioformat.md) (o la macro [**capSetAudioFormat**](/windows/desktop/api/Vfw/nf-vfw-capsetaudioformat) ) a una ventana de captura. Al establecer el formato de audio, puede pasar un puntero a una estructura [**WAVEFORMAT**](/windows/win32/api/mmreg/ns-mmreg-waveformat), **WAVEFORMATEX** o [**PCMWAVEFORMAT**](/windows/win32/api/mmreg/ns-mmreg-pcmwaveformat) , en función del formato de audio especificado.

 

 