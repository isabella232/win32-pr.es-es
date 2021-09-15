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
- Formato de sistemas avanzados (ASF), lectura sincrónica de archivos
- ASF (formato de sistemas avanzados), lectura de archivos sincrónica
- lectura asincrónica de archivos
- lectura sincrónica de archivos
- lectores sincrónicos, características de lectura de archivos
- lectura de archivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a83d3ce112d0d9e47626b4f7850f760da5c6583e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127570233"
---
# <a name="file-reading-features"></a>Características de lectura de archivos

La lectura de archivos ASF es una de las características principales del SDK Windows Media Format. Se admiten dos tipos de lectura: asincrónica y sincrónica. El objeto lector controla la lectura asincrónica de archivos. El objeto de lector sincrónico se usa para leer archivos de forma sincrónica. Para obtener más información sobre los diferentes objetos de lectura, vea [Objeto lector](reader-object.md) y Objeto de [lector sincrónico](synchronous-reader-object.md).

En el escenario de lectura de archivos asincrónicos más básico, debe implementar un método de devolución de llamada al que llamará el objeto lector cuando los ejemplos estén listos. Después de empezar a leer un archivo, la aplicación espera a que los ejemplos se entreguen al método de devolución de llamada. La lectura asincrónica es útil para las aplicaciones de reproductor y admite características que no están disponibles con lectura sincrónica. Si la aplicación necesita leer archivos de una ubicación de red o interactuar con un servidor que ejecuta Servicios de Windows Media, debe usar el objeto de lector. La desventaja del objeto lector es que se usa un subproceso independiente para cada salida entregada. Además, el objeto reader no es tan flexible como el lector sincrónico en cómo puede entregar ejemplos.

Con el lector sincrónico no es necesario usar ningún método de devolución de llamada. En su lugar, seleccione una parte del archivo para leer y recuperar los ejemplos de uno en uno con llamadas a métodos. El lector sincrónico es adecuado para las necesidades de las aplicaciones de edición de contenido, donde es esencial el acceso rápido a ejemplos específicos. Dado que el lector sincrónico no usa métodos de devolución de llamada, puede crear aplicaciones para leer archivos ASF con una sobrecarga de codificación mínima. Sin embargo, el lector sincrónico no puede abrir un archivo desde una ubicación de red, ni interactuar con un servidor que ejecuta Servicios de Windows Media o leer archivos protegidos con [*DRM.*](wmformat-glossary.md)

En los temas siguientes se tratan las características del lector y el lector sincrónico.



| Tema                                                              | Descripción                                                                                                        |
|--------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| [Compatibilidad con el ejemplo asignado por el usuario](user-allocated-sample-support.md) | Describe la asignación de búfer en el lector y el lector sincrónico, y cómo la asignación de usuarios puede mejorar el rendimiento. |
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

 

 




