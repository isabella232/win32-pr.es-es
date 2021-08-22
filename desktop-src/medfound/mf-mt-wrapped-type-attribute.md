---
description: Contiene un tipo de medio que se ha encapsulado en otro tipo de medio.
ms.assetid: 3bd94523-0206-44d8-83a2-e569e4ab7815
title: MF_MT_WRAPPED_TYPE atributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 69ec0b86f985e40f808862091d3ea4506d8c456ffbf05ebd749f15e8ba8bf0c4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119356365"
---
# <a name="mf_mt_wrapped_type-attribute"></a>Atributo MF \_ MT \_ WRAPPED \_ TYPE

Contiene un tipo de medio que se ha encapsulado en otro tipo de medio.

## <a name="data-type"></a>Tipo de datos

Byte array

## <a name="remarks"></a>Observaciones

Este atributo se usa en la [**función MFWrapMediaType,**](/windows/desktop/api/mfapi/nf-mfapi-mfwrapmediatype) que encapsula un tipo de medio dentro de otro tipo de medio.

La [**función MFWrapMediaType**](/windows/desktop/api/mfapi/nf-mfapi-mfwrapmediatype) hace lo siguiente:

1.  Convierte el tipo de medio original en una matriz binaria.
2.  Establece el **atributo MF MT WRAPPED \_ \_ \_ TYPE** en el nuevo tipo de medio. El valor del atributo es la matriz binaria.

Normalmente, las aplicaciones no usan este atributo directamente. Para desencapsular el tipo de medio original, llame [**a MFUnwrapMediaType**](/windows/desktop/api/mfapi/nf-mfapi-mfunwrapmediatype).

La constante GUID para este atributo se exporta desde mfuuid.lib.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Aplicaciones de escritorio de Vista \[ \| para aplicaciones para UWP\]<br/>                              |
| Servidor mínimo compatible<br/> | Windows Aplicaciones de escritorio de Server 2008 \[ \| aplicaciones para UWP\]<br/>                        |
| Header<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**ATTRIBUTEAttributes::GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[**ATTRIBUTEAttributes::SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[Atributos de tipo multimedia](media-type-attributes.md)
</dt> </dl>

 

 




