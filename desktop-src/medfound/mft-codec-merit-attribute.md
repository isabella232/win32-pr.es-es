---
description: Contiene el valor de la propiedad de un códec de hardware.
ms.assetid: 1df40a42-4c02-473f-a87f-2ae2d42e4f4e
title: MFT_CODEC_MERIT_Attribute atributo (Mftransform.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 74745244824bc766d0f7c1e691cb5f176d1da6a8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127468600"
---
# <a name="mft_codec_merit_attribute-attribute"></a>Atributo \_ ATTRIBUTE DE CÓDEC DE MFT \_ \_

Contiene el valor de la propiedad de un códec de hardware.

## <a name="data-type"></a>Tipo de datos

**UINT32**

## <a name="getset"></a>Obtener o establecer

Para obtener este atributo, llame [**aATTRIBUTEAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Para establecer este atributo, llame [**aATTRIBUTEAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="remarks"></a>Observaciones

Este atributo se establece en el objeto de activación para una Media Foundation transformación (MFT) que representa un códec de hardware. El valor del atributo es el valor de merececión del códec.

Este atributo controla el orden en el que la función [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) enumera códecs, si se establece la marca **\_ \_ \_ SORTANDFILTER de MFT ENUM FLAG.** Las MTA con un valor de valor de puntuación aparecen más arriba en la lista que otras MTA.

Este atributo no contiene un valor de confianza. Para comprobar el valor real del valor de la confiditud del códec, llame a la [**función MFGetMFTMerit.**](/windows/desktop/api/mfapi/nf-mfapi-mfgetmftmerit)

Si el valor del atributo ATTRIBUTE DE CÓDEC DE MFT NO coincide con el valor de crédito recuperado por \_ \_ \_ [**MFGetMFTMerit,**](/windows/desktop/api/mfapi/nf-mfapi-mfgetmftmerit)el método [**MFActivate::ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) **\_ \_ \_ \_** produce un error y devuelve MF E INVALID CODEC CONDENS .

La constante GUID para este atributo se exporta desde mfuuid.lib.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio aplicaciones para \| UWP\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Aplicaciones de escritorio para \[ UWP de Server 2008 R2 \|\]<br/>                           |
| Encabezado<br/>                   | <dl> <dt>Mftransform.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Transformar atributos](transform-attributes.md)
</dt> </dl>

 

 




