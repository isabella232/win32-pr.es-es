---
description: Habilita el procesamiento de vídeo mediante el Lector de origen.
ms.assetid: b1ec1c0e-8042-4486-822f-eb106577c0b1
title: MF_SOURCE_READER_ENABLE_VIDEO_PROCESSING atributo (Mfreadwrite.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9bfcbb076d5f42e784277dbd78101b473ec33905
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127263239"
---
# <a name="mf_source_reader_enable_video_processing-attribute"></a>Atributo MF \_ SOURCE READER ENABLE VIDEO \_ \_ \_ \_ PROCESSING

Habilita el procesamiento de vídeo mediante el [Lector de origen.](source-reader.md)

## <a name="data-type"></a>Tipo de datos

**UINT32**



| Value                                                                                                                                                                | Significado                                        |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <span id="Nonzero"></span><span id="nonzero"></span><span id="NONZERO"></span><dl> <dt>**Distinto**</dt> </dl> | Habilite el procesamiento de vídeo.<br/>            |
| <span id="Zero"></span><span id="zero"></span><span id="ZERO"></span><dl> <dt>**Cero**</dt> </dl>             | Deshabilite el procesamiento de vídeo. (Es el valor predeterminado).<br/> |



 

## <a name="getset"></a>Obtener o establecer

Para obtener este atributo, llame [**aATTRIBUTEAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Para establecer este atributo, llame [**aATTRIBUTEAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="remarks"></a>Observaciones

Si este atributo es **TRUE** (distinto de cero), el lector de origen puede realizar el siguiente procesamiento de vídeo limitado en fotogramas de vídeo sin comprimir:

-   Conversión de YUV a RGB-32.
-   Desentrelazado.

Estas operaciones se realizan en software y no están optimizadas para la reproducción. Esta característica está pensada para aplicaciones que procesan un pequeño número de fotogramas (por ejemplo, para crear una miniatura de vídeo) o aplicaciones que no descodifican fotogramas en tiempo real. La operación de desinterlace interpola los datos de un solo campo, por lo que es una pérdida.

Evite esta configuración si usa Direct3D para mostrar los fotogramas de vídeo, ya que la GPU generalmente proporciona mejores funcionalidades de procesamiento de vídeo.

Si este atributo es **TRUE**, los atributos siguientes deben ser **FALSE**:

-   [MF \_ SOURCE \_ READER \_ D3D \_ MANAGER](mf-source-reader-d3d-manager.md)
-   [MF \_ READWRITE \_ DISABLE \_ CONVERTERS](mf-readwrite-disable-converters.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio aplicaciones para \| UWP\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Aplicaciones de escritorio para \[ UWP de Server 2008 R2 \|\]<br/>                           |
| Encabezado<br/>                   | <dl> <dt>Mfreadwrite.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Lector de origen](source-reader.md)
</dt> <dt>

[Atributos del lector de origen](source-reader-attributes.md)
</dt> </dl>

 

 




