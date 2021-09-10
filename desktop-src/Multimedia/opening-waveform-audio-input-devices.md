---
title: Abrir Waveform-Audio dispositivos de entrada
description: Abrir Waveform-Audio dispositivos de entrada
ms.assetid: 46cdbce6-2433-433a-abd2-39e4146aa2e9
keywords:
- audio de onda, apertura de dispositivos de entrada
- interfaz de audio de onda, abrir dispositivos de entrada
- grabación de audio de forma de onda, apertura de dispositivos de entrada
- abrir dispositivos de entrada de audio y forma de onda
- waveInOpen , función
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c92b7f49b9d170ceb8ebce287025ce0e0c1c5530
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124371299"
---
# <a name="opening-waveform-audio-input-devices"></a>Abrir Waveform-Audio dispositivos de entrada

Use la [**función waveInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveinopen) para abrir un dispositivo de entrada de audio de forma de onda para la grabación. Esta función abre el dispositivo asociado al identificador de dispositivo especificado y devuelve un identificador del dispositivo abierto escribiendo el identificador de una ubicación de memoria especificada.

Algunos equipos multimedia tienen varios dispositivos de entrada de audio de forma de onda. A menos que sepa que desea abrir un dispositivo de entrada de audio de forma de onda específico en un sistema, debe usar la constante WAVE MAPPER para el identificador de dispositivo al \_ abrir un dispositivo. La [**función waveInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveinopen) elegirá el dispositivo en el sistema que mejor pueda grabar en el formato de datos especificado.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Grabación de audio de forma de onda](recording-waveform-audio.md)
</dt> </dl>

 

 