---
title: Apertura y cierre de controladores de dispositivos
description: Apertura y cierre de controladores de dispositivos
ms.assetid: 441bc0ec-41c9-4595-92f9-4c2304b10f16
keywords:
- Interfaz digital instrumentable (MIDI), abrir dispositivos
- MIDI (Interfaz digital instrumentable), apertura de dispositivos
- Servicios DE MIDI, abrir dispositivos
- abrir dispositivos MIDI
- Interfaz digital de instrumentar música (MIDI), cerrar dispositivos
- MIDI (Interfaz digital de instrumentar música), cerrar dispositivos
- Servicios DE MIDI, cerrar dispositivos
- cerrar dispositivos MIDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e935ab3d0d420e735bed6e01d08c80962e134338ea9e88eaa4899e0e81cb71f3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119806295"
---
# <a name="opening-and-closing-device-drivers"></a>Apertura y cierre de controladores de dispositivos

Debe abrir un dispositivo MIDI antes de usarlo y debe cerrarlo en cuanto termine de usarlo. Windows proporciona las siguientes funciones para abrir y cerrar distintos tipos de dispositivos MIDI.



| Valor                                | Significado                                            |
|--------------------------------------|----------------------------------------------------|
| [**midiInClose**](/windows/win32/api/mmeapi/nf-mmeapi-midiinclose)   | Cierra un dispositivo de entrada MIDI especificado.              |
| [**midiInOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen)     | Abre un dispositivo de entrada MIDI especificado para la grabación. |
| [**midiOutClose**](/windows/win32/api/mmeapi/nf-mmeapi-midioutclose) | Cierra un dispositivo de salida DE MIDI especificado.             |
| [**midiOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midioutopen)   | Abre un dispositivo de salida MIDI para la reproducción.           |



 

Cada función que abre un dispositivo MIDI toma como parámetros un identificador de dispositivo, una dirección de una ubicación de memoria y algunos parámetros únicos para los dispositivos MIDI. La ubicación de memoria se rellena con un identificador de dispositivo, que se usa para identificar el dispositivo de audio abierto en las llamadas a otras funciones de audio.

Muchas funciones DE MIDI pueden aceptar un identificador de dispositivo o un identificador de dispositivo. Aunque puede usar un identificador de dispositivo siempre que use un identificador de dispositivo, no siempre puede usar un identificador de dispositivo cuando se llama a un identificador.

> [!Note]  
> Los dispositivos MIDI no son necesariamente compartibles, por lo que es posible que un dispositivo determinado no esté disponible cuando un usuario lo solicite. Si esto ocurre, la aplicación debe notificar al usuario y permitir que intente abrir el dispositivo de nuevo.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Servicios DE MIDI](midi-services.md)
</dt> </dl>

 

 