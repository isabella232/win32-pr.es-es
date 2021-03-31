---
title: Waveform-Audio tipos de datos de entrada
description: Waveform-Audio tipos de datos de entrada
ms.assetid: dfedcb93-edfb-4a25-8445-95d4aee55734
keywords:
- audio de la onda, tipos de datos de entrada
- 'onda: interfaz de audio, tipos de datos de entrada'
- grabar audio de onda, tipos de datos de entrada
- Identificador de HWAVEIN
- WAVEFORMATEX (estructura)
- Estructura WAVEHDR
- Estructura WAVEINCAPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39a8d37869224fe2ce677e2b8b952030ca6e021f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104077683"
---
# <a name="waveform-audio-input-data-types"></a>Waveform-Audio tipos de datos de entrada

Los siguientes tipos de datos se definen para las funciones de entrada de audio de onda.



| Tipo                                 | Descripción                                                                                                                                                     |
|--------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **HWAVEIN**                          | Identificador de un dispositivo de entrada de audio de onda abierta.                                                                                                                  |
| [**WAVEFORMATEX**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) | Estructura que especifica los formatos de datos admitidos por un dispositivo de entrada de audio de forma de onda determinado. Esta estructura también se utiliza para los dispositivos de salida de onda-audio. |
| [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr)           | Estructura utilizada como encabezado para un bloque de datos de entrada de audio de forma de onda. Esta estructura también se utiliza para los dispositivos de salida de onda-audio.                             |
| [**WAVEINCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-waveincaps)     | Estructura usada para consultar las capacidades de un dispositivo de entrada de audio de forma de onda determinado.                                                                   |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Grabación de audio de onda](recording-waveform-audio.md)
</dt> </dl>

 

 