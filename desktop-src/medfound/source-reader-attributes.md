---
description: Atributos del lector de origen
ms.assetid: 312a588a-848b-4563-893a-fac49a4ca465
title: Atributos del lector de origen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a7bd9c5b3c5a71fb1b91515400fb0cf3670bd3b73b6635c811dcc79bd05e74f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118238333"
---
# <a name="source-reader-attributes"></a>Atributos del lector de origen

Los atributos siguientes se pueden usar para inicializar el [lector de origen.](source-reader.md)



| Atributo                                                                                                            | Descripción                                                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MF \_ LOW \_ LATENCY](mf-low-latency.md)                                                                               | Habilita el procesamiento de baja latencia.                                                                                                                                                                                                    |
| [MF \_ READWRITE \_ DISABLE \_ CONVERTERS](mf-readwrite-disable-converters.md)                                            | Habilita o deshabilita las conversiones de formato por el lector de origen.                                                                                                                                                                       |
| [MF \_ READWRITE \_ HABILITA LAS \_ TRANSFORMACIONES DE \_ HARDWARE](mf-readwrite-enable-hardware-transforms.md)                           | Permite que el lector de origen use transformaciones de Media Foundation basadas en hardware (MTA).                                                                                                                                                |
| [DEVOLUCIÓN DE LLAMADA ASINCRÓNICA DEL LECTOR \_ \_ DE ORIGEN \_ \_ DE MF](mf-source-reader-async-callback.md)                                           | Contiene un puntero a la interfaz de devolución de llamada de la aplicación para el lector de origen.                                                                                                                                                  |
| [MF \_ SOURCE \_ READER \_ D3D \_ MANAGER](mf-source-reader-d3d-manager.md)                                                 | Contiene un puntero a microsoft [direct3D Administrador de dispositivos](direct3d-device-manager.md).                                                                                                                                        |
| [MF \_ SOURCE \_ READER \_ DISABLE \_ DXVA](mf-source-reader-disable-dxva.md)                                               | Especifica si el lector de origen habilita la aceleración de vídeo directX (DXVA) en el descodificador de vídeo.                                                                                                                                |
| [MF \_ SOURCE \_ READER \_ DISCONNECT \_ MEDIASOURCE \_ ON \_ SHUTDOWN](mf-source-reader-disconnect-mediasource-on-shutdown.md) | Especifica si el lector de origen apaga el origen multimedia.<br/> Solo se aplica cuando la aplicación crea el lector de origen a partir de un objeto de origen multimedia existente.<br/>                                           |
| [MF \_ SOURCE READER HABILITA EL PROCESAMIENTO AVANZADO DE \_ \_ \_ \_ \_ VÍDEO](mf-source-reader-enable-advanced-video-processing.md)     | Habilita el procesamiento avanzado de vídeo mediante el Lector de [origen,](source-reader.md)incluida la conversión de espacio de color, el desinterlazado, el cambio de tamaño de vídeo y la conversión de velocidad de fotogramas.                                                           |
| [MF \_ SOURCE \_ READER \_ ENABLE \_ VIDEO \_ PROCESSING](mf-source-reader-enable-video-processing.md)                        | Habilita el procesamiento de vídeo limitado por el lector de origen.                                                                                                                                                                             |
| [MF \_ SOURCE \_ READER \_ MEDIASOURCE \_ CONFIG](mf-source-reader-mediasource-config.md)                                   | Contiene las propiedades de configuración para el origen de medios.                                                                                                                                                                            |
| [Atributo \_ MFT FIELDOFUSE \_ UNLOCK \_](mft-fieldofuse-unlock-attribute.md)                                            | Contiene un [**puntero IMFFieldOfUseMFTUnlock,**](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock) que se usa para desbloquear un MFT con restricciones de campo de uso. Para obtener más información, vea [Restricciones de campo de uso.](field-of-use-restrictions.md) |



 

Use estos atributos con los métodos y funciones siguientes:

-   [**IMFReadWriteClassFactory::CreateInstanceFromObject**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfreadwriteclassfactory-createinstancefromobject)
-   [**IMFReadWriteClassFactory::CreateInstanceFromURL**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfreadwriteclassfactory-createinstancefromurl)
-   [**MFCreateSourceReaderFromByteStream**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrombytestream)
-   [**MFCreateSourceReaderFromMediaSource**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrommediasource)
-   [**MFCreateSourceReaderFromURL**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfromurl)

Para usar cualquiera de estos atributos, primero llame a [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) para crear un nuevo almacén de atributos. A continuación, use [**la interfaz IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) para establecer los atributos deseados en el almacén de atributos. Pase el **puntero DEATTRIBUTEAttributes** al *parámetro pAttributes* de cualquiera de los métodos o funciones enumerados anteriormente.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Media Foundation atributos](media-foundation-attributes.md)
</dt> <dt>

[Lector de origen](source-reader.md)
</dt> <dt>

[**IMFSourceReader**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereader)
</dt> </dl>

 

 




