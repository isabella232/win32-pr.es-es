---
title: SDK de Windows Media Format 11
description: SDK de Windows Media Format 11
ms.assetid: 875e8914-b861-46f1-9391-8724ff77d26b
keywords:
- SDK de Windows Media Format, acerca de
- SDK de Windows Media
- Windows Media Format SDK, Advanced Systems Format (ASF)
- Advanced Systems Format (ASF), acerca de
- ASF (formato de sistemas avanzados), acerca de
- Windows Media Format SDK, características
- SDK de Windows Media Format, características clave
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 363c268194b476b6d3326a9c57fe1e709d17e2fe
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/09/2020
ms.locfileid: "104488440"
---
# <a name="windows-media-format-11-sdk"></a>SDK de Windows Media Format 11

En esta documentación se describe el kit de desarrollo de software (SDK) de Microsoft Windows Media Format y se aplica a las versiones de 32 bits y basadas en x64 del SDK.

El SDK de Windows Media Format es un componente del kit de desarrollo de software (SDK) de Microsoft Windows Media. Otros componentes incluyen Windows Media Services SDK, Windows Media Encoder SDK, Windows Media Rights Manager SDK, Windows Media Administrador de dispositivos SDK y Windows Media Player SDK.

El SDK de Windows Media Format proporciona a los desarrolladores de aplicaciones acceso a los componentes del formato de Windows Media. Estos componentes incluyen el contenedor de archivos Advanced Systems Format (ASF), los códecs de Windows Media Audio y vídeo, la funcionalidad básica de transmisión por secuencias de red y la administración de derechos digitales. Los objetos del SDK de Windows Media Format manipulan los componentes de Windows Media en un nivel bajo; los demás componentes del SDK de Windows Media incluyen objetos que funcionan en un nivel superior.

El propósito principal del SDK de Windows Media Format es permitir a los desarrolladores crear aplicaciones que reproduzcan, escriban, editen, cifren y entreguen archivos de formato de sistema avanzado (ASF) y secuencias de red. Estos archivos y secuencias suelen contener contenido de audio y vídeo codificado mediante los códecs de vídeo y Windows Media Audio. Sin embargo, ASF puede contener cualquier tipo de datos. Para obtener más información acerca de la estructura de contenedor de formato de sistemas avanzados, consulte [información general del formato ASF](overview-of-the-asf-format.md).

Las principales características del SDK de Windows Media Format son:

-   Compatibilidad con códecs líderes del sector. El SDK de Windows Media Format 11 incluye el códec Microsoft Windows Media Video 9 y el códec Microsoft Windows Media Audio 9,1. Ambos códecs proporcionan una codificación excepcional de contenido multimedia digital. Una novedad de esta versión es el códec de perfil avanzado de Windows Media Video 9, que proporciona optimizaciones para difundir vídeo. Este SDK también incluye el códec de pantalla de Microsoft Windows Media Video 9 para comprimir la actividad de la pantalla del equipo durante las sesiones de aplicaciones de usuario y el códec de voz Windows Media Audio 9,1, que codifica el audio de baja complejidad como la voz y se adapta de forma inteligente a audio más complejo, como música, para una representación superior de escenarios de música de voz combinados.
-   Compatibilidad para escribir archivos ASF. Los archivos se crean en función de los perfiles personalizables, lo que facilita la configuración y la normalización de los archivos. Este SDK se puede usar para escribir archivos de más de 2 gigabytes, lo que permite archivos de mayor calidad y continuos.
-   Compatibilidad para leer archivos ASF. Este SDK proporciona compatibilidad para leer archivos ASF locales, así como para leer datos ASF que se transmiten por secuencias a través de una red. También se proporciona compatibilidad con muchas características de lectura avanzadas, como la compatibilidad nativa con varios archivos de velocidad de bits (MBR), que contienen varias secuencias con el mismo contenido codificado a velocidades de bits diferentes. El lector selecciona automáticamente la secuencia MBR que se va a usar, en función del ancho de banda disponible en el momento de la reproducción.
-   Compatibilidad para entregar secuencias ASF a través de una red. Este SDK proporciona compatibilidad para entregar datos ASF a través de HTTP a equipos remotos en una red y también para entregar datos directamente a un servidor remoto de Windows Media.
-   Compatibilidad con la edición de metadatos en archivos ASF. La información sobre un archivo y su contenido se manipula fácilmente con este SDK. Los desarrolladores pueden usar el sólido sistema de atributos de metadatos que se incluyen en el SDK, o crear atributos personalizados para satisfacer sus necesidades.
-   Compatibilidad con aplicaciones de edición de contenido. Este SDK permite a las aplicaciones buscar puntos en un archivo por el tiempo de presentación y por el fotograma de vídeo. Además, los archivos creados con el SDK de Windows Media Format pueden mantener marcas de tiempo en los formatos usados en la producción de películas y televisión.
-   Compatibilidad con la lectura y la edición de metadatos en archivos MP3. Este SDK proporciona compatibilidad integrada para leer archivos MP3 con los mismos métodos que se usan para leer archivos ASF. Las aplicaciones compiladas con el SDK de Windows Media Format también pueden editar atributos de metadatos en archivos MP3 mediante la compatibilidad integrada con las etiquetas ID3 más comunes utilizadas por los creadores de contenido.
-   Compatibilidad con la protección de Rights Management digital. Este SDK proporciona métodos para leer y escribir archivos ASF y secuencias de red que están protegidos por Rights Management digitales para evitar la reproducción o copia no autorizadas del contenido.

Para descargar el SDK de Windows Media Format, consulte la página de [descargas de Windows Media](https://msdn.microsoft.com/windows/desktop/aa904949) en el sitio web de Microsoft.

En este documento se describe cómo puede desarrollar aplicaciones multimedia digitales con el SDK de Windows Media Format. Se divide en las secciones siguientes.

> [!Note]  
> Aunque este documento contiene información sobre la versión más reciente del SDK de Windows Media Format, la mayoría de las características que describe son compatibles con las versiones anteriores del SDK. Las páginas de referencia de los métodos, funciones, estructuras y enumeraciones del SDK de Windows Media Format incluyen requisitos de versión.

 



| Sección                                                                                                          | Descripción                                                                                                                                                                                              |
|------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Acerca del SDK de Windows Media Format](about-the-windows-media-format-sdk.md)                                     | Proporciona información general e información general que debe conocer antes de intentar crear aplicaciones.                                                                                  |
| [Guía de programación](programming-guide.md)                                                                       | Proporciona instrucciones detalladas para realizar varias tareas, como lectura, escritura e indexación de archivos, protección de archivos con Rights Management digital, transmisión de datos ASF a través de una red, etc. |
| [Referencia de programación](programming-reference.md)                                                               | Proporciona información de referencia para las interfaces, los métodos, las funciones, las estructuras, los tipos de enumeración y las constantes relacionadas con el formato de Windows Media.                                                     |
| [Interfaces de códec de Windows Media Audio y vídeo](windows-media-audio-and-video-codec-interfaces--deprecated.md) | Proporciona instrucciones para usar los objetos multimedia digitales (DMOs) de códec de vídeo y de Windows Media Audio directamente.                                                                                           |
| [*Glosario*](wmformat-glossary.md)                                                                              | Define los términos usados en la documentación del SDK de Windows Media Format.                                                                                                                                    |



 

 

 




