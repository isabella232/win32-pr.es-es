---
description: Especifica si está habilitado el modo de panorámica o de recorrido.
ms.assetid: 9e8746c6-13a4-4cf7-9748-82223d9529fa
title: MF_MT_PAN_SCAN_ENABLED atributo (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b347c898ce827ff37796a9698e843f6321db8a1d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104545030"
---
# <a name="mf_mt_pan_scan_enabled-attribute"></a>\_Atributo MF MT de \_ \_ examen panorámico \_ habilitado

Especifica si está habilitado el modo de panorámica o de recorrido.

## <a name="data-type"></a>Tipo de datos

**UINT32**

Trata como un valor booleano.

## <a name="remarks"></a>Observaciones

Si este atributo es **true**, solo se debe mostrar la región de Pan/Scan del vídeo. La región de Pan/Scan se especifica mediante el atributo [**MF \_ MT \_ pan \_ scan \_ abertura**](mf-mt-pan-scan-aperture-attribute.md) .

Si este atributo es **falso** o no está establecido, se debe mostrar la abertura de pantalla completa del vídeo. La abertura de pantalla se especifica mediante el atributo de [**\_ \_ \_ \_ abertura mínima de visualización MF MT**](mf-mt-minimum-display-aperture-attribute.md) .

Si establece este atributo en **true**, establezca también el valor del atributo [**MF \_ MT \_ pan \_ scan \_ abertura**](mf-mt-pan-scan-aperture-attribute.md) .

La constante GUID para este atributo se exporta desde mfuuid. lib.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows Vista \|\]<br/>                              |
| Servidor mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2008 \|\]<br/>                        |
| Encabezado<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**IMFAttributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[Atributos de tipo de medio](media-type-attributes.md)
</dt> <dt>

[Relación de aspecto de la imagen](picture-aspect-ratio.md)
</dt> </dl>

 

 




