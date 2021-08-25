---
description: Especifica si el cargador de topologías cambiará los tipos de medios en una Media Foundation transformación (MFT). Normalmente, las aplicaciones no usan este atributo.
ms.assetid: 96a99f35-f9db-407e-a4e3-7adc3caccb19
title: MF_ACTIVATE_MFT_LOCKED atributo (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 445447af46e1ce1da25aaa075dd4490d1210c1d01b2e7717829d2672dc74701f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120060915"
---
# <a name="mf_activate_mft_locked-attribute"></a>Atributo \_ MF ACTIVATE \_ MFT \_ LOCKED

Especifica si el cargador de topologías cambiará los tipos de medios en una Media Foundation transformación (MFT). Normalmente, las aplicaciones no usan este atributo.

## <a name="data-type"></a>Tipo de datos

**UINT32**

Tratar como un valor booleano.

## <a name="remarks"></a>Comentarios

Si el valor de este atributo es distinto de cero, el cargador de topologías no cambiará los tipos de medios en el MFT. El cargador de topologías establece este atributo después de cargar la topología.

La constante GUID para este atributo se exporta desde mfuuid.lib.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                     |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                               |
| Header<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**ATTRIBUTEAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**ATTRIBUTEAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[Transformar atributos](transform-attributes.md)
</dt> </dl>

 

 




