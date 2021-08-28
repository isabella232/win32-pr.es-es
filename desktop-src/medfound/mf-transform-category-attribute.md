---
description: Especifica la categoría de una transformación Media Foundation transformación (MFT).
ms.assetid: cebd64ea-b20f-4ccc-805f-0deab3096bc3
title: MF_TRANSFORM_CATEGORY_Attribute atributo (Mftransform.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66adac9b1b9f07b3053ff871a12d17163ae2b5f1a2ef644885b54cb8ed281437
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120113695"
---
# <a name="mf_transform_category_attribute-attribute"></a>Atributo MF \_ TRANSFORM \_ CATEGORY \_

Especifica la categoría de una transformación Media Foundation transformación (MFT).

## <a name="data-type"></a>Tipo de datos

**GUID**

Para obtener una lista de valores posibles, vea [**MFT \_ CATEGORY**](mft-category.md).

## <a name="getset"></a>Obtener o establecer

Para obtener este atributo, llame [**a IMFAttributes::GetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid).

Para establecer este atributo, llame [**a IMFAttributes::SetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid).

## <a name="remarks"></a>Comentarios

Este atributo se establece en los punteros [**DE TIPO IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) devueltos por la [**función MFTEnumEx.**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio para \| UWP\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Aplicaciones de escritorio para \[ UWP de Server 2008 R2 \|\]<br/>                           |
| Header<br/>                   | <dl> <dt>Mftransform.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Transformar atributos](transform-attributes.md)
</dt> </dl>

 

 




