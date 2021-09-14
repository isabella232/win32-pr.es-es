---
description: Relación de aspecto de píxeles para un tipo de medio de vídeo.
ms.assetid: e82cdd22-7d3f-4858-befd-43fa6f9f915e
title: MF_MT_PIXEL_ASPECT_RATIO atributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 50c0d28ea11ba664208fcfe5fc356f1f57f2878e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127363966"
---
# <a name="mf_mt_pixel_aspect_ratio-attribute"></a>Atributo MF \_ MT \_ PIXEL ASPECT \_ \_ RATIO

Relación de aspecto de píxeles para un tipo de medio de vídeo.

## <a name="data-type"></a>Tipo de datos

**UINT64**

## <a name="remarks"></a>Observaciones

Los 32 bits superiores contienen el numerador de la relación de aspecto de píxeles y los 32 bits inferiores contienen el denominador. El numerador es el componente horizontal de la relación de aspecto; el denominador es el componente vertical.

Para establecer este atributo, use la [**función MFSetAttributeRatio.**](/windows/desktop/api/mfapi/nf-mfapi-mfsetattributeratio) Para obtener este atributo, use la [**función MFGetAttributeRatio.**](/windows/desktop/api/mfapi/nf-mfapi-mfgetattributeratio)

La relación de aspecto de píxeles describe la forma de los píxeles de la imagen de vídeo mostrada. Establezca este atributo si la imagen tiene píxeles no cuadrados. Para mostrarse correctamente en un dispositivo de visualización con píxeles cuadrados, la imagen debe escalarse por el inverso de la relación de aspecto de píxeles de la imagen.

La constante GUID para este atributo se exporta desde mfuuid.lib.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Aplicaciones de escritorio de Vista \[ \| para aplicaciones para UWP\]<br/>                              |
| Servidor mínimo compatible<br/> | Windows Aplicaciones de escritorio de Server 2008 \[ \| aplicaciones para UWP\]<br/>                        |
| Encabezado<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos de tipo multimedia](media-type-attributes.md)
</dt> <dt>

[Media Foundation atributos](media-foundation-attributes.md)
</dt> <dt>

[Relación de aspecto de la imagen](picture-aspect-ratio.md)
</dt> </dl>

 

 




