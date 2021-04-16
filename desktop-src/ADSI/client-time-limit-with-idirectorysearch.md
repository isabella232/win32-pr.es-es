---
title: Límite de tiempo de cliente con IDirectorySearch
description: Un cliente puede imponer un límite de tiempo para que un servidor devuelva el conjunto de resultados. Cuando el servidor no responde a una consulta dentro del período de tiempo especificado, el cliente puede abandonar la búsqueda y volver a intentarlo más tarde.
ms.assetid: fe8a8b08-b34d-4aa5-a925-bcda6e72d437
ms.tgt_platform: multiple
keywords:
- Límite de tiempo de cliente con IDirectorySearch
- ADSI, búsqueda, IDirectorySearch, otras opciones de búsqueda, límite de tiempo de cliente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed25bd8499f7166d7ea494f71e6f78193f9c778a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105656191"
---
# <a name="client-time-limit-with-idirectorysearch"></a><span data-ttu-id="2c7ef-106">Límite de tiempo de cliente con IDirectorySearch</span><span class="sxs-lookup"><span data-stu-id="2c7ef-106">Client Time Limit with IDirectorySearch</span></span>

<span data-ttu-id="2c7ef-107">Un cliente puede imponer un límite de tiempo para que un servidor devuelva el conjunto de resultados.</span><span class="sxs-lookup"><span data-stu-id="2c7ef-107">A client can impose a time limit for a server to return the result set.</span></span> <span data-ttu-id="2c7ef-108">Cuando el servidor no responde a una consulta dentro del período de tiempo especificado, el cliente puede abandonar la búsqueda y volver a intentarlo más tarde.</span><span class="sxs-lookup"><span data-stu-id="2c7ef-108">When the server fails to respond to a query within the specified time period, the client can abandon the search and try it again later.</span></span>

<span data-ttu-id="2c7ef-109">La preferencia de límite de tiempo de cliente es útil cuando un cliente solicita una búsqueda asincrónica.</span><span class="sxs-lookup"><span data-stu-id="2c7ef-109">The client time limit preference is useful when a client requests an asynchronous search.</span></span> <span data-ttu-id="2c7ef-110">En una búsqueda asincrónica, el cliente realiza una solicitud y, a continuación, continúa con otras tareas mientras espera a que el servidor devuelva los resultados.</span><span class="sxs-lookup"><span data-stu-id="2c7ef-110">In an asynchronous search, the client makes a request and then proceeds with other tasks while waiting for the server to return the results.</span></span> <span data-ttu-id="2c7ef-111">Es posible que el servidor se quede sin conexión sin notificar al cliente.</span><span class="sxs-lookup"><span data-stu-id="2c7ef-111">It is possible that the server can go offline without notifying the client.</span></span> <span data-ttu-id="2c7ef-112">En este caso, el cliente no recibirá ninguna notificación de si el servidor sigue procesando la consulta o si ya no lo está.</span><span class="sxs-lookup"><span data-stu-id="2c7ef-112">In this case, the client will have no notification of whether the server is still processing the query, or if it no longer live.</span></span> <span data-ttu-id="2c7ef-113">La preferencia de límite de tiempo de cliente proporciona al cliente cierto control de situaciones como esta.</span><span class="sxs-lookup"><span data-stu-id="2c7ef-113">The client time limit preference gives the client some control of situations like this.</span></span>

<span data-ttu-id="2c7ef-114">El valor predeterminado para el límite de tiempo de cliente es sin límite.</span><span class="sxs-lookup"><span data-stu-id="2c7ef-114">The default for the client time limit is no limit.</span></span> <span data-ttu-id="2c7ef-115">Para establecer un límite de tiempo de cliente, establezca una opción de búsqueda de SEARCHPREF de tiempo de **\_ \_ espera de ADS** con un valor **\_ entero de ADSTYPE** que contenga el límite de tiempo de cliente, en segundos, en la matriz de [**\_ \_ información SEARCHPREF de ADS**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) pasada al método [**IDirectorySearch:: SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) .</span><span class="sxs-lookup"><span data-stu-id="2c7ef-115">To set a client time limit, set an **ADS\_SEARCHPREF\_TIMEOUT** search option with an **ADSTYPE\_INTEGER** value that contains the client time limit, in seconds, in the [**ADS\_SEARCHPREF\_INFO**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) array passed to the [**IDirectorySearch::SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) method.</span></span> <span data-ttu-id="2c7ef-116">Un límite de tiempo de cliente de cero indica que no hay ningún límite de tiempo.</span><span class="sxs-lookup"><span data-stu-id="2c7ef-116">A client time limit of zero indicates no time limit.</span></span>

<span data-ttu-id="2c7ef-117">En el ejemplo de código siguiente se muestra cómo establecer el límite de tiempo del cliente.</span><span class="sxs-lookup"><span data-stu-id="2c7ef-117">The following code example shows how to set the client time limit.</span></span>


```C++
ADS_SEARCHPREF_INFO SearchPref;
SearchPref.dwSearchPref = ADS_SEARCHPREF_TIMEOUT;
SearchPref.vValue.dwType = ADSTYPE_INTEGER;
SearchPref.vValue.Integer = 10;
```



 

 




