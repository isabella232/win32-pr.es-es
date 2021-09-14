---
title: Recepción Time-Stamped mensajes DE MIDI
description: Recepción Time-Stamped mensajes DE MIDI
ms.assetid: a91c85fe-f9c4-4cf6-b0bb-49aa8ed45644
keywords:
- Interfaz digital instrumentada (MIDI), mensajes con marca de tiempo
- MIDI (Interfaz digital instrumentada), mensajes con marca de tiempo
- grabación de audio MIDI, mensajes con marca de tiempo
- mensajes MIDI con marca de tiempo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7ead268c6d022f67a3607bb8a43a3d773bd7325
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127171569"
---
# <a name="receiving-time-stamped-midi-messages"></a>Recepción Time-Stamped mensajes DE MIDI

Debido al retraso entre el momento en que el controlador del dispositivo recibe un mensaje DE MIDI y el momento en que la aplicación recibe el mensaje, los controladores de dispositivos de entrada DE MIDI marcan el mensaje DE MIDI con la hora a la que se recibió el mensaje. Las marcas de tiempo de MIDI, que se definen como la hora a la que se recibió el primer byte del mensaje, se especifican en milisegundos. La [**función midiInStart**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstart) restablece las marcas de tiempo de un dispositivo a cero.

Como se indicó anteriormente, para recibir marcas de tiempo con la entrada de MIDI, debe usar una función de devolución de llamada. El *parámetro dwParam2* de la función de devolución de llamada especifica la marca de tiempo para los datos asociados con los MIM [**\_ DATA**](mim-data.md) [**y MIM mensajes \_ LONGDATA.**](mim-longdata.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Grabación de audio MIDI](recording-midi-audio.md)
</dt> </dl>

 

 