---
description: Especifica si el Lector de origen apaga el origen multimedia.
ms.assetid: c85f5994-8005-48c9-8a05-0316f48f4142
title: MF_SOURCE_READER_DISCONNECT_MEDIASOURCE_ON_SHUTDOWN atributo (Mfreadwrite.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 323340a0b95fd6f52d4ac7e8db2e9ff53bf70edb30442369f1ffd8f2f2c55fa1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119663895"
---
# <a name="mf_source_reader_disconnect_mediasource_on_shutdown-attribute"></a>MF \_ SOURCE READER DISCONNECT \_ \_ \_ MEDIASOURCE ON SHUTDOWN \_ \_ attribute

Especifica si el [Lector de origen](source-reader.md) apaga el origen multimedia.

## <a name="data-type"></a>Tipo de datos

**UINT32**

## <a name="getset"></a>Obtener o establecer

Para obtener este atributo, llame [**a IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Para establecer este atributo, llame [**a IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="remarks"></a>Comentarios

Este atributo solo se aplica cuando la aplicación crea el lector de origen a partir de un objeto de origen multimedia existente, ya sea mediante una llamada a [**MFCreateSourceReaderFromMediaSource**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrommediasource) o mediante una llamada a [**MFReadWriteClassFactory::CreateInstanceFromObject**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfreadwriteclassfactory-createinstancefromobject).

De forma predeterminada, cuando la aplicación libera el lector de origen, el lector de origen apaga el origen multimedia mediante una llamada a [**IMFMediaSource::Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown) en el origen de medios. En ese momento, la aplicación ya no puede usar el origen multimedia.

Sin embargo, si el atributo MF SOURCE READER DISCONNECT MEDIASOURCE ON SHUTDOWN es TRUE, el lector de origen no \_ \_ apaga el origen \_ \_ \_ \_ multimedia.  Esto significa que la aplicación todavía puede usar el origen multimedia después de que la aplicación libere el lector de origen. También significa que la aplicación es responsable de llamar [**a IMFMediaSource::Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown) en el origen multimedia.

Si la aplicación crea el lector de origen a partir de una dirección URL o de una secuencia de bytes, el lector de origen siempre apaga el origen multimedia. En este caso, se omite el atributo \_ MF SOURCE READER DISCONNECT \_ \_ \_ MEDIASOURCE ON \_ \_ SHUTDOWN.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio \| para UWP\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Aplicaciones de escritorio para \[ UWP de Server 2008 R2 \|\]<br/>                           |
| Header<br/>                   | <dl> <dt>Mfreadwrite.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Lector de origen](source-reader.md)
</dt> <dt>

[Atributos del lector de origen](source-reader-attributes.md)
</dt> </dl>

 

 




