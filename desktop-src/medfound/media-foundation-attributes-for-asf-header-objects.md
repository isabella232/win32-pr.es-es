---
description: Media Foundation atributos para objetos de encabezado asf
ms.assetid: 82d2bdeb-4ccf-4713-980e-59bddc7d9b6a
title: Media Foundation atributos para objetos de encabezado asf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 426f0125373000c370f848239717b00aa2615fc16faa84270236704e124cb3bc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120061185"
---
# <a name="media-foundation-attributes-for-asf-header-objects"></a>Media Foundation atributos para objetos de encabezado asf

El objeto de encabezado ASF de nivel superior para un archivo contiene varios objetos de subconsulte ASF. El objeto ContentInfo almacena información de todos estos objetos de encabezado y expone determinados valores a una aplicación a través de atributos.

## <a name="file-properties-object"></a>Objeto De propiedades de archivo

Este objeto de encabezado está presente en todos los archivos ASF. Estos campos describen los atributos de nivel de archivo de toda la presentación. En la tabla siguiente se enumeran los campos del objeto Propiedades de archivo y los atributos del descriptor de presentación correspondientes.



| Campo Objeto de propiedades de archivo | Atributo descriptor de presentación                                                                            | Descripción                                                                                    |
|------------------------------|--------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| Id. de archivo                      | [**MF \_ PD \_ ASF \_ FILEPROPERTIES \_ FILE \_ ID**](mf-pd-asf-fileproperties-file-id-attribute.md)                  | Identificador único para este archivo.                                                               |
| Tamaño de archivo                    | [**MF \_ PD \_ TOTAL \_ FILE \_ SIZE**](mf-pd-total-file-size-attribute.md)                                         | Tamaño del archivo, en bytes.                                                                    |
| Fecha de creación                | [**MF \_ PD \_ ASF \_ FILEPROPERTIES \_ CREATION \_ TIME**](mf-pd-asf-fileproperties-creation-time-attribute.md)      | Fecha y hora de creación del archivo.                                                               |
| Recuento de paquetes de datos           | [**PAQUETES \_ FILEPROPERTIES DE MF PD \_ ASF \_ \_**](mf-pd-asf-fileproperties-packets-attribute.md)                   | Número de paquetes de datos en el objeto de datos de ASF.                                                 |
| Duración del juego                | [**DURACIÓN \_ DE REPRODUCCIÓN DE FILEPROPERTIES DE MF PD \_ ASF \_ \_ \_**](mf-pd-asf-fileproperties-play-duration-attribute.md)      | Tiempo necesario para reproducir el archivo, en unidades de 100 nanosegundos. Este valor incluye el tiempo de inscripción previa. |
| Duración del envío                | [**DURACIÓN \_ DEL ENVÍO DE FILEPROPERTIES DE MF PD \_ ASF \_ \_ \_**](mf-pd-asf-fileproperties-send-duration-attribute.md)      | Tiempo necesario para enviar el archivo, en unidades de 100 nanosegundos.                                       |
| Predesplazamiento                      | [**MF \_ PD \_ ASF \_ FILEPROPERTIES \_ PREROLL**](mf-pd-asf-fileproperties-preroll-attribute.md)                   | Tiempo de almacenamiento en búfer de datos antes de reproducir el archivo, en unidades de 100 nanosegundos.            |
| Marcas                        | [**MF \_ PD \_ ASF \_ FILEPROPERTIES \_ FLAGS**](mf-pd-asf-fileproperties-flags-attribute.md)                       | Marcas que indican si el archivo es difusión o se puede buscar.                                    |
| Tamaño mínimo del paquete de datos     | [**MF \_ PD \_ ASF \_ FILEPROPERTIES \_ MIN \_ PACKET \_ SIZE**](mf-pd-asf-fileproperties-min-packet-size-attribute.md) | Tamaño mínimo de los paquetes de datos del archivo, en bytes.                                        |
| Tamaño máximo del paquete de datos     | [**MF \_ PD \_ ASF \_ FILEPROPERTIES \_ MAX \_ PACKET \_ SIZE**](mf-pd-asf-fileproperties-max-packet-size-attribute.md) | Tamaño máximo de los paquetes de datos del archivo, en bytes.                                        |
| Velocidad de bits máxima              | [**MF \_ PD \_ ASF \_ FILEPROPERTIES \_ MAX \_ BITRATE**](mf-pd-asf-fileproperties-max-bitrate-attribute.md)          | Velocidad de bits instantánea máxima, en bits por segundo.                                            |



 

