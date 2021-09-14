---
title: Apertura de dispositivos de salida de MIDI
description: Apertura de dispositivos de salida de MIDI
ms.assetid: 0a06611b-c0cd-4884-bc17-761c4aec4418
keywords:
- Interfaz digital de instrumentar música (MIDI), dispositivos de salida
- MIDI (Interfaz digital de instrumentar música), dispositivos de salida
- reproducir archivos MIDI, dispositivos de salida
- Dispositivos de salida DE MIDI
- Interfaz digital de instrumentar música (MIDI), abrir dispositivos de salida
- MIDI (Interfaz digital de instrumentar música), abrir dispositivos de salida
- reproducir archivos MIDI, abrir dispositivos de salida
- abrir dispositivos de salida DE MES
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ca7a7e1db461b29700ec7c7c61ee140073bc345
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127173622"
---
# <a name="opening-midi-output-devices"></a>Apertura de dispositivos de salida de MIDI

Para abrir un dispositivo de salida MIDI para la reproducción, use la [**función midiOutOpen.**](/windows/win32/api/mmeapi/nf-mmeapi-midioutopen) Esta función abre el dispositivo asociado al identificador de dispositivo especificado y devuelve un identificador del dispositivo abierto escribiendo el identificador en una ubicación de memoria especificada.

Uno de los parámetros de **midiOutOpen** es un valor doubleword. Este valor especifica un identificador de ventana o subproceso, un identificador de eventos o la dirección de una función de devolución de llamada que se usa para supervisar el progreso de la reproducción de búferes de flujo y datos exclusivos del sistema DE MIDI. La supervisión permite a la aplicación determinar cuándo enviar bloques de datos adicionales y cuándo liberar los bloques de datos que se han enviado. Para obtener más información sobre estos métodos, vea [Administrar bloques de datos DE MIDI.](managing-midi-data-blocks.md)

 

 