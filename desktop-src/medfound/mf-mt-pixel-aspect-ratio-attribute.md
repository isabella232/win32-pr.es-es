---
description: Relación de aspecto de píxeles para un tipo de medio de vídeo.
ms.assetid: e82cdd22-7d3f-4858-befd-43fa6f9f915e
title: MF_MT_PIXEL_ASPECT_RATIO atributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 230e14e07a8011f89d16b095728bc80cbe19faa16ef9427156868f93c2ccb412
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120060495"
---
# <a name="mf_mt_pixel_aspect_ratio-attribute"></a>Atributo MF \_ MT \_ PIXEL ASPECT \_ \_ RATIO

Relación de aspecto de píxeles para un tipo de medio de vídeo.

## <a name="data-type"></a>Tipo de datos

**UINT64**

## <a name="remarks"></a>Comentarios

Los 32 bits superiores contienen el numerador de la relación de aspecto de píxeles y los 32 bits inferiores contienen el denominador. El numerador es el componente horizontal de la relación de aspecto; el denominador es el componente vertical.

Para establecer este atributo, use la [**función MFSetAttributeRatio.**](/windows/desktop/api/mfapi/nf-mfapi-mfsetattributeratio) Para obtener este atributo, use la [**función MFGetAttributeRatio.**](/windows/desktop/api/mfapi/nf-mfapi-mfgetattributeratio)

La relación de aspecto de píxeles describe la forma de los píxeles de la imagen de vídeo mostrada. Establezca este atributo si la imagen tiene píxeles no cuadrados. Para mostrarse correctamente en un dispositivo de visualización con píxeles cuadrados, la imagen debe escalarse por la inversa de la relación de aspecto de píxeles de la imagen.

La constante GUID para este atributo se exporta desde mfuuid.lib.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Aplicaciones de escritorio de Vista \[ \| para aplicaciones para UWP\]<br/>                              |
| Servidor mínimo compatible<br/> | Windows Aplicaciones de escritorio de Server 2008 \[ \| para aplicaciones para UWP\]<br/>                        |
| Header<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos de tipo de medio](media-type-attributes.md)
</dt> <dt>

[Media Foundation atributos](media-foundation-attributes.md)
</dt> <dt>

[Relación de aspecto de la imagen](picture-aspect-ratio.md)
</dt> </dl>

 

 




