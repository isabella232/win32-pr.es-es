---
description: Contiene un puntero a la interfaz de devolución de llamada de aplicaciones para el Lector de origen.
ms.assetid: de226a5a-03c0-4bfe-bb20-8969ce43cf53
title: MF_SOURCE_READER_ASYNC_CALLBACK atributo (Mfreadwrite.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66542a155fbb6fa3e56958733626b1d0b750ab9c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127580337"
---
# <a name="mf_source_reader_async_callback-attribute"></a>Atributo MF \_ SOURCE \_ READER \_ ASYNC \_ CALLBACK

Contiene un puntero a la interfaz de devolución de llamada de la aplicación para el [lector de origen](source-reader.md).

## <a name="data-type"></a>Tipo de datos

**IMFSourceReaderCallback \* *_ almacenado como _* IUnknown\***

## <a name="getset"></a>Obtener o establecer

Para obtener este atributo, llame [**a IMFAttributes::GetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).

Para establecer este atributo, llame [**a IMFAttributes::SetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).

## <a name="remarks"></a>Observaciones

El valor de este atributo es un puntero a la interfaz [**IMFSourceReaderCallback de la**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereadercallback) aplicación.

Use este atributo con las siguientes funciones:

-   [**MFCreateSourceReaderFromByteStream**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrombytestream)
-   [**MFCreateSourceReaderFromMediaSource**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrommediasource)
-   [**MFCreateSourceReaderFromURL**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfromurl)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio para \| UWP\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Aplicaciones de escritorio para \[ UWP de Server 2008 R2 \|\]<br/>                           |
| Encabezado<br/>                   | <dl> <dt>Mfreadwrite.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Lector de origen](source-reader.md)
</dt> <dt>

[Atributos del lector de origen](source-reader-attributes.md)
</dt> </dl>

 

 




