---
description: Especifica el formato de salida del descodificador.
ms.assetid: fdccdbfa-2814-4d21-9a7f-4121b79718e6
title: Propiedad AVDecCommonOutputFormat (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3b69c536b3c9f1bf75e2a5741d0cdd16569b3dd8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127162142"
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
| CodecAPI \_ GUID \_ AVDecAudioOutputFormat \_ PCM \_ Alerones de PCM            | Audio PCM estéreo, con la mezcla a la izquierda o solo a la derecha (Lo/Ro)                                                                                                                                                        |
| CODECAPI \_ GUID \_ AVDecAudioOutputFormat \_ PCM \_ Stereo \_ Auto          | Audio PCM estéreo, mediante la selección automática del modo de mezclase estéreo (Lo/Ro o Lt/Rt). Puede usar este valor para los formatos de audio en los que el flujo de entrada define el modo de mezcla abajo preferido, como Dolby AC-3. |
| CODECAPI \_ GUID \_ AVDecAudioOutputFormat \_ PCM \_ Stereo \_ MatrixEncoded | Audio PCM estéreo, mediante la mezcla estéreo codificada en matriz (Lt/Rt)                                                                                                                                                       |
| CODECAPI \_ GUID \_ AVDecAudioOutputFormat \_ SPDIF \_ Bitstream           | Secuencia de bits comprimida de S/PDIF (formato de interfaz digital DeBas/Según se define en IEC-60958)                                                                                                                        |
| CODECAPI \_ GUID \_ AVDecAudioOutputFormat \_ SPDIF \_ PCM                 | S/PDIF PCM estéreo, tal como se define en IEC-60958                                                                                                                                                                          |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional aplicaciones \[ de escritorio \| para UWP\]<br/>                     |
| Servidor mínimo compatible<br/> | Windows aplicaciones de escritorio de UWP para 2000 \[ \| Server\]<br/>                           |
| Encabezado<br/>                   | <dl> <dt>Codecapi.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades de la API de códec](codec-api-properties.md)
</dt> <dt>

[**ICodecAPI (interfaz)**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




