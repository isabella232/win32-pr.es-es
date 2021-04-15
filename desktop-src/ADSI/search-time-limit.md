---
title: Límite de tiempo de búsqueda
description: Cuando se solicita una búsqueda en un servidor que está bajo una carga de trabajo pesada, puede que desee indicar al servidor que restrinja la búsqueda a un límite de tiempo especificado.
ms.assetid: 199ac73b-3624-4cd5-a1ee-6db418cd77ba
ms.tgt_platform: multiple
keywords:
- ADSI de límite de tiempo de búsqueda
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e11ff9de38a17fe6ebac4ebb045e2f8b896bc764
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105656151"
---
# <a name="search-time-limit"></a><span data-ttu-id="a0b00-104">Límite de tiempo de búsqueda</span><span class="sxs-lookup"><span data-stu-id="a0b00-104">Search Time Limit</span></span>

<span data-ttu-id="a0b00-105">Cuando se solicita una búsqueda en un servidor que está bajo una carga de trabajo pesada, puede que desee indicar al servidor que restrinja la búsqueda a un límite de tiempo especificado.</span><span class="sxs-lookup"><span data-stu-id="a0b00-105">When you request a search on a server that is under a heavy workload, you may want to instruct the server to restrict the search to a specified time limit.</span></span> <span data-ttu-id="a0b00-106">Por ejemplo, para ejecutar una aplicación con el fin de generar un informe semanal en un servidor que ejecute casi su capacidad, y para evitar maximizar el tiempo de CPU y evitar que se ejecuten otros trabajos, puede establecer el tiempo de búsqueda en un valor pequeño y volver a ejecutar la aplicación más adelante si no puede generar el informe.</span><span class="sxs-lookup"><span data-stu-id="a0b00-106">For example, to execute an application to generate a weekly report on a server that is running near capacity, and to avoid maximizing the CPU time and preventing other jobs from running, you can set the search time to a small value and rerun the application later if it fails to generate the report.</span></span>

<span data-ttu-id="a0b00-107">Algunos servidores pueden imponer su propio límite de tiempo administrativo.</span><span class="sxs-lookup"><span data-stu-id="a0b00-107">Some servers can impose their own administrative time limit.</span></span> <span data-ttu-id="a0b00-108">En estos casos, si especifica un valor de límite de tiempo de búsqueda mayor que el límite de tiempo administrativo, el servidor omite su especificación y usa su límite de tiempo administrativo interno en su lugar.</span><span class="sxs-lookup"><span data-stu-id="a0b00-108">In these cases, if you specify a search time limit value greater than the administrative time limit, the server ignores your specification and use its internal administrative time limit instead.</span></span>

<span data-ttu-id="a0b00-109">Para obtener más información sobre cómo usar la opción de límite de tiempo de búsqueda con una interfaz de búsqueda específica, vea:</span><span class="sxs-lookup"><span data-stu-id="a0b00-109">For more information about using the search time limit option with a specific search interface, see:</span></span>

-   [<span data-ttu-id="a0b00-110">Límite de tiempo del servidor con IDirectorySearch</span><span class="sxs-lookup"><span data-stu-id="a0b00-110">Server Time Limit with IDirectorySearch</span></span>](server-time-limit-with-idirectorysearch.md)
-   [<span data-ttu-id="a0b00-111">Buscar con Objetos de datos ActiveX</span><span class="sxs-lookup"><span data-stu-id="a0b00-111">Searching with ActiveX Data Objects</span></span>](searching-with-activex-data-objects-ado.md)
-   [<span data-ttu-id="a0b00-112">Buscar con OLE DB</span><span class="sxs-lookup"><span data-stu-id="a0b00-112">Searching with OLE DB</span></span>](searching-with-ole-db.md)

 

 




