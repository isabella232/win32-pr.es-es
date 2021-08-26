---
title: Envío de System-Exclusive mensajes
description: Envío de System-Exclusive mensajes
ms.assetid: 2bb95e4e-004e-46c8-9c56-25436fcc7f6c
keywords:
- Interfaz digital de instrumentar música (MIDI), enviar mensajes
- MIDI (Interfaz digital instrumenta de música), envío de mensajes
- reproducir archivos MIDI, enviar mensajes
- envío de mensajes MIDI
- Interfaz digital instrumentable (MIDI), mensajes exclusivos del sistema
- MIDI (Interfaz digital instrumentable), mensajes exclusivos del sistema
- reproducir archivos MIDI, mensajes exclusivos del sistema
- mensajes MIDI exclusivos del sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aad97371f56c042e5acd230aba6144f5f9734a594b370a791422b2e8f8148861
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120037265"
---
# <a name="sending-system-exclusive-messages"></a>Envío de System-Exclusive mensajes

Los mensajes exclusivos del sistema DE MIDI son los únicos mensajes MIDI que no caben en un solo valor doubleword. Los mensajes exclusivos del sistema pueden tener cualquier longitud. Windows proporciona la [**función midiOutLongMsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutlongmsg) para enviar mensajes exclusivos del sistema a los dispositivos de salida DE MIDI. Para especificar bloques de datos exclusivos del sistema DE MIDI, use la [**estructura MIDIHDR.**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr)

Después de enviar un bloque de datos exclusivo del sistema mediante **midiOutLongMsg**, debe esperar hasta que el controlador de dispositivo finalice con el bloque de datos antes de liberarlo. Si va a enviar varios bloques de datos, debe supervisar la finalización de cada bloque de datos para saber cuándo enviar bloques adicionales. Para obtener información sobre las distintas técnicas para supervisar la finalización de bloques de datos, vea [Managing MIDI Data Blocks](managing-midi-data-blocks.md).

> [!Note]  
> Cualquier byte de estado de MIDI que no sea un mensaje en tiempo real del sistema finalizará un mensaje exclusivo del sistema. Si usa varios bloques de datos para enviar un único mensaje exclusivo del sistema, no envíe ningún mensaje MIDI que no sea mensajes del sistema en tiempo real entre bloques de datos.

 

 

 