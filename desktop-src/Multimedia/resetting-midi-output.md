---
title: Restablecimiento de la salida DE MIDI
description: Restablecimiento de la salida DE MIDI
ms.assetid: 281a7cfa-f274-4c7a-b63a-c0573b9f1169
keywords:
- Interfaz digital instrumentable (MIDI), restablecimiento de dispositivos de salida
- MIDI (Interfaz digital instrumentable), restablecimiento de dispositivos de salida
- reproducir archivos MIDI, restablecer dispositivos de salida
- restablecer dispositivos de salida
- Interfaz digital instrumentable (MIDI), dispositivos de salida
- MIDI (Interfaz digital instrumentable), dispositivos de salida
- reproducir archivos MIDI, dispositivos de salida
- Dispositivos de salida de MIDI
- EOX (final de exclusivo)
- fin de exclusivo (EOX)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46c0073d9fc016e21e401e4cb2e7c28b4fd1aa5e3180801975df4e334243b953
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119689265"
---
# <a name="resetting-midi-output"></a>Restablecimiento de la salida DE MIDI

La [**función midiOutReset**](/windows/win32/api/mmeapi/nf-mmeapi-midioutreset) desactiva todas las notas de todos los canales MIDI para un dispositivo MIDI especificado. A continuación, la función marca los búferes exclusivos del sistema pendientes tal como están y los devuelve a la aplicación. Esta función puede ser útil en una aplicación que usa la salida DE MIDI para proporcionar al usuario la capacidad de restablecer la salida DE MIDI.

> [!Note]  
> La terminación de un mensaje exclusivo del sistema sin enviar un byte EOX (final de exclusivo) puede causar problemas en el dispositivo receptor. La **función midiOutReset** no envía un byte EOX cuando finaliza un mensaje exclusivo del sistema, porque las aplicaciones son responsables de hacer esto.

 

 

 