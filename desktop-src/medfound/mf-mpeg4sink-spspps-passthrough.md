---
description: Especifica si el receptor de archivos MPEG-4 filtra el conjunto de parámetros de secuencia (SPS) y el conjunto de parámetros de imagen (PPS) NALUs.
ms.assetid: B2574BE5-6334-4ED2-A008-86326CDC13B8
title: MF_MPEG4SINK_SPSPPS_PASSTHROUGH atributo (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f3c02f4f1cdcac17a104b5061c8899c92e0ad824
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103811857"
---
# <a name="mf_mpeg4sink_spspps_passthrough-attribute"></a>MF \_ MPEG4SINK \_ SPSPPS \_ PASSTHROUGH (atributo)

Especifica si el [**receptor de archivos MPEG-4**](mpeg-4-file-sink.md) filtra el conjunto de parámetros de secuencia (SPS) y el conjunto de parámetros de imagen (PPS) NALUs.

## <a name="data-type"></a>Tipo de datos

**Bool** almacenado como **UINT32**

## <a name="applies-to"></a>Se aplica a

[**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink)

## <a name="remarks"></a>Observaciones

El [**receptor de archivos MPEG-4**](mpeg-4-file-sink.md) escribe los parámetros de SPS y PPS en el cuadro Descripción de ejemplo del archivo MP4. De forma predeterminada, filtra los SPS y el NALUs de PPS del flujo de vídeo. Para invalidar este comportamiento, establezca el \_ atributo de paso MF MPEG4SINK \_ SPSPPS \_ en **true**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows 8 \|\]<br/>                                  |
| Servidor mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2012 \|\]<br/>                        |
| Encabezado<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




