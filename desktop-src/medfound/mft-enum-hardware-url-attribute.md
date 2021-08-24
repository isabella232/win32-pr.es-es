---
description: Contiene el vínculo simbólico para una transformación de Media Foundation basada en hardware (MFT).
ms.assetid: 7e153051-a167-4ff7-8178-b290d8a1345e
title: MFT_ENUM_HARDWARE_URL_Attribute atributo (Mftransform.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7119ea4bde7900087f706cb6fbc77c845721debab54dfa05b48f5c0094b1e29e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119722593"
---
# <a name="mft_enum_hardware_url_attribute-attribute"></a>Atributo MFT \_ ENUM \_ HARDWARE URL \_ \_ Attribute

Contiene el vínculo simbólico para una transformación de Media Foundation basada en hardware (MFT).

## <a name="data-type"></a>Tipo de datos

**Wchar\***

## <a name="getset"></a>Obtener o establecer

Para obtener este atributo, llame [**a IMFAttributes::GetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).

Para establecer este atributo, llame [**a IMFAttributes::SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).

## <a name="remarks"></a>Comentarios

Este atributo es compatible con las MTA basadas en hardware. El valor del atributo es el vínculo simbólico para el controlador de dispositivo. Este atributo también se establece en los punteros [**MFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) asignados por la función [**MFTEnumEx,**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) cuando esos punteros representan MFT basados en hardware.

El vínculo simbólico debe considerarse una cadena opaca. Para obtener el nombre para mostrar de un dispositivo, consulte el [atributo MFT \_ FRIENDLY \_ NAME.](mft-friendly-name-attribute.md)

Los MTA de software no deben tener este atributo establecido.

La constante GUID para este atributo se exporta desde mfuuid.lib.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio \| para UWP\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Aplicaciones de escritorio para \[ UWP de Server 2008 R2 \|\]<br/>                           |
| Header<br/>                   | <dl> <dt>Mftransform.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[MTA de hardware](hardware-mfts.md)
</dt> <dt>

[Transformar atributos](transform-attributes.md)
</dt> </dl>

 

 




