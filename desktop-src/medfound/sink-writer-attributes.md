---
description: Atributos del escritor de receptor
ms.assetid: f27b9beb-f35f-400e-a337-50d9de21e91e
title: Atributos del escritor de receptor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e23dbca06c3ff1a4ac80b8e68413fdd0816d71a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155316"
---
# <a name="sink-writer-attributes"></a>Atributos del escritor de receptor

Los siguientes atributos se pueden usar para inicializar el escritor del receptor.



| Atributo                                                                                  | Descripción                                                                                                                                                                                                                        |
|--------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [\_baja \_ latencia de MF](mf-low-latency.md)                                                     | Habilita el procesamiento de baja latencia.                                                                                                                                                                                                    |
| [MF \_ ReadWrite \_ deshabilitar \_ convertidores](mf-readwrite-disable-converters.md)                  | Habilita o deshabilita las conversiones de formato del escritor del receptor.                                                                                                                                                                         |
| [MF \_ ReadWrite \_ habilitar \_ \_ transformaciones de hardware](mf-readwrite-enable-hardware-transforms.md) | Permite al escritor del receptor usar transformaciones de Media Foundation basadas en hardware (MFTs).                                                                                                                                                  |
| [\_devolución de \_ \_ llamada asincrónica de escritor del receptor MF \_](mf-sink-writer-async-callback.md)                     | Contiene un puntero a la interfaz de devolución de llamada de la aplicación para el escritor del receptor.                                                                                                                                                    |
| [\_limitación de \_ \_ deshabilitación de escritor de receptor MF \_](mf-sink-writer-disable-throttling.md)             | Especifica si el escritor del receptor limita la velocidad de los datos entrantes.                                                                                                                                                                |
| [\_CONTAINERTYPE de TRANSCODIFICACIÓN MF \_](mf-transcode-containertype.md)                             | Especifica el tipo de contenedor del archivo de salida.                                                                                                                                                                                   |
| [\_Atributo de \_ desbloqueo FIELDOFUSE de MFT \_](mft-fieldofuse-unlock-attribute.md)                  | Contiene un puntero [**IMFFieldOfUseMFTUnlock**](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock) , que se usa para desbloquear una MFT con restricciones de campo de uso. Para obtener más información, consulte el [campo de restricciones de uso](field-of-use-restrictions.md). |
| [\_Administrador de \_ D3D del escritor de receptores MF \_ \_](mf-sink-writer-d3d-manager.md)                           | Use este atributo para proporcionar un dispositivo Direct3D para cualquier codificador de vídeo o receptor de medios cargados por el escritor del receptor.                                                                                                                   |



 

Utilice estos atributos con los siguientes métodos y funciones:

-   [**IMFReadWriteClassFactory::CreateInstanceFromObject**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfreadwriteclassfactory-createinstancefromobject)
-   [**IMFReadWriteClassFactory::CreateInstanceFromURL**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfreadwriteclassfactory-createinstancefromurl)
-   [**MFCreateSinkWriterFromMediaSink**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfrommediasink)
-   [**MFCreateSinkWriterFromURL**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfromurl)

Para usar cualquiera de estos atributos, llame primero a [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) para crear un nuevo almacén de atributos. A continuación, use la interfaz [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) para establecer los atributos deseados en el almacén de atributos. Pase el puntero **IMFAttributes** al parámetro *pAttributes* de cualquiera de los métodos o funciones enumerados anteriormente.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**IMFSinkWriter**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsinkwriter)
</dt> <dt>

[Atributos de Media Foundation](media-foundation-attributes.md)
</dt> </dl>

 

 



