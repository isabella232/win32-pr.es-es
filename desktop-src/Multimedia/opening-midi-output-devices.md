---
title: Abrir dispositivos de salida MIDI
description: Abrir dispositivos de salida MIDI
ms.assetid: 0a06611b-c0cd-4884-bc17-761c4aec4418
keywords:
- Interfaz digital de instrumentos musicales (MIDI), dispositivos de salida
- MIDI (interfaz digital de instrumentos musicales), dispositivos de salida
- reproducir archivos MIDI, dispositivos de salida
- Dispositivos de salida MIDI
- Interfaz digital de instrumentos musicales (MIDI), abrir dispositivos de salida
- MIDI (interfaz digital de instrumentos musicales), abrir dispositivos de salida
- reproducir archivos MIDI, abrir dispositivos de salida
- abrir dispositivos de salida MIDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ca7a7e1db461b29700ec7c7c61ee140073bc345
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104487643"
---
# <a name="opening-midi-output-devices"></a>Abrir dispositivos de salida MIDI

Para abrir un dispositivo de salida MIDI para la reproducción, utilice la función [**midiOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-midioutopen) . Esta función abre el dispositivo asociado al identificador de dispositivo especificado y devuelve un identificador del dispositivo abierto escribiendo el identificador en una ubicación de memoria especificada.

Uno de los parámetros de **midiOutOpen** es un valor de palabra. Este valor especifica un identificador de ventana o de subproceso, un identificador de evento o la dirección de una función de devolución de llamada que se usa para supervisar el progreso de la reproducción de datos y búferes de secuencia exclusivos del sistema MIDI. La supervisión permite a la aplicación determinar cuándo se deben enviar bloques de datos adicionales y cuándo liberar los bloques de datos que se han enviado. Para obtener más información acerca de estos métodos, consulte [administrar bloques de datos MIDI](managing-midi-data-blocks.md).

 

 