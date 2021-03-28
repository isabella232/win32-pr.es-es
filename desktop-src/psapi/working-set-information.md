---
title: Información del espacio de trabajo
description: El espacio de trabajo de un proceso es la cantidad de memoria asignada físicamente a su contexto de proceso. PSAPI permite tomar instantáneas del espacio de trabajo o supervisar el espacio de trabajo.
ms.assetid: 33c42f79-cc77-4d44-84c3-8bf0a4a60019
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea3942796ec1150dee411d6074b13f9ee2be4a22
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104149533"
---
# <a name="working-set-information"></a>Información del espacio de trabajo

El espacio de trabajo de un proceso es la cantidad de memoria asignada físicamente a su contexto de proceso. PSAPI permite tomar instantáneas del espacio de trabajo o supervisar el espacio de trabajo.

La función [**QueryWorkingSet**](/windows/desktop/api/Psapi/nf-psapi-queryworkingset) o [**QueryWorkingSetEx**](/windows/desktop/api/Psapi/nf-psapi-queryworkingsetex) llena un búfer con una instantánea de la información de cada página del espacio de trabajo actual del proceso especificado. La función solo informa de las páginas que están físicamente presentes en el momento exacto en el que se llama.

Puede usar la supervisión del conjunto de trabajo para averiguar la cantidad de RAM adicional que toma una operación concreta (por ejemplo, guardar un archivo). Para empezar a supervisar el espacio de trabajo, llame a la función [**InitializeProcessForWsWatch**](/windows/desktop/api/Psapi/nf-psapi-initializeprocessforwswatch) . No todos los procesos permiten leer su información de espacio de trabajo, por lo que debe asegurarse de que la función devuelve un valor distinto de cero antes de continuar. A continuación, llame a la función [**GetWsChanges**](/windows/desktop/api/Psapi/nf-psapi-getwschanges) . Esta función solo informa de las páginas que se han cargado en la memoria desde que comenzó a supervisar el espacio de trabajo. La función devuelve los datos en una matriz de estructuras de [**\_ \_ \_ información de psapi WS WS**](/windows/desktop/api/Psapi/ns-psapi-psapi_ws_watch_information) , una estructura para cada nueva página agregada al espacio de trabajo del proceso. La estructura indica qué páginas están en la memoria y lo que hizo que el sistema las paginara.

La función [**EmptyWorkingSet**](/windows/desktop/api/Psapi/nf-psapi-emptyworkingset) toma un identificador de proceso. Quita tantas páginas como sea posible del espacio de trabajo del proceso. Esta operación es útil principalmente para pruebas y ajustes. Tenga en cuenta que la función [**SetProcessWorkingSetSize**](/windows/desktop/api/winbase/nf-winbase-setprocessworkingsetsize) hace lo mismo si se pasa-1 para los tamaños mínimo y máximo.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Espacio de trabajo](/windows/desktop/Memory/working-set)
</dt> </dl>

 

 