---
description: Especifica la rotación de un fotograma de vídeo en la dirección en sentido contrario a las agujas del reloj.
ms.assetid: 7C0911A6-6D7C-4510-891F-A6F56CE1EC2B
title: MF_MT_VIDEO_ROTATION atributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: adf3d909b29757a02d46cc842b30f04bfb0463d6f734eecb74bfb957fa206fb7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117876705"
---
# <a name="mf_mt_video_rotation-attribute"></a>Atributo MF \_ MT \_ VIDEO \_ ROTATION

Especifica la rotación de un fotograma de vídeo en la dirección en sentido contrario a las agujas del reloj.

## <a name="data-type"></a>Tipo de datos

**MFVideoRotationFormat almacenado** como **UINT32**

## <a name="remarks"></a>Comentarios

El vídeo de un dispositivo portátil, como un teléfono móvil, suele girar 90, 180 o 270 grados. Si la cámara almacena la orientación como metadatos en el archivo de vídeo, la imagen se puede ajustar en el momento de la reproducción.

Si este atributo se establece en **MFVideoRotationFormat \_ 90**, significa que el contenido se ha girado 90 grados en la dirección en sentido contrario a las agujas del reloj. Si el contenido se gira 90 grados en el sentido de las agujas del reloj, el valor del atributo sería **MFVideoRotationFormat \_ 270.**

Los valores admitidos para este atributo se enumeran [**en MFVideoRotationFormat**](/windows/desktop/api/mfapi/ne-mfapi-mfvideorotationformat).

La constante GUID para este atributo se exporta desde mfuuid.lib.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 aplicaciones de escritorio \| aplicaciones para UWP\]<br/>                                  |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 aplicaciones de escritorio \| aplicaciones para UWP\]<br/>                        |
| Header<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Tipos de medios](media-types.md)
</dt> </dl>

 

 




