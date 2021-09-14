---
description: Especifica para un tipo de medio si los datos multimedia están comprimidos.
ms.assetid: b44fb757-4390-4392-b1cb-37772b4ae3fb
title: MF_MT_COMPRESSED atributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d049795f09845b5d32daf29ef033ab2e4b23007f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127364054"
---
# <a name="mf_mt_compressed-attribute"></a>Atributo MF \_ MT \_ COMPRESSED

Especifica para un tipo de medio si los datos multimedia están comprimidos.

## <a name="data-type"></a>Tipo de datos

**UINT32**

Tratar como un valor booleano.

## <a name="remarks"></a>Observaciones

Si este atributo es **TRUE,** el tipo de medio es un formato comprimido. De lo contrario, el tipo de medio está descomprimido o no se conoce el tipo de compresión.

No se garantiza que este atributo se establezca en **TRUE** para todos los formatos comprimidos, por lo que las aplicaciones generalmente no deben confiar en este atributo. La manera más confiable de determinar si un formato está comprimido es mantener una lista de formatos conocidos. Si una aplicación no reconoce un formato, como se especifica en el atributo [**MF \_ MT \_ SUBTYPE,**](mf-mt-subtype-attribute.md) no debe suponer nada sobre la compresión del formato.

Para determinar si un formato usa la compresión temporal (lo que significa que algunas muestras se calculan como deltas de ejemplos anteriores), compruebe el atributo [**MF MT ALL SAMPLES \_ \_ \_ \_ INDEPENDENT.**](mf-mt-all-samples-independent-attribute.md)

La constante GUID para este atributo se exporta desde mfuuid.lib.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Aplicaciones de escritorio de Vista \[ \| para aplicaciones para UWP\]<br/>                              |
| Servidor mínimo compatible<br/> | Windows Aplicaciones de escritorio de Server 2008 \[ \| para aplicaciones para UWP\]<br/>                        |
| Encabezado<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**ATTRIBUTEAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**ATTRIBUTEAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[Atributos de tipo de medio](media-type-attributes.md)
</dt> </dl>

 

 




