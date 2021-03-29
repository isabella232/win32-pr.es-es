---
title: Abrir y cerrar controladores de dispositivos
description: Abrir y cerrar controladores de dispositivos
ms.assetid: 441bc0ec-41c9-4595-92f9-4c2304b10f16
keywords:
- Interfaz digital de instrumentos musicales (MIDI), abrir dispositivos
- MIDI (interfaz digital de instrumentos musicales), abrir dispositivos
- Servicios MIDI, abrir dispositivos
- apertura de dispositivos MIDI
- Interfaz digital de instrumentos musicales (MIDI), cerrar dispositivos
- MIDI (interfaz digital de instrumentos musicales), cerrar dispositivos
- Servicios MIDI, cerrar dispositivos
- cerrar dispositivos MIDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53d7035455baa067b81af7da980a4ae043500c7b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103789958"
---
# <a name="opening-and-closing-device-drivers"></a>Abrir y cerrar controladores de dispositivos

Debe abrir un dispositivo MIDI antes de usarlo y debe cerrar el dispositivo tan pronto como termine de usarlo. Windows proporciona las siguientes funciones para abrir y cerrar diferentes tipos de dispositivos MIDI.



| Value                                | Significado                                            |
|--------------------------------------|----------------------------------------------------|
| [**midiInClose**](/windows/win32/api/mmeapi/nf-mmeapi-midiinclose)   | Cierra un dispositivo de entrada MIDI especificado.              |
| [**midiInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen)     | Abre un dispositivo de entrada MIDI especificado para grabar. |
| [**midiOutClose**](/windows/win32/api/mmeapi/nf-mmeapi-midioutclose) | Cierra un dispositivo de salida MIDI especificado.             |
| [**midiOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midioutopen)   | Abre un dispositivo de salida MIDI para la reproducción.           |



 

Cada función que abre un dispositivo MIDI toma como parámetros un identificador de dispositivo, una dirección de una ubicación de memoria y algunos parámetros exclusivos de los dispositivos MIDI. La ubicación de memoria se rellena con un identificador de dispositivo, que se usa para identificar el dispositivo de audio abierto en llamadas a otras funciones de audio.

Muchas funciones MIDI pueden aceptar un identificador de dispositivo o un identificador de dispositivo. Aunque puede usar un identificador de dispositivo siempre que use un identificador de dispositivo, no puede usar siempre un identificador de dispositivo cuando se llama a un identificador para.

> [!Note]  
> Los dispositivos MIDI no se pueden compartir necesariamente, por lo que es posible que un dispositivo determinado no esté disponible cuando un usuario lo solicite. Si esto ocurre, la aplicación debe notificar al usuario y permitir que el usuario intente abrir el dispositivo de nuevo.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Servicios MIDI](midi-services.md)
</dt> </dl>

 

 