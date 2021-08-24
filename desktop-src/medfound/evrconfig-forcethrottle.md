---
description: Fuerza al representador de vídeo mejorado (EVR) a limitar su salida para que coincida con el ancho de banda de GPU.
ms.assetid: e81e67d6-aa72-44c1-90e9-72ab18bca1c9
title: EVRConfig_ForceThrottle atributo (Uuids.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad09d0c3133039975a04a026ec84233987dfd4033b120a4b8fc6272e2fd72b9f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119346145"
---
# <a name="evrconfig_forcethrottle-attribute"></a>Atributo \_ ForceThrottle de EVRConfig

Fuerza al representador de vídeo mejorado (EVR) a limitar su salida para que coincida con el ancho de banda de GPU.

## <a name="data-type"></a>Tipo de datos

**UINT32**

## <a name="getset"></a>Obtener o establecer

Para obtener este atributo, llame [**aATTRIBUTEAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Para establecer este atributo, llame [**aATTRIBUTEAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="remarks"></a>Comentarios

Este atributo se puede establecer en el receptor de medios EVR. Para establecer el atributo, use **IUnknown::QueryInterface** para consultar el receptor de medios EVR para la [**interfazATTRIBUTEAttributes.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes)

Establecer este atributo tiene el mismo efecto que establecer la marca **MFVideoRenderPrefs \_ ForceOutputThrottling** en la EVR. Consulte [**MFVideoRenderPrefs para**](/windows/desktop/api/evr/ne-evr-mfvideorenderprefs) obtener una descripción de esta marca.

La constante GUID para este atributo se exporta desde strmiids.lib.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>                                         |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[ R2\]<br/>                            |
| Header<br/>                   | <dl> <dt>Uuids.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos de EVR](enhanced-video-renderer-attributes.md)
</dt> <dt>

[Administración de calidad de vídeo](video-quality-management.md)
</dt> </dl>

 

 




