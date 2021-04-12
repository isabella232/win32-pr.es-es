---
title: Leer archivos ASF
description: Leer archivos ASF
ms.assetid: e0aabe05-b317-42ac-85fc-5a75165722d4
keywords:
- SDK de Windows Media Format, leer archivos ASF
- Windows Media Format SDK, Advanced Systems Format (ASF)
- Advanced Systems Format (ASF), leer archivos
- ASF (formato de sistemas avanzados), lectura de archivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32f35cbd0e9a7dde800e23f83337ac30cdd66582
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357587"
---
# <a name="reading-asf-files"></a>Leer archivos ASF

El SDK de Windows Media Format se puede usar para proporcionar ejemplos de medios desde un archivo ASF. Se usan dos objetos para recuperar ejemplos, el objeto lector y el objeto lector sincrónico.

El objeto lector es el objeto de lectura original en el SDK de Windows Media Format. El objeto lector utiliza una arquitectura asincrónica para enviar ejemplos a una aplicación. Las aplicaciones compiladas con el objeto lector deben implementar funciones de devolución de llamada que respondan a los distintos mensajes y eventos que son el resultado de este modelo multiproceso. Para mayor claridad, en esta sección se hará referencia al objeto lector como lector asincrónico.

El objeto lector sincrónico es nuevo en esta versión del SDK de Windows Media Format. El lector sincrónico no utiliza varios subprocesos para procesar muestras de archivos ASF. Una aplicación compilada con el lector sincrónico recupera ejemplos a petición, en lugar de esperar a que el lector los envíe.

Al crear una aplicación para leer archivos ASF, debe elegir qué objeto de lector se va a usar. En general, las aplicaciones diseñadas para ofrecer contenido basado en Windows Media deben crearse mediante el lector asincrónico, mientras que las aplicaciones diseñadas para editar archivos ASF deben crearse con el lector sincrónico.

En la tabla siguiente se enumeran las características principales de ambos objetos de lector. Use esta tabla para ayudar a determinar qué objeto se va a utilizar para la aplicación.



| Característica                                                                    | Lector asincrónico | Lector de sincronización |
|----------------------------------------------------------------------------|--------------|-------------|
| Leer muestras sin comprimir por número de salida                                 | Sí          | Sí         |
| Leer muestras comprimidas por número de secuencia                                   | Sí          | Sí         |
| Leer muestras sin comprimir por número de secuencia                                 | No           | Sí         |
| Leer del sitio de Internet                                                    | Sí          | No          |
| Leer metadatos                                                              | Sí          | Sí         |
| Buscar en el tiempo de presentación                                                  | Sí          | Sí         |
| Buscar en marco                                                              | Sí          | Sí         |
| Buscar en el marcador                                                             | Sí          | No          |
| Cambiar entre la entrega de muestras comprimidas y sin comprimir durante la reproducción | No           | Sí         |
| Abrir archivos mediante la interfaz **IStream**                                     | Sí          | Sí         |



 

En las secciones siguientes se proporciona más información sobre cómo trabajar con los dos objetos de lector.



| Sección                                                                                      | Descripción                                                                                                                             |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| [Trabajar con salidas](working-with-outputs.md)                                             | Describe cómo usar y manipular salidas. Se aplica a ambos objetos de lector.                                                            |
| [Asignar búferes para la lectura de archivos](allocating-buffers-for-file-reading.md)               | Describe cómo usar su propio grupo de búferes para contener ejemplos entregados por el lector o el lector sincrónico.                            |
| [Leer metadatos en la reproducción](reading-metadata-at-playback.md)                             | Describe cómo aprovechar la compatibilidad de metadatos en la reproducción. Se aplica a ambos objetos de lector.                                        |
| [Obtención de información de perfil en la reproducción](getting-profile-information-at-playback.md)       | Describe cómo obtener acceso a la información de Perfil de los archivos abiertos. Se aplica a ambos objetos de lector.                                           |
| [Lectura de audio multicanal](reading-multichannel-audio.md)                                 | Describe cómo configurar el escritor para descodificar correctamente audio multicanal.                                                            |
| [Representación de contenido](rendering-content.md)                                                   | Describe los problemas relacionados con la representación de ejemplos sin comprimir. Se aplica a ambos objetos de lector.                                         |
| [Obtención del mejor rendimiento de búsqueda de vídeo](getting-the-best-video-seeking-performance.md) | Describe formas de mejorar el rendimiento de búsqueda de vídeo.                                                                                    |
| [Leer archivos con el lector asincrónico](reading-files-with-the-asynchronous-reader.md) | Describe cómo leer archivos ASF con el objeto lector asincrónico.                                                                   |
| [Leer archivos con el lector sincrónico](reading-files-with-the-synchronous-reader.md)   | Describe cómo leer archivos ASF con el objeto lector sincrónico.                                                                    |
| [Habilitar la aceleración de vídeo de DirectX](enabling-directx-video-acceleration.md)               | Describe cómo implementar la aceleración de vídeo de DirectX para usar las características de aceleración de hardware de algunas tarjetas de vídeo para descodificar vídeo. |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Guía de programación**](programming-guide.md)
</dt> <dt>

[**Objeto del lector**](reader-object.md)
</dt> <dt>

[**Objeto del lector sincrónico**](synchronous-reader-object.md)
</dt> </dl>

 

 




