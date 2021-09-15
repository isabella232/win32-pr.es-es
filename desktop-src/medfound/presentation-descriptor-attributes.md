---
description: Atributos del descriptor de presentación
ms.assetid: 2a092a6a-956b-4c1f-955f-529ec08665fe
title: Atributos del descriptor de presentación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18bba97a0e0428bf2ceb91b04c79f69b557876a2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127474045"
---
# <a name="presentation-descriptor-attributes"></a>Atributos del descriptor de presentación

## <a name="common-presentation-descriptor-attributes"></a>Atributos comunes del descriptor de presentación

Los atributos siguientes se pueden aplicar a cualquier descriptor de presentación.



| Atributo                                                                          | Descripción                                                                                                                                     |
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CONTEXTO \_ DE APLICACIÓN DE PD DE \_ \_ MF**](mf-pd-app-context-attribute.md)                        | Contiene un puntero al descriptor de presentación desde la ruta de acceso multimedia protegida (PMP).                                                          |
| [**VELOCIDAD \_ DE BITS DE \_ CODIFICACIÓN DE AUDIO \_ MF \_ PD**](mf-pd-audio-encoding-bitrate-attribute.md) | Especifica la velocidad de bits de codificación de audio para la presentación, en bits por segundo.                                                                 |
| [MF \_ PD \_ AUDIO \_ ISVARIABLEBITRATE](mf-pd-audio-isvariablebitrate.md)              | Especifica si las secuencias de audio de la presentación tienen una velocidad de bits variable.                                                               |
| [**DURACIÓN \_ DEL PD \_ DE MF**](mf-pd-duration-attribute.md)                               | Especifica la duración de una presentación, en unidades de 100 nanosegundos.                                                                              |
| [**HORA \_ DE ÚLTIMA MODIFICACIÓN \_ \_ DE MF PD \_**](mf-pd-last-modified-time-attribute.md)         | Especifica cuándo se modificó por última vez una presentación.                                                                                                |
| [**TIPO \_ MIME MF PD \_ \_**](mf-pd-mime-type-attribute.md)                            | Especifica el tipo MIME del contenido.                                                                                                         |
| [HORA LÍMITE \_ DE REPRODUCCIÓN DE MF PD \_ \_ \_](mf-pd-playback-boundary-time.md)               | Hora a la que debe comenzar la presentación, en relación con el inicio del origen multimedia.                                                       |
| [ID. \_ DE ELEMENTO DE REPRODUCCIÓN DE MF \_ \_ \_ PD](mf-pd-playback-element-id.md)                     | Identificador del elemento de lista de reproducción de la presentación.                                                                                     |
| [**CONTEXTO \_ DE \_ PMPHOST de MF PD \_**](mf-pd-pmphost-context-attribute.md)                | Contiene un puntero al objeto proxy para el descriptor de presentación de la aplicación.                                                           |
| [MF \_ PD \_ PREFERRED \_ LANGUAGE](mf-pd-preferred-language.md)                        | Contiene el idioma RFC 1766 preferido del origen multimedia.                                                                                   |
| [**MF \_ PD \_ SAMI \_ STYLELIST**](mf-pd-sami-stylelist-attribute.md)                  | Contiene el nombre descriptivo de los estilos de intercambio multimedia accesible sincronizado (SAMI) admitidos. Este atributo solo se aplica a los archivos SAMI. |
| [**TAMAÑO \_ TOTAL DE ARCHIVO DE MF \_ PD \_ \_**](mf-pd-total-file-size-attribute.md)               | Especifica el tamaño total del archivo de origen, en bytes.                                                                                          |
| [**VELOCIDAD \_ DE BITS DE \_ \_ CODIFICACIÓN DE VÍDEO MF \_ PD**](mf-pd-video-encoding-bitrate-attribute.md) | Especifica la velocidad de bits de codificación de vídeo para la presentación, en bits por segundo.                                                                 |



 

## <a name="presentation-descriptor-attributes-for-asf"></a>Atributos del descriptor de presentación para ASF

Los atributos siguientes se aplican a los descriptores de presentación para los archivos de formato de sistemas avanzados (ASF).



