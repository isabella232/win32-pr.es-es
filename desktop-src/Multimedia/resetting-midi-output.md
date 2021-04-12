---
title: Restablecimiento de la salida MIDI
description: Restablecimiento de la salida MIDI
ms.assetid: 281a7cfa-f274-4c7a-b63a-c0573b9f1169
keywords:
- Interfaz digital de instrumentos musicales (MIDI), restablecimiento de dispositivos de salida
- MIDI (interfaz digital de instrumentos musicales), restablecimiento de dispositivos de salida
- reproducir archivos MIDI, restablecer los dispositivos de salida
- restablecimiento de dispositivos de salida
- Interfaz digital de instrumentos musicales (MIDI), dispositivos de salida
- MIDI (interfaz digital de instrumentos musicales), dispositivos de salida
- reproducir archivos MIDI, dispositivos de salida
- Dispositivos de salida MIDI
- EOX (final de exclusivo)
- fin de exclusivo (EOX)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15778fc8a1a48c34b69915aafb7e3139153b5882
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104358824"
---
# <a name="resetting-midi-output"></a>Restablecimiento de la salida MIDI

La función [**midiOutReset**](/windows/win32/api/mmeapi/nf-mmeapi-midioutreset) desactiva todas las notas en todos los canales MIDI para un dispositivo MIDI especificado. A continuación, la función marca todos los búferes exclusivos del sistema pendientes como terminados y los devuelve a la aplicación. Esta función puede ser útil en una aplicación que usa la salida MIDI para proporcionar al usuario la capacidad de restablecer la salida MIDI.

> [!Note]  
> La finalización de un mensaje exclusivo del sistema sin enviar un byte de EOX (final de exclusión) puede causar problemas en el dispositivo receptor. La función **midiOutReset** no envía un byte de EOX cuando finaliza un mensaje exclusivo del sistema, ya que las aplicaciones son responsables de hacerlo.

 

 

 