---
title: Búsquedas asincrónicas
description: La habilitación de los resultados de búsqueda asincrónicos (asincrónicos) en una llamada a GetFirstRow o la primera llamada a GetNextRow se bloquea hasta que la primera entrada se devuelve desde el servidor.
ms.assetid: f80e2c62-71c5-4a05-bd17-465962be3c2d
ms.tgt_platform: multiple
keywords:
- ADSI búsquedas asincrónicas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfe8b8fff875af18b85cdffa4ce67d631d94ed14
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103993872"
---
# <a name="asynchronous-searches"></a><span data-ttu-id="23229-104">Búsquedas asincrónicas</span><span class="sxs-lookup"><span data-stu-id="23229-104">Asynchronous Searches</span></span>

<span data-ttu-id="23229-105">La habilitación de los resultados de búsqueda asincrónicos (asincrónicos) en una llamada a **GetFirstRow** o la primera llamada a **GetNextRow** se bloquea hasta que la primera entrada se devuelve desde el servidor.</span><span class="sxs-lookup"><span data-stu-id="23229-105">Enabling asynchronous (async) search results in a call to **GetFirstRow** or the first call to **GetNextRow** blocks until the first entry is returned from the server.</span></span> <span data-ttu-id="23229-106">Es decir, si la búsqueda en el servidor requiere mucho tiempo, los primeros resultados se devuelven rápidamente.</span><span class="sxs-lookup"><span data-stu-id="23229-106">That is, if the search on the server requires much time, the first few results are returned quickly.</span></span> <span data-ttu-id="23229-107">Esto puede ayudar al rellenar un cuadro de lista con los resultados de la búsqueda.</span><span class="sxs-lookup"><span data-stu-id="23229-107">This can help when populating a list box with search results.</span></span> <span data-ttu-id="23229-108">Los resultados de la búsqueda se muestran a medida que se devuelven.</span><span class="sxs-lookup"><span data-stu-id="23229-108">Search results are displayed as they are returned.</span></span>

<span data-ttu-id="23229-109">Si Async está deshabilitado, la primera llamada a **GetFirstRow** o **GetNextRow** se bloqueará hasta que el servidor calcule todo el conjunto de resultados y devuelva.</span><span class="sxs-lookup"><span data-stu-id="23229-109">If async is disabled, the first call to **GetFirstRow** or **GetNextRow** will block until the server computes the entire result set and returns.</span></span> <span data-ttu-id="23229-110">Solo entonces es la primera fila devuelta.</span><span class="sxs-lookup"><span data-stu-id="23229-110">Only then is the first row returned.</span></span> <span data-ttu-id="23229-111">Esto no se recomienda si se espera que el conjunto de resultados sea grande.</span><span class="sxs-lookup"><span data-stu-id="23229-111">This is not recommended if the result set is expected to be large.</span></span>

<span data-ttu-id="23229-112">Si tanto la paginación como la asincrónica están habilitadas, la primera llamada a **GetFirstRow** o **GetNextRow** se bloqueará hasta que el servidor genere y envíe la primera página de resultados.</span><span class="sxs-lookup"><span data-stu-id="23229-112">If both paging and async are enabled, the first call to **GetFirstRow** or **GetNextRow** will block until the server generates and sends the first page of results.</span></span> <span data-ttu-id="23229-113">Si se ha establecido un tamaño de Página razonable, los resultados aparecerán inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="23229-113">If a reasonable page size was set, results will appear immediately.</span></span> <span data-ttu-id="23229-114">Lo que es más importante, si se espera que los resultados de la búsqueda sean muy grandes y busca una entrada determinada, no es necesario que solicite más resultados del servidor una vez que haya encontrado las entradas que le interesen.</span><span class="sxs-lookup"><span data-stu-id="23229-114">More importantly, if the search results are expected to be very large, and you search for a particular entry, it is not required that you request more results from the server after you have found the entries that interest you.</span></span>

<span data-ttu-id="23229-115">Una búsqueda asincrónica paginada proporciona un control exhaustivo de una búsqueda.</span><span class="sxs-lookup"><span data-stu-id="23229-115">A paged async search provides fine control of a search.</span></span> <span data-ttu-id="23229-116">Esto resulta útil si los resultados de la búsqueda pueden ser muy grandes y requieren mucho tiempo desde el servidor.</span><span class="sxs-lookup"><span data-stu-id="23229-116">This is useful if the search results may be very large and require extensive time from the server.</span></span>

<span data-ttu-id="23229-117">Para obtener más información sobre el uso de búsquedas asincrónicas con una interfaz de búsqueda específica, vea:</span><span class="sxs-lookup"><span data-stu-id="23229-117">For more information about using asynchronous searches with a specific search interface, see:</span></span>

-   [<span data-ttu-id="23229-118">Búsquedas sincrónicas y asincrónicas con IDirectorySearch</span><span class="sxs-lookup"><span data-stu-id="23229-118">Synchronous and Asynchronous Searches with IDirectorySearch</span></span>](synchronous-and-asynchronous-searches-with-idirectorysearch.md)
-   [<span data-ttu-id="23229-119">Buscar con Objetos de datos ActiveX</span><span class="sxs-lookup"><span data-stu-id="23229-119">Searching with ActiveX Data Objects</span></span>](searching-with-activex-data-objects-ado.md)
-   [<span data-ttu-id="23229-120">Buscar con OLE DB</span><span class="sxs-lookup"><span data-stu-id="23229-120">Searching with OLE DB</span></span>](searching-with-ole-db.md)

 

 




