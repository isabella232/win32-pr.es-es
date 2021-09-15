---
description: Especifica la velocidad máxima de bits de vídeo para el receptor multimedia de Digital Living Network Alliance (DLNA).
ms.assetid: 5805f930-6cbd-4089-a052-522b4d152cc1
title: MF_MP2DLNA_VIDEO_BIT_RATE atributo (Mfmp2dlna.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 503625e6879b202f3fcd1f38bce38ebf48677d77
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127580393"
---
# <a name="mf_mp2dlna_video_bit_rate-attribute"></a>Atributo \_ MP2DLNA \_ VIDEO BIT RATE \_ \_ de MF

Especifica la velocidad máxima de bits de vídeo para el receptor multimedia de Digital Living Network Alliance (DLNA).

## <a name="data-type"></a>Tipo de datos

**UINT32**

El valor es la velocidad de bits máxima de destino para la secuencia de vídeo codificada, en bits por segundo. El valor máximo es 9800000 (9,8 Mbps), que también es el valor predeterminado.

## <a name="getset"></a>Obtener o establecer

Para obtener este atributo, llame [**aATTRIBUTEAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Para establecer este atributo, llame [**aATTRIBUTEAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="remarks"></a>Observaciones

Para establecer este atributo en el receptor de medios DLNA, consulte el receptor de medios para la [**interfazATTRIBUTEAttributes.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) Establezca el atributo antes de que comience el streaming.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio solo\]<br/>                                             |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[ R2\]<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Mfmp2dlna.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




