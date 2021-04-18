---
description: El codificador de Windows Media Audio Voice está optimizado para codificar las proporciones de la voz humana a alta compresión. Este es el codificador preferido para las secuencias que se componen principalmente de palabras pronunciadas.
ms.assetid: b3cfa845-4fe1-405f-88e5-4555398639ef
title: Codificador de Windows Media Audio Voice (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bef79f2c3d0c48fee8ec33e08bfb9fdf21c3656b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700208"
---
# <a name="windows-media-audio-voice-encoder"></a>Codificador de voz Windows Media Audio

El codificador de Windows Media Audio Voice está optimizado para codificar las proporciones de la voz humana a alta compresión. Este es el codificador preferido para las secuencias que se componen principalmente de palabras pronunciadas.

## <a name="class-identifier"></a>Identificador de clase

El identificador de clase (CLSID) del codificador de Windows Media Audio Voice se representa mediante la constante **\_ CWMSPEncMediaObject2 de CLSID**. Puede crear una instancia del codificador de voz llamando a **CoCreateInstance**.

## <a name="output-formats"></a>Formatos de salida

Windows Media Audio contenido codificado por voz se identifica mediante la etiqueta de formato 0x00A.

## <a name="encoder-properties"></a>Propiedades del codificador

El codificador de Windows Media Audio Voice admite las siguientes propiedades.



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
<td>Especifica la latencia del codificador en unidades de paquetes.<br/> <dl> Windows XP y versiones posteriores.<br />
De solo escritura.<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="mfpkey-wmavoice-enc-edlproperty.md">MFPKEY_WMAVOICE_ENC_EDL</a></td>
<td>Especifica las partes de contenido que el códec de voz debe codificar como música.<br/> <dl> Windows XP y versiones posteriores.<br />
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
| Remoto<br/> | Windows XP, Windows Vista o Windows 7<br/>                                       |
| Encabezado<br/> | <dl> <dt>Wmcodecdsp. h</dt> </dl> |
| Archivo DLL<br/>    | <dl> <dt>Wmspdmoe.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Objetos Codec](codecobjects.md)
</dt> <dt>

[Usar el códec Windows Media Audio Voice](usingthewindowsmediaaudio9voicecodec.md)
</dt> </dl>

 

 




