---
description: Especifica el formato de salida del descodificador.
ms.assetid: fdccdbfa-2814-4d21-9a7f-4121b79718e6
title: Propiedad AVDecCommonOutputFormat (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 129f9a1171c5870eab243108fc0ed6992be4993b886cbd36d72fe91988f321b5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119586755"
---
# <a name="avdeccommonoutputformat-property"></a>Propiedad AVDecCommonOutputFormat

Especifica el formato de salida del descodificador.

Esta propiedad es de lectura y escritura.

## <a name="data-type"></a>Tipo de datos

**BSTR** (**VT \_ BSTR**)

## <a name="property-guid"></a>GUID de propiedad

**CODECAPI \_ AVDecCommonOutputFormat**

## <a name="property-value"></a>Valor de propiedad



| GUID                                                               | Descripción                                                                                                                                                                                                         |
|--------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CODECAPI \_ GUID \_ AVDecAudioOutputFormat \_ PCM                        | Audio PCM, con cualquier número de canales                                                                                                                                                                             |
| CodecAPI \_ GUID \_ AVDecAudioOutputFormat \_ PCM \_ Conchas            | Audio PCM estéreo, con la mezclada solo izquierda/derecha (Lo/Ro)                                                                                                                                                        |
| CODECAPI \_ GUID \_ AVDecAudioOutputFormat \_ PCM \_ Stereo \_ Auto          | Audio PCM estéreo, mediante la selección automática del modo de bajada estéreo (Lo/Ro o Lt/Rt). Puede usar este valor para los formatos de audio en los que el flujo de entrada define el modo de mezclación preferido, como Dolby AC-3. |
| CODECAPI \_ GUID \_ AVDecAudioOutputFormat \_ PCM \_ Stereo \_ MatrixEncoded | Audio PCM estéreo, mediante la mezcla estéreo codificada en matriz (Lt/Rt)                                                                                                                                                       |
| CODECAPI \_ GUID \_ AVDecAudioOutputFormat \_ SPDIF \_ Bitstream           | Secuencia de bits comprimida S/PDIF (formato de interfaz digital de Sony/Erc), tal como se define en IEC-60958                                                                                                                        |
| CODECAPI \_ GUID \_ AVDecAudioOutputFormat \_ SPDIF \_ PCM                 | S/PDIF PCM estéreo, tal como se define en IEC-60958                                                                                                                                                                          |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional aplicaciones \[ de escritorio \| para UWP\]<br/>                     |
| Servidor mínimo compatible<br/> | Windows aplicaciones de escritorio de UWP para 2000 \[ \| Server\]<br/>                           |
| Header<br/>                   | <dl> <dt>Codecapi.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Propiedades de la API de códec](codec-api-properties.md)
</dt> <dt>

[**ICodecAPI (interfaz)**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




