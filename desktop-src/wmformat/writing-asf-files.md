---
title: Escribir archivos ASF
description: Escribir archivos ASF
ms.assetid: d722b676-bf65-4f91-8118-bb12d3bbb6cb
keywords:
- SDK de Windows Media Format, escribir archivos ASF
- SDK de Windows Media Format, crear archivos ASF
- Windows Media Format SDK, Advanced Systems Format (ASF)
- Advanced Systems Format (ASF), escribir archivos
- ASF (formato de sistemas avanzados), escribir archivos
- Advanced Systems Format (ASF), crear archivos
- ASF (formato de sistemas avanzados), crear archivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c13c1af0d3699c89d26f007e00675ea563639c4e
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "103904404"
---
# <a name="writing-asf-files"></a>Escribir archivos ASF

Puede usar el objeto escritor del SDK de Windows Media Format para crear archivos ASF a partir de datos multimedia digitales. Para crear una instancia del objeto de escritor, llame a la función [**WMCreateWriter**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriter) . El objeto escritor coordina la funcionalidad de una serie de componentes, incluidos los códecs, que son externos al SDK de Windows Media Format.

La funcionalidad básica del objeto escritor se puede desglosar en los pasos siguientes. En estos pasos, "la aplicación" hace referencia al programa que se escribe con el SDK de Windows Media Format.

1.  La aplicación proporciona al escritor un perfil que se utilizará para crear el archivo ASF. Cuando el escritor carga los datos del perfil, asigna un número de entrada a cada conexión del perfil.
2.  La aplicación proporciona al escritor un nombre de archivo de salida para el archivo que se va a escribir. El escritor crea un objeto de receptor del archivo de escritura para administrar la entrada y la creación del archivo. Para obtener más información, consulte [objeto de receptor del archivo de escritura](writer-file-sink-object.md).
3.  El escritor crea un encabezado para el nuevo archivo basándose en la información del perfil.
4.  La aplicación pasa muestras sin comprimir al escritor. Las muestras se pasan de una en una en los búferes encapsulados en los objetos de búfer. La aplicación debe pasar ejemplos para cada flujo simultáneamente para que el escritor reciba todos los ejemplos en el orden en tiempo de presentación.
5.  El escritor pasa los ejemplos al códec adecuado para la compresión. Cuando el escritor recibe los ejemplos comprimidos, los intercala con ejemplos de las otras secuencias para que los ejemplos se incluyan en el archivo en el orden temporal de la presentación, independientemente de la secuencia. Los datos de ejemplo se convierten en paquetes y se escriben en la sección de datos del archivo.
6.  Cuando se procesan todos los ejemplos, el sistema de escritura puede Agregar un índice al archivo para mejorar el rendimiento de búsqueda.

Estos pasos se muestran en la aplicación de ejemplo WMStats, entre otros. Para obtener más información, vea [aplicaciones de ejemplo](sample-applications.md).

El escritor también admite una funcionalidad más avanzada, lo que le permite hacer lo siguiente:

-   Edite los metadatos en el encabezado del archivo.
-   Escribir muestras precomprimidas.
-   Escribir en receptores de red para transmitir datos en directo.
-   Escribir en los receptores de archivos para opciones avanzadas de control de archivos.
-   Escriba los receptores de envío para la distribución en los servidores que entregarán contenido a los usuarios finales.
-   Proporcione ejemplos de postview para la comprobación de la salida.
-   Entregue las estadísticas de rendimiento del escritor.

En las secciones siguientes se describe detalladamente el uso del objeto de escritura.



| Sección                                                                    | Descripción                                                                                            |
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [Para el uso de perfiles con Writer](to-use-profiles-with-the-writer.md)     | Describe cómo especificar un perfil para usarlo con el escritor.                                             |
| [Trabajar con entradas](working-with-inputs.md)                             | Describe cómo identificar y configurar los valores de entrada en el escritor.                              |
| [Para editar los metadatos con el escritor](to-edit-metadata-with-the-writer.md)   | Describe cómo utilizar el escritor para editar los metadatos de un archivo nuevo.                                       |
| [Para escribir ejemplos](to-write-samples.md)                                   | Describe cómo pasar ejemplos al escritor.                                                           |
| [Configuración de las extensiones de unidad de datos](setting-data-unit-extensions.md)           | Describe cómo agregar datos extendidos a ejemplos.                                                         |
| [Escribir ejemplos comprimidos](writing-compressed-samples.md)               | Describe cómo pasar ejemplos previamente comprimidos al escritor.                                            |
| [Escribir secuencias de imagen](writing-image-streams.md)                         | Describe cómo configurar una entrada para un flujo de imagen.                                               |
| [Escribir ejemplos de imagen de vídeo](writing-video-image-samples.md)             | Describe cómo configurar los ejemplos de imagen de vídeo.                                                        |
| [Escribir secuencias de velocidad de bits variable](writing-variable-bit-rate-streams.md) | Describe cómo escribir secuencias de velocidad de bits variable (VBR).                                                |
| [Uso de la codificación de Two-Pass](using-two-pass-encoding.md)                     | Describe cómo hacer que el códec realice una fase preliminar antes de escribir el archivo.                    |
| [Para forzar la inserción de Key-Frame](to-force-key-frame-insertion.md)           | Describe cómo forzar manualmente el códec para codificar un ejemplo como un fotograma clave.                           |
| [Para administrar la latencia del escritor](to-manage-writer-latency.md)                   | Describe cómo minimizar el tiempo que tarda el escritor en procesar muestras en un archivo o receptor de salida. |
| [Trabajar con receptores de escritor](working-with-writer-sinks.md)                 | Describe cómo usar receptores de escritor para enviar el contenido a archivos o ubicaciones de red.               |
| [Para obtener estadísticas del escritor](to-get-writer-statistics.md)                   | Describe cómo obtener estadísticas para el escritor.                                                        |
| [Para usar la vista previa del escritor](to-use-writer-postview.md)                       | Describe cómo obtener ejemplos sin comprimir mientras escribe un archivo para su comprobación.                        |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Guía de programación**](programming-guide.md)
</dt> <dt>

[**Objeto receptor de archivos de Writer**](writer-file-sink-object.md)
</dt> <dt>

[**Objeto de receptor de red del escritor**](writer-network-sink-object.md)
</dt> <dt>

[**Objeto de Writer**](writer-object.md)
</dt> </dl>

 

 




