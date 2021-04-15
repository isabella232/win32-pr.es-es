---
title: Apertura de Waveform-Audio dispositivos de entrada
description: Apertura de Waveform-Audio dispositivos de entrada
ms.assetid: 46cdbce6-2433-433a-abd2-39e4146aa2e9
keywords:
- audio de onda, abrir dispositivos de entrada
- 'onda: interfaz de audio, abrir dispositivos de entrada'
- grabar audio de onda, abrir dispositivos de entrada
- apertura de dispositivos de entrada de audio de onda
- waveInOpen función)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c92b7f49b9d170ceb8ebce287025ce0e0c1c5530
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "105676357"
---
# <a name="opening-waveform-audio-input-devices"></a>Apertura de Waveform-Audio dispositivos de entrada

Use la función [**waveInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveinopen) para abrir un dispositivo de entrada de onda-audio para grabar. Esta función abre el dispositivo asociado al identificador de dispositivo especificado y devuelve un identificador del dispositivo abierto escribiendo el identificador de una ubicación de memoria especificada.

Algunos equipos multimedia tienen varios dispositivos de entrada de audio de onda. A menos que sepa que desea abrir un dispositivo de entrada de audio de forma de onda específico en un sistema, debe usar la \_ constante asignador de onda para el identificador de dispositivo al abrir un dispositivo. La función [**waveInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveinopen) elegirá el dispositivo en el sistema que mejor se puede registrar en el formato de datos especificado.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Grabación de audio de onda](recording-waveform-audio.md)
</dt> </dl>

 

 