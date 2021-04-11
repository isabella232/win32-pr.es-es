---
description: Especifica la velocidad de bits de vídeo máxima del receptor de medios de la Alianza de redes digitales (DLNA).
ms.assetid: 5805f930-6cbd-4089-a052-522b4d152cc1
title: MF_MP2DLNA_VIDEO_BIT_RATE atributo (Mfmp2dlna. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 503625e6879b202f3fcd1f38bce38ebf48677d77
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275954"
---
# <a name="mf_mp2dlna_video_bit_rate-attribute"></a>\_Atributo de \_ velocidad de bits de vídeo MF MP2DLNA \_ \_

Especifica la velocidad de bits de vídeo máxima del receptor de medios de la Alianza de redes digitales (DLNA).

## <a name="data-type"></a>Tipo de datos

**UINT32**

El valor es la velocidad de bits máxima de destino para la secuencia de vídeo codificada, en bits por segundo. El valor máximo es 9,8 millones (9,8 Mbps), que también es el valor predeterminado.

## <a name="getset"></a>Obtener o establecer

Para obtener este atributo, llame a [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Para establecer este atributo, llame a [**IMFAttributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="remarks"></a>Observaciones

Para establecer este atributo en el receptor de medios DLNA, consulte el receptor de medios de la interfaz [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) . Establezca el atributo antes de que comience la transmisión por secuencias.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>                                             |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Mfmp2dlna. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




