---
title: Uso de midiOutShortMsg para enviar mensajes MIDI individuales
description: Uso de midiOutShortMsg para enviar mensajes MIDI individuales
ms.assetid: 7a8f7c6c-28ac-4aa6-9073-969fc8e59f4e
keywords:
- Interfaz digital de instrumentos musicales (MIDI), enviar mensajes
- MIDI (interfaz digital de instrumentos musicales), enviar mensajes
- envío de mensajes MIDI
- Interfaz digital de instrumentos musicales (MIDI), función midiOutShortMsg
- MIDI (interfaz digital de instrumentos musicales), función midiOutShortMsg
- midiOutShortMsg función)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 905b0ce924f9aebce67f515fc0714fdc855cbe33
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104487650"
---
# <a name="using-midioutshortmsg-to-send-individual-midi-messages"></a>Uso de midiOutShortMsg para enviar mensajes MIDI individuales

En el ejemplo siguiente se usa la función [**midiOutShortMsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutshortmsg) para enviar un evento MIDI especificado a un dispositivo de salida MIDI determinado:


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
> No es necesario que los controladores de salida MIDI comprueben los datos antes de enviarlos a un puerto de salida. Las aplicaciones deben asegurarse de que solo se envíen los datos válidos.

 

 

 