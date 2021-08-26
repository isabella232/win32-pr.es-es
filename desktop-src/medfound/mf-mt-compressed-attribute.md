---
description: Especifica para un tipo de medio si los datos multimedia están comprimidos.
ms.assetid: b44fb757-4390-4392-b1cb-37772b4ae3fb
title: MF_MT_COMPRESSED atributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: afea99ffb0c9f7f9f53fb6edd0b4b87b2ecd4ff4f451e5fd0e56d47a70aee994
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120060695"
---
# <a name="mf_mt_compressed-attribute"></a>Atributo \_ MF MT \_ COMPRESSED

Especifica para un tipo de medio si los datos multimedia están comprimidos.

## <a name="data-type"></a>Tipo de datos

**UINT32**

Tratar como un valor booleano.

## <a name="remarks"></a>Comentarios

Si este atributo es **TRUE**, el tipo de medio es un formato comprimido. De lo contrario, el tipo de medio está descomprimido o no se conoce el tipo de compresión.

No se garantiza que este atributo se establezca en **TRUE para** todos los formatos comprimidos, por lo que las aplicaciones generalmente no deben confiar en este atributo. La manera más confiable de determinar si un formato está comprimido es mantener una lista de formatos conocidos. Si una aplicación no reconoce un formato, como se especifica en el atributo [**MF \_ MT \_ SUBTYPE,**](mf-mt-subtype-attribute.md) no debe suponer nada sobre la compresión del formato.

Para determinar si un formato usa la compresión temporal (lo que significa que algunas muestras se calculan como diferencias de ejemplos anteriores), compruebe el atributo [**MF MT ALL SAMPLES \_ \_ \_ \_ INDEPENDENT.**](mf-mt-all-samples-independent-attribute.md)

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

[**ATTRIBUTEAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**ATTRIBUTEAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[Atributos de tipo multimedia](media-type-attributes.md)
</dt> </dl>

 

 




