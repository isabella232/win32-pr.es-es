---
title: Información general del formato ASF
description: Información general del formato ASF
ms.assetid: ef22a493-d6cf-40d2-ab17-d87159066d1d
keywords:
- Windows SDK de formato multimedia, introducción al formato ASF
- Formato de sistemas avanzados (ASF), introducción al formato
- ASF (formato de sistemas avanzados),introducción al formato
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2858ae1845629c25b52d4c15b5ce7fbb5eb82146
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127360931"
---
# <a name="overview-of-the-asf-format"></a>Información general del formato ASF

El formato de sistemas avanzados (ASF) es un formato de archivo extensible diseñado principalmente para almacenar y reproducir secuencias de medios digitales sincronizadas y transmitirlas a través de redes. ASF es el formato de contenedor para Windows audio multimedia y Windows contenido basado en vídeo multimedia. La extensión wma o wmv se usa para especificar un archivo ASF que contiene contenido codificado con los códecs Windows Media Audio o Windows Media Video. El SDK Windows Media Format se puede usar para crear y leer archivos multimedia Windows, así como archivos ASF que contienen otros tipos de datos comprimidos o sin comprimir.

En esta sección se proporciona una descripción general del formato ASF como información de fondo. Dado que los objetos lector y escritor controlan todas las tareas de formato y análisis de archivos de bajo nivel, no es necesario tener un conocimiento detallado de ASF antes de usar este SDK para crear archivos ASF. La especificación completa de ASF se puede encontrar en el [sitio web de Microsoft](https://download.microsoft.com/download/7/9/0/790fecaa-f64a-4a5e-a430-0bccdab3f1b4/ASF_Specification.doc).

Los objetivos principales del formato ASF son:

-   Para admitir una reproducción eficaz desde servidores multimedia, servidores HTTP y dispositivos de almacenamiento local.
-   Para admitir tipos de medios escalables, como audio y vídeo.
-   Para permitir que una sola composición multimedia se presente a través de una amplia gama de anchos de banda.
-   Para permitir el control de creación sobre las relaciones de flujo multimedia, especialmente en escenarios de ancho de banda restringido.
-   Para ser independiente de cualquier sistema de composición multimedia, sistema operativo de equipo o protocolo de comunicaciones de datos determinado.

Un archivo ASF puede contener varias secuencias independientes o dependientes, incluidas varias secuencias de audio para audio multicanal o varias secuencias de vídeo de velocidad de bits adecuadas para la transmisión a través de anchos de banda diferentes. Las secuencias pueden estar en cualquier formato comprimido o sin comprimir; sin embargo, la mejor compresión se logra con los códecs de la serie Microsoft Windows Media Audio y Video 9. Además de los tipos estándar de secuencias multimedia de audio y vídeo, un archivo ASF también puede contener secuencias de texto, páginas web y comandos de script, y cualquier otro tipo de datos arbitrario. ASF admite contenido multimedia en directo y a petición. Se puede usar como vehículo para grabar o reproducir conferencias H.32X (por ejemplo, H.323 y H.324) o MMATE.

Un archivo ASF se organiza en secciones denominadas "objetos". Hay tres objetos de nivel superior, un objeto Header y un objeto Data (ambos obligatorios), además de un objeto Index opcional. El objeto Header contiene información general sobre el archivo, como el tamaño del archivo, el número de secuencias, los métodos de corrección de errores y los códecs usados. Los metadatos también se almacenan aquí. El objeto Header es el único objeto de nivel superior que puede contener otros objetos. El objeto Data contiene los datos de flujo, organizados en paquetes. El objeto Índice simple contiene una lista de pares de índice/fotograma clave asociados que permiten a las aplicaciones buscar a través de un archivo de forma eficaz. El índice asociado a cada fotograma clave puede ser un tiempo de presentación, un número de fotograma de vídeo o una marca de tiempo de referencia.

Cada objeto de nivel superior o inferior comienza con un identificador único global (GUID) y un valor de tamaño. Estos números permiten al lector de archivos analizar la información en los lugares adecuados en objetos identificables. Debido a estos GUID, los objetos de nivel inferior se pueden enviar en cualquier orden y seguir siendo reconocidos. El formato ASF está diseñado para superar la recepción de datos inexacta. Todavía se puede leer un archivo ASF descargado parcialmente, siempre que contenga el objeto Header y al menos un objeto Data.

Información detallada sobre ASF en presentada en la especificación de ASF. Puede descargar la especificación desde el [sitio web de Microsoft](https://download.microsoft.com/download/7/9/0/790fecaa-f64a-4a5e-a430-0bccdab3f1b4/ASF_Specification.doc).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Acerca del SDK Windows Media Format**](about-the-windows-media-format-sdk.md)
</dt> </dl>

 

 




