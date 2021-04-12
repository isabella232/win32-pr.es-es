---
title: Características de lectura de archivos
description: Características de lectura de archivos
ms.assetid: ba6dd328-2250-4867-94e0-f66c70ac1bac
keywords:
- SDK de Windows Media Format, características de lectura de archivos
- SDK de Windows Media Format, lectura asincrónica de archivos
- SDK de Windows Media Format, lectura sincrónica de archivos
- Advanced Systems Format (ASF), características de lectura de archivos
- ASF (formato de sistemas avanzados), características de lectura de archivos
- Advanced Systems Format (ASF), lectura asincrónica de archivos
- ASF (formato de sistemas avanzados), lectura asincrónica de archivos
- Advanced Systems Format (ASF), lectura de archivos sincrónicos
- ASF (formato de sistemas avanzados), lectura de archivos sincrónicos
- lectura asincrónica de archivos
- lectura de archivos sincrónicos
- lectores sincrónicos, características de lectura de archivos
- lectura de archivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a83d3ce112d0d9e47626b4f7850f760da5c6583e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357683"
---
# <a name="file-reading-features"></a>Características de lectura de archivos

La lectura de archivos ASF es una de las características principales del SDK de Windows Media Format. Se admiten dos tipos de lectura: asincrónicos y sincrónicos. El objeto lector controla la lectura asincrónica de archivos. El objeto lector sincrónico se usa para leer archivos de forma sincrónica. Para obtener más información sobre los diferentes objetos de lectura, vea [objeto lector](reader-object.md) y [objeto lector sincrónico](synchronous-reader-object.md).

En el escenario de lectura de archivos asincrónico más básico, debe implementar un método de devolución de llamada al que el objeto lector llamará cuando los ejemplos estén listos. Después de empezar a leer un archivo, la aplicación espera a que se entreguen los ejemplos en el método de devolución de llamada. La lectura asincrónica es útil para las aplicaciones de reproductor y admite características no disponibles con lectura sincrónica. Si la aplicación necesita leer archivos de una ubicación de red o interactuar con un servidor que ejecuta Windows Media Services, debe usar el objeto lector. El inconveniente del objeto lector es que se usa un subproceso independiente para cada salida entregada. Además, el objeto de lector no es tan flexible como el lector sincrónico en cómo puede proporcionar ejemplos.

Con el lector sincrónico no es necesario usar ningún método de devolución de llamada. En su lugar, se selecciona una parte del archivo que se va a leer y se recuperan los ejemplos de uno en uno con llamadas a métodos. El lector sincrónico está bien adaptado a las necesidades de las aplicaciones de edición de contenido, donde es esencial el acceso rápido a ejemplos específicos. Dado que el lector sincrónico no usa ningún método de devolución de llamada, puede crear aplicaciones para leer archivos ASF con una sobrecarga de codificación mínima. Sin embargo, el lector sincrónico no puede abrir un archivo desde una ubicación de red o interactuar con un servidor que ejecuta Windows Media Services o leer archivos protegidos con [*DRM*](wmformat-glossary.md).

En los temas siguientes se describen las características del lector y el lector sincrónico.



| Tema                                                              | Descripción                                                                                                        |
|--------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| [Compatibilidad de ejemplo asignada por el usuario](user-allocated-sample-support.md) | Describe la asignación de búferes en el lector y el lector sincrónico, y cómo la asignación de usuarios puede mejorar el rendimiento. |
| [Enumeración del formato de salida](output-format-enumeration.md)         | Describe la enumeración del formato de salida.                                                                               |



 

Además, los siguientes temas de la sección características de escritura también se aplican a la lectura de archivos:

-   [Cambio de tamaño de vídeo](video-resizing.md)
-   [Conversión de espacio de colores](color-space-conversion.md)
-   [Remuestreo de audio](audio-resampling.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Características**](features.md)
</dt> <dt>

[**Leer archivos ASF**](reading-asf-files.md)
</dt> </dl>

 

 




