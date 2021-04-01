---
description: Especifica el giro de un fotograma de vídeo en el sentido contrario a las agujas del reloj.
ms.assetid: 7C0911A6-6D7C-4510-891F-A6F56CE1EC2B
title: MF_MT_VIDEO_ROTATION atributo (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f46a67c9861b8094e909e5c6fd7bc82e46166dc3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913554"
---
# <a name="mf_mt_video_rotation-attribute"></a>\_Atributo de \_ rotación de vídeo MF MT \_

Especifica el giro de un fotograma de vídeo en el sentido contrario a las agujas del reloj.

## <a name="data-type"></a>Tipo de datos

**MFVideoRotationFormat** almacenado como **UINT32**

## <a name="remarks"></a>Observaciones

El vídeo de un dispositivo de mano, como un teléfono móvil, a menudo gira en 90, 180 o 270 grados. Si la cámara almacena la orientación como metadatos en el archivo de vídeo, la imagen se puede ajustar en el momento de la reproducción.

Si este atributo se establece en **MFVideoRotationFormat \_ 90**, significa que el contenido se ha girado 90 grados en el sentido contrario a las agujas del reloj. Si el contenido se gira 90 grados en sentido de las agujas del reloj, el valor del atributo sería **MFVideoRotationFormat \_ 270**.

Los valores admitidos para este atributo se enumeran en [**MFVideoRotationFormat**](/windows/desktop/api/mfapi/ne-mfapi-mfvideorotationformat).

La constante GUID para este atributo se exporta desde mfuuid. lib.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows 8 \|\]<br/>                                  |
| Servidor mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2012 \|\]<br/>                        |
| Encabezado<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Tipos de medios](media-types.md)
</dt> </dl>

 

 




