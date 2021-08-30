---
description: Contiene el valor de meritorio de un códec de hardware.
ms.assetid: 1df40a42-4c02-473f-a87f-2ae2d42e4f4e
title: MFT_CODEC_MERIT_Attribute atributo (Mftransform.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d6b79579b20eaee3fb933cb0eb430cf841b9242f411d79b8a3ba5134ba58790
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119887515"
---
# <a name="mft_codec_merit_attribute-attribute"></a>Atributo ATTRIBUTE \_ DE CODEC \_ DE MFT \_

Contiene el valor de meritorio de un códec de hardware.

## <a name="data-type"></a>Tipo de datos

**UINT32**

## <a name="getset"></a>Obtener o establecer

Para obtener este atributo, llame [**a IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Para establecer este atributo, llame [**a IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="remarks"></a>Comentarios

Este atributo se establece en el objeto de activación para una transformación de Media Foundation (MFT) que representa un códec de hardware. El valor del atributo es el valor de valor del códec.

Este atributo controla el orden en que la función [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) enumera los códecs, si se establece la marca **\_ \_ \_ SORTANDFILTER de MFT ENUM FLAG.** Las MTA con un valor de meritorio aparecen más arriba en la lista que otras MTA.

Este atributo no contiene un valor de confianza. Para comprobar el valor de meritorio real del códec, llame a la [**función MFGetMFTMerit.**](/windows/desktop/api/mfapi/nf-mfapi-mfgetmftmerit)

Si el valor del atributo MFT CODEC ATTRIBUTE no coincide con el valor de meritorio recuperado por MFGetMFTMerit, se produce un error en el método \_ \_ \_ [**IMFActivate::ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) [](/windows/desktop/api/mfapi/nf-mfapi-mfgetmftmerit)y devuelve **MF E INVALID \_ \_ \_ \_ CODECATTRIBUTE**.

La constante GUID para este atributo se exporta desde mfuuid.lib.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio \| para UWP\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Aplicaciones de escritorio para \[ UWP de Server 2008 R2 \|\]<br/>                           |
| Header<br/>                   | <dl> <dt>Mftransform.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Transformar atributos](transform-attributes.md)
</dt> </dl>

 

 




