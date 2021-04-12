---
description: Atributos de descriptor de presentación
ms.assetid: 2a092a6a-956b-4c1f-955f-529ec08665fe
title: Atributos de descriptor de presentación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18bba97a0e0428bf2ceb91b04c79f69b557876a2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104543830"
---
# <a name="presentation-descriptor-attributes"></a>Atributos de descriptor de presentación

## <a name="common-presentation-descriptor-attributes"></a>Atributos de descriptor de presentación comunes

Los atributos siguientes pueden aplicarse a cualquier descriptor de presentación.



| Atributo                                                                          | Descripción                                                                                                                                     |
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| [**contexto de la \_ aplicación MF PD \_ \_**](mf-pd-app-context-attribute.md)                        | Contiene un puntero al descriptor de presentación de la ruta de acceso a medios protegidos (PMP).                                                          |
| [**\_velocidad de \_ bits de codificación de audio MF PD \_ \_**](mf-pd-audio-encoding-bitrate-attribute.md) | Especifica la velocidad de bits de codificación de audio de la presentación, en bits por segundo.                                                                 |
| [\_ISVARIABLEBITRATE de \_ audio MF PD \_](mf-pd-audio-isvariablebitrate.md)              | Especifica si las secuencias de audio de la presentación tienen una velocidad de bits variable.                                                               |
| [**duración de MF \_ PD \_**](mf-pd-duration-attribute.md)                               | Especifica la duración de una presentación, en unidades de 100-nanosegundos.                                                                              |
| [**\_hora de \_ última \_ modificación \_ de MF PD**](mf-pd-last-modified-time-attribute.md)         | Especifica cuándo se modificó por última vez una presentación.                                                                                                |
| [**\_ \_ tipo MIME PD de MF \_**](mf-pd-mime-type-attribute.md)                            | Especifica el tipo MIME del contenido.                                                                                                         |
| [\_ \_ hora límite de reproducción MF PD \_ \_](mf-pd-playback-boundary-time.md)               | La hora a la que debe comenzar la presentación, en relación con el inicio del origen del medio.                                                       |
| [\_identificador de \_ elemento de reproducción MF PD \_ \_](mf-pd-playback-element-id.md)                     | Identificador del elemento de lista de reproducción en la presentación.                                                                                     |
| [**\_contexto de \_ PMPHOST MF PD \_**](mf-pd-pmphost-context-attribute.md)                | Contiene un puntero al objeto de proxy para el descriptor de presentación de la aplicación.                                                           |
| [\_ \_ idioma preferido de MF PD \_](mf-pd-preferred-language.md)                        | Contiene el idioma RFC 1766 preferido del origen multimedia.                                                                                   |
| [**MF \_ PD \_ Sami \_ STYLELIST**](mf-pd-sami-stylelist-attribute.md)                  | Contiene el nombre descriptivo de los estilos de intercambio de medios accesibles (SAMI) sincronizados admitidos. Este atributo solo se aplica a los archivos SAMI. |
| [**\_ \_ Tamaño total de \_ archivo MF PD \_**](mf-pd-total-file-size-attribute.md)               | Especifica el tamaño total del archivo de código fuente, en bytes.                                                                                          |
| [**\_velocidad de \_ bits de codificación de vídeo MF PD \_ \_**](mf-pd-video-encoding-bitrate-attribute.md) | Especifica la velocidad de bits de codificación de vídeo de la presentación, en bits por segundo.                                                                 |



 

## <a name="presentation-descriptor-attributes-for-asf"></a>Atributos de descriptor de presentación para ASF

Los siguientes atributos se aplican a los descriptores de presentación para los archivos de formato de sistema avanzado (ASF).



