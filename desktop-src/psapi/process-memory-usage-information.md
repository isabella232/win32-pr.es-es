---
title: Procesar información de uso de memoria
description: La función GetProcessMemoryInfo toma un identificador de proceso como entrada y rellena una estructura PROCESS MEMORY COUNTERS con información sobre las estadísticas de \_ \_ memoria del proceso.
ms.assetid: 683c899e-a7e8-4440-8f13-2a713c1618bf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac85a62853cf95dcf42380c76b914f23045152b32499870182a47ee2449e8ed1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119094707"
---
# <a name="process-memory-usage-information"></a>Procesar información de uso de memoria

La [**función GetProcessMemoryInfo**](/windows/desktop/api/Psapi/nf-psapi-getprocessmemoryinfo) toma un identificador de proceso como entrada y rellena una estructura [**PROCESS MEMORY \_ \_ COUNTERS**](/windows/desktop/api/Psapi/ns-psapi-process_memory_counters) con información sobre las estadísticas de memoria del proceso. El **miembro cb** recibe el tamaño de la estructura . El **miembro PageFaultCount** recibe el número de errores de página. Los miembros restantes reciben el uso de memoria actual y máximo en las siguientes categorías:

-   Espacio de trabajo
-   grupo paginado
-   grupo no páginas
-   Paginación

El *espacio de trabajo* es la cantidad de memoria asignada físicamente al contexto del proceso en un momento dado. La memoria del *grupo paginado* es la memoria del sistema que se puede transferir al archivo de paginación en disco (paginado) cuando no se está utilizando. La memoria del *grupo no paginado* es la memoria del sistema que no se puede paginar en el disco siempre y cuando se asignen los objetos correspondientes. El *uso del archivo* de paginación representa la cantidad de memoria que se reserva para el proceso en el archivo de paginación del sistema. Cuando el uso de memoria es demasiado alto, el administrador de memoria virtual pagina la memoria seleccionada en el disco. Cuando un subproceso necesita una página que no está en memoria, el administrador de memoria lo vuelve a cargar desde el archivo de paginación.

 

 




