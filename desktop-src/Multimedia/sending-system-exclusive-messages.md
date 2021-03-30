---
title: Envío de mensajes de System-Exclusive
description: Envío de mensajes de System-Exclusive
ms.assetid: 2bb95e4e-004e-46c8-9c56-25436fcc7f6c
keywords:
- Interfaz digital de instrumentos musicales (MIDI), enviar mensajes
- MIDI (interfaz digital de instrumentos musicales), enviar mensajes
- reproducir archivos MIDI, enviar mensajes
- envío de mensajes MIDI
- Interfaz digital de instrumentos musicales (MIDI), mensajes exclusivos del sistema
- MIDI (interfaz digital de instrumentos musicales), mensajes exclusivos del sistema
- reproducir archivos MIDI, mensajes exclusivos del sistema
- mensajes MIDI exclusivos del sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 073ebc0fe111ef19e2edb098e6bdb170c13abc3e
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103904517"
---
# <a name="sending-system-exclusive-messages"></a>Envío de mensajes de System-Exclusive

Los mensajes exclusivos del sistema MIDI son los únicos mensajes MIDI que no caben en un único valor de palabra. Los mensajes exclusivos del sistema pueden tener cualquier longitud. Windows proporciona la función [**midiOutLongMsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutlongmsg) para enviar mensajes exclusivos del sistema a dispositivos de salida MIDI. Para especificar los bloques de datos exclusivos del sistema MIDI, use la estructura [**MIDIHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) .

Después de enviar un bloque de datos exclusivo del sistema mediante **midiOutLongMsg**, debe esperar hasta que el controlador de dispositivo termine con el bloque de datos antes de liberarlo. Si va a enviar varios bloques de datos, debe supervisar la finalización de cada bloque de datos para saber cuándo enviar bloques adicionales. Para obtener información sobre las distintas técnicas para supervisar la finalización de bloque de datos, vea [administrar bloques de datos MIDI](managing-midi-data-blocks.md).

> [!Note]  
> Cualquier byte de estado de MIDI que no sea un mensaje en tiempo real del sistema finalizará un mensaje exclusivo del sistema. Si está utilizando varios bloques de datos para enviar un único mensaje exclusivo del sistema, no envíe mensajes MIDI que no sean mensajes en tiempo real del sistema entre bloques de datos.

 

 

 