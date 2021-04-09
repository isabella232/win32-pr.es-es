---
title: Trabajar con índices
description: Trabajar con índices
ms.assetid: 7daa4b29-0597-462d-ad65-135d0ef7362d
keywords:
- Windows Media Format SDK, índices
- Advanced Systems Format (ASF), índices
- ASF (formato de sistemas avanzados), índices
- índices, acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34057046223daf2e16950e0e38b1b0db5df32c4a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903284"
---
# <a name="working-with-indexes"></a>Trabajar con índices

El SDK de Windows Media Format admite la búsqueda y el progresado a través del contenido. La búsqueda le permite especificar un lugar en la escala de tiempo del archivo para comenzar la reproducción. El avance le permite avanzar y rebobinar la salida de un archivo de forma rápida. Los archivos se deben indizar para aprovechar las ventajas de estas características. Un índice es una serie de valores que representan las posiciones del archivo (tiempos de presentación, números de marco o códigos de tiempo de SMTP) con los desplazamientos correspondientes en la sección de datos del archivo para cada uno. La indexación es más importante para las secuencias de vídeo, ya que el tiempo de presentación de la secuencia de audio se puede estimar fácilmente. Sin embargo, algunas secuencias de audio también pueden requerir índices. De forma predeterminada, el escritor indexará cada nuevo archivo ASF. Si se realizan cambios en el contenido de un archivo, debe actualizar el índice mediante el objeto indexador.

El indexador admite la indexación temporal y la basada en tramas, así como la indexación basada en códigos de tiempo de SMPTE (si existen). El escritor creará un índice temporal de forma predeterminada para cada nueva secuencia de vídeo codificada en un archivo. Debe configurar y llamar explícitamente al indexador para crear un índice de código de tiempo basado en marco o SMPTE.

Cuando se realizan cambios en el contenido de un archivo ASF, se debe volver a indexar.

En las secciones siguientes se muestra código de ejemplo para realizar tareas de indexación comunes.

-   [Para deshabilitar la indexación automática](to-disable-automatic-indexing.md)
-   [Para configurar el indexador](to-configure-the-indexer.md)
-   [Para indexar un archivo ASF](to-index-an-asf-file.md)
-   [Para detener la indización en curso](to-stop-indexing-in-progress.md)

Además, la aplicación de ejemplo DSCopy muestra el uso del indexador. Para obtener más información, vea [aplicaciones de ejemplo](sample-applications.md).

 

 




