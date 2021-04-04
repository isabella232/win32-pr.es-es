---
description: Contiene un puntero a la interfaz de devolución de llamada de aplicaciones para el lector de origen.
ms.assetid: de226a5a-03c0-4bfe-bb20-8969ce43cf53
title: MF_SOURCE_READER_ASYNC_CALLBACK atributo (Mfreadwrite. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66542a155fbb6fa3e56958733626b1d0b750ab9c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277682"
---
# <a name="mf_source_reader_async_callback-attribute"></a>\_Atributo de \_ devolución de \_ llamada Async del lector de origen MF \_

Contiene un puntero a la interfaz de devolución de llamada de la aplicación para el [lector de origen](source-reader.md).

## <a name="data-type"></a>Tipo de datos

**IMFSourceReaderCallback \** _ almacenado como _*IUnknown \**_

## <a name="getset"></a>Obtener o establecer

Para obtener este atributo, llame a [_ *IMFAttributes:: GetUnknown* *](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).

Para establecer este atributo, llame a [**IMFAttributes:: setunknown (**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).

## <a name="remarks"></a>Observaciones

El valor de este atributo es un puntero a la interfaz [**IMFSourceReaderCallback**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereadercallback) de la aplicación.

Utilice este atributo con las siguientes funciones:

-   [**MFCreateSourceReaderFromByteStream**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrombytestream)
-   [**MFCreateSourceReaderFromMediaSource**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrommediasource)
-   [**MFCreateSourceReaderFromURL**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfromurl)

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

 

 




