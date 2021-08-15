---
title: Índices
description: Índices
ms.assetid: 54c694f6-3c10-4d7c-bcd1-f2b17d652e8e
keywords:
- Windows SDK de formato multimedia, índices
- Formato de sistemas avanzados (ASF), índices
- ASF (formato de sistemas avanzados), índices
- Windows SDK de formato multimedia, índices temporales
- Formato de sistemas avanzados (ASF), índices temporales
- ASF (formato de sistemas avanzados), índices temporales
- Windows SDK de formato multimedia, índices basados en fotogramas
- Formato de sistemas avanzados (ASF), índices basados en fotogramas
- ASF (formato de sistemas avanzados), índices basados en fotogramas
- Windows SDK de formato multimedia, códigos de tiempo SMPTE
- Formato de sistemas avanzados (ASF), códigos de tiempo SMPTE
- ASF (formato de sistemas avanzados), códigos de tiempo SMPTE
- indexes,about
- índices temporales
- índices basados en fotogramas
- Códigos de tiempo de SMPTE, índices
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71af891ba2986d3ece1eb2d4cc7eb7ff4086c06eee1f60eabb2210bdc8b6bacd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118702489"
---
# <a name="indexes"></a>Índices

Un requisito común para las aplicaciones que leen archivos multimedia digitales es la capacidad de buscar un punto específico en el contenido. La búsqueda puede ser difícil porque no hay ninguna garantía de que las distintas secuencias de un archivo tengan ejemplos con horas de inicio simultáneas. Este problema se aborda con el uso de *índices*. Un índice es un objeto de un archivo ASF que equivale a los ejemplos de vídeo con sus tiempos de presentación. No se requiere ningún índice para las secuencias de audio porque los datos de audio están más estrechamente conectados con el tiempo de presentación que los datos de vídeo.

El objeto indexador del SDK Windows Media Format puede crear tres tipos diferentes de índices: índices temporales, índices basados en fotogramas e índices de código de tiempo SMPTE.

Los índices temporales son el tipo más común. Simplemente equivalen los ejemplos de vídeo con los tiempos de presentación correspondientes.

Un índice basado en fotogramas equivale a ejemplos de vídeo con números de fotogramas de vídeo y tiempos de presentación. Los números de fotogramas son especialmente útiles en las aplicaciones que editan vídeo.

Un índice de código de tiempo SMTPE es el tipo de índice más poco frecuente. Usa el código de tiempo SMPTE como base del índice y solo se puede usar en secuencias que tienen marcas de tiempo de SMPTE incluidas con sus ejemplos. Para obtener más información sobre el código de hora de SMPTE, vea Compatibilidad con código [de tiempo de SMPTE.](smpte-time-code-support.md)

Un archivo ASF puede contener un índice de cada tipo para cada secuencia de vídeo que contiene. De forma predeterminada, se incluye un índice temporal para cada secuencia de vídeo en los archivos creados por el objeto de escritor. Puede cambiar la configuración de indexación automática de los archivos para que se adapte a sus necesidades.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Características del archivo ASF**](asf-file-features.md)
</dt> <dt>

[**Trabajar con índices**](working-with-indexes.md)
</dt> <dt>

[**Lectura de archivos con el lector asincrónico**](reading-files-with-the-asynchronous-reader.md)
</dt> <dt>

[**Lectura de archivos con el lector sincrónico**](reading-files-with-the-synchronous-reader.md)
</dt> </dl>

 

 




