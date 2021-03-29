---
title: Almacenar en caché el resultado (cliente)
description: El almacenamiento en caché del lado cliente almacena el conjunto de resultados en la memoria del cliente, lo que proporciona mejoras de rendimiento para el lado cliente.
ms.assetid: 6e61b2f6-dd58-466e-9cef-5bc6301e983f
ms.tgt_platform: multiple
keywords:
- Almacenar en caché el resultado (cliente) ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb965da1da0c791db215dd7eee925a7c9f67ccf8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103993867"
---
# <a name="caching-the-result-client-side"></a><span data-ttu-id="3c8f2-104">Almacenar en caché el resultado (cliente)</span><span class="sxs-lookup"><span data-stu-id="3c8f2-104">Caching the Result (Client Side)</span></span>

<span data-ttu-id="3c8f2-105">El almacenamiento en caché del lado cliente almacena el conjunto de resultados en la memoria del cliente, lo que proporciona mejoras de rendimiento para el lado cliente.</span><span class="sxs-lookup"><span data-stu-id="3c8f2-105">Client-side caching stores the result set in the client memory, providing performance enhancements for the client side.</span></span> <span data-ttu-id="3c8f2-106">Un cliente puede volver a visitar un objeto varias veces sin necesidad de varios recorridos al servidor.</span><span class="sxs-lookup"><span data-stu-id="3c8f2-106">A client can revisit an object repeatedly without multiple trips to the server.</span></span> <span data-ttu-id="3c8f2-107">De forma predeterminada, ADSI almacena en caché el conjunto de resultados de los clientes.</span><span class="sxs-lookup"><span data-stu-id="3c8f2-107">By default, ADSI caches the result set for the clients.</span></span> <span data-ttu-id="3c8f2-108">Esto permite a ADSI proporcionar a los clientes compatibilidad con cursores de tipo SQL.</span><span class="sxs-lookup"><span data-stu-id="3c8f2-108">This enables ADSI to provide clients with SQL-like cursor support.</span></span> <span data-ttu-id="3c8f2-109">Puede recorrer en iteración un conjunto de resultados determinado varias veces.</span><span class="sxs-lookup"><span data-stu-id="3c8f2-109">You may iterate through a given result set several times.</span></span>

<span data-ttu-id="3c8f2-110">ADSI también permite a los clientes desactivar la memoria caché para reducir los requisitos de memoria.</span><span class="sxs-lookup"><span data-stu-id="3c8f2-110">ADSI also enables clients to turn off the cache to reduce memory requirements.</span></span> <span data-ttu-id="3c8f2-111">Si el almacenamiento en caché del lado cliente está deshabilitado, el cliente no mantiene el conjunto de resultados en la memoria.</span><span class="sxs-lookup"><span data-stu-id="3c8f2-111">If client-side caching is disabled, the client does not maintain the result set in memory.</span></span> <span data-ttu-id="3c8f2-112">Cada fila se libera una vez que la aplicación la recupera.</span><span class="sxs-lookup"><span data-stu-id="3c8f2-112">Each row is freed after the application retrieves it.</span></span> <span data-ttu-id="3c8f2-113">Deshabilitar el almacenamiento en caché del lado cliente puede ser útil para reducir los requisitos de memoria del lado cliente en tales casos, como cuando solo se desea realizar un único paso a través del conjunto de resultados.</span><span class="sxs-lookup"><span data-stu-id="3c8f2-113">Disabling client-side caching can be useful for decreasing the client-side memory requirements in such cases as when you intend only to make a single pass through the result set.</span></span> <span data-ttu-id="3c8f2-114">Sin embargo, cuando los clientes optan por no almacenar en caché el resultado, proporcionan compatibilidad con los cursores.</span><span class="sxs-lookup"><span data-stu-id="3c8f2-114">However, when clients elect not to cache the result, they give up cursor support.</span></span>

<span data-ttu-id="3c8f2-115">Para obtener más información sobre el almacenamiento en caché de resultados con una interfaz de búsqueda específica, vea:</span><span class="sxs-lookup"><span data-stu-id="3c8f2-115">For more information about results caching with a specific search interface, see:</span></span>

-   [<span data-ttu-id="3c8f2-116">Almacenamiento en caché de resultados con IDirectorySearch</span><span class="sxs-lookup"><span data-stu-id="3c8f2-116">Result Caching with IDirectorySearch</span></span>](result-caching-with-idirectorysearch.md)
-   [<span data-ttu-id="3c8f2-117">Buscar con Objetos de datos ActiveX</span><span class="sxs-lookup"><span data-stu-id="3c8f2-117">Searching with ActiveX Data Objects</span></span>](searching-with-activex-data-objects-ado.md)
-   [<span data-ttu-id="3c8f2-118">Buscar con OLE DB</span><span class="sxs-lookup"><span data-stu-id="3c8f2-118">Searching with OLE DB</span></span>](searching-with-ole-db.md)

 

 




