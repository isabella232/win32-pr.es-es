---
description: Relación de aspecto de píxeles para un tipo de medio de vídeo.
ms.assetid: e82cdd22-7d3f-4858-befd-43fa6f9f915e
title: MF_MT_PIXEL_ASPECT_RATIO atributo (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 50c0d28ea11ba664208fcfe5fc356f1f57f2878e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104542158"
---
# <a name="mf_mt_pixel_aspect_ratio-attribute"></a>\_Atributo de \_ relación de aspecto de píxeles MF MT \_ \_

Relación de aspecto de píxeles para un tipo de medio de vídeo.

## <a name="data-type"></a>Tipo de datos

**UINT64**

## <a name="remarks"></a>Observaciones

Los 32 bits superiores contienen el numerador de la relación de aspecto de píxeles y los 32 bits inferiores contienen el denominador. El numerador es el componente horizontal de la relación de aspecto; el denominador es el componente vertical.

Para establecer este atributo, utilice la función [**MFSetAttributeRatio**](/windows/desktop/api/mfapi/nf-mfapi-mfsetattributeratio) . Para obtener este atributo, utilice la función [**MFGetAttributeRatio**](/windows/desktop/api/mfapi/nf-mfapi-mfgetattributeratio) .

La relación de aspecto de píxeles describe la forma de los píxeles de la imagen de vídeo mostrada. Establezca este atributo si la imagen tiene píxeles no cuadrados. Para que se muestre correctamente en un dispositivo de pantalla con píxeles cuadrados, la imagen se debe escalar mediante el inverso de la relación de aspecto de píxeles de la imagen.

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

[Atributos de tipo de medio](media-type-attributes.md)
</dt> <dt>

[Atributos de Media Foundation](media-foundation-attributes.md)
</dt> <dt>

[Relación de aspecto de la imagen](picture-aspect-ratio.md)
</dt> </dl>

 

 




