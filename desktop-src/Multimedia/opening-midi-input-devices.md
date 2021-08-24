---
title: Apertura de dispositivos de entrada DE LÍNEA
description: Apertura de dispositivos de entrada DE LÍNEA
ms.assetid: fd6ebd0c-6985-49d3-8015-a636d4c70ff3
keywords:
- Interfaz digital de instrumentar música (MIDI), dispositivos de entrada
- MIDI (Interfaz digital de instrumentar música), dispositivos de entrada
- grabación de audio DE AUDIO, dispositivos de entrada
- Dispositivos de entrada MIDI
- Interfaz digital de instrumentar música (MIDI), abrir dispositivos de entrada
- MIDI (Interfaz digital de instrumentar música), abrir dispositivos de entrada
- grabación de audio MIDI, apertura de dispositivos de entrada
- abrir dispositivos de entrada DE LÍNEA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d260674194e7f066e5095e30a78c94b241a60b32304888aceb8db9ae06ccfea6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119806275"
---
# <a name="opening-midi-input-devices"></a>Apertura de dispositivos de entrada DE LÍNEA

Para abrir un dispositivo de entrada MIDI para la grabación, use la [**función midiInOpen.**](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen) Esta función abre el dispositivo asociado al identificador de dispositivo especificado y devuelve un identificador del dispositivo abierto escribiendo el identificador en una ubicación de memoria especificada.

Si usa la marca DE ESTADO DE E/S DE MIDI con \_ \_ **midiInOpen,** el sistema usa el mensaje [**\_ MOREDATA**](mim-moredata.md) de MIM para alertar de la función de devolución de llamada de la aplicación cuando no procesa los datos DE MIDI lo suficientemente rápido como para mantenerse al día con el controlador de dispositivo de entrada. (El [**mensaje MM MIM \_ \_ MOREDATA**](mm-mim-moredata.md) realiza el mismo trabajo con devoluciones de llamada de ventana. Sin embargo, por motivos de rendimiento, la mayoría de las aplicaciones usarán funciones de devolución de llamada en lugar de devoluciones de llamada de ventana). Si la aplicación procesa datos MIDI en un subproceso independiente, aumentar la prioridad del subproceso puede tener un impacto significativo en la capacidad de la aplicación para mantenerse al día con el flujo de datos.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Grabación de audio DE AUDIO DE AUDIO](recording-midi-audio.md)
</dt> </dl>

 

 