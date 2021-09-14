---
title: Escritura de archivos ASF
description: Escritura de archivos ASF
ms.assetid: d722b676-bf65-4f91-8118-bb12d3bbb6cb
keywords:
- Windows SDK de formato multimedia, escritura de archivos ASF
- Windows SDK de formato multimedia, creación de archivos ASF
- Windows SDK de formato multimedia, formato de sistemas avanzados (ASF)
- Formato de sistemas avanzados (ASF), escribir archivos
- ASF (formato de sistemas avanzados), escribir archivos
- Formato de sistemas avanzados (ASF), crear archivos
- ASF (formato de sistemas avanzados), crear archivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c13c1af0d3699c89d26f007e00675ea563639c4e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127247142"
---
# <a name="writing-asf-files"></a>Escritura de archivos ASF

Puede usar el objeto de escritor del SDK Windows Media Format para crear archivos ASF a partir de datos multimedia digitales. Para crear una instancia del objeto writer, llame a la [**función WMCreateWriter.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriter) El objeto de escritor coordina la funcionalidad de varios componentes, incluidos los códecs, que son externos al SDK Windows Media Format.

La funcionalidad básica del objeto de escritor se puede dividir en los pasos siguientes. En estos pasos, "la aplicación" hace referencia al programa que escribe con el SDK Windows Media Format.

1.  La aplicación proporciona al escritor un perfil para usarlo en la creación del archivo ASF. Cuando el escritor carga los datos del perfil, asigna un número de entrada a cada conexión del perfil.
2.  La aplicación proporciona al escritor un nombre de archivo de salida para el archivo que se va a escribir. El escritor crea un objeto de receptor de archivos de escritor para administrar la creación y la entrada del archivo. Para obtener más información, vea [Objeto receptor de archivo de escritor](writer-file-sink-object.md).
3.  El sistema de escritura crea un encabezado para el nuevo archivo basándose en la información del perfil.
4.  La aplicación pasa ejemplos sin comprimir al escritor. Las muestras se pasan de uno en uno en búferes encapsulados en objetos de búfer. La aplicación debe pasar ejemplos para cada secuencia simultáneamente para que el escritor reciba todas las muestras en el orden de presentación.
5.  El escritor pasa los ejemplos al códec adecuado para la compresión. Cuando el sistema de escritura recibe las muestras comprimidas, las intercala con muestras de las otras secuencias para que las muestras vayan al archivo en orden de tiempo de presentación independientemente de la secuencia. A continuación, los datos de ejemplo se convierten en paquetes y se escriben en la sección de datos del archivo.
6.  Cuando se procesan todos los ejemplos, el escritor puede agregar un índice al archivo para mejorar el rendimiento de la búsqueda.

Estos pasos se ilustran en la aplicación de ejemplo WMStats, entre otros. Para obtener más información, vea [Aplicaciones de ejemplo.](sample-applications.md)

El escritor también admite una funcionalidad más avanzada, lo que le permite hacer lo siguiente:

-   Edite los metadatos en el encabezado del archivo.
-   Escribir ejemplos comprimidos previamente.
-   Escribir en receptores de red para streaming de datos en directo.
-   Escriba en receptores de archivos para obtener opciones avanzadas de control de archivos.
-   Escriba en receptores de inserción para su distribución en servidores que entregarán contenido a los usuarios finales.
-   Entregar ejemplos de vista posterior para la comprobación de la salida.
-   Entregar estadísticas de rendimiento del escritor.

En las secciones siguientes se describe el uso del objeto de escritor en detalle.



| Sección                                                                    | Descripción                                                                                            |
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [Para el uso de perfiles con Writer](to-use-profiles-with-the-writer.md)     | Describe cómo especificar un perfil para usarlo con el escritor.                                             |
| [Trabajar con entradas](working-with-inputs.md)                             | Describe cómo identificar y configurar los valores de entrada en el sistema de escritura.                              |
| [Para editar metadatos con el escritor](to-edit-metadata-with-the-writer.md)   | Describe cómo usar el sistema de escritura para editar los metadatos de un nuevo archivo.                                       |
| [Para escribir ejemplos](to-write-samples.md)                                   | Describe cómo pasar ejemplos al escritor.                                                           |
| [Establecer extensiones de unidad de datos](setting-data-unit-extensions.md)           | Describe cómo agregar datos extendidos a ejemplos.                                                         |
| [Escribir ejemplos comprimidos](writing-compressed-samples.md)               | Describe cómo pasar muestras precomprimidas al escritor.                                            |
| [Escribir imágenes Secuencias](writing-image-streams.md)                         | Describe cómo configurar una entrada para un flujo de imagen.                                               |
| [Escribir ejemplos de imágenes de vídeo](writing-video-image-samples.md)             | Describe cómo configurar ejemplos de imágenes de vídeo.                                                        |
| [Escritura de velocidad de bits variable Secuencias](writing-variable-bit-rate-streams.md) | Describe cómo escribir secuencias de velocidad de bits variable (VBR).                                                |
| [Uso de Two-Pass codificación](using-two-pass-encoding.md)                     | Describe cómo hacer que el códec realice un paso preliminar antes de escribir el archivo.                    |
| [Para forzar la Key-Frame inserción](to-force-key-frame-insertion.md)           | Describe cómo forzar manualmente el códec para codificar un ejemplo como fotograma clave.                           |
| [Para administrar la latencia del escritor](to-manage-writer-latency.md)                   | Describe cómo minimizar el tiempo que tarda el escritor en procesar ejemplos en un archivo de salida o receptor. |
| [Trabajar con receptores de escritor](working-with-writer-sinks.md)                 | Describe cómo usar receptores de escritor para entregar el contenido a archivos o ubicaciones de red.               |
| [Para obtener estadísticas del escritor](to-get-writer-statistics.md)                   | Describe cómo obtener estadísticas para el escritor.                                                        |
| [Para usar la vista posterior del escritor](to-use-writer-postview.md)                       | Describe cómo obtener ejemplos sin comprimir a medida que escribe un archivo para la comprobación.                        |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Guía de programación**](programming-guide.md)
</dt> <dt>

[**Objeto receptor de archivos de Writer**](writer-file-sink-object.md)
</dt> <dt>

[**Objeto receptor de red writer**](writer-network-sink-object.md)
</dt> <dt>

[**Objeto de Writer**](writer-object.md)
</dt> </dl>

 

 




