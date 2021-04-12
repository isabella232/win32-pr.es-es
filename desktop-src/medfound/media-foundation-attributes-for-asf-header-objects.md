---
description: Media Foundation atributos para los objetos de encabezado ASF
ms.assetid: 82d2bdeb-4ccf-4713-980e-59bddc7d9b6a
title: Media Foundation atributos para los objetos de encabezado ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4db74ccb03536c7766dd7e1564119edbd41d5dbe
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "104361919"
---
# <a name="media-foundation-attributes-for-asf-header-objects"></a>Media Foundation atributos para los objetos de encabezado ASF

El objeto de encabezado ASF de nivel superior de un archivo contiene varios objetos de subencabezado ASF. El objeto ContentInfo almacena información de todos estos objetos de encabezado y expone ciertos valores en una aplicación a través de atributos.

## <a name="file-properties-object"></a>Objeto de propiedades de archivo

Este objeto de encabezado está presente en todos los archivos ASF. En estos campos se describen los atributos de nivel de archivo de toda la presentación. En la tabla siguiente se enumeran los campos del objeto de propiedades de archivo y los atributos de descriptor de presentación correspondientes.



| Campo de objeto de propiedades de archivo | Descriptor de presentación (atributo)                                                                            | Descripción                                                                                    |
|------------------------------|--------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| Id. de archivo                      | [**MF \_ PD \_ ASF \_ FILEPROPERTIES \_ \_ ID. de archivo**](mf-pd-asf-fileproperties-file-id-attribute.md)                  | Identificador único para este archivo.                                                               |
| Tamaño de archivo                    | [**\_ \_ Tamaño total de \_ archivo MF PD \_**](mf-pd-total-file-size-attribute.md)                                         | Tamaño del archivo, en bytes.                                                                    |
| Fecha de creación                | [**MF \_ PD \_ ASF \_ \_ hora de creación FILEPROPERTIES \_**](mf-pd-asf-fileproperties-creation-time-attribute.md)      | Fecha y hora de creación del archivo.                                                               |
| Recuento de paquetes de datos           | [**\_ \_ \_ paquetes FILEPROPERTIES MF de \_ ASF**](mf-pd-asf-fileproperties-packets-attribute.md)                   | Número de paquetes de datos en el objeto de datos ASF.                                                 |
| Duración de la reproducción                | [**MF \_ PD \_ ASF \_ FILEPROPERTIES \_ \_ duración de la reproducción**](mf-pd-asf-fileproperties-play-duration-attribute.md)      | Tiempo necesario para reproducir el archivo, en unidades de 100-nanosegundos. Este valor incluye el tiempo de prelanzamiento. |
| Duración del envío                | [**MF \_ PD \_ ASF \_ FILEPROPERTIES \_ duración del envío \_**](mf-pd-asf-fileproperties-send-duration-attribute.md)      | Tiempo necesario para enviar el archivo, en unidades de 100-nanosegundos.                                       |
| Preprocesará                      | [**preFILEPROPERTIES MF \_ PD \_ ASF \_ \_**](mf-pd-asf-fileproperties-preroll-attribute.md)                   | Período de tiempo para almacenar en búfer los datos antes de reproducir el archivo, en unidades de 100-nanosegundos.            |
| Marcas                        | [**etiquetas FILEPROPERTIES de MF \_ PD \_ ASF \_ \_**](mf-pd-asf-fileproperties-flags-attribute.md)                       | Marcas que indican si el archivo se va a difundir o a buscar.                                    |
| Tamaño mínimo de paquete de datos     | [**MF \_ PD \_ ASF \_ FILEPROPERTIES \_ min \_ Packet \_ size**](mf-pd-asf-fileproperties-min-packet-size-attribute.md) | Tamaño mínimo de los paquetes de datos en el archivo, en bytes.                                        |
| Tamaño máximo de paquete de datos     | [**MF \_ PD \_ ASF \_ FILEPROPERTIES \_ tamaño máximo de \_ paquete \_**](mf-pd-asf-fileproperties-max-packet-size-attribute.md) | Tamaño máximo de los paquetes de datos en el archivo, en bytes.                                        |
| Velocidad de bits máxima              | [**MF \_ PD \_ ASF \_ FILEPROPERTIES \_ de \_ velocidad de bits máxima**](mf-pd-asf-fileproperties-max-bitrate-attribute.md)          | Velocidad de bits instantánea máxima, en bits por segundo.                                            |



 

