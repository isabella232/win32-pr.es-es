---
description: Especifica si el receptor de archivos MPEG-4 filtra las NALU del conjunto de parámetros de secuencia (SPS) y del conjunto de parámetros de imagen (PPS).
ms.assetid: B2574BE5-6334-4ED2-A008-86326CDC13B8
title: MF_MPEG4SINK_SPSPPS_PASSTHROUGH atributo (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f3c02f4f1cdcac17a104b5061c8899c92e0ad824
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127580392"
---
# <a name="mf_mpeg4sink_spspps_passthrough-attribute"></a>Atributo \_ PASSTHROUGH DE MF MPEG4SINK \_ SPSPPS \_

Especifica si el receptor de archivos [**MPEG-4**](mpeg-4-file-sink.md) filtra las NALU del conjunto de parámetros de secuencia (SPS) y del conjunto de parámetros de imagen (PPS).

## <a name="data-type"></a>Tipo de datos

**BOOL almacenado** como **UINT32**

## <a name="applies-to"></a>Se aplica a

[**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink)

## <a name="remarks"></a>Observaciones

El [**receptor de archivos MPEG-4**](mpeg-4-file-sink.md) escribe los parámetros SPS y PPS en el cuadro de descripción de ejemplo del archivo MP4. De forma predeterminada, filtra las NALUs de SPS y PPS de la secuencia de vídeo. Para invalidar este comportamiento, establezca el atributo \_ PASSTHROUGH MF MPEG4SINK \_ SPSPPS \_ en **TRUE.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 aplicaciones de escritorio \| aplicaciones para UWP\]<br/>                                  |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 aplicaciones de escritorio \| aplicaciones para UWP\]<br/>                        |
| Encabezado<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




