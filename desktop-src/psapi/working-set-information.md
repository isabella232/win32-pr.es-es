---
title: Información del conjunto de trabajo
description: El espacio de trabajo de un proceso es la cantidad de memoria asignada físicamente a su contexto de proceso. PSAPI permite tomar instantáneas del conjunto de trabajo o supervisar el conjunto de trabajo.
ms.assetid: 33c42f79-cc77-4d44-84c3-8bf0a4a60019
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b56e1e4dc0a68a9d4507a94ad1f5356432f8488a
ms.sourcegitcommit: b01ad017c152c6756f3638623fe335877644d414
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/06/2021
ms.locfileid: "111549867"
---
# <a name="working-set-information"></a>Información del conjunto de trabajo

El espacio de trabajo de un proceso es la cantidad de memoria asignada físicamente a su contexto de proceso. PSAPI permite tomar instantáneas del conjunto de trabajo o supervisar el conjunto de trabajo.

Las [**funciones QueryWorkingSet**](/windows/desktop/api/Psapi/nf-psapi-queryworkingset) o [**QueryWorkingSetEx**](/windows/desktop/api/Psapi/nf-psapi-queryworkingsetex) rellenan un búfer con una instantánea de la información de cada página del conjunto de trabajo actual del proceso especificado. La función notifica solo las páginas que están físicamente presentes en el momento exacto en que se llama.

Puede usar la supervisión del espacio de trabajo para averiguar cuánta RAM adicional toma una operación determinada (por ejemplo, guardar un archivo). Para empezar a supervisar el conjunto de trabajo, llame a [**la función InitializeProcessForWsWatch.**](/windows/desktop/api/Psapi/nf-psapi-initializeprocessforwswatch) No todos los procesos permiten leer la información del conjunto de trabajo, así que asegúrese de que la función devuelve un valor distinto de cero antes de continuar. A continuación, llame [**a la función GetWsChanges.**](/windows/desktop/api/Psapi/nf-psapi-getwschanges) Esta función notifica solo las páginas que se han cargado en memoria desde que empezó a supervisar el espacio de trabajo. La función devuelve datos en una matriz de estructuras DE INFORMACIÓN de [**\_ PSAPI WS \_ WATCH, \_**](/windows/desktop/api/Psapi/ns-psapi-psapi_ws_watch_information) una estructura para cada nueva página agregada al conjunto de trabajo del proceso. La estructura indica qué páginas están en memoria y qué hizo que el sistema las paginase.

La [**función EmptyWorkingSet**](/windows/desktop/api/Psapi/nf-psapi-emptyworkingset) toma un identificador de proceso. Quita tantas páginas como sea posible del conjunto de trabajo del proceso. Esta operación es útil principalmente para las pruebas y el ajuste. Tenga en cuenta que la función [**SetProcessWorkingSetSize**](/windows/desktop/api/memoryapi/nf-memoryapi-setprocessworkingsetsize) hace lo mismo si se pasa -1 para los tamaños mínimo y máximo.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Espacio de trabajo](/windows/desktop/Memory/working-set)
</dt> </dl>

 

 