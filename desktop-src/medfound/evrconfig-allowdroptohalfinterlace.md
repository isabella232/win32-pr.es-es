---
description: Permite que el representador de vídeo mejorado (EVR) mejore el rendimiento omitiendo el segundo campo de cada fotograma entrelazado.
ms.assetid: de7efc6a-19ae-4f3a-8675-38fda3c979e2
title: EVRConfig_AllowDropToHalfInterlace atributo (Uuids.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c9989fe833ea763166ba870c331add5c18bcb45
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127172210"
---
# <a name="evrconfig_allowdroptohalfinterlace-attribute"></a>Atributo EVRConfig \_ AllowDropToHalfInterlace

Permite que el representador de vídeo mejorado (EVR) mejore el rendimiento omitiendo el segundo campo de cada fotograma entrelazado.

## <a name="data-type"></a>Tipo de datos

**UINT32**

## <a name="getset"></a>Obtener o establecer

Para obtener este atributo, llame [**aATTRIBUTEAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Para establecer este atributo, llame [**aATTRIBUTEAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="remarks"></a>Observaciones

Este atributo se puede establecer en el receptor de medios EVR. Para establecer el atributo, use **QueryInterface para** consultar el receptor de medios EVR para la [**interfaz DEATTRIBUTEAttributes.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes)

Establecer este atributo tiene el mismo efecto que establecer la marca **MFVideo MixPrefs \_ AllowDropToHalfInterlace** en la EVR. Consulte [**MFVideoMixPrefs para**](/windows/desktop/api/evr/ne-evr-mfvideomixprefs) obtener una descripción de esta marca.

La constante GUID para este atributo se exporta desde strmiids.lib.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>                                         |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[ R2\]<br/>                            |
| Encabezado<br/>                   | <dl> <dt>Uuids.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos de EVR](enhanced-video-renderer-attributes.md)
</dt> <dt>

[Administración de calidad de vídeo](video-quality-management.md)
</dt> </dl>

 

 




