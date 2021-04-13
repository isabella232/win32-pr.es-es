---
title: Recibir mensajes de Time-Stamped MIDI
description: Recibir mensajes de Time-Stamped MIDI
ms.assetid: a91c85fe-f9c4-4cf6-b0bb-49aa8ed45644
keywords:
- Interfaz digital de instrumentos musicales (MIDI), mensajes con marca de tiempo
- MIDI (interfaz digital de instrumentos musicales), mensajes con marca de tiempo
- grabar mensajes MIDI de audio y con marca de tiempo
- mensajes MIDI con marca de tiempo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7ead268c6d022f67a3607bb8a43a3d773bd7325
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104358883"
---
# <a name="receiving-time-stamped-midi-messages"></a>Recibir mensajes de Time-Stamped MIDI

Debido al retraso entre el momento en que el controlador de dispositivo recibe un mensaje MIDI y el momento en que la aplicación recibe el mensaje, los controladores de dispositivos de entrada MIDI marcan el mensaje MIDI con la hora en que se recibió el mensaje. Las marcas de tiempo MIDI, que se definen como la hora en que se recibió el primer byte del mensaje, se especifican en milisegundos. La función [**midiInStart**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstart) restablece las marcas de tiempo de un dispositivo a cero.

Como se indicó anteriormente, para recibir marcas de tiempo con entrada de MIDI, debe usar una función de devolución de llamada. El parámetro *dwParam2* de la función de devolución de llamada especifica la marca de tiempo para los datos asociados a los [**\_ datos de MIM**](mim-data.md) y los mensajes [**\_ LONGDATA de MIM**](mim-longdata.md) .

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Grabación de audio MIDI](recording-midi-audio.md)
</dt> </dl>

 

 