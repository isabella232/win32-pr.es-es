---
title: Apertura de dispositivos de salida DE MIDI
description: Apertura de dispositivos de salida DE MIDI
ms.assetid: 0a06611b-c0cd-4884-bc17-761c4aec4418
keywords:
- Interfaz digital instrumentable (MIDI), dispositivos de salida
- MIDI (Interfaz digital instrumentable), dispositivos de salida
- reproducir archivos MIDI, dispositivos de salida
- Dispositivos de salida de MIDI
- Interfaz digital instrumentable (MIDI), apertura de dispositivos de salida
- MIDI (Interfaz digital instrumentable), apertura de dispositivos de salida
- reproducir archivos MIDI, abrir dispositivos de salida
- abrir dispositivos de salida DE MIDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0976e265fe253d02bc9662e6ea9b376d5acc4b5fd9f62e56642b56df53ce135
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118136714"
---
# <a name="opening-midi-output-devices"></a>Apertura de dispositivos de salida DE MIDI

Para abrir un dispositivo de salida MIDI para la reproducción, use la [**función midiOutOpen.**](/windows/win32/api/mmeapi/nf-mmeapi-midioutopen) Esta función abre el dispositivo asociado al identificador de dispositivo especificado y devuelve un identificador del dispositivo abierto escribiendo el identificador en una ubicación de memoria especificada.

Uno de los parámetros de **midiOutOpen** es un valor doubleword. Este valor especifica un identificador de ventana o subproceso, un identificador de eventos o la dirección de una función de devolución de llamada que se usa para supervisar el progreso de la reproducción de los búferes de flujo y datos exclusivos del sistema DE MIDI. La supervisión permite a la aplicación determinar cuándo enviar bloques de datos adicionales y cuándo liberar los bloques de datos que se han enviado. Para obtener más información sobre estos métodos, vea [Managing MIDI Data Blocks](managing-midi-data-blocks.md).

 

 