## <a name="stream-properties-object"></a>Stream Properties (objeto)

Este objeto de encabezado describe las propiedades de las secuencias del archivo ASF. En Media Foundation, esto lo administra el objeto de perfil y el objeto de configuración de la secuencia. Para obtener más información, vea [crear y configurar secuencias ASF](creating-and-configuring-asf-streams.md).

## <a name="codec-list-object"></a>Objeto de lista de códecs

Si este objeto de encabezado está presente, el atributo [**MF \_ PD \_ ASF \_ CODECLIST**](mf-pd-asf-codeclist-attribute.md) proporciona una lista de códecs que se usaron para codificar los flujos en el archivo ASF. Cada flujo debe tener su información de códec en este objeto.

## <a name="script-command-object"></a>Script (objeto de comando)

Si este objeto de encabezado está presente, especifica una lista de comandos de script que se admiten en el archivo ASF. Un comando de script consta de un tipo de comando, un nombre de comando y un tiempo de presentación. El tipo de comando y el nombre del comando son cadenas de caracteres anchos. Estos comandos se pueden usar para notificar al cliente que realice una acción en un punto determinado de la presentación. Por ejemplo, una aplicación puede usar el tipo de comando "FILENAME" para reproducir una secuencia continua de archivos ASF.

Para obtener la lista de comandos de script, obtenga el atributo de secuencia de comandos [**\_ \_ ASF \_ de MF PD**](mf-pd-asf-script-attribute.md) del descriptor de presentación. Una aplicación debe recuperar todos los comandos de script antes de iniciar la reproducción.

## <a name="marker-object"></a>Objeto de marcador

Un marcador es un marcador dentro de un archivo ASF. Una aplicación puede usar marcadores para buscar varios puntos dentro del contenido. Cada marcador está formado por un nombre de marcador, el tiempo de presentación asociado y el desplazamiento desde el inicio del archivo. El atributo de [**\_ \_ \_ marcador MF PD ASF**](mf-pd-asf-marker-attribute.md) proporciona una lista de marcadores que están disponibles para el archivo.

## <a name="stream-bitrate-properties-object"></a>Objeto de propiedades de velocidad de bits de flujo

Este encabezado almacena la velocidad de bits media de cada flujo presente en el archivo ASF. Este valor se almacena en el descriptor de flujo de la secuencia en el atributo [**MF \_ SD \_ ASF \_ STREAMBITRATES \_ bitrate**](mf-sd-asf-streambitrates-bitrate-attribute.md) .

## <a name="content-encryption-object"></a>Objeto de cifrado de contenido

Este objeto de encabezado está presente si el proveedor de contenido protegió el contenido mediante Microsoft Digital Rights Management. En la tabla siguiente se enumeran los campos del objeto de cifrado de contenido y los atributos de descriptor de presentación correspondientes:



| Campo de objeto de cifrado de contenido | Descriptor de presentación (atributo)                                                                         | Descripción                                                                                        |
|---------------------------------|-----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| Datos secretos                     | [**MF \_ PD \_ ASF \_ CONTENTENCRYPTION \_ \_ datos secretos**](mf-pd-asf-contentencryption-secret-data-attribute.md) | Matriz de bytes que contiene datos secretos.                                                                 |
| Tipo de protección                 | [**MF \_ PD \_ ASF \_ \_ tipo CONTENTENCRYPTION**](mf-pd-asf-contentencryption-type-attribute.md)                | Cadena terminada en null que tiene el valor "DRM".                                                       |
| Id. de clave                          | [**ID. de CONTENTENCRYPTION de MF \_ PD \_ ASF \_ \_**](mf-pd-asf-contentencryption-keyid-attribute.md)              | Cadena terminada en null que describe el identificador de clave.                                          |
| Dirección URL de licencia                     | [**\_dirección URL de licencia MF PD \_ ASF \_ CONTENTENCRYPTION \_ \_**](mf-pd-asf-contentencryption-license-url-attribute.md) | Cadena terminada en null que contiene la dirección URL de la que se va a adquirir la licencia para usar el contenido. |



 

## <a name="extended-content-encryption-object"></a>Objeto de cifrado de contenido extendido

