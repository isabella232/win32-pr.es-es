---
description: Especifica el modo del códec de voz.
ms.assetid: 8425cdab-e43c-41ca-9c20-09ab6a5f06f4
title: Propiedad MFPKEY_WMAVOICE_ENC_MusicSpeechClassMode (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9776c76f2a8863afe73626f5a2940de2c0ccb7cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696686"
---
# <a name="mfpkey_wmavoice_enc_musicspeechclassmode-property"></a>MFPKEY \_ WMAVOICE \_ enc \_ MusicSpeechClassMode propiedad

Especifica el modo del códec de voz.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

g \_ wszWMACMusicSpeechClassMode

## <a name="data-type"></a>Tipo de datos

VT \_ I4

## <a name="default-value"></a>Valor predeterminado

1

## <a name="remarks"></a>Observaciones

Un valor de 1 informa al códec de que el contenido es de solo voz, un valor de 2 tiene el códec determina el modo automáticamente y cualquier otro valor informa al códec de que use el modo de música.

Si el modo automático no está codificando voz mixta y música correctamente, puede especificar la codificación para secciones individuales del archivo mediante la propiedad [MFPKEY \_ WMAVOICE \_ enc \_ EDL](mfpkey-wmavoice-enc-edlproperty.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                             |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                    |
| Encabezado<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Propiedades de Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 




