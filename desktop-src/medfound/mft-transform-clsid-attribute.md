---
description: Contiene el identificador de clase (CLSID) de una Media Foundation transformación (MFT).
ms.assetid: 99ee6f50-1de7-41ea-be5b-135730138d5d
title: MFT_TRANSFORM_CLSID_Attribute atributo (Mftransform.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0122b783d8b321aa2a5c7788a589e19625b6a2bde8e37b0b659b0a1192f8c7a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118240203"
---
# <a name="mft_transform_clsid_attribute-attribute"></a>Atributo \_ \_ CLSID de MFT TRANSFORM \_

Contiene el identificador de clase (CLSID) de una Media Foundation transformación (MFT).

## <a name="data-type"></a>Tipo de datos

**GUID**

## <a name="getset"></a>Obtener o establecer

Para obtener este atributo, llame [**a IMFAttributes::GetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid).

Para establecer este atributo, llame [**a IMFAttributes::SetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid).

## <a name="remarks"></a>Comentarios

Este atributo se establece en los punteros [**DE TIPO IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) devueltos por la [**función MFTEnumEx.**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex)

El objeto de activación utiliza internamente este atributo cuando crea el MFT. Las aplicaciones no deben usar este CLSID directamente para crear el MFT, ya que es posible que el objeto de activación tenga que inicializar el MFT. Por lo tanto, para crear una instancia de MFT, llame a [**IMFActivate::ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) en el objeto de activación.

Tenga en cuenta [**que la función MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) se comporta de forma diferente a la función [**MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) en este sentido. La **función MFTEnum** devuelve CLID, que la aplicación pasa a la **función CoCreateInstance.** La **función MFTEnumEx** devuelve objetos de activación en lugar de CLID.

La constante GUID para este atributo se exporta desde mfuuid.lib.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio para \| UWP\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Aplicaciones de escritorio para \[ UWP de Server 2008 R2 \|\]<br/>                           |
| Header<br/>                   | <dl> <dt>Mftransform.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Transformar atributos](transform-attributes.md)
</dt> </dl>

 

 




