---
description: Contiene un puntero a la interfaz de devolución de llamada de aplicaciones para el escritor del receptor.
ms.assetid: 22df1fa0-469d-4501-aaf0-a0379b7ed096
title: MF_SINK_WRITER_ASYNC_CALLBACK atributo (Mfreadwrite. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f11bed051df9107ca3a2247b6c3d0cf2058224c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103817782"
---
# <a name="mf_sink_writer_async_callback-attribute"></a>\_Atributo de \_ devolución de \_ llamada asincrónica de escritor de receptor MF \_

Contiene un puntero a la interfaz de devolución de llamada de la aplicación para el escritor del receptor.

## <a name="data-type"></a>Tipo de datos

**[](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsinkwritercallback) IMFSinkWriterCallback \** _ almacenado como _*IUnknown \**_

## <a name="getset"></a>Obtener o establecer

Para obtener este atributo, llame a [_ *IMFAttributes:: GetUnknown* *](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).

Para establecer este atributo, llame a [**IMFAttributes:: setunknown (**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).

## <a name="remarks"></a>Observaciones

El valor de este atributo es un puntero a la interfaz [**IMFSinkWriterCallback**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsinkwritercallback) de la aplicación.

Utilice este atributo con las siguientes funciones:

-   [**MFCreateSinkWriterFromMediaSink**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfrommediasink)
-   [**MFCreateSinkWriterFromURL**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfromurl)

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

[Atributos del escritor de receptor](sink-writer-attributes.md)
</dt> </dl>

 

 




