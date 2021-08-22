---
title: Información del conjunto de trabajo
description: El espacio de trabajo de un proceso es la cantidad de memoria asignada físicamente a su contexto de proceso. PSAPI permite tomar instantáneas del conjunto de trabajo o supervisar el conjunto de trabajo.
ms.assetid: 33c42f79-cc77-4d44-84c3-8bf0a4a60019
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b6003886d50cb47b128bfce92cba4c28950ee078dbe13499d8909676d938aad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119032983"
---
# <a name="working-set-information"></a>Información del conjunto de trabajo

El espacio de trabajo de un proceso es la cantidad de memoria asignada físicamente a su contexto de proceso. PSAPI permite tomar instantáneas del conjunto de trabajo o supervisar el conjunto de trabajo.

La [**función QueryWorkingSet**](/windows/desktop/api/Psapi/nf-psapi-queryworkingset) o [**QueryWorkingSetEx**](/windows/desktop/api/Psapi/nf-psapi-queryworkingsetex) rellena un búfer con una instantánea de la información de cada página del espacio de trabajo actual del proceso especificado. La función notifica solo las páginas que están físicamente presentes en el momento exacto en que se llama.

Puede usar la supervisión del espacio de trabajo para averiguar cuánta RAM adicional toma una operación determinada (por ejemplo, guardar un archivo). Para empezar a supervisar el conjunto de trabajo, llame a [**la función InitializeProcessForWsWatch.**](/windows/desktop/api/Psapi/nf-psapi-initializeprocessforwswatch) No todos los procesos permiten leer la información del conjunto de trabajo, por lo que debe asegurarse de que la función devuelve un valor distinto de cero antes de continuar. A continuación, llame [**a la función GetWsChanges.**](/windows/desktop/api/Psapi/nf-psapi-getwschanges) Esta función notifica solo las páginas que se han cargado en memoria desde que comenzó a supervisar el espacio de trabajo. La función devuelve datos en una matriz de estructuras DE INFORMACIÓN de [**\_ WS \_ WATCH \_ de PSAPI,**](/windows/desktop/api/Psapi/ns-psapi-psapi_ws_watch_information) una estructura para cada nueva página agregada al conjunto de trabajo del proceso. La estructura indica qué páginas están en memoria y qué hizo que el sistema las paginase.

La [**función EmptyWorkingSet**](/windows/desktop/api/Psapi/nf-psapi-emptyworkingset) toma un identificador de proceso. Quita tantas páginas como sea posible del conjunto de trabajo del proceso. Esta operación es útil principalmente para las pruebas y el ajuste. Tenga en cuenta que la función [**SetProcessWorkingSetSize**](/windows/desktop/api/memoryapi/nf-memoryapi-setprocessworkingsetsize) hace lo mismo si se pasa -1 para los tamaños mínimo y máximo.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Espacio de trabajo](/windows/desktop/Memory/working-set)
</dt> </dl>

 

 