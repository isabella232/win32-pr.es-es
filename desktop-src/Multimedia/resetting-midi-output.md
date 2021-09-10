---
title: Restablecimiento de la salida de MIDI
description: Restablecimiento de la salida de MIDI
ms.assetid: 281a7cfa-f274-4c7a-b63a-c0573b9f1169
keywords:
- Interfaz digital de instrumentar música (MIDI), restablecer dispositivos de salida
- MIDI (Interfaz digital de instrumentador), restablecer dispositivos de salida
- reproducir archivos MIDI, restablecer dispositivos de salida
- restablecer dispositivos de salida
- Interfaz digital de instrumentar música (MIDI), dispositivos de salida
- MIDI (Interfaz digital de instrumentar música), dispositivos de salida
- reproducir archivos MIDI, dispositivos de salida
- Dispositivos de salida DE MIDI
- EOX (fin de exclusivo)
- fin de exclusivo (EOX)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15778fc8a1a48c34b69915aafb7e3139153b5882
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124371005"
---
# <a name="resetting-midi-output"></a>Restablecimiento de la salida de MIDI

La [**función midiOutReset**](/windows/win32/api/mmeapi/nf-mmeapi-midioutreset) desactiva todas las notas de todos los canales MIDI para un dispositivo MIDI especificado. A continuación, la función marca los búferes exclusivos del sistema pendientes como se ha hecho y los devuelve a la aplicación. Esta función puede ser útil en una aplicación que usa la salida DE MIDI para proporcionar al usuario la capacidad de restablecer la salida de MIDI.

> [!Note]  
> La terminación de un mensaje exclusivo del sistema sin enviar un byte EOX (final de exclusivo) puede causar problemas para el dispositivo receptor. La **función midiOutReset** no envía un byte EOX cuando finaliza un mensaje exclusivo del sistema, ya que las aplicaciones son responsables de hacer esto.

 

 

 