---
description: Habilita el procesamiento de vídeo por el lector de origen.
ms.assetid: b1ec1c0e-8042-4486-822f-eb106577c0b1
title: MF_SOURCE_READER_ENABLE_VIDEO_PROCESSING atributo (Mfreadwrite. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9bfcbb076d5f42e784277dbd78101b473ec33905
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497357"
---
# <a name="mf_source_reader_enable_video_processing-attribute"></a>\_Lector de código fuente MF \_ \_ Habilitar atributo de \_ procesamiento de vídeo \_

Habilita el procesamiento de vídeo por el [lector de origen](source-reader.md).

## <a name="data-type"></a>Tipo de datos

**UINT32**



| Value                                                                                                                                                                | Significado                                        |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <span id="Nonzero"></span><span id="nonzero"></span><span id="NONZERO"></span><dl> <dt>**Distinto**</dt> </dl> | Habilitar el procesamiento de vídeo.<br/>            |
| <span id="Zero"></span><span id="zero"></span><span id="ZERO"></span><dl> <dt>**Nulo**</dt> </dl>             | Deshabilitar el procesamiento de vídeo. (Es el valor predeterminado).<br/> |



 

## <a name="getset"></a>Obtener o establecer

Para obtener este atributo, llame a [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Para establecer este atributo, llame a [**IMFAttributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="remarks"></a>Observaciones

Si este atributo es **true** (distinto de cero), el lector de origen puede realizar el siguiente procesamiento de vídeo limitado en fotogramas de vídeo sin comprimir:

-   Conversión de YUV a RGB-32.
-   Desentrelazado.

Estas operaciones se realizan en el software y no están optimizadas para la reproducción. Esta característica está destinada a las aplicaciones que procesan un pequeño número de fotogramas, por ejemplo, para crear una miniatura de vídeo, o aplicaciones que no descodifican fotogramas en tiempo real. La operación de desentrelazado interpola los datos de un solo campo, por lo que es una pérdida.

Evite esta opción si usa Direct3D para mostrar los fotogramas de vídeo, ya que la GPU suele proporcionar mejores capacidades de procesamiento de vídeo.

Si este atributo es **true**, los siguientes atributos deben ser **false**:

-   [\_Administrador de \_ D3D de lector de origen MF \_ \_](mf-source-reader-d3d-manager.md)
-   [MF \_ ReadWrite \_ deshabilitar \_ convertidores](mf-readwrite-disable-converters.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows 7 \|\]<br/>                                        |
| Servidor mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2008 R2 \|\]<br/>                           |
| Encabezado<br/>                   | <dl> <dt>Mfreadwrite. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Lector de origen](source-reader.md)
</dt> <dt>

[Atributos del lector de código fuente](source-reader-attributes.md)
</dt> </dl>

 

 




