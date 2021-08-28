---
description: Especifica el modo del códec de voz.
ms.assetid: 8425cdab-e43c-41ca-9c20-09ab6a5f06f4
title: MFPKEY_WMAVOICE_ENC_MusicSpeechClassMode (Propiedad, Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 303a86adbf9c443149ff78a47d19922284e38d2c0aeb56dcc13a74ca20cd54a1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120113125"
---
# <a name="mfpkey_wmavoice_enc_musicspeechclassmode-property"></a>Propiedad MFPKEY \_ WMAVOICE \_ ENC \_ MusicSpeechClassMode

Especifica el modo del códec de voz.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

g \_ wszWMACModeSpeechClassMode

## <a name="data-type"></a>Tipo de datos

VT \_ I4

## <a name="default-value"></a>Valor predeterminado

1

## <a name="remarks"></a>Comentarios

El valor 1 informa al códec de que el contenido es de solo voz, un valor de 2 hace que el códec determine el modo automáticamente y cualquier otro valor informa al códec de que use el modo de música.

Si el modo automático no codifica correctamente la voz mixta y la música, puede especificar la codificación para secciones individuales del archivo mediante la propiedad [ \_ \_ \_ EDL MFPKEY WMAVOICE ENC.](mfpkey-wmavoice-enc-edlproperty.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP \[ solo aplicaciones de escritorio\]<br/>                                             |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Media Foundation propiedades](media-foundation-properties.md)
</dt> </dl>

 

 