| Atributo                                                                                                             | Descripción                                                                                          |
|-----------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [**MF \_ PD \_ ASF \_ CODECLIST**](mf-pd-asf-codeclist-attribute.md)                                                       | Contiene información sobre los códecs usados para codificar el contenido en un archivo ASF.                     |
| [**MF \_ PD \_ ASF \_ CONTENTENCRYPTION \_ KEYID**](mf-pd-asf-contentencryption-keyid-attribute.md)                          | Especifica el identificador de clave para un archivo ASF cifrado.                                              |
| [**DIRECCIÓN \_ URL DE LICENCIA DE \_ \_ CONTENTENCRYPTION \_ DE \_ MF PD ASF**](mf-pd-asf-contentencryption-license-url-attribute.md)             | Especifica la dirección URL de adquisición de licencias para un archivo ASF cifrado.                                     |
| [**DATOS \_ SECRETOS \_ DE \_ CONTENTENCRYPTION \_ DE MF PD ASF \_**](mf-pd-asf-contentencryption-secret-data-attribute.md)             | Contiene datos secretos para un archivo ASF cifrado.                                                      |
| [**MF \_ PD \_ ASF \_ CONTENTENCRYPTION \_ TYPE**](mf-pd-asf-contentencryption-type-attribute.md)                            | Especifica el tipo de mecanismo de protección utilizado en un archivo ASF.                                      |
| [**MF \_ PD \_ ASF \_ CONTENTENCRYPTIONEX \_ ENCRYPTION \_ DATA**](mf-pd-asf-contentencryptionex-encryption-data-attribute.md) | Contiene datos de cifrado para un archivo ASF.                                                            |
| [**LONGITUD \_ DE DATOS DE \_ ASF de MF PD \_ \_**](mf-pd-asf-data-length-attribute.md)                                                  | Especifica el tamaño, en bytes, de la sección de datos de un archivo ASF.                                    |
| [**DESPLAZAMIENTO \_ DE INICIO DE DATOS DE \_ ASF de MF PD \_ \_ \_**](mf-pd-asf-data-start-offset-attribute.md)                                     | Especifica el desplazamiento, en bytes, desde el inicio de un archivo ASF hasta el inicio del primer paquete de datos. |
| [**MF \_ PD \_ ASF \_ FILEPROPERTIES \_ CREATION \_ TIME**](mf-pd-asf-fileproperties-creation-time-attribute.md)               | Especifica la fecha y hora en que se creó inicialmente un archivo ASF.                                  |
| [**MF \_ PD \_ ASF \_ FILEPROPERTIES \_ FILE \_ ID**](mf-pd-asf-fileproperties-file-id-attribute.md)                           | Especifica el identificador de archivo de un archivo ASF.                                                        |
| [**MF \_ PD \_ ASF \_ FILEPROPERTIES \_ FLAGS**](mf-pd-asf-fileproperties-flags-attribute.md)                                | Contiene varias marcas de un encabezado ASF.                                                     |
| [**MF \_ PD \_ ASF \_ FILEPROPERTIES \_ MAX \_ BITRATE**](mf-pd-asf-fileproperties-max-bitrate-attribute.md)                   | Especifica la velocidad de bits instantánea máxima, en bits por segundo, para un archivo ASF.                   |
| [**ARCHIVO \_ \_ ASF MF \_ PDPROPIEDADES \_ TAMAÑO MÁXIMO DE \_ \_ PAQUETES**](mf-pd-asf-fileproperties-max-packet-size-attribute.md)          | Especifica el tamaño máximo del paquete, en bytes, para un archivo ASF.                                         |
| [**ARCHIVO \_ \_ ASF MF \_ PDPROPIEDADES \_ TAMAÑO MÍNIMO DE \_ \_ PAQUETE**](mf-pd-asf-fileproperties-min-packet-size-attribute.md)          | Especifica el tamaño mínimo del paquete, en bytes, para un archivo ASF.                                        |
| [**PAQUETES \_ \_ FILEPROPERTIES DE ASF DE MF PD \_ \_**](mf-pd-asf-fileproperties-packets-attribute.md)                            | Especifica el número de paquetes en la sección de datos de un archivo ASF.                                  |
| [**DURACIÓN \_ DE REPRODUCCIÓN DE FILEPROPERTIES DE MF PD \_ ASF \_ \_ \_**](mf-pd-asf-fileproperties-play-duration-attribute.md)               | Especifica el tiempo necesario para reproducir un archivo ASF, en unidades de 100 nanosegundos.                              |
| [**MF \_ PD \_ ASF \_ FILEPROPERTIES \_ PREROLL**](mf-pd-asf-fileproperties-preroll-attribute.md)                            | Especifica la cantidad de tiempo para almacenar en búfer los datos antes de empezar a reproducir un archivo ASF, en milisegundos.    |
| [**DURACIÓN DEL ENVÍO DE ARCHIVOS ASF DE \_ MF \_ \_ \_ PDPROPIEDADES \_**](mf-pd-asf-fileproperties-send-duration-attribute.md)               | Especifica el tiempo necesario para enviar un archivo ASF, en unidades de 100 nanosegundos.                              |
| [**MF \_ PD \_ ASF \_ INFO \_ HAS \_ AUDIO**](mf-pd-asf-info-has-audio-attribute.md)                                           | Especifica si un archivo ASF contiene al menos una secuencia de audio.                                    |
| [**MF \_ PD \_ ASF \_ INFO \_ HAS \_ NON \_ AUDIO \_ VIDEO**](mf-pd-asf-info-has-non-audio-video-attribute.md)                     | Especifica si un archivo ASF contiene secuencias que no son de audio y que no son de vídeo.                             |
| [**MF \_ PD \_ ASF \_ INFO \_ HAS \_ VIDEO**](mf-pd-asf-info-has-video-attribute.md)                                           | Especifica si un archivo ASF contiene al menos una secuencia de vídeo.                                    |
| [**MF \_ PD \_ ASF \_ LANGLIST**](mf-pd-asf-langlist-attribute.md)                                                         | Especifica la lista de idiomas usados en un archivo ASF.                                                 |
| [MF \_ PD \_ ASF \_ LANGLIST \_ LEGACYORDER](mf-pd-asf-langlist-legacyorder.md)                                              | Contiene una lista de los idiomas RFC 1766 usados en la presentación actual.                              |
| [**MF \_ PD \_ ASF \_ MARKER**](mf-pd-asf-marker-attribute.md)                                                             | Especifica los marcadores de un archivo ASF.                                                                |
| [**LOS \_ METADATOS DE ASF DE MF PD \_ SON \_ \_ \_ VBR**](mf-pd-asf-metadata-is-vbr-attribute.md)                                         | Especifica si un archivo ASF usa la codificación de velocidad de bits variable (VBR).                                 |
| [**PARES DE CUBOS CON PÉRDIDA DE METADATOS DE \_ \_ ASF \_ \_ \_ DE \_ MF PD**](mf-pd-asf-metadata-leaky-bucket-pairs-attribute.md)                | Describe los requisitos de almacenamiento en búfer para un archivo ASF de VBR.                                             |
| [**MF \_ PD \_ ASF \_ METADATA \_ V8 \_ BUFFERAVERAGE**](mf-pd-asf-metadata-v8-bufferaverage-attribute.md)                     | Especifica el tamaño medio de búfer necesario para un archivo ASF de VBR.                                         |
| [**MF \_ PD \_ ASF \_ METADATA \_ V8 \_ VBRPEAK**](mf-pd-asf-metadata-v8-vbrpeak-attribute.md)                                 | Especifica la velocidad de bits momentánuaria más alta en un archivo ASF de VBR.                                          |
| [**\_SCRIPT DE \_ ASF de MF PD \_**](mf-pd-asf-script-attribute.md)                                                             | Especifica los comandos de script en un archivo ASF.                                                        |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Media Foundation atributos](media-foundation-attributes.md)
</dt> <dt>

[Descriptores de presentación](presentation-descriptors.md)
</dt> <dt>

[**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> </dl>

 

 



