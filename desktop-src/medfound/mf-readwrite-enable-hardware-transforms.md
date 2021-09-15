---
description: Permite que el lector de origen o el escritor de receptores usen transformaciones de Media Foundation basadas en hardware (MFT).
ms.assetid: 03f2fa76-b828-40b1-929d-60e7d5ab49bb
title: MF_READWRITE_ENABLE_HARDWARE_TRANSFORMS atributo (Mfreadwrite.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 642be732a51f064d07e57609a886810f2a9c40b2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127474130"
---
# <a name="mf_readwrite_enable_hardware_transforms-attribute"></a>Atributo MF \_ READWRITE \_ ENABLE \_ HARDWARE \_ TRANSFORMS

Permite que el lector de origen o el escritor de receptores usen transformaciones de Media Foundation basadas en hardware (MFT).

## <a name="data-type"></a>Tipo de datos

**UINT32**

## <a name="getset"></a>Obtener o establecer

Para obtener este atributo, llame [**a IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Para establecer este atributo, llame [**a IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="remarks"></a>Observaciones

De forma predeterminada, el lector de origen y el escritor de receptores no usan codificadores ni descodificadores de hardware. Para habilitar el uso de MTA de hardware, establezca este atributo en **TRUE** al crear el lector de origen o el escritor de receptores.

Use este atributo con las siguientes funciones:

-   [**MFCreateSourceReaderFromByteStream**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrombytestream)
-   [**MFCreateSourceReaderFromMediaSource**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrommediasource)
-   [**MFCreateSourceReaderFromURL**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfromurl)
-   [**MFCreateSinkWriterFromMediaSink**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfrommediasink)
-   [**MFCreateSinkWriterFromURL**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfromurl)

Hay una excepción al comportamiento predeterminado. El lector de origen y el sistema de escritura del receptor usan automáticamente MTA registrados localmente en el proceso del autor de la llamada. Para registrar un MFT localmente, llame a [**MFTRegisterLocal**](/windows/desktop/api/mfapi/nf-mfapi-mftregisterlocal) o [**MFTRegisterLocalByCLSID**](/windows/desktop/api/mfapi/nf-mfapi-mftregisterlocalbyclsid). Los MTA de hardware registrados localmente se usan incluso si no se ha establecido el atributo **MF \_ READWRITE \_ ENABLE HARDWARE \_ \_ TRANSFORMS.**

Este atributo no afecta a lacodización de vídeo acelerada por hardware que usa la aceleración de vídeo directX (DXVA). Para habilitar la decodificación dxva en el lector de origen, establezca el atributo [MF \_ SOURCE READER \_ \_ D3D \_ MANAGER.](mf-source-reader-d3d-manager.md)

Si este atributo es **TRUE,** no establezca el atributo [MF \_ READWRITE \_ DISABLE \_ CONVERTERS.](mf-readwrite-disable-converters.md)

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

[Atributos del escritor de receptores](sink-writer-attributes.md)
</dt> <dt>

[Atributos del lector de origen](source-reader-attributes.md)
</dt> </dl>

 

 




