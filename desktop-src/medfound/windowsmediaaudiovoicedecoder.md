---
description: El descodificador de voz de Windows Media Audio descodifica los flujos codificados por el codificador de Windows Media Audio Voice.
ms.assetid: 8bb5c8bd-949f-4faa-b679-8854f78076a4
title: Descodificador de Windows Media Audio Voice (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4565a511f2816d2914ec96f3ae89f3af5dd19016
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699554"
---
# <a name="windows-media-audio-voice-decoder"></a>Descodificador de Windows Media Audio Voice

El descodificador de voz de Windows Media Audio descodifica los flujos codificados por el [**codificador de Windows Media Audio Voice**](windowsmediaaudiovoiceencoder.md).

## <a name="class-identifier"></a>Identificador de clase

El identificador de clase (CLSID) para el descodificador de Windows Media Audio Voice se representa mediante la **constante \_ CWMSPDecMediaObject de CLSID**. Puede crear una instancia del descodificador de voz llamando a **CoCreateInstance**.

## <a name="input-formats"></a>Formatos de entrada

Windows Media Audio contenido codificado por voz se identifica mediante la etiqueta de formato 0x00A.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-----------------------------------------------------------------------------------------|
| Remoto<br/> | Windows XP, Windows Vista o Windows 7<br/>                                       |
| Encabezado<br/> | <dl> <dt>Wmcodecdsp. h</dt> </dl> |
| Archivo DLL<br/>    | <dl> <dt>Wmspdmod.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Objetos Codec](codecobjects.md)
</dt> <dt>

[Usar el códec Windows Media Audio Voice](usingthewindowsmediaaudio9voicecodec.md)
</dt> <dt>

[Codificador de voz Windows Media Audio](windowsmediaaudiovoiceencoder.md)
</dt> </dl>

 

 




