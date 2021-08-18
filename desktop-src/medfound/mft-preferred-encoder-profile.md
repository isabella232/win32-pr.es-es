---
description: Contiene las propiedades de configuración de un codificador.
ms.assetid: f9bd8a50-e43e-4668-86a0-c9d5f517f4cf
title: MFT_PREFERRED_ENCODER_PROFILE atributo (Mftransform.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85acf742e518d91c6512b2b887cca910c3b19d21180500bd1180e6972255e54f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119722510"
---
# <a name="mft_preferred_encoder_profile-attribute"></a>Atributo MFT \_ PREFERRED \_ ENCODER \_ PROFILE

Contiene las propiedades de configuración de un codificador.

## <a name="data-type"></a>Tipo de datos

**[**ATTRIBUTEAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) \* *_ almacenado como _* Iunknown\***

## <a name="getset"></a>Obtener o establecer

Para obtener este atributo, llame [**a IMFAttributes::GetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).

Para establecer este atributo, llame [**a IMFAttributes::SetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).

## <a name="applies-to"></a>Se aplica a

[**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate)

## <a name="remarks"></a>Comentarios

Este atributo se puede establecer en el objeto de activación devuelto por la [**función MFCreateTransformActivate.**](/windows/desktop/api/mftransform/nf-mftransform-mfcreatetransformactivate) El atributo solo se aplica cuando el objeto de activación está configurado para crear un codificador. El valor del atributo es un puntero a un almacén de atributos, que a su vez contiene propiedades para establecer en el codificador.

La constante GUID para este atributo se exporta desde mfuuid.lib.

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

[**MFCreateTransformActivate**](/windows/desktop/api/mftransform/nf-mftransform-mfcreatetransformactivate)
</dt> <dt>

[Transformar atributos](transform-attributes.md)
</dt> </dl>

 

 




