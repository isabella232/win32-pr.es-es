---
title: Windows SDK de formato multimedia 11
description: Windows SDK de formato multimedia 11
ms.assetid: 875e8914-b861-46f1-9391-8724ff77d26b
keywords:
- Windows SDK de formato multimedia, acerca de
- Windows SDK de multimedia
- Windows SDK de formato multimedia, formato de sistemas avanzados (ASF)
- Formato de sistemas avanzados (ASF), acerca de
- ASF (formato de sistemas avanzados), acerca de
- Windows SDK de formato multimedia, características
- Windows SDK de formato multimedia, características clave
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70af68402ea5a22a9499ca09fd4b2e4022f304ee5ebf68a4f877a978ad168e4f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119839435"
---
# <a name="windows-media-format-11-sdk"></a>Windows SDK de formato multimedia 11

En esta documentación se describe el Kit de desarrollo de software (SDK) de formato multimedia (SDK) de Microsoft Windows y se aplica a las versiones basadas en x64 y de 32 bits del SDK.

El SDK Windows Media Format es un componente del Kit de desarrollo de software multimedia (SDK) de Microsoft Windows. Otros componentes incluyen el SDK de Servicios de Windows Media, el SDK de Windows Media Encoder, el SDK de Windows Media Rights Manager, el SDK de Windows Media Administrador de dispositivos SDK y Reproductor de Windows Media SDK.

El SDK Windows Media Format proporciona a los desarrolladores de aplicaciones acceso a los componentes de Windows Media Format. Estos componentes incluyen el contenedor de archivos Advanced Systems Format (ASF), los códecs Windows Media Audio y Video, la funcionalidad básica de streaming de red y la administración de derechos digitales. Los objetos del SDK Windows Media Format manipulan los componentes de Windows Media en un nivel bajo; los demás componentes del SDK Windows Media incluyen objetos que funcionan en un nivel superior.

El propósito principal del SDK de Windows Media Format es permitir a los desarrolladores crear aplicaciones que reproducen, escriben, editan, cifran y entregan archivos y secuencias de red de Advanced Systems Format (ASF). Estos archivos y secuencias normalmente contienen contenido de audio y vídeo codificado mediante los códecs Windows audio multimedia y vídeo. Sin embargo, ASF puede contener cualquier tipo de datos. Para obtener más información sobre la estructura de contenedores Advanced Systems Format, vea [Overview of the ASF Format](overview-of-the-asf-format.md).

Las características clave del SDK Windows Media Format son:

-   Compatibilidad con códecs líderes del sector. El SDK Windows Media Format 11 incluye el códec Microsoft Windows Media Video 9 y el códec Microsoft Windows Media Audio 9.1. Ambos códecs proporcionan una codificación excepcional del contenido multimedia digital. La novedad de esta versión es el códec de perfil avanzado Windows Media Video 9, que proporciona optimizaciones para el vídeo de difusión. Este SDK también incluye el códec de pantalla Microsoft Windows Media Video 9 para comprimir la actividad de pantalla del equipo durante las sesiones de las aplicaciones de usuario, y el códec de voz Windows Media Audio 9.1, que codifica audio de baja complejidad, como voz, y se adapta de forma inteligente a audio más complejo, como música, para una representación superior de escenarios combinados de voz y música.
-   Compatibilidad con la escritura de archivos ASF. Los archivos se crean en función de perfiles personalizables, lo que permite una configuración y normalización sencillas de los archivos. Este SDK se puede usar para escribir archivos de más de 2 gigabytes, lo que permite archivos continuos más largos y de mejor calidad.
-   Compatibilidad con la lectura de archivos ASF. Este SDK proporciona compatibilidad para leer archivos ASF locales, así como para leer los datos de ASF que se transmiten a través de una red. También se proporciona compatibilidad con muchas características avanzadas de lectura, como la compatibilidad nativa con varios archivos de velocidad de bits (MBR), que contienen varias secuencias con el mismo contenido codificado a velocidades de bits diferentes. El lector selecciona automáticamente la secuencia de MBR que se va a usar, en función del ancho de banda disponible en el momento de la reproducción.
-   Compatibilidad con la entrega de flujos de ASF a través de una red. Este SDK proporciona compatibilidad para entregar datos de ASF a través de HTTP a equipos remotos de una red y también para entregar datos directamente a un servidor multimedia Windows remoto.
-   Compatibilidad con la edición de metadatos en archivos ASF. La información sobre un archivo y su contenido se manipula fácilmente con este SDK. Los desarrolladores pueden usar el sólido sistema de atributos de metadatos incluidos en el SDK o crear atributos personalizados para satisfacer sus necesidades.
-   Compatibilidad con aplicaciones de edición de contenido. Este SDK permite a las aplicaciones buscar puntos dentro de un archivo por tiempo de presentación y por fotograma de vídeo. Además, los archivos creados mediante el SDK Windows Media Format pueden mantener marcas de tiempo en formatos usados en producción de películas y televisión.
-   Compatibilidad con la lectura y edición de metadatos en archivos MP3. Este SDK proporciona compatibilidad integrada para leer archivos MP3 con los mismos métodos que se usan para leer archivos ASF. Las aplicaciones creadas con el SDK Windows Media Format también pueden editar atributos de metadatos en archivos MP3 mediante la compatibilidad integrada con las etiquetas ID3 más comunes que usan los creadores de contenido.
-   Compatibilidad con la protección Rights Management digital. Este SDK proporciona métodos para leer y escribir archivos ASF y secuencias de red que están protegidos por Digital Rights Management para evitar la reproducción no autorizada o la copia del contenido.

Para descargar el SDK Windows Media Format, consulte la [página Windows descargas](https://msdn.microsoft.com/windows/desktop/aa904949) multimedia en el sitio web de Microsoft.

En este documento se describe cómo puede desarrollar aplicaciones multimedia digitales mediante Windows SDK de formato multimedia. Se divide en las secciones siguientes.

> [!Note]  
> Aunque este documento contiene información sobre la versión más reciente del SDK de Windows Media Format, la mayoría de las características que describe son compatibles con versiones anteriores del SDK. Las páginas de referencia de los métodos, funciones, estructuras y enumeraciones del SDK Windows Media Format incluyen requisitos de versión.

 



| Sección                                                                                                          | Descripción                                                                                                                                                                                              |
|------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Acerca del SDK Windows Media Format](about-the-windows-media-format-sdk.md)                                     | Proporciona información general e información general con la que debe estar familiarizado antes de intentar crear aplicaciones.                                                                                  |
| [Guía de programación](programming-guide.md)                                                                       | Proporciona instrucciones detalladas para realizar varias tareas, como leer, escribir e indexar archivos, proteger archivos con Digital Rights Management, transmitir datos de ASF a través de una red, y así sucesivamente. |
| [Referencia de programación](programming-reference.md)                                                               | Proporciona información de referencia para las interfaces, métodos, funciones, estructuras, tipos de enumeración y constantes relacionadas con Windows media format.                                                     |
| [Windows Interfaces de códecs de audio y vídeo multimedia](windows-media-audio-and-video-codec-interfaces--deprecated.md) | Proporciona instrucciones para usar los objetos multimedia (DMO) Windows códec de audio multimedia y vídeo directamente.                                                                                           |
| [*Glosario*](wmformat-glossary.md)                                                                              | Define los términos usados en la documentación del SDK Windows Media Format.                                                                                                                                    |



 

 

 




