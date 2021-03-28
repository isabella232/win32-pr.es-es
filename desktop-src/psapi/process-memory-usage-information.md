---
title: Información de uso de memoria de proceso
description: La función GetProcessMemoryInfo toma un identificador de proceso como entrada y rellena una \_ estructura de contadores de memoria de proceso \_ con información sobre las estadísticas de memoria para el proceso.
ms.assetid: 683c899e-a7e8-4440-8f13-2a713c1618bf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 133032b8cfb8a9af4ccea5661c9e0e0181ab4d93
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903705"
---
# <a name="process-memory-usage-information"></a>Información de uso de memoria de proceso

La función [**GetProcessMemoryInfo**](/windows/desktop/api/Psapi/nf-psapi-getprocessmemoryinfo) toma un identificador de proceso como entrada y rellena una estructura de [**\_ \_ contadores de memoria de proceso**](/windows/desktop/api/Psapi/ns-psapi-process_memory_counters) con información sobre las estadísticas de memoria para el proceso. El miembro **CB** recibe el tamaño de la estructura. El miembro **PageFaultCount** recibe el número de errores de página. Los miembros restantes reciben el uso actual y máximo de memoria en las siguientes categorías:

-   Espacio de trabajo
-   Grupo paginado
-   bloque no paginado
-   paginación

El espacio de *trabajo* es la cantidad de memoria asignada físicamente al contexto del proceso en un momento dado. La memoria del *Grupo paginado* es la memoria del sistema que puede transferirse al archivo de paginación en el disco (paginado) cuando no se utiliza. La memoria del *bloque no paginado* es la memoria del sistema que no se puede paginar en el disco, siempre y cuando se asignen los objetos correspondientes. El uso del archivo de *paginación* representa la cantidad de memoria que se reserva para el proceso en el archivo de paginación del sistema. Cuando el uso de memoria es demasiado alto, el administrador de memoria virtual pagina la memoria en el disco. Cuando un subproceso necesita una página que no está en la memoria, el administrador de memoria la vuelve a cargar desde el archivo de paginación.

 

 




