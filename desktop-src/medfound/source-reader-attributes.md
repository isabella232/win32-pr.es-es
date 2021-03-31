---
description: Atributos del lector de código fuente
ms.assetid: 312a588a-848b-4563-893a-fac49a4ca465
title: Atributos del lector de código fuente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f425710139b2aebf23ff13a2593ba6931c78fe2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103811546"
---
# <a name="source-reader-attributes"></a>Atributos del lector de código fuente

Los siguientes atributos se pueden usar para inicializar el [lector de origen](source-reader.md).



| Atributo                                                                                                            | Descripción                                                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [\_baja \_ latencia de MF](mf-low-latency.md)                                                                               | Habilita el procesamiento de baja latencia.                                                                                                                                                                                                    |
| [MF \_ ReadWrite \_ deshabilitar \_ convertidores](mf-readwrite-disable-converters.md)                                            | Habilita o deshabilita las conversiones de formato del lector de código fuente.                                                                                                                                                                       |
| [MF \_ ReadWrite \_ habilitar \_ \_ transformaciones de hardware](mf-readwrite-enable-hardware-transforms.md)                           | Permite al lector de código fuente usar transformaciones de Media Foundation basadas en hardware (MFTs).                                                                                                                                                |
| [\_devolución de \_ \_ llamada asincrónica del lector de origen MF \_](mf-source-reader-async-callback.md)                                           | Contiene un puntero a la interfaz de devolución de llamada de la aplicación para el lector de origen.                                                                                                                                                  |
| [\_Administrador de \_ D3D de lector de origen MF \_ \_](mf-source-reader-d3d-manager.md)                                                 | Contiene un puntero al Administrador de dispositivos de Microsoft [Direct3D](direct3d-device-manager.md).                                                                                                                                        |
| [\_lector de origen MF \_ \_ deshabilitar \_ DXVA](mf-source-reader-disable-dxva.md)                                               | Especifica si el lector de origen habilita la aceleración de vídeo DirectX (DXVA) en el descodificador de vídeo.                                                                                                                                |
| [el \_ \_ lector de origen MF \_ desconecta \_ MEDIASOURCE \_ al \_ apagarse](mf-source-reader-disconnect-mediasource-on-shutdown.md) | Especifica si el lector de origen cierra el origen del medio.<br/> Solo se aplica cuando la aplicación crea el lector de origen a partir de un objeto de origen multimedia existente.<br/>                                           |
| [\_lector de código fuente MF \_ Habilitar el \_ \_ \_ procesamiento de vídeo avanzado \_](mf-source-reader-enable-advanced-video-processing.md)     | Permite el procesamiento de vídeo avanzado por el [lector de origen](source-reader.md), incluida la conversión del espacio de colores, el desentrelazado, el cambio de tamaño de vídeo y la conversión de velocidad de fotogramas.                                                           |
| [\_lector de código fuente MF \_ Habilitar el \_ \_ procesamiento de vídeo \_](mf-source-reader-enable-video-processing.md)                        | Habilita el procesamiento de vídeo limitado por el lector de origen.                                                                                                                                                                             |
| [\_configuración de \_ MEDIASOURCE del lector de origen MF \_ \_](mf-source-reader-mediasource-config.md)                                   | Contiene las propiedades de configuración para el origen de medios.                                                                                                                                                                            |
| [\_Atributo de \_ desbloqueo FIELDOFUSE de MFT \_](mft-fieldofuse-unlock-attribute.md)                                            | Contiene un puntero [**IMFFieldOfUseMFTUnlock**](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock) , que se usa para desbloquear una MFT con restricciones de campo de uso. Para obtener más información, consulte el [campo de restricciones de uso](field-of-use-restrictions.md). |



 

Utilice estos atributos con los siguientes métodos y funciones:

-   [**IMFReadWriteClassFactory::CreateInstanceFromObject**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfreadwriteclassfactory-createinstancefromobject)
-   [**IMFReadWriteClassFactory::CreateInstanceFromURL**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfreadwriteclassfactory-createinstancefromurl)
-   [**MFCreateSourceReaderFromByteStream**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrombytestream)
-   [**MFCreateSourceReaderFromMediaSource**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrommediasource)
-   [**MFCreateSourceReaderFromURL**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfromurl)

Para usar cualquiera de estos atributos, llame primero a [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) para crear un nuevo almacén de atributos. A continuación, use la interfaz [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) para establecer los atributos deseados en el almacén de atributos. Pase el puntero **IMFAttributes** al parámetro *pAttributes* de cualquiera de los métodos o funciones enumerados anteriormente.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Atributos de Media Foundation](media-foundation-attributes.md)
</dt> <dt>

[Lector de origen](source-reader.md)
</dt> <dt>

[**IMFSourceReader**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereader)
</dt> </dl>

 

 




