---
title: Consulta de Waveform-Audio dispositivos de entrada
description: Consulta de Waveform-Audio dispositivos de entrada
ms.assetid: 573b33bc-f445-496e-a0e6-0194d30bb668
keywords:
- audio de onda, consulta de dispositivos de entrada
- interfaz de audio de onda, consulta de dispositivos de entrada
- grabación de audio de forma de onda, consulta de dispositivos de entrada
- consultar dispositivos de entrada de audio de forma de onda
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8fd22a2b65746202a831d475fcde38b31259619dbc645a5cbca3b91d03ff6e0f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118371927"
---
# <a name="querying-waveform-audio-input-devices"></a>Consulta de Waveform-Audio dispositivos de entrada

Antes de grabar audio de forma de onda, debe llamar a la [**función waveInGetDevCaps**](/windows/win32/api/mmeapi/nf-mmeapi-waveingetdevcaps) para determinar las funcionalidades de entrada de audio de forma de onda del sistema. Esta función rellena una [**estructura WAVEINCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-waveincaps) con información sobre las funcionalidades de un dispositivo especificado. Esta información incluye los identificadores de fabricante y producto, un nombre de producto para el dispositivo y el número de versión del controlador del dispositivo. Además, la estructura **WAVEINCAPS proporciona** información sobre los formatos estándar de audio de forma de onda que admite el dispositivo.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Grabación de audio de forma de onda](recording-waveform-audio.md)
</dt> </dl>

 

 