---
title: Uso de midiOutShortMsg para enviar mensajes INDIVIDUALES DE MIDI
description: Uso de midiOutShortMsg para enviar mensajes INDIVIDUALES DE MIDI
ms.assetid: 7a8f7c6c-28ac-4aa6-9073-969fc8e59f4e
keywords:
- Interfaz digital de instrumentar música (MIDI), enviar mensajes
- MIDI (Interfaz digital instrumenta instrumentable), envío de mensajes
- envío de mensajes MIDI
- Interfaz digital instrumentable (MIDI), función midiOutShortMsg
- FUNCIÓN MIDI (Interfaz digital de instrumentado),midiOutShortMsg
- función midiOutShortMsg
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 905b0ce924f9aebce67f515fc0714fdc855cbe33
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127245780"
---
# <a name="using-midioutshortmsg-to-send-individual-midi-messages"></a>Uso de midiOutShortMsg para enviar mensajes INDIVIDUALES DE MIDI

En el ejemplo siguiente se [**usa la función midiOutShortMsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutshortmsg) para enviar un evento MIDI especificado a un dispositivo de salida DE MIDI determinado:


```C++
UINT sendMIDIEvent(HMIDIOUT hmo, BYTE bStatus, BYTE bData1, 
    BYTE bData2) 
{ 
    union { 
        DWORD dwData; 
        BYTE bData[4]; 
    } u; 
 
    // Construct the MIDI message. 
 
    u.bData[0] = bStatus;  // MIDI status byte 
    u.bData[1] = bData1;   // first MIDI data byte 
    u.bData[2] = bData2;   // second MIDI data byte 
    u.bData[3] = 0; 
 
    // Send the message. 
    return midiOutShortMsg(hmo, u.dwData); 
} 
```



> [!Note]  
> Los controladores de salida de MIDI no son necesarios para comprobar los datos antes de enviarlos a un puerto de salida. Las aplicaciones deben asegurarse de que solo se envían datos válidos.

 

 

 