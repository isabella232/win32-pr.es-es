---
description: Especifica si el receptor de archivos MPEG-4 filtra las NALU del conjunto de parámetros de secuencia (SPS) y del conjunto de parámetros de imagen (PPS).
ms.assetid: B2574BE5-6334-4ED2-A008-86326CDC13B8
title: MF_MPEG4SINK_SPSPPS_PASSTHROUGH atributo (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b939302999fc7e095abbc97aed5910976972c860440a2c865248949e0f052aa3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119104631"
---
# <a name="mf_mpeg4sink_spspps_passthrough-attribute"></a>Atributo \_ PASSTHROUGH DE MF MPEG4SINK \_ SPSPPS \_

Especifica si el receptor de [**archivos MPEG-4**](mpeg-4-file-sink.md) filtra el conjunto de parámetros de secuencia (SPS) y las NALU del conjunto de parámetros de imagen (PPS).

## <a name="data-type"></a>Tipo de datos

**BOOL almacenado** como **UINT32**

## <a name="applies-to"></a>Se aplica a

[**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink)

## <a name="remarks"></a>Comentarios

El [**receptor de archivos MPEG-4**](mpeg-4-file-sink.md) escribe los parámetros SPS y PPS en el cuadro de descripción de ejemplo del archivo MP4. De forma predeterminada, filtra las NALUs de SPS y PPS de la secuencia de vídeo. Para invalidar este comportamiento, establezca el atributo \_ PASSTHROUGH MF MPEG4SINK \_ SPSPPS \_ en **TRUE.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 aplicaciones de escritorio \| aplicaciones para UWP\]<br/>                                  |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 aplicaciones de escritorio \| aplicaciones para UWP\]<br/>                        |
| Header<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




