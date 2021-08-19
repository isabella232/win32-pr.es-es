---
description: Todo permite que el representador de vídeo mejorado (EVR) mezcle el vídeo dentro de un rectángulo que sea menor que el rectángulo de salida y, a continuación, escale el resultado.
ms.assetid: 7e3b8fe1-959b-4391-a715-5d5a7a7dda39
title: EVRConfig_AllowScaling atributo (Uuids.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c83323c42ac81d4cce0bb42733bd4246959cf0fc9a58b5705579a86aee9b2bd6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117879429"
---
# <a name="evrconfig_allowscaling-attribute"></a>Atributo \_ AllowScaling de EVRConfig

Todo permite que el representador de vídeo mejorado (EVR) mezcle el vídeo dentro de un rectángulo que sea menor que el rectángulo de salida y, a continuación, escale el resultado.

## <a name="data-type"></a>Tipo de datos

**UINT32**

## <a name="getset"></a>Obtener o establecer

Para obtener este atributo, llame [**aATTRIBUTEAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Para establecer este atributo, llame [**aATTRIBUTEAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="remarks"></a>Comentarios

Este atributo se puede establecer en el receptor de medios EVR. Para establecer el atributo, use **QueryInterface para** consultar el receptor de medios EVR para la [**interfaz DEATTRIBUTEAttributes.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes)

Establecer este atributo tiene el mismo efecto que establecer la marca **\_ allowScaling MFVideoRenderPrefs** en la EVR. Consulte [**MFVideoRenderPrefs para**](/windows/desktop/api/evr/ne-evr-mfvideorenderprefs) obtener una descripción de esta marca.

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

 

 