| Atributo                                                                                                             | Descripción                                                                                          |
|-----------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [**MF \_ PD \_ ASF \_ CODECLIST**](mf-pd-asf-codeclist-attribute.md)                                                       | Contiene información acerca de los códecs que se usan para codificar el contenido de un archivo ASF.                     |
| [**ID. de CONTENTENCRYPTION de MF \_ PD \_ ASF \_ \_**](mf-pd-asf-contentencryption-keyid-attribute.md)                          | Especifica el identificador de clave para un archivo ASF cifrado.                                              |
| [**\_dirección URL de licencia MF PD \_ ASF \_ CONTENTENCRYPTION \_ \_**](mf-pd-asf-contentencryption-license-url-attribute.md)             | Especifica la dirección URL de adquisición de licencias para un archivo ASF cifrado.                                     |
| [**MF \_ PD \_ ASF \_ CONTENTENCRYPTION \_ \_ datos secretos**](mf-pd-asf-contentencryption-secret-data-attribute.md)             | Contiene datos secretos para un archivo ASF cifrado.                                                      |
| [**MF \_ PD \_ ASF \_ \_ tipo CONTENTENCRYPTION**](mf-pd-asf-contentencryption-type-attribute.md)                            | Especifica el tipo de mecanismo de protección usado en un archivo ASF.                                      |
| [**MF \_ PD \_ ASF \_ CONTENTENCRYPTIONEX \_ datos de cifrado \_**](mf-pd-asf-contentencryptionex-encryption-data-attribute.md) | Contiene los datos de cifrado de un archivo ASF.                                                            |
| [**\_longitud de \_ \_ datos ASF \_ de MF PD**](mf-pd-asf-data-length-attribute.md)                                                  | Especifica el tamaño, en bytes, de la sección de datos de un archivo ASF.                                    |
| [**\_desplazamiento de \_ \_ Inicio de datos ASF \_ \_ de MF PD**](mf-pd-asf-data-start-offset-attribute.md)                                     | Especifica el desplazamiento, en bytes, desde el inicio de un archivo ASF hasta el inicio del primer paquete de datos. |
| [**MF \_ PD \_ ASF \_ \_ hora de creación FILEPROPERTIES \_**](mf-pd-asf-fileproperties-creation-time-attribute.md)               | Especifica la fecha y hora en que se creó inicialmente un archivo ASF.                                  |
| [**MF \_ PD \_ ASF \_ FILEPROPERTIES \_ \_ ID. de archivo**](mf-pd-asf-fileproperties-file-id-attribute.md)                           | Especifica el identificador de archivo de un archivo ASF.                                                        |
| [**etiquetas FILEPROPERTIES de MF \_ PD \_ ASF \_ \_**](mf-pd-asf-fileproperties-flags-attribute.md)                                | Contiene marcas misceláneas de un encabezado ASF.                                                     |
| [**MF \_ PD \_ ASF \_ FILEPROPERTIES \_ de \_ velocidad de bits máxima**](mf-pd-asf-fileproperties-max-bitrate-attribute.md)                   | Especifica la velocidad de bits instantánea máxima, en bits por segundo, de un archivo ASF.                   |
| [**MF \_ PD \_ ASF \_ FILEPROPERTIES \_ tamaño máximo de \_ paquete \_**](mf-pd-asf-fileproperties-max-packet-size-attribute.md)          | Especifica el tamaño máximo de paquete, en bytes, para un archivo ASF.                                         |
| [**MF \_ PD \_ ASF \_ FILEPROPERTIES \_ min \_ Packet \_ size**](mf-pd-asf-fileproperties-min-packet-size-attribute.md)          | Especifica el tamaño mínimo de paquete, en bytes, para un archivo ASF.                                        |
| [**\_ \_ \_ paquetes FILEPROPERTIES MF de \_ ASF**](mf-pd-asf-fileproperties-packets-attribute.md)                            | Especifica el número de paquetes en la sección de datos de un archivo ASF.                                  |
| [**MF \_ PD \_ ASF \_ FILEPROPERTIES \_ \_ duración de la reproducción**](mf-pd-asf-fileproperties-play-duration-attribute.md)               | Especifica el tiempo necesario para reproducir un archivo ASF, en unidades de 100-nanosegundos.                              |
| [**preFILEPROPERTIES MF \_ PD \_ ASF \_ \_**](mf-pd-asf-fileproperties-preroll-attribute.md)                            | Especifica la cantidad de tiempo de almacenamiento en búfer de los datos antes de empezar a reproducir un archivo ASF, en milisegundos.    |
| [**MF \_ PD \_ ASF \_ FILEPROPERTIES \_ duración del envío \_**](mf-pd-asf-fileproperties-send-duration-attribute.md)               | Especifica el tiempo necesario para enviar un archivo ASF, en unidades de 100-nanosegundos.                              |
| [**MF \_ PD \_ ASF \_ info \_ tiene \_ audio**](mf-pd-asf-info-has-audio-attribute.md)                                           | Especifica si un archivo ASF contiene al menos una secuencia de audio.                                    |
| [**MF \_ PD \_ ASF \_ info \_ tiene \_ \_ vídeo no audio \_**](mf-pd-asf-info-has-non-audio-video-attribute.md)                     | Especifica si un archivo ASF contiene cualquier secuencia que no sea de audio y que no sea de vídeo.                             |
| [**MF \_ PD \_ ASF \_ info \_ tiene \_ vídeo**](mf-pd-asf-info-has-video-attribute.md)                                           | Especifica si un archivo ASF contiene al menos una secuencia de vídeo.                                    |
| [**MF \_ PD \_ ASF \_ LANGLIST**](mf-pd-asf-langlist-attribute.md)                                                         | Especifica la lista de idiomas utilizados en un archivo ASF.                                                 |
| [MF \_ PD \_ ASF \_ LANGLIST \_ LEGACYORDER](mf-pd-asf-langlist-legacyorder.md)                                              | Contiene una lista de los lenguajes RFC 1766 usados en la presentación actual.                              |
| [**\_marcador MF PD \_ ASF \_**](mf-pd-asf-marker-attribute.md)                                                             | Especifica los marcadores de un archivo ASF.                                                                |
| [**los \_ \_ metadatos ASF de MF PD \_ \_ son \_ VBR**](mf-pd-asf-metadata-is-vbr-attribute.md)                                         | Especifica si un archivo ASF utiliza codificación de velocidad de bits variable (VBR).                                 |
| [**\_pares de \_ \_ \_ \_ cubos de pérdida de metadatos ASF de MF PD \_**](mf-pd-asf-metadata-leaky-bucket-pairs-attribute.md)                | Describe los requisitos de almacenamiento en búfer para un archivo ASF de VBR.                                             |
| [**MF \_ PD \_ ASF \_ Metadata \_ V8 \_ BUFFERAVERAGE**](mf-pd-asf-metadata-v8-bufferaverage-attribute.md)                     | Especifica el tamaño de búfer promedio necesario para un archivo ASF de VBR.                                         |
| [**MF \_ PD \_ ASF \_ Metadata \_ V8 \_ VBRPEAK**](mf-pd-asf-metadata-v8-vbrpeak-attribute.md)                                 | Especifica la velocidad de bits más alta en un archivo ASF de VBR.                                          |
| [**\_ \_ comando ASF de MF PD \_**](mf-pd-asf-script-attribute.md)                                                             | Especifica los comandos de script en un archivo ASF.                                                        |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Atributos de Media Foundation](media-foundation-attributes.md)
</dt> <dt>

[Descriptores de presentación](presentation-descriptors.md)
</dt> <dt>

[**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> </dl>

 

 



