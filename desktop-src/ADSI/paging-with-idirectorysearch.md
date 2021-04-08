---
title: Paginación con IDirectorySearch
description: La paginación especifica el número de filas que devuelve el servidor al cliente.
ms.assetid: cf4aa56a-c6f7-47c8-956d-512a5cffbf22
ms.tgt_platform: multiple
keywords:
- Paginación con ADSI de IDirectorySearch
- ADSI, búsqueda, IDirectorySearch, otras opciones de búsqueda, paginación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6e9fdf001f5908f6c3fc7321c8c94cda09f1b96
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103993848"
---
# <a name="paging-with-idirectorysearch"></a><span data-ttu-id="945b7-105">Paginación con IDirectorySearch</span><span class="sxs-lookup"><span data-stu-id="945b7-105">Paging with IDirectorySearch</span></span>

<span data-ttu-id="945b7-106">La paginación especifica el número de filas que devuelve el servidor al cliente.</span><span class="sxs-lookup"><span data-stu-id="945b7-106">Paging specifies how many rows that the server returns to the client.</span></span> <span data-ttu-id="945b7-107">Una página puede definirse por el número de filas o un límite de tiempo.</span><span class="sxs-lookup"><span data-stu-id="945b7-107">A page can be defined by the number of rows or a time limit.</span></span> <span data-ttu-id="945b7-108">El objeto COM ADSI recupera cada página de resultados basándose en los valores que se muestran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="945b7-108">The ADSI COM object retrieves each page of results based on the values listed in the following table.</span></span> <span data-ttu-id="945b7-109">El llamador llama a [**IDirectorySearch:: GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) cuando ha alcanzado el final de la página y el objeto com ADSI recupera la página siguiente.</span><span class="sxs-lookup"><span data-stu-id="945b7-109">The caller calls [**IDirectorySearch::GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) when it has reached the page end, and the ADSI COM object retrieves the next page.</span></span>



| <span data-ttu-id="945b7-110">Value</span><span class="sxs-lookup"><span data-stu-id="945b7-110">Value</span></span>                                   | <span data-ttu-id="945b7-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="945b7-111">Description</span></span>                                                                                                                                                                                                                                          |
|-----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="945b7-112">**\_paginación de ADS SEARCHPREF \_**</span><span class="sxs-lookup"><span data-stu-id="945b7-112">**ADS\_SEARCHPREF\_PAGESIZE**</span></span>           | <span data-ttu-id="945b7-113">Especifica el número máximo de filas que se van a devolver en una página.</span><span class="sxs-lookup"><span data-stu-id="945b7-113">Specifies the maximum number of rows to return in a page.</span></span>                                                                                                                                                                                            |
| <span data-ttu-id="945b7-114">**\_límite de \_ tiempo paginado de SEARCHPREF ADS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="945b7-114">**ADS\_SEARCHPREF\_PAGED\_TIME\_LIMIT**</span></span> | <span data-ttu-id="945b7-115">Especifica el tiempo máximo, en segundos, que el servidor debe gastar en recopilar una página de resultados antes de devolver la página al cliente.</span><span class="sxs-lookup"><span data-stu-id="945b7-115">Specifies the maximum time, in seconds, that the server should spend collecting a page of results before returning the page to the client.</span></span> <span data-ttu-id="945b7-116">Si se alcanza el límite, el servidor detiene la búsqueda y devuelve las filas ya recuperadas para la página.</span><span class="sxs-lookup"><span data-stu-id="945b7-116">If the limit is reached, the server stops the search and returns the rows already retrieved for the page.</span></span> |



 

<span data-ttu-id="945b7-117">Si no se establece ninguna de estas preferencias de búsqueda, el valor predeterminado es sin paginación.</span><span class="sxs-lookup"><span data-stu-id="945b7-117">If neither of these search preferences is set, the default is no paging.</span></span> <span data-ttu-id="945b7-118">Las búsquedas de Active Directory realizadas sin paginación se limitan a devolver un máximo de los primeros 1000 registros, por lo que debe usar una búsqueda paginada si existe la posibilidad de que el conjunto de resultados contenga más de 1000 elementos.</span><span class="sxs-lookup"><span data-stu-id="945b7-118">Searches of the Active Directory performed without paging are limited to returning a maximum of the first 1000 records, so you must use a paged search if there is the possibility that the result set will contain more than 1000 items.</span></span>

