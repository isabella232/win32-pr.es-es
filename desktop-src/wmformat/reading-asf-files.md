---
title: Lectura de archivos ASF
description: Lectura de archivos ASF
ms.assetid: e0aabe05-b317-42ac-85fc-5a75165722d4
keywords:
- Windows SDK de formato multimedia, lectura de archivos ASF
- Windows SDK de formato multimedia, formato de sistemas avanzados (ASF)
- Formato de sistemas avanzados (ASF), leer archivos
- ASF (formato de sistemas avanzados), leer archivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32f35cbd0e9a7dde800e23f83337ac30cdd66582
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127466669"
---
# <a name="reading-asf-files"></a>Lectura de archivos ASF

El SDK Windows media format se puede usar para entregar ejemplos multimedia desde un archivo ASF. Se usan dos objetos para recuperar ejemplos, el objeto de lector y el objeto de lector sincrónico.

El objeto lector es el objeto de lectura original del SDK Windows Media Format. El objeto lector usa una arquitectura asincrónica para insertar ejemplos en una aplicación. Las aplicaciones creadas con el objeto reader deben implementar funciones de devolución de llamada que respondan a los distintos mensajes y eventos resultantes de este modelo multiproceso. Para mayor claridad, esta sección hará referencia al objeto lector como lector asincrónico.

El objeto de lector sincrónico es nuevo para esta versión del SDK Windows Media Format. El lector sincrónico no usa varios subprocesos en el procesamiento de ejemplos de archivos ASF. Una aplicación creada con el lector sincrónico recupera ejemplos a petición, en lugar de esperar a que el lector los envíe.

Al crear una aplicación para leer archivos ASF, debe elegir el objeto de lector que se va a usar. En general, las aplicaciones diseñadas para proporcionar Windows contenido basado en multimedia deben crearse mediante el lector asincrónico, mientras que las aplicaciones diseñadas para editar archivos ASF deben crearse con el lector sincrónico.

En la tabla siguiente se enumeran las características principales de ambos objetos de lector. Use esta tabla para ayudar a determinar qué objeto se va a usar para la aplicación.



| Característica                                                                    | Lector asincrónico | Lector de sincronización |
|----------------------------------------------------------------------------|--------------|-------------|
| Lectura de ejemplos sin comprimir por número de salida                                 | Sí          | Sí         |
| Lectura de ejemplos comprimidos por número de secuencia                                   | Sí          | Sí         |
| Lectura de ejemplos sin comprimir por número de secuencia                                 | No           | Sí         |
| Lectura desde el sitio de Internet                                                    | Sí          | No          |
| Leer metadatos                                                              | Sí          | Sí         |
| Buscar el tiempo de presentación                                                  | Sí          | Sí         |
| Buscar para enmarcar                                                              | Sí          | Sí         |
| Buscar en marcador                                                             | Sí          | No          |
| Cambio entre la entrega de muestras comprimida y sin comprimir durante la reproducción | No           | Sí         |
| Abrir archivos mediante **la interfaz IStream**                                     | Sí          | Sí         |



 

En las secciones siguientes se proporciona más información sobre cómo trabajar con los dos objetos de lector.



| Sección                                                                                      | Descripción                                                                                                                             |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| [Trabajar con salidas](working-with-outputs.md)                                             | Describe cómo usar y manipular salidas. Se aplica a ambos objetos de lector.                                                            |
| [Asignación de búferes para la lectura de archivos](allocating-buffers-for-file-reading.md)               | Describe cómo usar su propio grupo de búferes para contener ejemplos entregados por el lector o el lector sincrónico.                            |
| [Leer metadatos en reproducción](reading-metadata-at-playback.md)                             | Describe cómo aprovechar la compatibilidad con metadatos en la reproducción. Se aplica a ambos objetos de lector.                                        |
| [Obtener información de perfil en reproducción](getting-profile-information-at-playback.md)       | Describe cómo acceder a la información de perfil de los archivos abiertos. Se aplica a ambos objetos de lector.                                           |
| [Lectura de audio multicanal](reading-multichannel-audio.md)                                 | Describe cómo configurar el escritor para descodificar correctamente el audio multicanal.                                                            |
| [Contenido de representación](rendering-content.md)                                                   | Describe los problemas relacionados con la representación de muestras sin comprimir. Se aplica a ambos objetos de lector.                                         |
| [Obtención del mejor rendimiento de búsqueda de vídeo](getting-the-best-video-seeking-performance.md) | Describe formas de mejorar el rendimiento de la búsqueda de vídeo.                                                                                    |
| [Leer archivos con el lector asincrónico](reading-files-with-the-asynchronous-reader.md) | Describe cómo leer archivos ASF mediante el objeto de lector asincrónico.                                                                   |
| [Lectura de archivos con el lector sincrónico](reading-files-with-the-synchronous-reader.md)   | Describe cómo leer archivos ASF mediante el objeto de lector sincrónico.                                                                    |
| [Habilitación de la aceleración de vídeo de DirectX](enabling-directx-video-acceleration.md)               | Describe cómo implementar la aceleración de vídeo de DirectX para usar las características de aceleración de hardware de algunas tarjetas de vídeo para la decodificación de vídeo. |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Guía de programación**](programming-guide.md)
</dt> <dt>

[**Objeto del lector**](reader-object.md)
</dt> <dt>

[**Objeto del lector sincrónico**](synchronous-reader-object.md)
</dt> </dl>

 

 




