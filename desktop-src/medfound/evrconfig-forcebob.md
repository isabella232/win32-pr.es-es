---
description: Fuerza al representador de vídeo mejorado (EVR) a usar el desinterlazado bob.
ms.assetid: 56f808b3-c2eb-46e4-84a1-c478a5db78e7
title: EVRConfig_ForceBob atributo (Uuids.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41248eb48f089cf88ecd66dcf823cc83c243b3a2f637aef7633d13ac755c9584
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119958355"
---
# <a name="evrconfig_forcebob-attribute"></a>Atributo ForceBob de EVRConfig \_

Fuerza al representador de vídeo mejorado (EVR) a usar el desinterlazado bob.

## <a name="data-type"></a>Tipo de datos

**UINT32**

## <a name="getset"></a>Obtener o establecer

Para obtener este atributo, llame [**a IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Para establecer este atributo, llame [**a IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="remarks"></a>Comentarios

Este atributo se puede establecer en el receptor de medios EVR. Para establecer el atributo, use **QueryInterface para** consultar el receptor de medios EVR para la [**interfaz IMFAttributes.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes)

Establecer este atributo tiene el mismo efecto que establecer la **marca \_ ForceBob MFVideoMixPrefs** en la EVR. Consulte [**MFVideoMixPrefs para**](/windows/desktop/api/evr/ne-evr-mfvideomixprefs) obtener una descripción de esta marca.

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

[Atributos evr](enhanced-video-renderer-attributes.md)
</dt> <dt>

[Administración de calidad de vídeo](video-quality-management.md)
</dt> </dl>

 

 




