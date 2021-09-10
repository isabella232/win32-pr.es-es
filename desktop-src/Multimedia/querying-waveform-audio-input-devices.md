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
ms.openlocfilehash: 91b915b3f39ad417a3d92396d887e5fb66092119
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124371300"
---
# <a name="querying-waveform-audio-input-devices"></a>Consulta de Waveform-Audio dispositivos de entrada

Antes de grabar audio de forma de onda, debe llamar a la [**función waveInGetDevCaps**](/windows/win32/api/mmeapi/nf-mmeapi-waveingetdevcaps) para determinar las funcionalidades de entrada de audio de forma de onda del sistema. Esta función rellena una [**estructura WAVEINCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-waveincaps) con información sobre las funcionalidades de un dispositivo especificado. Esta información incluye el fabricante y los identificadores de producto, un nombre de producto para el dispositivo y el número de versión del controlador del dispositivo. Además, la estructura **WAVEINCAPS proporciona** información sobre los formatos estándar de audio de forma de onda que admite el dispositivo.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Grabación de audio de forma de onda](recording-waveform-audio.md)
</dt> </dl>

 

 