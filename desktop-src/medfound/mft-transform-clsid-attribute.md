---
description: Contiene el identificador de clase (CLSID) de una transformación de Media Foundation (MFT).
ms.assetid: 99ee6f50-1de7-41ea-be5b-135730138d5d
title: MFT_TRANSFORM_CLSID_Attribute atributo (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b5ca1aa6a9d7691200761509e1a5e407a6c7db6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001451"
---
# <a name="mft_transform_clsid_attribute-attribute"></a>\_Atributo de \_ atributo CLSID de transformación de MFT \_

Contiene el identificador de clase (CLSID) de una transformación de Media Foundation (MFT).

## <a name="data-type"></a>Tipo de datos

**GUID**

## <a name="getset"></a>Obtener o establecer

Para obtener este atributo, llame a [**IMFAttributes:: GetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid).

Para establecer este atributo, llame a [**IMFAttributes:: SetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid).

## <a name="remarks"></a>Observaciones

Este atributo se establece en los punteros [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) devueltos por la función [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) .

Este atributo lo usa internamente el objeto de activación cuando crea la MFT. Las aplicaciones no deben usar este CLSID directamente para crear la MFT, ya que es posible que el objeto de activación tenga que inicializar la MFT. Por lo tanto, para crear una instancia de MFT, llame a [**IMFActivate:: ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) en el objeto de activación.

Tenga en cuenta que la función [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) se comporta de forma diferente a la función [**MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) en este sentido. La función **MFTEnum** devuelve CLSIDs, que la aplicación pasa a la función **CoCreateInstance** . La función **MFTEnumEx** devuelve objetos de activación en lugar de CLSID.

La constante GUID para este atributo se exporta desde mfuuid. lib.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows 7 \|\]<br/>                                        |
| Servidor mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2008 R2 \|\]<br/>                           |
| Encabezado<br/>                   | <dl> <dt>Mftransform. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos de transformación](transform-attributes.md)
</dt> </dl>

 

 