Este objeto de encabezado está presente si el proveedor de contenido protegió el contenido mediante el SDK de Windows Media Rights Manager 7. El atributo [**MF \_ PD \_ ASF \_ CONTENTENCRYPTION \_ \_ URL**](mf-pd-asf-contentencryption-license-url-attribute.md) de la licencia proporciona una matriz de bytes que corresponde al campo de datos del objeto de encabezado. Este campo es necesario para usar el contenido.

## <a name="extended-stream-properties-object"></a>Extended Stream Properties (objeto)

Este encabezado forma parte del objeto de extensión de encabezado. El objeto Extended Stream Properties proporciona propiedades de la secuencia que no están definidas en el objeto Stream Properties. Estas propiedades se utilizan principalmente para determinar los parámetros de "depósito de fugas", que usa el descodificador. El codificador también utiliza estas propiedades al comprimir los datos. Lo administra el objeto de perfil y el objeto de configuración de la secuencia. Para obtener más información, vea [crear y configurar secuencias ASF](creating-and-configuring-asf-streams.md).

En la tabla siguiente se enumeran los campos de objeto de propiedades de secuencia extendida y los atributos de descriptor de secuencia correspondientes.



| Campo de propiedades de secuencia extendida | Atributo de descriptor de secuencia                                                                                | Descripción                                                                                                              |
|----------------------------------|------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| Velocidad de bits de datos                     | [**\_velocidad de \_ \_ \_ bits promedio de \_ datos \_ ASF SD EXTSTRMPROP**](mf-sd-asf-extstrmprop-avg-data-bitrate-attribute.md)   | Promedio de velocidad de datos, en bits por segundo.                                                                                   |
| Tamaño del búfer                      | [**MF \_ SD \_ ASF \_ EXTSTRMPROP \_ AVG \_ BUFFERSIZE**](mf-sd-asf-extstrmprop-avg-buffersize-attribute.md)        | Tamaño del depósito con fugas. El valor es el número de milisegundos de datos que pueden caber en el búfer en la velocidad de datos media.      |
| Velocidad de bits de datos alternativa           | [**\_velocidad de \_ \_ bits de \_ datos Max SD ASF EXTSTRMPROP máx \_ \_ .**](mf-sd-asf-extstrmprop-max-data-bitrate-attribute.md)   | Velocidad de datos máxima, en pequeñas por segundo. La velocidad de datos máxima se usa para las secuencias con una velocidad de bits variable.                    |
| Tamaño de búfer alternativo            | [**MF \_ SD \_ ASF \_ EXTSTRMPROP \_ Max \_ BUFFERSIZE**](mf-sd-asf-extstrmprop-max-buffersize-attribute.md)        | Tamaño máximo de depósito con fugas. Valor es el número de milisegundos de datos que pueden caber en el búfer en la velocidad de datos máxima. |
| ID. de lenguaje de secuencia               | [**\_Índice de \_ \_ \_ \_ ID. de idioma \_ de MF SD ASF EXTSTRMPROP**](mf-sd-asf-extstrmprop-language-id-index-attribute.md) | Lenguaje que utiliza la secuencia, especificado como un índice en la lista de idiomas del objeto de lista de idiomas.         |



 

## <a name="language-list-object"></a>Objeto de lista de idiomas

Este objeto de encabezado forma parte del objeto de extensión de encabezado. Si está presente, el atributo [**MF \_ PD \_ ASF \_ LANGLIST**](mf-pd-asf-langlist-attribute.md) proporciona una lista de los identificadores de idioma que se admiten en el archivo. Los identificadores son compatibles con RFC 1766 para especificar los idiomas.

## <a name="mutual-exclusion-object"></a>Objeto de exclusión mutua

Este encabezado especifica grupos de secuencias y sus propiedades, solo una de las cuales se entregará a la vez. Para obtener más información, consulte [uso de la exclusión mutua para secuencias ASF](using-mutual-exclusion-for-asf-streams.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Objeto ContentInfo de ASF](asf-contentinfo-object.md)
</dt> <dt>

[Objeto de encabezado ASF](asf-file-structure.md)
</dt> <dt>

[Compatibilidad con ASF en Media Foundation](asf-support-in-media-foundation.md)
</dt> </dl>

 

 



