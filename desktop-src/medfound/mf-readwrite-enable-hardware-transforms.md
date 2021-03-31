---
description: Permite al lector de código fuente o al escritor de receptores usar transformaciones de Media Foundation basadas en hardware (MFTs).
ms.assetid: 03f2fa76-b828-40b1-929d-60e7d5ab49bb
title: MF_READWRITE_ENABLE_HARDWARE_TRANSFORMS atributo (Mfreadwrite. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 642be732a51f064d07e57609a886810f2a9c40b2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361100"
---
# <a name="mf_readwrite_enable_hardware_transforms-attribute"></a>MF \_ ReadWrite \_ habilitar \_ el \_ atributo de transformaciones de hardware

Permite al lector de código fuente o al escritor de receptores usar transformaciones de Media Foundation basadas en hardware (MFTs).

## <a name="data-type"></a>Tipo de datos

**UINT32**

## <a name="getset"></a>Obtener o establecer

Para obtener este atributo, llame a [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Para establecer este atributo, llame a [**IMFAttributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="remarks"></a>Observaciones

De forma predeterminada, el lector de origen y el escritor del receptor no usan descodificadores ni codificadores de hardware. Para habilitar el uso de MFTs de hardware, establezca este atributo en **true** al crear el lector de origen o el escritor del receptor.

Utilice este atributo con las siguientes funciones:

-   [**MFCreateSourceReaderFromByteStream**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrombytestream)
-   [**MFCreateSourceReaderFromMediaSource**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrommediasource)
-   [**MFCreateSourceReaderFromURL**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfromurl)
-   [**MFCreateSinkWriterFromMediaSink**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfrommediasink)
-   [**MFCreateSinkWriterFromURL**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfromurl)

Existe una excepción al comportamiento predeterminado. El lector de origen y el escritor de receptores usan automáticamente MFTs que se registran localmente en el proceso del llamador. Para registrar una MFT localmente, llame a [**MFTRegisterLocal**](/windows/desktop/api/mfapi/nf-mfapi-mftregisterlocal) o [**MFTRegisterLocalByCLSID**](/windows/desktop/api/mfapi/nf-mfapi-mftregisterlocalbyclsid). Los MFTs de hardware que se registran localmente se usan aunque no se haya establecido el atributo **MF \_ ReadWrite \_ habilitar \_ \_ transformaciones de hardware** .

Este atributo no afecta a la descodificación de vídeo acelerado por hardware que usa la aceleración de vídeo de DirectX (DXVA). Para habilitar la descodificación de DXVA en el lector de origen, establezca el atributo de [Administrador de D3D del \_ lector de origen \_ \_ \_ MF](mf-source-reader-d3d-manager.md) .

Si este atributo es **true**, no establezca el atributo [MF \_ ReadWrite \_ Disable \_ Converters](mf-readwrite-disable-converters.md) .

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
</dt> <dt>

[Atributos del lector de código fuente](source-reader-attributes.md)
</dt> </dl>

 

 




