---
title: Consulta de dispositivos de entrada Waveform-Audio
description: Consulta de dispositivos de entrada Waveform-Audio
ms.assetid: 573b33bc-f445-496e-a0e6-0194d30bb668
keywords:
- audio de onda, consulta de dispositivos de entrada
- 'onda: interfaz de audio, consulta de dispositivos de entrada'
- grabación de audio de onda, consulta de dispositivos de entrada
- consultar los dispositivos de entrada de onda-audio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91b915b3f39ad417a3d92396d887e5fb66092119
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103995193"
---
# <a name="querying-waveform-audio-input-devices"></a>Consulta de dispositivos de entrada Waveform-Audio

Antes de grabar audio de onda de onda, debe llamar a la función [**waveInGetDevCaps**](/windows/win32/api/mmeapi/nf-mmeapi-waveingetdevcaps) para determinar las capacidades de entrada de audio de onda del sistema. Esta función rellena una estructura [**WAVEINCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-waveincaps) con información sobre las capacidades de un dispositivo especificado. Esta información incluye los identificadores de fabricante y de producto, un nombre de producto para el dispositivo y el número de versión del controlador de dispositivo. Además, la estructura **WAVEINCAPS** proporciona información sobre los formatos de audio de forma de onda estándar que admite el dispositivo.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Grabación de audio de onda](recording-waveform-audio.md)
</dt> </dl>

 

 