---
description: Especifica para un tipo de medio si se comprimen los datos multimedia.
ms.assetid: b44fb757-4390-4392-b1cb-37772b4ae3fb
title: MF_MT_COMPRESSED atributo (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d049795f09845b5d32daf29ef033ab2e4b23007f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104544342"
---
# <a name="mf_mt_compressed-attribute"></a>\_ \_ Atributo comprimido MF MT

Especifica para un tipo de medio si se comprimen los datos multimedia.

## <a name="data-type"></a>Tipo de datos

**UINT32**

Trata como un valor booleano.

## <a name="remarks"></a>Observaciones

Si este atributo es **true**, el tipo de medio es un formato comprimido. De lo contrario, el tipo de medio se descomprime o no se conoce el tipo de compresión.

No se garantiza que este atributo esté establecido en **true** para todos los formatos comprimidos, por lo que las aplicaciones no deben confiar normalmente en este atributo. La forma más confiable de determinar si un formato está comprimido es mantener una lista de formatos conocidos. Si una aplicación no reconoce un formato, tal y como se especifica en el atributo [**MF \_ MT \_ SubType**](mf-mt-subtype-attribute.md) , no debe suponer nada sobre la compresión del formato.

Para determinar si un formato utiliza la compresión temporal (lo que significa que algunos ejemplos se calculan como deltas de los ejemplos anteriores), compruebe el atributo [**\_ independiente MF MT \_ All \_ Samples \_**](mf-mt-all-samples-independent-attribute.md) .

La constante GUID para este atributo se exporta desde mfuuid. lib.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows Vista \|\]<br/>                              |
| Servidor mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2008 \|\]<br/>                        |
| Encabezado<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**IMFAttributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[Atributos de tipo de medio](media-type-attributes.md)
</dt> </dl>

 

 




