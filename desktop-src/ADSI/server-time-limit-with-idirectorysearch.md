---
title: Límite de tiempo del servidor con IDirectorySearch
description: Para evitar el uso de todo el tiempo de CPU y evitar que se ejecuten otras operaciones, especifique el límite de tiempo de búsqueda en un valor pequeño y, después, vuelva a ejecutar la aplicación más adelante si no puede generar el informe.
ms.assetid: 0fd4d8a2-36fc-4179-aeee-1cd3f3996e19
ms.tgt_platform: multiple
keywords:
- Límite de tiempo del servidor con ADSI de IDirectorySearch
- ADSI, búsqueda, IDirectorySearch, otras opciones de búsqueda, límite de tiempo del servidor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ba5f80f9b83f20affaf7ad03de6b1609e9951b7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103993840"
---
# <a name="server-time-limit-with-idirectorysearch"></a><span data-ttu-id="44805-105">Límite de tiempo del servidor con IDirectorySearch</span><span class="sxs-lookup"><span data-stu-id="44805-105">Server Time Limit with IDirectorySearch</span></span>

<span data-ttu-id="44805-106">Cuando solicita una búsqueda en un servidor ocupado, es posible que desee solicitar que el servidor restrinja la búsqueda a un límite de tiempo especificado.</span><span class="sxs-lookup"><span data-stu-id="44805-106">When you request a search on a busy server, you may want to request that the server to restrict the search to a specified time limit.</span></span> <span data-ttu-id="44805-107">Por ejemplo, desea ejecutar una aplicación para generar un informe semanal en un servidor que ejecute cerca de su capacidad.</span><span class="sxs-lookup"><span data-stu-id="44805-107">For example, you want to run an application to generate a weekly report on a server that is running near its capacity.</span></span> <span data-ttu-id="44805-108">Para evitar el uso de todo el tiempo de CPU y evitar que se ejecuten otras operaciones, especifique el límite de tiempo de búsqueda en un valor pequeño y, después, vuelva a ejecutar la aplicación más adelante si no puede generar el informe.</span><span class="sxs-lookup"><span data-stu-id="44805-108">To avoid using all the CPU time and preventing other operations from running, specify the search time limit to a small value and then rerun the application later if it fails to generate the report.</span></span>

<span data-ttu-id="44805-109">Algunos servidores pueden imponer su propio límite de tiempo administrativo.</span><span class="sxs-lookup"><span data-stu-id="44805-109">Some servers might impose their own administrative time limit.</span></span> <span data-ttu-id="44805-110">En estos casos, si especifica un valor de límite de tiempo de búsqueda mayor que el límite de tiempo administrativo, el servidor pasará por alto su especificación y usará su valor de límite de tiempo interno en su lugar.</span><span class="sxs-lookup"><span data-stu-id="44805-110">In these cases, if you specify a search time limit value greater than the administrative time limit, the server will ignore your specification and use its internal time limit value instead.</span></span>

<span data-ttu-id="44805-111">El valor predeterminado para el límite de tiempo del servidor no es límite.</span><span class="sxs-lookup"><span data-stu-id="44805-111">The default for the server time limit is no limit.</span></span> <span data-ttu-id="44805-112">Para establecer un límite de tiempo de servidor, establezca una opción de búsqueda de límite de tiempo de SEARCHPREF de ADS con un valor **\_ entero de ADSTYPE** que contenga el límite de tiempo del servidor, en segundos, en la matriz de [**\_ \_ información SEARCHPREF de ADS**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) pasada al método [**IDirectorySearch:: SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) . **\_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="44805-112">To set a server time limit, set an **ADS\_SEARCHPREF\_TIME\_LIMIT** search option with an **ADSTYPE\_INTEGER** value that contains the server time limit, in seconds, in the [**ADS\_SEARCHPREF\_INFO**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) array passed to the [**IDirectorySearch::SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) method.</span></span> <span data-ttu-id="44805-113">Esta operación se muestra en el ejemplo de código siguiente.</span><span class="sxs-lookup"><span data-stu-id="44805-113">This operation is shown in the following code example.</span></span> <span data-ttu-id="44805-114">Un límite de tiempo de servidor de cero indica que no hay ningún límite de tiempo.</span><span class="sxs-lookup"><span data-stu-id="44805-114">A server time limit of zero indicates no time limit.</span></span>


```C++
ADS_SEARCHPREF_INFO SearchPref;
SearchPref.dwSearchPref = ADS_SEARCHPREF_TIME_LIMIT;
SearchPref.vValue.dwType = ADSTYPE_INTEGER;
SearchPref.vValue.Integer = 10;
```



 

 




