---
description: Atributos del escritor de receptores
ms.assetid: f27b9beb-f35f-400e-a337-50d9de21e91e
title: Atributos del escritor de receptores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e23dbca06c3ff1a4ac80b8e68413fdd0816d71a5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127574765"
---
# <a name="sink-writer-attributes"></a>Atributos del escritor de receptores

Los atributos siguientes se pueden usar para inicializar el escritor de receptores.



| Atributo                                                                                  | Descripción                                                                                                                                                                                                                        |
|--------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MF \_ LOW \_ LATENCY](mf-low-latency.md)                                                     | Habilita el procesamiento de baja latencia.                                                                                                                                                                                                    |
| [MF \_ READWRITE \_ DISABLE \_ CONVERTERS](mf-readwrite-disable-converters.md)                  | Habilita o deshabilita las conversiones de formato del escritor receptor.                                                                                                                                                                         |
| [MF \_ READWRITE \_ HABILITA LAS \_ TRANSFORMACIONES DE \_ HARDWARE](mf-readwrite-enable-hardware-transforms.md) | Permite que el escritor de receptores use transformaciones de Media Foundation basadas en hardware (MFT).                                                                                                                                                  |
| [DEVOLUCIÓN DE LLAMADA ASINCRÓNICA DE MF \_ SINK \_ WRITER \_ \_](mf-sink-writer-async-callback.md)                     | Contiene un puntero a la interfaz de devolución de llamada de la aplicación para el escritor de receptores.                                                                                                                                                    |
| [MF \_ SINK \_ WRITER \_ DISABLE \_ THROTTLING](mf-sink-writer-disable-throttling.md)             | Especifica si el escritor de receptores limita la velocidad de los datos entrantes.                                                                                                                                                                |
| [MF \_ TRANSCODE \_ CONTAINERTYPE](mf-transcode-containertype.md)                             | Especifica el tipo de contenedor del archivo de salida.                                                                                                                                                                                   |
| [Atributo \_ MFT FIELDOFUSE \_ UNLOCK \_](mft-fieldofuse-unlock-attribute.md)                  | Contiene un [**puntero IMFFieldOfUseMFTUnlock,**](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock) que se usa para desbloquear un MFT con restricciones de campo de uso. Para obtener más información, vea [Restricciones de campo de uso.](field-of-use-restrictions.md) |
| [MF \_ SINK \_ WRITER \_ D3D \_ MANAGER](mf-sink-writer-d3d-manager.md)                           | Use este atributo para proporcionar un dispositivo Direct3D para los codificadores de vídeo o receptores multimedia cargados por el escritor del receptor.                                                                                                                   |



 

Use estos atributos con los métodos y funciones siguientes:

-   [**IMFReadWriteClassFactory::CreateInstanceFromObject**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfreadwriteclassfactory-createinstancefromobject)
-   [**IMFReadWriteClassFactory::CreateInstanceFromURL**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfreadwriteclassfactory-createinstancefromurl)
-   [**MFCreateSinkWriterFromMediaSink**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfrommediasink)
-   [**MFCreateSinkWriterFromURL**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfromurl)

Para usar cualquiera de estos atributos, primero llame a [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) para crear un nuevo almacén de atributos. A continuación, use [**la interfaz IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) para establecer los atributos deseados en el almacén de atributos. Pase el **puntero DEATTRIBUTEAttributes** al *parámetro pAttributes* de cualquiera de los métodos o funciones enumerados anteriormente.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**IMFSinkWriter**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsinkwriter)
</dt> <dt>

[Media Foundation atributos](media-foundation-attributes.md)
</dt> </dl>

 

 