<span data-ttu-id="945b7-119">Una operación de búsqueda puede dar lugar a que se devuelva un gran número de objetos.</span><span class="sxs-lookup"><span data-stu-id="945b7-119">A search operation may result in a large number of objects being returned.</span></span> <span data-ttu-id="945b7-120">Si el servidor devuelve el resultado en un conjunto, podría reducir el rendimiento del cliente y del servidor, así como afectar a la carga de la red.</span><span class="sxs-lookup"><span data-stu-id="945b7-120">If the server returns the result in one set, it could decrease the performance of the client and server, as well as affect the network load.</span></span> <span data-ttu-id="945b7-121">Las búsquedas paginadas se pueden usar para evitar esto.</span><span class="sxs-lookup"><span data-stu-id="945b7-121">Paged searches can be used to prevent this.</span></span> <span data-ttu-id="945b7-122">En una búsqueda paginada, el cliente puede aceptar los paquetes más pequeños.</span><span class="sxs-lookup"><span data-stu-id="945b7-122">In a paged search, the client can accept results in smaller packets.</span></span> <span data-ttu-id="945b7-123">El tamaño de un paquete se conoce como el tamaño de la página de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="945b7-123">The size of a packet is known as the search page size.</span></span>

<span data-ttu-id="945b7-124">Las búsquedas paginadas ofrecen ventajas tanto para el cliente como para el servidor.</span><span class="sxs-lookup"><span data-stu-id="945b7-124">Paged searches offer benefits to both the client and the server.</span></span> <span data-ttu-id="945b7-125">El cliente puede tener mayor capacidad de respuesta en la presentación de los resultados a los usuarios.</span><span class="sxs-lookup"><span data-stu-id="945b7-125">The client can be more responsive in presenting the results to users.</span></span> <span data-ttu-id="945b7-126">Esto es especialmente relevante para las herramientas de interfaz gráfica de usuario que pueden iniciar el proceso de visualización de la ventana mientras el otro subproceso recibe los datos simultáneamente.</span><span class="sxs-lookup"><span data-stu-id="945b7-126">This is especially relevant to graphical user interface tools that can begin the window display process while the other thread concurrently receives the data.</span></span>

<span data-ttu-id="945b7-127">En el lado del servidor, las búsquedas paginadas hacen que la operación sea escalable.</span><span class="sxs-lookup"><span data-stu-id="945b7-127">On the server side, paged searches make the operation scalable.</span></span> <span data-ttu-id="945b7-128">Por ejemplo, si los clientes 100 emiten solicitudes de búsqueda simultáneamente y, en el promedio, cada cliente recibe 200 objetos.</span><span class="sxs-lookup"><span data-stu-id="945b7-128">For example, if one hundred clients issue search requests simultaneously and, on the average, each client receives two hundred objects.</span></span> <span data-ttu-id="945b7-129">Si no se especifica ningún tamaño de página, en el peor de los casos, el servidor debe tener suficiente memoria para contener 20.000 objetos.</span><span class="sxs-lookup"><span data-stu-id="945b7-129">If no page size is specified, in the worst-case scenario, the server must have sufficient memory to hold 20,000 objects.</span></span> <span data-ttu-id="945b7-130">Por el contrario, si cada cliente especifica un tamaño de página, por ejemplo, diez objetos, el requisito de memoria en el servidor se reduce por un factor de 20.</span><span class="sxs-lookup"><span data-stu-id="945b7-130">Conversely, if each client specifies a page size to be, for example, ten objects, the memory requirement on the server is thus reduced by a factor of 20.</span></span>

<span data-ttu-id="945b7-131">Además, mediante una búsqueda paginada, un cliente puede abandonar la operación en curso.</span><span class="sxs-lookup"><span data-stu-id="945b7-131">In addition, using a paged search, a client can abandon the operation in progress.</span></span> <span data-ttu-id="945b7-132">Por el contrario, en una búsqueda no paginada, el cliente recibe un conjunto de resultados en un paquete.</span><span class="sxs-lookup"><span data-stu-id="945b7-132">In contrast, in a non-paged search, the client receives a result set in one packet.</span></span> <span data-ttu-id="945b7-133">Esto puede reducir el rendimiento de la red.</span><span class="sxs-lookup"><span data-stu-id="945b7-133">This can decrease network performance.</span></span>

