---
title: Recepción de Time-Stamped mensajes MIDI
description: Recepción de Time-Stamped mensajes MIDI
ms.assetid: a91c85fe-f9c4-4cf6-b0bb-49aa8ed45644
keywords:
- Interfaz digital de instrumentar música (MIDI), mensajes con marca de tiempo
- MIDI (Interfaz digital instrumentada), mensajes con marca de tiempo
- grabación de audio DE AUDIO, mensajes con marca de tiempo
- mensajes MIDI con marca de tiempo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ec36628a417c19824e25c7ad013da9c539fe88cb6e58fd829a32205bce35679
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118371295"
---
# <a name="receiving-time-stamped-midi-messages"></a>Recepción de Time-Stamped mensajes MIDI

Debido al retraso entre el momento en que el controlador del dispositivo recibe un mensaje MIDI y el momento en que la aplicación recibe el mensaje, los controladores de dispositivos de entrada DE LÍNEA marcan el mensaje MIDI con la hora a la que se recibió el mensaje. Las marcas de tiempo de MIDI, que se definen como la hora a la que se recibió el primer byte del mensaje, se especifican en milisegundos. La [**función midiInStart**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstart) restablece las marcas de tiempo de un dispositivo a cero.

Como se indicó anteriormente, para recibir marcas de tiempo con la entrada MIDI, debe usar una función de devolución de llamada. El *parámetro dwParam2* de la función de devolución de llamada especifica la marca de tiempo para los datos asociados a MIM [**\_ DATA**](mim-data.md) y [**MIM mensajes \_ LONGDATA.**](mim-longdata.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Grabación de audio DE AUDIO DE AUDIO](recording-midi-audio.md)
</dt> </dl>

 

 