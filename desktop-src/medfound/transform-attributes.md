---
description: Transformar atributos
ms.assetid: 9beb1306-1378-499c-b9e1-c768a7b4c8bc
title: Transformar atributos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e68240f5341319db2b06ad6160cf8153f107eca9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127268676"
---
# <a name="transform-attributes"></a>Transformar atributos

Los atributos siguientes se aplican [a Media Foundation transformaciones automáticas](media-foundation-transforms.md) (MTA), a objetos [de](activation-objects.md) activación para MTA o a ambos.



| Atributo                                                                                                     | Descripción                                                                                                                                                                                   | Se aplica a                  |
|---------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| [**MF \_ ACTIVATE \_ MFT \_ LOCKED**](mf-activate-mft-locked-attribute.md)                                         | Especifica si el cargador de topologías cambiará los tipos de medios en un MFT.                                                                                                                  | MFT                        |
| [**MF \_ SA \_ D3D \_ AWARE**](mf-sa-d3d-aware-attribute.md)                                                       | Especifica si una transformación Media Foundation (MFT) admite la aceleración de vídeo de DirectX.                                                                                                     | MFT                        |
| [MF \_ TRANSFORM \_ ASYNC](mf-transform-async.md)                                                                | Especifica si un MFT realiza el procesamiento asincrónico.                                                                                                                                    | MFT                        |
| [DESBLOQUEO \_ ASINCRÓNICO DE TRANSFORMACIÓN DE \_ \_ MF](mf-transform-async-unlock.md)                                                 | Habilita el uso de un MFT asincrónico.                                                                                                                                                       | MFT                        |
| [Atributo MF \_ TRANSFORM \_ CATEGORY \_](mf-transform-category-attribute.md)                                     | Especifica la categoría de un MFT.                                                                                                                                                            | Objetos de activación de MFT      |
| [Atributo \_ MF TRANSFORM \_ FLAGS \_](mf-transform-flags-attribute.md)                                           | Contiene marcas para un objeto de activación de MFT.                                                                                                                                                  | Objetos de activación de MFT      |
| [Atributo DE CODEC DE MFT \_ \_ PARA LA \_ PROPIEDAD](mft-codec-merit-attribute.md)                                                 | Contiene el valor de la propiedad de un códec de hardware.                                                                                                                                                 | Objetos de activación de MFT      |
| [ATRIBUTO DE FLUJO \_ CONECTADO \_ DE \_ MFT](mft-connected-stream-attribute.md)                                       | Contiene un puntero a los atributos de secuencia de la secuencia conectada en un MFT basado en hardware.                                                                                                  | MFT                        |
| [MFT \_ CONECTADO A HW \_ \_ \_ STREAM](mft-connected-to-hw-stream.md)                                              | Especifica si un MFT basado en hardware está conectado a otro MFT basado en hardware.                                                                                                            | MFT                        |
| [EL DESCODIFICADOR DE MFT \_ EXPONE LOS TIPOS DE SALIDA EN ORDEN \_ \_ \_ \_ \_ \_ NATIVO](mft-decoder-expose-output-types-in-native-order.md) | Especifica si un descodificador expone tipos de salida IYUV/I420 (adecuados para la transcodificación) antes que otros formatos.                                                                                   | MFT                        |
| [SUGERENCIA DE RESOLUCIÓN \_ FINAL DE VÍDEO DEL \_ DESCODIFICADOR \_ \_ DE \_ MFT](mft-decoder-final-video-resolution-hint.md)                   | Especifica la resolución de salida final de la imagen descodificada, después del procesamiento de vídeo.                                                                                                           | MFT                        |
| [MFT \_ ENCODER ADMITE EL EVENTO \_ \_ CONFIG \_](mft-encoder-supports-config-event.md)                                | Especifica que el codificador MFT admite la recepción de [eventos MEEncodingParameter](meencodingparameters.md) durante el streaming.                                                                     | MFT                        |
| [LUID DEL \_ ADAPTADOR DE \_ ENUMERACIÓN \_ MFT](mft-enum-adapter-luid.md)                                                         | Especifica un identificador único para un adaptador de vídeo. Use este atributo al llamar a MFTEnum2 para enumerar los MFT asociados a un adaptador específico.                                             | MFT                        |
| [Atributo de dirección URL de hardware de MFT \_ ENUM \_ \_ \_](mft-enum-hardware-url-attribute.md)                                    | Contiene el vínculo simbólico para un MFT basado en hardware.                                                                                                                                          | Objetos de activación MFT/MFT |
| [Atributo de identificador de proveedor de hardware de MFT \_ ENUM \_ \_ \_ \_](mft-enum-hardware-vendor-id-attribute.md)                       | Especifica el identificador de proveedor para una transformación de Media Foundation hardware                                                                                                                       | MFT                        |
| [ATRIBUTO MFT \_ ENUM \_ TRANSCODE \_ ONLY \_](mft-enum-transcode-only-attribute.md)                                | Especifica si un descodificador está optimizado para transcodificación en lugar de para reproducción.                                                                                                            | MFT                        |
| [Atributo \_ MFT FIELDOFUSE \_ UNLOCK \_](mft-fieldofuse-unlock-attribute.md)                                     | Contiene un [**puntero DE TIPO IMFFieldOfUseMFTUnlock,**](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock) que se puede usar para desbloquear el MFT.                                                                            | Objetos de activación de MFT      |
| [Atributo MFT \_ FRIENDLY \_ NAME \_](mft-friendly-name-attribute.md)                                             | Contiene el nombre para mostrar de un MFT basado en hardware.                                                                                                                                           | Objetos de activación de MFT      |
| [Atributos de tipos \_ de entrada \_ de MFT \_](mft-input-types-attributes.md)                                               | Contiene los tipos de entrada registrados para un MFT.                                                                                                                                               | Objetos de activación de MFT      |
| [Atributos de tipos \_ de salida \_ de MFT \_](mft-output-types-attributes.md)                                             | Contiene los tipos de salida registrados para un MFT.                                                                                                                                              | Objetos de activación de MFT      |
| [PERFIL DE CODIFICADOR \_ \_ PREFERIDO DE \_ MFT](mft-preferred-encoder-profile.md)                                         | Contiene las propiedades de configuración de un codificador.                                                                                                                                             | Objetos de activación de MFT      |
| [Atributo MFT \_ PREFERRED \_ \_ OUTPUTTYPE](mft-preferred-outputtype-attribute.md)                               | Especifica el formato de salida preferido para un codificador.                                                                                                                                         | Objetos de activación de MFT      |
| [Atributo MFT \_ PREFERRED \_ \_ OUTPUTTYPE](mft-preferred-outputtype-attribute.md)                               | Especifica el formato de salida preferido para un codificador.                                                                                                                                         | Objetos de activación de MFT      |
| [Atributo \_ LOCAL DE PROCESO \_ de \_ MFT](mft-process-local-attribute.md)                                             | Especifica si un MFT solo se registra en el proceso de la aplicación.                                                                                                                     | Objetos de activación de MFT      |
| [MFT \_ REMUX \_ MARK \_ I \_ PICTURE \_ AS \_ CLEAN \_ POINT](mft-remux-mark-i-picture-as-clean-point.md)                 | Especifica si el archivo MFT de remux de vídeo H.264 debe marcar I pictures como punto limpio para mejorar la capacidad de búsqueda. Esto tiene la posibilidad de daños en las búsquedas en archivos MP4 finales no conformes. | Objetos de activación de MFT      |
| [MFT \_ SUPPORT \_ 3DVIDEO](mft-support-3dvideo.md)                                                              | Especifica si una transformación Media Foundation (MFT) admite vídeo estereocopiado 3D.                                                                                                          | Objetos de activación de MFT      |
| [**MFT \_ ADMITE EL CAMBIO DE FORMATO \_ \_ \_ DINÁMICO**](mft-support-dynamic-format-change-attribute.md)                  | Especifica si una transformación Media Foundation (MFT) admite cambios de formato dinámicos.                                                                                                         | MFT                        |
| [Atributo \_ CLSID de transformación de MFT \_ \_](mft-transform-clsid-attribute.md)                                         | Contiene el identificador de clase (CLSID) de un MFT.                                                                                                                                              | Objetos de activación de MFT      |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)
</dt> <dt>

[Media Foundation atributos](media-foundation-attributes.md)
</dt> <dt>

[Media Foundation transformaciones](media-foundation-transforms.md)
</dt> </dl>

 

 