<span data-ttu-id="945b7-134">ADSI controla el tamaño de página para el cliente.</span><span class="sxs-lookup"><span data-stu-id="945b7-134">ADSI handles the page size for the client.</span></span> <span data-ttu-id="945b7-135">El cliente no tiene que contar el número de objetos en curso.</span><span class="sxs-lookup"><span data-stu-id="945b7-135">The client does not have to count the number of objects in progress.</span></span> <span data-ttu-id="945b7-136">ADSI encapsula la interacción del servidor para el cliente.</span><span class="sxs-lookup"><span data-stu-id="945b7-136">ADSI encapsulates the server interaction for the client.</span></span> <span data-ttu-id="945b7-137">Desde la perspectiva del cliente, la búsqueda devuelve un conjunto de resultados completo.</span><span class="sxs-lookup"><span data-stu-id="945b7-137">From the client perspective, the search returns a complete result set.</span></span>

<span data-ttu-id="945b7-138">Se recomienda usar la paginación.</span><span class="sxs-lookup"><span data-stu-id="945b7-138">It is recommended that paging is used.</span></span>

<span data-ttu-id="945b7-139">Para especificar un tamaño de página máximo, establezca la opción de búsqueda de **\_ \_ SEARCHPREF de anuncios de ADS** con un valor **\_ entero de ADSTYPE** establecido en el número máximo de filas por página de la matriz de [**\_ \_ información SEARCHPREF de ADS**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) pasada al método [**IDirectorySearch:: SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) .</span><span class="sxs-lookup"><span data-stu-id="945b7-139">To specify a maximum page size, set an **ADS\_SEARCHPREF\_PAGESIZE** search option with an **ADSTYPE\_INTEGER** value set to the maximum number of rows per page in the [**ADS\_SEARCHPREF\_INFO**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) array passed to the [**IDirectorySearch::SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) method.</span></span>

<span data-ttu-id="945b7-140">En el ejemplo de código siguiente se muestra cómo establecer el tamaño máximo de página.</span><span class="sxs-lookup"><span data-stu-id="945b7-140">The following code example shows how to set the maximum page size.</span></span>


```C++
ADS_SEARCHPREF_INFO SearchPref;
SearchPref.dwSearchPref = ADS_SEARCHPREF_PAGESIZE;
SearchPref.vValue.dwType = ADSTYPE_INTEGER;
SearchPref.vValue.Integer = 1000;
```



<span data-ttu-id="945b7-141">Para especificar un tiempo de página, establezca una opción de búsqueda de **\_ \_ \_ \_ límite de tiempo paginado de SEARCHPREF** con un valor **\_ entero de ADSTYPE** establecido en el número máximo de segundos que el servidor debe invertir en recuperar una página en la matriz de [**\_ \_ información SEARCHPREF de ADS**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) pasada al método [**IDirectorySearch:: SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) .</span><span class="sxs-lookup"><span data-stu-id="945b7-141">To specify a page time, set an **ADS\_SEARCHPREF\_PAGED\_TIME\_LIMIT** search option with an **ADSTYPE\_INTEGER** value set to the maximum number of seconds that the server should spend retrieving a page in the [**ADS\_SEARCHPREF\_INFO**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) array passed to the [**IDirectorySearch::SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) method.</span></span>

<span data-ttu-id="945b7-142">En el ejemplo de código siguiente se muestra cómo especificar la hora de la página.</span><span class="sxs-lookup"><span data-stu-id="945b7-142">The following code example shows how to specify page time.</span></span>


```C++
ADS_SEARCHPREF_INFO SearchPref;
SearchPref.dwSearchPref = ADS_SEARCHPREF_PAGED_TIME_LIMIT;
SearchPref.vValue.dwType = ADSTYPE_INTEGER;
SearchPref.vValue.Integer = 60;
```



 

 