## <a name="stream-properties-object"></a>Objeto De propiedades de secuencia

Este objeto de encabezado describe las propiedades de las secuencias en el archivo ASF. En Media Foundation, esto se administra mediante el objeto de perfil y el objeto de configuración de flujo. Para obtener más información, [vea Creating and Configuring ASF Secuencias](creating-and-configuring-asf-streams.md).

## <a name="codec-list-object"></a>Objeto De lista de códecs

Si este objeto de encabezado está presente, el atributo [**MF \_ PD \_ ASF \_ CODECLIST**](mf-pd-asf-codeclist-attribute.md) proporciona una lista de códecs que se usaron para codificar las secuencias dentro del archivo ASF. Cada secuencia debe tener su información de códec en este objeto.

## <a name="script-command-object"></a>Script Command (objeto)

Si este objeto de encabezado está presente, especifica una lista de comandos de script que se admiten en el archivo ASF. Un comando de script consta de un tipo de comando, un nombre de comando y un tiempo de presentación. El tipo de comando y el nombre del comando son cadenas de caracteres anchos. Estos comandos se pueden usar para notificar al cliente que realice una acción en un punto determinado de la presentación. Por ejemplo, una aplicación puede usar el tipo de comando "FILENAME" para reproducir una secuencia continua de archivos ASF.

Para obtener la lista de comandos de script, obtenga el atributo [**\_ MF PD \_ ASF \_ SCRIPT**](mf-pd-asf-script-attribute.md) del descriptor de presentación. Una aplicación debe recuperar todos los comandos de script antes de iniciar la reproducción.

## <a name="marker-object"></a>Objeto Marker

Un marcador es un marcador dentro de un archivo ASF. Una aplicación puede usar marcadores para buscar en varios puntos dentro del contenido. Cada marcador consta de un nombre de marcador, el tiempo de presentación asociado y el desplazamiento desde el inicio del archivo. El [**atributo MF PD \_ \_ ASF \_ MARKER**](mf-pd-asf-marker-attribute.md) proporciona una lista de marcadores que están disponibles para el archivo.

## <a name="stream-bitrate-properties-object"></a>Objeto de propiedades de velocidad de bits de secuencia

Este encabezado almacena la velocidad de bits media de cada secuencia presente en el archivo ASF. Este valor se almacena en el descriptor de flujo de la secuencia en el atributo [**\_ MF SD \_ ASF \_ STREAMBITRATES \_ BITRATE.**](mf-sd-asf-streambitrates-bitrate-attribute.md)

## <a name="content-encryption-object"></a>Objeto de cifrado de contenido

Este objeto de encabezado está presente si el proveedor de contenido ha protegido el contenido mediante Microsoft Digital Rights Management. En la tabla siguiente se enumeran los campos del objeto de cifrado de contenido y los atributos del descriptor de presentación correspondientes:



| Campo Objeto de cifrado de contenido | Atributo descriptor de presentación                                                                         | Descripción                                                                                        |
|---------------------------------|-----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| Datos secretos                     | [**DATOS \_ SECRETOS \_ DE \_ CONTENTENCRYPTION \_ \_ DE MF PD ASF**](mf-pd-asf-contentencryption-secret-data-attribute.md) | Matriz de bytes que contiene datos secretos.                                                                 |
| Tipo de protección                 | [**TIPO \_ \_ \_ CONTENTENCRYPTION DE MF PD ASF \_**](mf-pd-asf-contentencryption-type-attribute.md)                | Cadena terminada en NULL que tiene el valor "DRM".                                                       |
| Id. de clave                          | [**MF \_ PD \_ ASF \_ CONTENTENCRYPTION \_ KEYID**](mf-pd-asf-contentencryption-keyid-attribute.md)              | Cadena terminada en NULL que describe el identificador de clave.                                          |
| Dirección URL de licencia                     | [**DIRECCIÓN \_ URL DE LICENCIA DE MF PD \_ ASF \_ CONTENTENCRYPTION \_ \_**](mf-pd-asf-contentencryption-license-url-attribute.md) | Cadena terminada en NULL que contiene la dirección URL desde la que adquirir la licencia para usar el contenido. |



 

