---
title: Características de lectura de archivos
description: Características de lectura de archivos
ms.assetid: ba6dd328-2250-4867-94e0-f66c70ac1bac
keywords:
- Windows SDK de formato multimedia, características de lectura de archivos
- Windows SDK de formato multimedia, lectura asincrónica de archivos
- Windows SDK de formato multimedia, lectura de archivos sincrónica
- Advanced Systems Format (ASF), características de lectura de archivos
- ASF (formato de sistemas avanzados), características de lectura de archivos
- Formato de sistemas avanzados (ASF), lectura asincrónica de archivos
- ASF (formato de sistemas avanzados), lectura asincrónica de archivos
- Formato de sistemas avanzados (ASF), lectura de archivos sincrónica
- ASF (formato de sistemas avanzados), lectura de archivos sincrónica
- lectura asincrónica de archivos
- lectura de archivos sincrónica
- lectores sincrónicos, características de lectura de archivos
- lectura de archivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e8efb7bc0fca898c1a63db586b158b39b4bb9daa9ad051e7a61fe8c4a5d6b24
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119930535"
---
# <a name="file-reading-features"></a>Características de lectura de archivos

La lectura de archivos ASF es una de las características principales del SDK Windows Media Format. Se admiten dos tipos de lectura: asincrónica y sincrónica. El objeto lector controla la lectura asincrónica de archivos. El objeto de lector sincrónico se usa para leer archivos sincrónicamente. Para obtener más información sobre los diferentes objetos de lectura, vea [Objeto lector](reader-object.md) y Objeto de [lector sincrónico](synchronous-reader-object.md).

En el escenario de lectura de archivos asincrónicos más básico, debe implementar un método de devolución de llamada al que llamará el objeto lector cuando los ejemplos estén listos. Después de empezar a leer un archivo, la aplicación espera a que los ejemplos se entreguen al método de devolución de llamada. La lectura asincrónica es útil para las aplicaciones de reproductor y admite características que no están disponibles con lectura sincrónica. Si la aplicación necesita leer archivos desde una ubicación de red o interactuar con un servidor que ejecuta Servicios de Windows Media, debe usar el objeto lector. La desventaja del objeto de lector es que se usa un subproceso independiente para cada salida entregada. Además, el objeto reader no es tan flexible como el lector sincrónico en cómo puede entregar ejemplos.

Con el lector sincrónico no es necesario usar ningún método de devolución de llamada. En su lugar, seleccione una parte del archivo para leer y recuperar los ejemplos de uno en uno con llamadas a métodos. El lector sincrónico es adecuado para las necesidades de las aplicaciones de edición de contenido, donde el acceso rápido a ejemplos específicos es esencial. Dado que el lector sincrónico no usa métodos de devolución de llamada, puede crear aplicaciones para leer archivos ASF con un mínimo de sobrecarga de codificación. Sin embargo, el lector sincrónico no puede abrir un archivo desde una ubicación de red, ni interactuar con un servidor que ejecuta Servicios de Windows Media o leer archivos protegidos con [*DRM.*](wmformat-glossary.md)

En los temas siguientes se tratan las características del lector y del lector sincrónico.



| Tema                                                              | Descripción                                                                                                        |
|--------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| [Compatibilidad con ejemplos asignados por el usuario](user-allocated-sample-support.md) | Describe la asignación de búfer en el lector y el lector sincrónico, y cómo la asignación de usuarios puede mejorar el rendimiento. |
| [Enumeración de formato de salida](output-format-enumeration.md)         | Describe la enumeración de formato de salida.                                                                               |



 

Además, los temas siguientes de la sección de características de escritura también se aplican a la lectura de archivos:

-   [Tamaño de vídeo](video-resizing.md)
-   [Conversión de espacio de color](color-space-conversion.md)
-   [Remuestreo de audio](audio-resampling.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Características**](features.md)
</dt> <dt>

[**Lectura de archivos ASF**](reading-asf-files.md)
</dt> </dl>

 

 




