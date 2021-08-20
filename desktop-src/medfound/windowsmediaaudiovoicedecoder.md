---
description: El Windows media audio voice descodifica las secuencias codificadas por el codificador de voz Windows media audio.
ms.assetid: 8bb5c8bd-949f-4faa-b679-8854f78076a4
title: Windows Descodificador de voz de audio multimedia (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae2aaae504cd0909b4c7fc86d84e00d43492d695f86ff71c487f3b56ee81190f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118057426"
---
# <a name="windows-media-audio-voice-decoder"></a>Windows Descodificador de voz de audio multimedia

El Windows media audio voice descodifica las secuencias codificadas por el codificador de voz [**de Windows**](windowsmediaaudiovoiceencoder.md)media audio .

## <a name="class-identifier"></a>Identificador de clase

El identificador de clase (CLSID) del descodificador Windows Media Audio Voice se representa mediante la constante **CLSID \_ CWMSPDecMediaObject**. Puede crear una instancia del descodificador de voz llamando a **CoCreateInstance**.

## <a name="input-formats"></a>Formatos de entrada

Windows El contenido codificado de Media Audio Voice se identifica mediante la etiqueta de formato 0x00A.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|-----------------------------------------------------------------------------------------|
| Cliente<br/> | Windows XP, Windows Vista o Windows 7<br/>                                       |
| Header<br/> | <dl> <dt>Wmcodecdsp.h</dt> </dl> |
| Archivo DLL<br/>    | <dl> <dt>Wmspdmod.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Objetos de códec](codecobjects.md)
</dt> <dt>

[Uso del códec Windows media audio voice](usingthewindowsmediaaudio9voicecodec.md)
</dt> <dt>

[Windows Codificador de voz de audio multimedia](windowsmediaaudiovoiceencoder.md)
</dt> </dl>

 

 