## <a name="extended-content-encryption-object"></a>Objeto de cifrado de contenido extendido

Este objeto de encabezado está presente si el proveedor de contenido ha protegido el contenido mediante el SDK Windows Media Rights Manager 7. El [**atributo MF PD \_ \_ ASF \_ CONTENTENCRYPTION \_ LICENSE \_ URL**](mf-pd-asf-contentencryption-license-url-attribute.md) proporciona una matriz de bytes que corresponde al campo Datos del objeto de encabezado. Este campo es necesario para usar el contenido.

## <a name="extended-stream-properties-object"></a>Extended Stream Properties (Objeto)

Este encabezado forma parte del objeto de extensión de encabezado. El objeto propiedades de secuencia extendida proporciona propiedades de la secuencia que no están definidas en el objeto Propiedades de secuencia. Estas propiedades se usan principalmente para determinar los parámetros del "cubo de fugas", que usa el descodificador. El codificador también usa estas propiedades al comprimir los datos. Esto se administra mediante el objeto de perfil y el objeto de configuración de flujo. Para obtener más información, [vea Creating and Configuring ASF Secuencias](creating-and-configuring-asf-streams.md).

En la tabla siguiente se enumeran los campos Objeto de propiedades de secuencia extendida y los atributos de descriptor de flujo correspondientes.



| Campo Propiedades de flujo extendidas | Atributo descriptor de flujo                                                                                | Descripción                                                                                                              |
|----------------------------------|------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| Velocidad de bits de datos                     | [**MF \_ SD \_ ASF \_ EXTSTRMPROP \_ AVG \_ DATA \_ BITRATE**](mf-sd-asf-extstrmprop-avg-data-bitrate-attribute.md)   | Velocidad media de datos, en bits por segundo.                                                                                   |
| Tamaño del búfer                      | [**MF \_ SD \_ ASF \_ EXTSTRMPROP \_ AVG \_ BUFFERSIZE**](mf-sd-asf-extstrmprop-avg-buffersize-attribute.md)        | Tamaño del cubo con pérdidas. El valor es el número de milisegundos de datos que pueden caber en el búfer a la velocidad media de datos.      |
| Velocidad de bits de datos alternativa           | [**MF \_ SD \_ ASF \_ EXTSTRMPROP \_ MAX \_ DATA \_ BITRATE**](mf-sd-asf-extstrmprop-max-data-bitrate-attribute.md)   | Velocidad máxima de datos, en bits por segundo. La velocidad máxima de datos se usa para secuencias con una velocidad de bits variable.                    |
| Tamaño de búfer alternativo            | [**MF \_ SD \_ ASF \_ EXTSTRMPROP \_ MAX \_ BUFFERSIZE**](mf-sd-asf-extstrmprop-max-buffersize-attribute.md)        | Tamaño máximo del depósito con pérdida. El valor es el número de milisegundos de datos que pueden caber en el búfer a la velocidad máxima de datos. |
| Id. de lenguaje de secuencia               | [**MF \_ SD \_ ASF \_ EXTSTRMPROP \_ LANGUAGE \_ ID \_ INDEX**](mf-sd-asf-extstrmprop-language-id-index-attribute.md) | Idioma que usa la secuencia, especificado como índice en la lista de idiomas del objeto de lista de idiomas.         |



 

## <a name="language-list-object"></a>Objeto de lista de idioma

Este objeto de encabezado forma parte del objeto de extensión de encabezado. Si está presente, el [**atributo \_ \_ ASF \_ LANGLIST**](mf-pd-asf-langlist-attribute.md) de MF PD proporciona una lista de identificadores de idioma que se admiten en el archivo. Los identificadores son compatibles con RFC 1766 para especificar idiomas.

## <a name="mutual-exclusion-object"></a>Objeto de exclusión mutua

Este encabezado especifica grupos de flujos y sus propiedades, solo uno de los cuales se entregará a la vez. Para obtener más información, [vea Using Mutual Exclusion for ASF Secuencias](using-mutual-exclusion-for-asf-streams.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Objeto ContentInfo de ASF](asf-contentinfo-object.md)
</dt> <dt>

[Objeto de encabezado ASF](asf-file-structure.md)
</dt> <dt>

[Compatibilidad con ASF en Media Foundation](asf-support-in-media-foundation.md)
</dt> </dl>

 

 



