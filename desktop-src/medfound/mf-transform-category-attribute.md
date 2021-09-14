---
description: Especifica la categoría de una transformación Media Foundation transformación (MFT).
ms.assetid: cebd64ea-b20f-4ccc-805f-0deab3096bc3
title: MF_TRANSFORM_CATEGORY_Attribute atributo (Mftransform.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd3c64fd5e19bba10646957e7c247294b6d82a97
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127363886"
---
# <a name="mf_transform_category_attribute-attribute"></a>Atributo MF \_ TRANSFORM \_ CATEGORY \_

Especifica la categoría de una transformación Media Foundation transformación (MFT).

## <a name="data-type"></a>Tipo de datos

**GUID**

Para obtener una lista de los valores posibles, vea [**CATEGORÍA DE MFT \_**](mft-category.md).

## <a name="getset"></a>Obtener o establecer

Para obtener este atributo, llame [**aATTRIBUTEAttributes::GetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid).

Para establecer este atributo, llame [**aATTRIBUTEAttributes::SetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid).

## <a name="remarks"></a>Observaciones

Este atributo se establece en los punteros [**DE LAACTIVATE**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) devueltos por la [**función MFTEnumEx.**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio \| para UWP\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Aplicaciones de escritorio para \[ UWP de Server 2008 R2 \|\]<br/>                           |
| Encabezado<br/>                   | <dl> <dt>Mftransform.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Transformar atributos](transform-attributes.md)
</dt> </dl>

 

 




