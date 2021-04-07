---
title: Índices
description: Índices
ms.assetid: 54c694f6-3c10-4d7c-bcd1-f2b17d652e8e
keywords:
- Windows Media Format SDK, índices
- Advanced Systems Format (ASF), índices
- ASF (formato de sistemas avanzados), índices
- SDK de Windows Media Format, índices temporales
- Advanced Systems Format (ASF), índices temporales
- ASF (formato de sistemas avanzados), índices temporales
- SDK de Windows Media Format, índices basados en marcos
- Advanced Systems Format (ASF), índices basados en tramas
- ASF (formato de sistemas avanzados), índices basados en tramas
- SDK de Windows Media Format, códigos de tiempo SMPTE
- Advanced Systems Format (ASF), códigos de tiempo SMPTE
- ASF (formato de sistemas avanzados), códigos de tiempo SMPTE
- índices, acerca de
- índices temporales
- índices basados en marcos
- Códigos de tiempo SMPTE, índices
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d2e5a194f9c495720cbc40ccdb192509723eee0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903750"
---
# <a name="indexes"></a>Índices

Un requisito común para las aplicaciones que leen archivos multimedia digitales es la capacidad de buscar en un punto específico del contenido. La búsqueda puede ser difícil porque no hay ninguna garantía de que los distintos flujos de un archivo tienen muestras con horas de inicio simultáneas. Este problema se soluciona con el uso de *índices*. Un índice es un objeto de un archivo ASF que equipara las muestras de vídeo con los tiempos de presentación. No se requiere ningún índice para las secuencias de audio porque los datos de audio se conectan más estrechamente con el tiempo de presentación que los datos de vídeo.

El objeto indexador del SDK de Windows Media Format puede crear tres tipos diferentes de índices: índices temporales, índices basados en marcos y índices de código de tiempo SMPTE.

Los índices temporales son el tipo más común. Simplemente son equivalentes a los ejemplos de vídeo con los tiempos de presentación correspondientes.

Un índice basado en fotogramas equipara las muestras de vídeo con los números de fotogramas de vídeo y los tiempos de presentación. Los números de fotogramas son especialmente útiles en aplicaciones que editan vídeo.

Un índice de código de tiempo de SMTP es el tipo de índice más raro. Utiliza el código de tiempo SMPTE como base del índice y solo se puede usar en flujos que tienen marcas de tiempo de SMPTE incluidas con sus ejemplos. Para obtener más información sobre el código de tiempo SMPTE, consulte [compatibilidad con código de tiempo SMPTE](smpte-time-code-support.md).

Un archivo ASF puede contener un índice de cada tipo para cada flujo de vídeo que contenga. De forma predeterminada, se incluye un índice temporal para cada secuencia de vídeo en los archivos creados por el objeto de escritura. Puede cambiar la configuración de indexación automática de los archivos para que se adapte a sus necesidades.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Características de archivos ASF**](asf-file-features.md)
</dt> <dt>

[**Trabajar con índices**](working-with-indexes.md)
</dt> <dt>

[**Leer archivos con el lector asincrónico**](reading-files-with-the-asynchronous-reader.md)
</dt> <dt>

[**Leer archivos con el lector sincrónico**](reading-files-with-the-synchronous-reader.md)
</dt> </dl>

 

 




