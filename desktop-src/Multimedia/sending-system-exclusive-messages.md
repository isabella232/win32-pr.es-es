---
title: Envío de System-Exclusive mensajes
description: Envío de System-Exclusive mensajes
ms.assetid: 2bb95e4e-004e-46c8-9c56-25436fcc7f6c
keywords:
- Interfaz digital de instrumentar música (MIDI), enviar mensajes
- MIDI (Interfaz digital de instrumentar música), enviar mensajes
- reproducir archivos MIDI, enviar mensajes
- envío de mensajes MIDI
- Interfaz digital de instrumentar música (MIDI), mensajes exclusivos del sistema
- MIDI (Interfaz digital de instrumentar música), mensajes exclusivos del sistema
- reproducir archivos MIDI, mensajes exclusivos del sistema
- mensajes MIDI exclusivos del sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 073ebc0fe111ef19e2edb098e6bdb170c13abc3e
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124370927"
---
# <a name="sending-system-exclusive-messages"></a>Envío de System-Exclusive mensajes

Los mensajes exclusivos del sistema DE MIDI son los únicos mensajes MIDI que no caben en un solo valor doubleword. Los mensajes exclusivos del sistema pueden tener cualquier longitud. Windows proporciona la [**función midiOutLongMsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutlongmsg) para enviar mensajes exclusivos del sistema a dispositivos de salida DE MIDI. Para especificar bloques de datos exclusivos del sistema de MIDI, use la [**estructura MIDIHDR.**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr)

Después de enviar un bloque de datos exclusivo del sistema mediante **midiOutLongMsg**, debe esperar hasta que el controlador del dispositivo finalice con el bloque de datos antes de liberarlo. Si va a enviar varios bloques de datos, debe supervisar la finalización de cada bloque de datos para saber cuándo enviar bloques adicionales. Para obtener información sobre las distintas técnicas para supervisar la finalización de bloques de datos, vea [Managing MIDI Data Blocks](managing-midi-data-blocks.md).

> [!Note]  
> Cualquier byte de estado DE MIDI que no sea un mensaje en tiempo real del sistema finalizará un mensaje exclusivo del sistema. Si usa varios bloques de datos para enviar un único mensaje exclusivo del sistema, no envíe ningún mensaje MIDI que no sea mensajes en tiempo real del sistema entre bloques de datos.

 

 

 