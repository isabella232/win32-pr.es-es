---
description: Atributos de transformación
ms.assetid: 9beb1306-1378-499c-b9e1-c768a7b4c8bc
title: Atributos de transformación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e68240f5341319db2b06ad6160cf8153f107eca9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497758"
---
# <a name="transform-attributes"></a>Atributos de transformación

Los siguientes atributos se aplican a las [transformaciones Media Foundation](media-foundation-transforms.md) (MFTs) o a los [objetos de activación](activation-objects.md) de MFTs, o a ambos.



| Atributo                                                                                                     | Descripción                                                                                                                                                                                   | Se aplica a                  |
|---------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| [**MF \_ activar \_ MFT \_ bloqueado**](mf-activate-mft-locked-attribute.md)                                         | Especifica si el cargador de topología cambiará los tipos de medios en una MFT.                                                                                                                  | MFTs                        |
| [**Compatible con el D3D de MF \_ SA \_ \_**](mf-sa-d3d-aware-attribute.md)                                                       | Especifica si una transformación de Media Foundation (MFT) es compatible con la aceleración de vídeo de DirectX.                                                                                                     | MFTs                        |
| [MF \_ transformación \_ asincrónica](mf-transform-async.md)                                                                | Especifica si un MFT realiza el procesamiento asincrónico.                                                                                                                                    | MFTs                        |
| [\_desbloqueo asincrónico de transformación MF \_ \_](mf-transform-async-unlock.md)                                                 | Habilita el uso de una MFT asincrónica.                                                                                                                                                       | MFTs                        |
| [MF \_ ( \_ atributo de categoría de transformación) \_](mf-transform-category-attribute.md)                                     | Especifica la categoría de un MFT.                                                                                                                                                            | Objetos de activación de MFT      |
| [MF \_ Transform \_ Flags ( \_ atributo)](mf-transform-flags-attribute.md)                                           | Contiene marcas para un objeto de activación de MFT.                                                                                                                                                  | Objetos de activación de MFT      |
| [\_Atributo de \_ mérito del códec MFT \_](mft-codec-merit-attribute.md)                                                 | Contiene el valor de mérito de un códec de hardware.                                                                                                                                                 | Objetos de activación de MFT      |
| [atributo de secuencia de MFT \_ conectado \_ \_](mft-connected-stream-attribute.md)                                       | Contiene un puntero a los atributos de secuencia de la secuencia conectada en un MFT basado en hardware.                                                                                                  | MFTs                        |
| [MFT \_ conectado \_ al \_ flujo de HW \_](mft-connected-to-hw-stream.md)                                              | Especifica si un MFT basado en hardware está conectado a otro MFT basado en hardware.                                                                                                            | MFTs                        |
| [el \_ DEScodificador \_ de MFT expone \_ \_ tipos \_ de salida en \_ \_ orden nativo](mft-decoder-expose-output-types-in-native-order.md) | Especifica si un descodificador expone los tipos de salida IYUV/i420 (adecuados para la transcodificación) antes de otros formatos.                                                                                   | MFTs                        |
| [\_sugerencia de resolución de \_ vídeo final del \_ \_ DEScodificador de MFT \_](mft-decoder-final-video-resolution-hint.md)                   | Especifica la resolución de salida final de la imagen descodificada, después del procesamiento de vídeo.                                                                                                           | MFTs                        |
| [el \_ codificador MFT \_ admite \_ el \_ evento de configuración](mft-encoder-supports-config-event.md)                                | Especifica que el codificador MFT admite la recepción de eventos [MEEncodingParameter](meencodingparameters.md) durante el streaming.                                                                     | MFTs                        |
| [\_LUID de adaptador de enumeración de MFT \_ \_](mft-enum-adapter-luid.md)                                                         | Especifica un identificador único para un adaptador de vídeo. Use este atributo al llamar a MFTEnum2 para enumerar MFTs asociados a un adaptador específico.                                             | MFTs                        |
| [\_Atributo de \_ \_ dirección URL de hardware enum de MFT \_](mft-enum-hardware-url-attribute.md)                                    | Contiene el vínculo simbólico para un MFT basado en hardware.                                                                                                                                          | Objetos de activación de MFTs/MFT |
| [\_Atributo de \_ \_ identificador de proveedor de hardware de ENUMERAción de \_ MFT \_](mft-enum-hardware-vendor-id-attribute.md)                       | Especifica el identificador de proveedor para una transformación de Media Foundation basada en hardware.                                                                                                                       | MFTs                        |
| [\_atributo de \_ solo Unicode de enumeración de \_ MFT \_](mft-enum-transcode-only-attribute.md)                                | Especifica si un descodificador está optimizado para la transcodificación en lugar de para la reproducción.                                                                                                            | MFTs                        |
| [\_Atributo de \_ desbloqueo FIELDOFUSE de MFT \_](mft-fieldofuse-unlock-attribute.md)                                     | Contiene un puntero [**IMFFieldOfUseMFTUnlock**](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock) , que se puede usar para desbloquear la MFT.                                                                            | Objetos de activación de MFT      |
| [\_Atributo de \_ nombre \_ descriptivo de MFT](mft-friendly-name-attribute.md)                                             | Contiene el nombre para mostrar de un MFT basado en hardware.                                                                                                                                           | Objetos de activación de MFT      |
| [\_Atributos de \_ tipos de entrada de MFT \_](mft-input-types-attributes.md)                                               | Contiene los tipos de entrada registrados para una MFT.                                                                                                                                               | Objetos de activación de MFT      |
| [\_Atributos de \_ tipos de salida de MFT \_](mft-output-types-attributes.md)                                             | Contiene los tipos de salida registrados para una MFT.                                                                                                                                              | Objetos de activación de MFT      |
| [\_Perfil de \_ codificador preferido de MFT \_](mft-preferred-encoder-profile.md)                                         | Contiene las propiedades de configuración de un codificador.                                                                                                                                             | Objetos de activación de MFT      |
| [\_ \_ Atributo OUTPUTTYPE preferido de MFT \_](mft-preferred-outputtype-attribute.md)                               | Especifica el formato de salida preferido para un codificador.                                                                                                                                         | Objetos de activación de MFT      |
| [\_ \_ Atributo OUTPUTTYPE preferido de MFT \_](mft-preferred-outputtype-attribute.md)                               | Especifica el formato de salida preferido para un codificador.                                                                                                                                         | Objetos de activación de MFT      |
| [\_ \_ Atributo local de proceso de MFT \_](mft-process-local-attribute.md)                                             | Especifica si un MFT solo está registrado en el proceso de la aplicación.                                                                                                                     | Objetos de activación de MFT      |
| [\_REMUX \_ de MFT marca \_ I \_ imagen \_ como \_ \_ punto limpio](mft-remux-mark-i-picture-as-clean-point.md)                 | Especifica si el Remux de vídeo H. 264 debe marcar las imágenes como punto limpio para mejorar la capacidad de búsqueda. Esto tiene la posibilidad de que se produzcan daños en las búsquedas en archivos MP4 finales no conformes. | Objetos de activación de MFT      |
| [\_Compatibilidad con MFT \_ 3DVIDEO](mft-support-3dvideo.md)                                                              | Especifica si una transformación de Media Foundation (MFT) admite vídeo Stereoscopic 3D.                                                                                                          | Objetos de activación de MFT      |
| [**la MFT \_ admite el \_ \_ cambio de formato dinámico \_**](mft-support-dynamic-format-change-attribute.md)                  | Especifica si una transformación de Media Foundation (MFT) admite cambios de formato dinámico.                                                                                                         | MFTs                        |
| [\_ \_ Atributo CLSID de transformación de MFT \_](mft-transform-clsid-attribute.md)                                         | Contiene el identificador de clase (CLSID) de un MFT.                                                                                                                                              | Objetos de activación de MFT      |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)
</dt> <dt>

[Atributos de Media Foundation](media-foundation-attributes.md)
</dt> <dt>

[Media Foundation transformaciones](media-foundation-transforms.md)
</dt> </dl>

 

 



