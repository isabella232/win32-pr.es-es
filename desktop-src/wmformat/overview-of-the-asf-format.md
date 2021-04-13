---
title: Información general del formato ASF
description: Información general del formato ASF
ms.assetid: ef22a493-d6cf-40d2-ab17-d87159066d1d
keywords:
- Windows Media Format SDK, información general sobre el formato ASF
- Advanced Systems Format (ASF), información general sobre el formato
- ASF (formato de sistemas avanzados), información general de formato
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2858ae1845629c25b52d4c15b5ce7fbb5eb82146
ms.sourcegitcommit: d230e7720c0b566919f8ca11ff7fe3c6b32e028c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/26/2020
ms.locfileid: "104420465"
---
# <a name="overview-of-the-asf-format"></a>Información general del formato ASF

El formato de sistemas avanzados (ASF) es un formato de archivo extensible diseñado principalmente para almacenar y reproducir secuencias multimedia digitales sincronizadas y transmitirlas a través de redes. ASF es el formato de contenedor para Windows Media Audio y el contenido basado en Windows Media Video. La extensión WMA o WMV se usa para especificar un archivo ASF que contiene contenido codificado con los códecs de Windows Media Audio y/o Windows Media Video. El SDK de Windows Media Format se puede usar para crear y leer archivos de Windows Media, así como archivos ASF que contienen otros tipos de datos comprimidos o sin comprimir.

En esta sección se proporciona una descripción general del formato ASF como información general. Dado que los objetos de lectura y escritura controlan todas las tareas de formato y análisis de archivos de bajo nivel, no es necesario tener un conocimiento detallado de ASF antes de usar este SDK para crear archivos ASF. La especificación ASF completa se puede encontrar en el [sitio web de Microsoft](https://download.microsoft.com/download/7/9/0/790fecaa-f64a-4a5e-a430-0bccdab3f1b4/ASF_Specification.doc).

Los principales objetivos del formato ASF son:

-   Para admitir la reproducción eficaz desde servidores multimedia, servidores HTTP y dispositivos de almacenamiento local.
-   Para admitir tipos de medios escalables como audio y vídeo.
-   Para permitir que se presente una única composición multimedia a través de una amplia gama de anchos de banda.
-   Permite el control de la creación de relaciones de flujo multimedia, especialmente en escenarios de ancho de banda restringido.
-   Ser independiente de cualquier sistema de composición multimedia, sistema operativo de equipo o protocolo de comunicaciones de datos determinado.

Un archivo ASF puede contener varios flujos independientes o dependientes, como varias secuencias de audio para audio multicanal o secuencias de vídeo de varias velocidades de bits adecuadas para su transmisión a través de diferentes anchos de banda. Los flujos pueden estar en cualquier formato comprimido o sin comprimir. sin embargo, la mejor compresión se logra con los códecs de Microsoft Windows Media Audio y de la serie de vídeo 9. Además de los tipos de secuencias de medios de audio y vídeo estándar, un archivo ASF también puede contener secuencias de texto, páginas web y comandos de script, y cualquier otro tipo de datos arbitrario. ASF admite contenido multimedia en directo y a petición. Puede usarse como vehículo para grabar o reproducir H. 32X (por ejemplo, H. 323 y H. 324) o conferencias de MBONE.

Un archivo ASF se organiza en secciones denominadas "objetos". Hay tres objetos de nivel superior, un objeto de encabezado y un objeto de datos (ambos obligatorios), además de un objeto de índice opcional. El objeto de encabezado contiene información general sobre el archivo, como el tamaño del archivo, el número de secuencias, los métodos de corrección de errores y los códecs usados. Los metadatos también se almacenan aquí. El objeto de encabezado es el único objeto de nivel superior que puede contener otros objetos. El objeto de datos contiene los datos de la secuencia, organizados en paquetes. El objeto de índice simple contiene una lista de pares de clave-fotograma o índice asociados que permite que las aplicaciones busquen un archivo de forma eficaz. El índice asociado a cada fotograma clave puede ser un tiempo de presentación, un número de fotogramas de vídeo o una marca de tiempo de referencia.

Cada objeto de nivel superior o de nivel inferior comienza con un identificador único global (GUID) y un valor de tamaño. Estos números permiten que el lector de archivos analice la información en los lugares adecuados en objetos identificables. Debido a estos GUID, se pueden enviar objetos de nivel inferior en cualquier orden y seguir siendo reconocidos. El formato ASF está diseñado para evitar la recepción de datos inexactos. Todavía se puede leer un archivo ASF descargado parcialmente, siempre que contenga el objeto de encabezado y al menos un objeto de datos.

Información detallada sobre ASF en presentada en la especificación ASF. Puede descargar la especificación desde el [sitio web de Microsoft](https://download.microsoft.com/download/7/9/0/790fecaa-f64a-4a5e-a430-0bccdab3f1b4/ASF_Specification.doc).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Acerca del SDK de Windows Media Format**](about-the-windows-media-format-sdk.md)
</dt> </dl>

 

 




