---
description: Contiene el identificador de clase (CLSID) de una Media Foundation transformación (MFT).
ms.assetid: 99ee6f50-1de7-41ea-be5b-135730138d5d
title: MFT_TRANSFORM_CLSID_Attribute atributo (Mftransform.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b5ca1aa6a9d7691200761509e1a5e407a6c7db6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127363742"
---
# <a name="mft_transform_clsid_attribute-attribute"></a>Atributo \_ CLSID de transformación de MFT \_ \_

Contiene el identificador de clase (CLSID) de una Media Foundation transformación (MFT).

## <a name="data-type"></a>Tipo de datos

**GUID**

## <a name="getset"></a>Obtener o establecer

Para obtener este atributo, llame [**aATTRIBUTEAttributes::GetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid).

Para establecer este atributo, llame [**aATTRIBUTEAttributes::SetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid).

## <a name="remarks"></a>Observaciones

Este atributo se establece en los punteros [**DE LAACTIVATE**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) devueltos por la [**función MFTEnumEx.**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex)

El objeto de activación utiliza internamente este atributo cuando crea el MFT. Las aplicaciones no deben usar este CLSID directamente para crear el MFT, ya que es posible que el objeto de activación tenga que inicializar el MFT. Por lo tanto, para crear una instancia de MFT, llame [**a RECORDSETActivate::ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) en el objeto de activación.

Tenga en cuenta [**que la función MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) se comporta de forma diferente que la [**función MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) en este sentido. La **función MFTEnum** devuelve CLSID, que la aplicación pasa a la **función CoCreateInstance.** La **función MFTEnumEx** devuelve objetos de activación en lugar de CLSID.

La constante GUID para este atributo se exporta desde mfuuid.lib.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio aplicaciones para \| UWP\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Aplicaciones de escritorio para \[ UWP de Server 2008 R2 \|\]<br/>                           |
| Encabezado<br/>                   | <dl> <dt>Mftransform.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Transformar atributos](transform-attributes.md)
</dt> </dl>

 

 




