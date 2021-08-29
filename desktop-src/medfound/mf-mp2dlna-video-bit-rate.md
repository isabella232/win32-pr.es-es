---
description: Especifica la velocidad máxima de bits de vídeo para el receptor multimedia de Digital Living Network Alliance (DLNA).
ms.assetid: 5805f930-6cbd-4089-a052-522b4d152cc1
title: MF_MP2DLNA_VIDEO_BIT_RATE atributo (Mfmp2dlna.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d8f1e518ded74435f88d823bebe90bde0c6f2355714c1d67c3238207a4a4565
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119104751"
---
# <a name="mf_mp2dlna_video_bit_rate-attribute"></a>Atributo \_ MF MP2DLNA \_ VIDEO BIT \_ \_ RATE

Especifica la velocidad máxima de bits de vídeo para el receptor multimedia de Digital Living Network Alliance (DLNA).

## <a name="data-type"></a>Tipo de datos

**UINT32**

El valor es la velocidad de bits máxima de destino para la secuencia de vídeo codificada, en bits por segundo. El valor máximo es 9800000 (9,8 Mbps), que también es el valor predeterminado.

## <a name="getset"></a>Obtener o establecer

Para obtener este atributo, llame [**a IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Para establecer este atributo, llame [**a IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="remarks"></a>Comentarios

Para establecer este atributo en el receptor de medios DLNA, consulte el receptor de medios para la [**interfaz DEATTRIBUTEAttributes.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) Establezca el atributo antes de que comience el streaming.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>                                             |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[ R2\]<br/>                                |
| Header<br/>                   | <dl> <dt>Mfmp2dlna.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




