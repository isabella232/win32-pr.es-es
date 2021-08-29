---
description: Fuerza al representador de vídeo mejorado (EVR) a omitir el segundo campo de cada fotograma entrelazado.
ms.assetid: b79d9230-b127-4e9b-b73b-685ce27aefa9
title: EVRConfig_ForceHalfInterlace atributo (Uuids.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf3d73eceb1728b8bdc043ba69ee62249783ee109c29ff173a9e563f68505d9b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120061595"
---
# <a name="evrconfig_forcehalfinterlace-attribute"></a>Atributo EVRConfig \_ ForceHalfInterlace

Fuerza al representador de vídeo mejorado (EVR) a omitir el segundo campo de cada fotograma entrelazado.

## <a name="data-type"></a>Tipo de datos

**UINT32**

## <a name="getset"></a>Obtener o establecer

Para obtener este atributo, llame [**aATTRIBUTEAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Para establecer este atributo, llame [**aATTRIBUTEAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="remarks"></a>Comentarios

Este atributo se puede establecer en el receptor de medios EVR. Para establecer el atributo, use **QueryInterface para** consultar el receptor de medios EVR para la [**interfaz DEATTRIBUTEAttributes.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes)

Establecer este atributo tiene el mismo efecto que establecer la marca **MFVideo MixPrefs \_ ForceHalfInterlace** en la EVR. Consulte [**MFVideoMixPrefs para**](/windows/desktop/api/evr/ne-evr-mfvideomixprefs) obtener una descripción de esta marca.

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

 

 




