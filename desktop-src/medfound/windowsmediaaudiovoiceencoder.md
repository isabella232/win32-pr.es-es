---
description: El Windows Media Audio Voice está optimizado para codificar la voz humana con relaciones de compresión altas. Este es el codificador preferido para las secuencias que constan principalmente de palabras habladas.
ms.assetid: b3cfa845-4fe1-405f-88e5-4555398639ef
title: Windows Codificador de voz de audio multimedia (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c107e4e09309ff0ed56e899d3ec2cd0c9d372261b48231b4530ed3222ee3a68
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119462435"
---
# <a name="windows-media-audio-voice-encoder"></a>Windows Codificador de voz de audio multimedia

El Windows Media Audio Voice está optimizado para codificar la voz humana con relaciones de compresión altas. Este es el codificador preferido para las secuencias que constan principalmente de palabras habladas.

## <a name="class-identifier"></a>Identificador de clase

El identificador de clase (CLSID) del codificador Windows Media Audio Voice se representa mediante la constante **CLSID \_ CWMSPEncMediaObject2**. Puede crear una instancia del codificador de voz llamando a **CoCreateInstance**.

## <a name="output-formats"></a>Formatos de salida

Windows El contenido codificado de Media Audio Voice se identifica mediante la etiqueta de formato 0x00A.

## <a name="encoder-properties"></a>Propiedades del codificador

El Windows Media Audio Voice admite las siguientes propiedades.



<table>
<thead>
<tr class="header">
<th>Propiedad</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="mfpkey-wmavoice-enc-bufferwindowproperty.md">MFPKEY_WMAVOICE_ENC_BufferWindow</a></td>
<td>Especifica la ventana de búfer, en milisegundos, que se usa para el códec de voz.<br/> <dl> Windows XP y versiones posteriores.<br />
De solo escritura.<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-wmavoice-enc-decoderdelayproperty.md">MFPKEY_WMAVOICE_ENC_DecoderDelay</a></td>
<td>Especifica la latencia del codificador en las unidades de paquete.<br/> <dl> Windows XP y versiones posteriores.<br />
De solo escritura.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-wmavoice-enc-edlproperty.md">MFPKEY_WMAVOICE_ENC_EDL</a></td>
<td>Especifica las partes del contenido que el códec de voz codificará como música.<br/> <dl> Windows XP y versiones posteriores.<br />
Lectura/escritura<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="mfpkey-wmavoice-enc-musicspeechclassmodeproperty.md">MFPKEY_WMAVOICE_ENC_MusicSpeechClassMode</a></td>
<td>Especifica el modo del códec de voz.<br/> <dl> Windows XP y versiones posteriores.<br />
Lectura/escritura<br />
</dl></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-----------------------------------------------------------------------------------------|
| Cliente<br/> | Windows XP, Windows Vista o Windows 7<br/>                                       |
| Header<br/> | <dl> <dt>Wmcodecdsp.h</dt> </dl> |
| Archivo DLL<br/>    | <dl> <dt>Wmspdmoe.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Objetos de códec](codecobjects.md)
</dt> <dt>

[Uso del códec Windows media audio voice](usingthewindowsmediaaudio9voicecodec.md)
</dt> </dl>

 

 




