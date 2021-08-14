---
title: Apertura de Waveform-Audio entrada de datos
description: Apertura de Waveform-Audio entrada de datos
ms.assetid: 46cdbce6-2433-433a-abd2-39e4146aa2e9
keywords:
- audio de forma de onda, abrir dispositivos de entrada
- interfaz de audio de forma de onda, abrir dispositivos de entrada
- grabación de audio de forma de onda, apertura de dispositivos de entrada
- abrir dispositivos de entrada de audio de forma de onda
- función waveInOpen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e6391ca5bfe0690d2235504057865fb588f08d0359417ccbcc04b6a7e5eb082
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117802312"
---
# <a name="opening-waveform-audio-input-devices"></a>Apertura de Waveform-Audio entrada de datos

Use la [**función waveInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveinopen) para abrir un dispositivo de entrada de audio de forma de onda para la grabación. Esta función abre el dispositivo asociado al identificador de dispositivo especificado y devuelve un identificador del dispositivo abierto escribiendo el identificador de una ubicación de memoria especificada.

Algunos equipos multimedia tienen varios dispositivos de entrada de audio de forma de onda. A menos que sepa que desea abrir un dispositivo de entrada de audio de forma de onda específico en un sistema, debe usar la constante WAVE MAPPER para el identificador de dispositivo al \_ abrir un dispositivo. La [**función waveInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveinopen) elegirá el dispositivo en el sistema que mejor pueda grabar en el formato de datos especificado.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Grabación de audio de forma de onda](recording-waveform-audio.md)
</dt> </dl>

 

 