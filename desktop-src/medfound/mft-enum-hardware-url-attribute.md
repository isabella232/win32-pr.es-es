---
description: Contiene el vínculo simbólico para una transformación de Media Foundation basada en hardware (MFT).
ms.assetid: 7e153051-a167-4ff7-8178-b290d8a1345e
title: MFT_ENUM_HARDWARE_URL_Attribute atributo (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 539aa1ecbf8bf322e7397a50bb16175dbcca806f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276223"
---
# <a name="mft_enum_hardware_url_attribute-attribute"></a>\_Atributo de \_ \_ atributo de dirección URL de hardware enum de MFT \_

Contiene el vínculo simbólico para una transformación de Media Foundation basada en hardware (MFT).

## <a name="data-type"></a>Tipo de datos

**WCHAR \** _

## <a name="getset"></a>Obtener o establecer

Para obtener este atributo, llame a [_ *IMFAttributes:: GetString* *](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).

Para establecer este atributo, llame a [**IMFAttributes:: setString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).

## <a name="remarks"></a>Observaciones

Este atributo es compatible con MFTs basados en hardware. El valor del atributo es el vínculo simbólico del controlador de dispositivo. Este atributo también se establece en los punteros [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) asignados por la función [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) , cuando esos punteros representan MFTs basados en hardware.

El vínculo simbólico debe considerarse una cadena opaca. Para obtener el nombre para mostrar de un dispositivo, consulte el atributo [ \_ \_ nombre descriptivo de MFT](mft-friendly-name-attribute.md) .

El software MFTs no debe tener establecido este atributo.

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

[MFTs de hardware](hardware-mfts.md)
</dt> <dt>

[Atributos de transformación](transform-attributes.md)
</dt> </dl>

 

 




