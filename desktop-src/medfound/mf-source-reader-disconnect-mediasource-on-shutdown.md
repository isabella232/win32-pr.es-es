---
description: Especifica si el lector de origen cierra el origen del medio.
ms.assetid: c85f5994-8005-48c9-8a05-0316f48f4142
title: MF_SOURCE_READER_DISCONNECT_MEDIASOURCE_ON_SHUTDOWN atributo (Mfreadwrite. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7a9474e7fb19bb6531baf31a97238bbe6b10e46
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "104361942"
---
# <a name="mf_source_reader_disconnect_mediasource_on_shutdown-attribute"></a>El \_ \_ lector de origen MF \_ desconecta \_ MEDIASOURCE en el \_ \_ atributo Shutdown

Especifica si el [lector de origen](source-reader.md) cierra el origen del medio.

## <a name="data-type"></a>Tipo de datos

**UINT32**

## <a name="getset"></a>Obtener o establecer

Para obtener este atributo, llame a [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Para establecer este atributo, llame a [**IMFAttributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="remarks"></a>Observaciones

Este atributo solo se aplica cuando la aplicación crea el lector de origen a partir de un objeto de origen multimedia existente, ya sea llamando a [**MFCreateSourceReaderFromMediaSource**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrommediasource) o llamando a [**IMFReadWriteClassFactory:: CreateInstanceFromObject**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfreadwriteclassfactory-createinstancefromobject).

De forma predeterminada, cuando la aplicación libera el lector de origen, el lector de origen cierra el origen del medio llamando a [**IMFMediaSource:: Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown) en el origen del medio. En ese momento, la aplicación ya no puede usar el origen de medios.

Sin embargo, si el \_ \_ atributo del lector de origen MF \_ desconectar \_ MEDIASOURCE \_ al cerrar el \_ atributo es **true**, el lector de origen no apaga el origen de medios. Esto significa que la aplicación todavía puede usar el origen de medios una vez que la aplicación libera el lector de origen. También significa que la aplicación es responsable de llamar a [**IMFMediaSource:: Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown) en el origen del medio.

Si la aplicación crea el lector de origen a partir de una dirección URL o de una secuencia de bytes, el lector de origen siempre cierra el origen del medio. \_ \_ \_ En este caso, se omite el atributo del lector de código de MF desconectar \_ MEDIASOURCE \_ al \_ cerrar.

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

 

 




