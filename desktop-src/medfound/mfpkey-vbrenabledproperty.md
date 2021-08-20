---
description: Especifica si el codificador usa la codificación de velocidad de bits variable (VBR).
ms.assetid: e6826802-99b7-4a38-9b58-8a9cb8b753fb
title: MFPKEY_VBRENABLED (Propiedad, Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7346e665c05ee9246371946e312f340148a455a3bdc613437383de1055b911d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117873009"
---
# <a name="mfpkey_vbrenabled-property"></a>Propiedad MFPKEY \_ VBRENABLED

Especifica si el codificador usa la codificación de velocidad de bits variable (VBR). Lectura y escritura.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

**g \_ wszWMVCVBREnabled**, **g \_ wszWMCPAudioVBRSupported**

## <a name="data-type"></a>Tipo de datos

**VT \_ BOOL**

## <a name="default-value"></a>Valor predeterminado

**VARIANT \_ FALSE**

## <a name="remarks"></a>Comentarios

Este valor debe establecerse en **VARIANT \_ TRUE** para cualquiera de las otras propiedades de VBR que va a usar el códec.

Después de establecer este valor en **VARIANT \_ TRUE** en el codificador de audio, los tipos de salida recuperados mediante el método [**IMediaObject::GetOutputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getoutputtype) son tipos VBR.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP \[ solo aplicaciones de escritorio\]<br/>                                             |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**MFPKEY \_ CONSTRAIN \_ ENUMERATED \_ VBRQUALITY**](mfpkey-constrain-enumerated-vbrqualityproperty.md)
</dt> <dt>

[**\_VBRQUALITY DESEADO DE MFPKEY \_**](mfpkey-desired-vbrqualityproperty.md)
</dt> <dt>

[Media Foundation propiedades](media-foundation-properties.md)
</dt> </dl>

 

 
