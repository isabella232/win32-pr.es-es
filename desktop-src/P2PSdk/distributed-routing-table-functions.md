---
description: La API de la tabla de enrutamiento distribuida (DRT) emplea las siguientes funciones.
ms.assetid: 1ceff217-d410-47fa-99a2-8588f001859e
title: Funciones de tabla de enrutamiento distribuido
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5cd48c3a60f458285ce5f607f9ab6bcf7a557cd9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667445"
---
# <a name="distributed-routing-table-functions"></a><span data-ttu-id="91926-103">Funciones de tabla de enrutamiento distribuido</span><span class="sxs-lookup"><span data-stu-id="91926-103">Distributed Routing Table Functions</span></span>

<span data-ttu-id="91926-104">La API de la tabla de enrutamiento distribuida (DRT) emplea las siguientes funciones.</span><span class="sxs-lookup"><span data-stu-id="91926-104">The Distributed Routing Table (DRT) API utilizes the following functions.</span></span>

## <a name="lifetime-management-functions"></a><span data-ttu-id="91926-105">Funciones de administración de la duración</span><span class="sxs-lookup"><span data-stu-id="91926-105">Lifetime Management Functions</span></span>



| <span data-ttu-id="91926-106">Función</span><span class="sxs-lookup"><span data-stu-id="91926-106">Function</span></span>                                           | <span data-ttu-id="91926-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="91926-107">Description</span></span>                                                                                                    |
|----------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="91926-108">**DrtOpen**</span><span class="sxs-lookup"><span data-stu-id="91926-108">**DrtOpen**</span></span>](/windows/desktop/api/drt/nf-drt-drtopen)                         | <span data-ttu-id="91926-109">Crea una instancia de DRT local mediante los criterios especificados por la estructura de [**\_ configuración de DRT**](/windows/desktop/api/drt/ns-drt-drt_settings) .</span><span class="sxs-lookup"><span data-stu-id="91926-109">Creates a local DRT instance using criteria specified by the [**DRT\_SETTINGS**](/windows/desktop/api/drt/ns-drt-drt_settings) structure.</span></span>  |
| [<span data-ttu-id="91926-110">**DrtClose**</span><span class="sxs-lookup"><span data-stu-id="91926-110">**DrtClose**</span></span>](/windows/desktop/api/drt/nf-drt-drtclose)                       | <span data-ttu-id="91926-111">Cierra y quita la instancia local de DRT.</span><span class="sxs-lookup"><span data-stu-id="91926-111">Closes and removes the local instance of the DRT.</span></span>                                                              |
| [<span data-ttu-id="91926-112">**DrtGetEventData**</span><span class="sxs-lookup"><span data-stu-id="91926-112">**DrtGetEventData**</span></span>](/windows/desktop/api/drt/nf-drt-drtgeteventdata)         | <span data-ttu-id="91926-113">Recupera los datos de evento asociados a un evento señalado.</span><span class="sxs-lookup"><span data-stu-id="91926-113">Retrieves event data associated with a signaled event.</span></span>                                                         |
| [<span data-ttu-id="91926-114">**DrtGetEventDataSize**</span><span class="sxs-lookup"><span data-stu-id="91926-114">**DrtGetEventDataSize**</span></span>](/windows/desktop/api/drt/nf-drt-drtgeteventdatasize) | <span data-ttu-id="91926-115">Devuelve el tamaño de la estructura de [**\_ \_ datos de eventos de DRT**](/windows/desktop/api/drt/ns-drt-drt_event_data) asociada a un evento señalado.</span><span class="sxs-lookup"><span data-stu-id="91926-115">Returns the size of the [**DRT\_EVENT\_DATA**](/windows/desktop/api/drt/ns-drt-drt_event_data) structure associated with a signaled event.</span></span> |



 

## <a name="module-management-functions"></a><span data-ttu-id="91926-116">Funciones de administración de módulos</span><span class="sxs-lookup"><span data-stu-id="91926-116">Module Management Functions</span></span>



| <span data-ttu-id="91926-117">Función</span><span class="sxs-lookup"><span data-stu-id="91926-117">Function</span></span>                                                                           | <span data-ttu-id="91926-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="91926-118">Description</span></span>                                                                                                                           |
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="91926-119">**DrtCreatePnrpBootstrapResolver**</span><span class="sxs-lookup"><span data-stu-id="91926-119">**DrtCreatePnrpBootstrapResolver**</span></span>](/windows/desktop/api/drt/nf-drt-drtcreatepnrpbootstrapresolver)           | <span data-ttu-id="91926-120">Crea una resolución de bootstrap basada en el protocolo PNRP.</span><span class="sxs-lookup"><span data-stu-id="91926-120">Creates a bootstrap resolver based on the PNRP protocol.</span></span>                                                                              |
| [<span data-ttu-id="91926-121">**DrtDeletePnrpBootstrapResolver**</span><span class="sxs-lookup"><span data-stu-id="91926-121">**DrtDeletePnrpBootstrapResolver**</span></span>](/windows/desktop/api/drt/nf-drt-drtdeletepnrpbootstrapresolver)           | <span data-ttu-id="91926-122">Elimina una resolución de bootstrap basada en el protocolo PNRP.</span><span class="sxs-lookup"><span data-stu-id="91926-122">Deletes a bootstrap resolver based on the PNRP protocol.</span></span>                                                                              |
| [<span data-ttu-id="91926-123">**DrtCreateDnsBootstrapResolver**</span><span class="sxs-lookup"><span data-stu-id="91926-123">**DrtCreateDnsBootstrapResolver**</span></span>](/windows/desktop/api/drt/nf-drt-drtcreatednsbootstrapresolver)             | <span data-ttu-id="91926-124">Crea un proveedor de arranque que se pondrá en contacto con un host conocido por nombre.</span><span class="sxs-lookup"><span data-stu-id="91926-124">Creates a bootstrap provider that will contact a well known host by name.</span></span>                                                             |
| [<span data-ttu-id="91926-125">**DrtDeleteDnsBootstrapResolver**</span><span class="sxs-lookup"><span data-stu-id="91926-125">**DrtDeleteDnsBootstrapResolver**</span></span>](/windows/desktop/api/drt/nf-drt-drtdeletednsbootstrapresolver)             | <span data-ttu-id="91926-126">Elimina un proveedor de arranque que se pondrá en contacto con un host conocido por nombre.</span><span class="sxs-lookup"><span data-stu-id="91926-126">Deletes a bootstrap provider that will contact a well known host by name.</span></span>                                                             |
| [<span data-ttu-id="91926-127">**DrtCreateIpv6UdpTransport**</span><span class="sxs-lookup"><span data-stu-id="91926-127">**DrtCreateIpv6UdpTransport**</span></span>](/windows/desktop/api/drt/nf-drt-drtcreateipv6udptransport)                     | <span data-ttu-id="91926-128">Crea un transporte basado en el protocolo UDP de IPv6.</span><span class="sxs-lookup"><span data-stu-id="91926-128">Creates a transport based on the IPv6 UDP protocol.</span></span>                                                                                   |
| [<span data-ttu-id="91926-129">**DrtDeleteIpv6UdpTransport**</span><span class="sxs-lookup"><span data-stu-id="91926-129">**DrtDeleteIpv6UdpTransport**</span></span>](/windows/desktop/api/drt/nf-drt-drtdeleteipv6udptransport)                     | <span data-ttu-id="91926-130">Elimina un transporte basado en el protocolo UDP de IPv6.</span><span class="sxs-lookup"><span data-stu-id="91926-130">Deletes a transport based on the IPv6 UDP protocol.</span></span>                                                                                   |
| [<span data-ttu-id="91926-131">**DrtCreateDerivedKeySecurityProvider**</span><span class="sxs-lookup"><span data-stu-id="91926-131">**DrtCreateDerivedKeySecurityProvider**</span></span>](/windows/desktop/api/drt/nf-drt-drtcreatederivedkeysecurityprovider) | <span data-ttu-id="91926-132">Crea un proveedor de seguridad de clave derivada para DRT.</span><span class="sxs-lookup"><span data-stu-id="91926-132">Creates a derived key security provider for the DRT.</span></span>                                                                                  |
| [<span data-ttu-id="91926-133">**DrtCreateDerivedKey**</span><span class="sxs-lookup"><span data-stu-id="91926-133">**DrtCreateDerivedKey**</span></span>](/windows/desktop/api/drt/nf-drt-drtcreatederivedkey)                                 | <span data-ttu-id="91926-134">Crea una clave que puede ser utilizada por [**DrtRegisterKey**](/windows/desktop/api/drt/nf-drt-drtregisterkey) cuando DRT usa un proveedor de seguridad de clave derivado.</span><span class="sxs-lookup"><span data-stu-id="91926-134">Creates a key that can be utilized by [**DrtRegisterKey**](/windows/desktop/api/drt/nf-drt-drtregisterkey) when the DRT is using a derived key security provider.</span></span> |
| [<span data-ttu-id="91926-135">**DrtDeleteDerivedKeySecurityProvider**</span><span class="sxs-lookup"><span data-stu-id="91926-135">**DrtDeleteDerivedKeySecurityProvider**</span></span>](/windows/desktop/api/drt/nf-drt-drtdeletederivedkeysecurityprovider) | <span data-ttu-id="91926-136">Elimina un proveedor de seguridad de clave derivada para DRT.</span><span class="sxs-lookup"><span data-stu-id="91926-136">Deletes a derived key security provider for the DRT.</span></span>                                                                                  |
| [<span data-ttu-id="91926-137">**DrtCreateNullSecurityProvider**</span><span class="sxs-lookup"><span data-stu-id="91926-137">**DrtCreateNullSecurityProvider**</span></span>](/windows/desktop/api/drt/nf-drt-drtcreatenullsecurityprovider)             | <span data-ttu-id="91926-138">Crea un proveedor de seguridad null.</span><span class="sxs-lookup"><span data-stu-id="91926-138">Creates a null security provider.</span></span> <span data-ttu-id="91926-139">Este proveedor de seguridad no requiere que los nodos autentiquen las claves.</span><span class="sxs-lookup"><span data-stu-id="91926-139">This security provider does not require nodes to authenticate keys.</span></span>                                 |
| [<span data-ttu-id="91926-140">**DrtDeleteNullSecurityProvider**</span><span class="sxs-lookup"><span data-stu-id="91926-140">**DrtDeleteNullSecurityProvider**</span></span>](/windows/desktop/api/drt/nf-drt-drtdeletenullsecurityprovider)             | <span data-ttu-id="91926-141">Elimina un proveedor de seguridad null.</span><span class="sxs-lookup"><span data-stu-id="91926-141">Deletes a null security provider.</span></span>                                                                                                     |



 

## <a name="registration-functions"></a><span data-ttu-id="91926-142">Funciones de registro</span><span class="sxs-lookup"><span data-stu-id="91926-142">Registration Functions</span></span>



| <span data-ttu-id="91926-143">Función</span><span class="sxs-lookup"><span data-stu-id="91926-143">Function</span></span>                                     | <span data-ttu-id="91926-144">Descripción</span><span class="sxs-lookup"><span data-stu-id="91926-144">Description</span></span>                                                    |
|----------------------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="91926-145">**DrtRegisterKey**</span><span class="sxs-lookup"><span data-stu-id="91926-145">**DrtRegisterKey**</span></span>](/windows/desktop/api/drt/nf-drt-drtregisterkey)     | <span data-ttu-id="91926-146">Registra una clave en la DRT.</span><span class="sxs-lookup"><span data-stu-id="91926-146">Registers a key in the DRT.</span></span>                                    |
| [<span data-ttu-id="91926-147">**DrtUpdateKey**</span><span class="sxs-lookup"><span data-stu-id="91926-147">**DrtUpdateKey**</span></span>](/windows/desktop/api/drt/nf-drt-drtupdatekey)         | <span data-ttu-id="91926-148">Actualiza los datos de aplicación asociados a una clave registrada.</span><span class="sxs-lookup"><span data-stu-id="91926-148">Updates the application data associated with a registered key.</span></span> |
| [<span data-ttu-id="91926-149">**DrtUnregisterKey**</span><span class="sxs-lookup"><span data-stu-id="91926-149">**DrtUnregisterKey**</span></span>](/windows/desktop/api/drt/nf-drt-drtunregisterkey) | <span data-ttu-id="91926-150">Anula el registro de una clave de DRT.</span><span class="sxs-lookup"><span data-stu-id="91926-150">Deregisters a key from the DRT.</span></span>                                |



 

## <a name="search-functions"></a><span data-ttu-id="91926-151">Funciones de búsqueda</span><span class="sxs-lookup"><span data-stu-id="91926-151">Search Functions</span></span>



| <span data-ttu-id="91926-152">Función</span><span class="sxs-lookup"><span data-stu-id="91926-152">Function</span></span>                                                 | <span data-ttu-id="91926-153">Descripción</span><span class="sxs-lookup"><span data-stu-id="91926-153">Description</span></span>                                                                                                                                                                                                             |
|----------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="91926-154">**DrtStartSearch**</span><span class="sxs-lookup"><span data-stu-id="91926-154">**DrtStartSearch**</span></span>](/windows/desktop/api/drt/nf-drt-drtstartsearch)                 | <span data-ttu-id="91926-155">Busca una clave en el DRT mediante los criterios especificados en la estructura de [**\_ \_ información de búsqueda de DRT**](/windows/desktop/api/drt/ns-drt-drt_search_info) .</span><span class="sxs-lookup"><span data-stu-id="91926-155">Searches the DRT for a key using criteria specified in the [**DRT\_SEARCH\_INFO**](/windows/desktop/api/drt/ns-drt-drt_search_info) structure.</span></span>                                                                                                      |
| [<span data-ttu-id="91926-156">**DrtContinueSearch**</span><span class="sxs-lookup"><span data-stu-id="91926-156">**DrtContinueSearch**</span></span>](/windows/desktop/api/drt/nf-drt-drtcontinuesearch)           | <span data-ttu-id="91926-157">Continúa una \_ \_ \_ búsqueda de la ruta de acceso de retorno de búsqueda de DRT para una clave en la DRT.</span><span class="sxs-lookup"><span data-stu-id="91926-157">Continues a DRT\_SEARCH\_RETURN\_PATH search for a key in the DRT.</span></span> <span data-ttu-id="91926-158">Esta función solo se usa cuando la marca **fIterative** está establecida en **true** en la estructura [**de \_ \_ información de búsqueda de DRT**](/windows/desktop/api/drt/ns-drt-drt_search_info) asociada.</span><span class="sxs-lookup"><span data-stu-id="91926-158">This function is used only when the **fIterative** flag is set to **TRUE** in the associated [**DRT\_SEARCH\_INFO**](/windows/desktop/api/drt/ns-drt-drt_search_info) structure.</span></span> |
| [<span data-ttu-id="91926-159">**DrtGetSearchResult**</span><span class="sxs-lookup"><span data-stu-id="91926-159">**DrtGetSearchResult**</span></span>](/windows/desktop/api/drt/nf-drt-drtgetsearchresult)         | <span data-ttu-id="91926-160">Recupera los resultados de la búsqueda.</span><span class="sxs-lookup"><span data-stu-id="91926-160">Retrieves the search result(s).</span></span>                                                                                                                                                                                         |
| [<span data-ttu-id="91926-161">**DrtGetSearchResultSize**</span><span class="sxs-lookup"><span data-stu-id="91926-161">**DrtGetSearchResultSize**</span></span>](/windows/desktop/api/drt/nf-drt-drtgetsearchresultsize) | <span data-ttu-id="91926-162">Devuelve el tamaño del siguiente resultado de búsqueda disponible.</span><span class="sxs-lookup"><span data-stu-id="91926-162">Returns the size of the next available search result.</span></span>                                                                                                                                                                   |
| [<span data-ttu-id="91926-163">**DrtGetSearchPath**</span><span class="sxs-lookup"><span data-stu-id="91926-163">**DrtGetSearchPath**</span></span>](/windows/desktop/api/drt/nf-drt-drtgetsearchpath)             | <span data-ttu-id="91926-164">Devuelve una lista de nodos contactados durante la operación de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="91926-164">Returns a list of nodes contacted during the search operation.</span></span>                                                                                                                                                          |
| [<span data-ttu-id="91926-165">**DrtGetSearchPathSize**</span><span class="sxs-lookup"><span data-stu-id="91926-165">**DrtGetSearchPathSize**</span></span>](/windows/desktop/api/drt/nf-drt-drtgetsearchpathsize)     | <span data-ttu-id="91926-166">Devuelve el tamaño de la ruta de acceso de búsqueda, que representa el número de nodos que se usan en la operación de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="91926-166">Returns the size of the search path, which represents the number of nodes utilized in the search operation.</span></span>                                                                                                             |
| [<span data-ttu-id="91926-167">**DrtEndSearch**</span><span class="sxs-lookup"><span data-stu-id="91926-167">**DrtEndSearch**</span></span>](/windows/desktop/api/drt/nf-drt-drtendsearch)                     | <span data-ttu-id="91926-168">Cancela una búsqueda de una clave en un DRT y, como resultado, se detiene el [**\_ \_ resultado**](/windows/desktop/api/drt/ns-drt-drt_search_result) de la devolución de resultados a través de la búsqueda de DRT.</span><span class="sxs-lookup"><span data-stu-id="91926-168">Cancels a search for a key in a DRT, and as a result, the return of results via [**DRT\_SEARCH\_RESULT**](/windows/desktop/api/drt/ns-drt-drt_search_result) is stopped.</span></span> <span data-ttu-id="91926-169">Se puede llamar a esta API en cualquier momento después de la emisión de una búsqueda.</span><span class="sxs-lookup"><span data-stu-id="91926-169">This API can be called at any point after a search is issued.</span></span>              |



 

## <a name="instance-name-functions"></a><span data-ttu-id="91926-170">Funciones de nombre de instancia</span><span class="sxs-lookup"><span data-stu-id="91926-170">Instance Name Functions</span></span>



| <span data-ttu-id="91926-171">Función</span><span class="sxs-lookup"><span data-stu-id="91926-171">Function</span></span>                                                 | <span data-ttu-id="91926-172">Descripción</span><span class="sxs-lookup"><span data-stu-id="91926-172">Description</span></span>                                                      |
|----------------------------------------------------------|------------------------------------------------------------------|
| [<span data-ttu-id="91926-173">**DrtGetInstanceName**</span><span class="sxs-lookup"><span data-stu-id="91926-173">**DrtGetInstanceName**</span></span>](/windows/desktop/api/drt/nf-drt-drtgetinstancename)         | <span data-ttu-id="91926-174">Obtiene el nombre asociado a una instancia de DRT.</span><span class="sxs-lookup"><span data-stu-id="91926-174">Gets the name associated with a DRT instance.</span></span>                    |
| [<span data-ttu-id="91926-175">**DrtGetInstanceNameSize**</span><span class="sxs-lookup"><span data-stu-id="91926-175">**DrtGetInstanceNameSize**</span></span>](/windows/desktop/api/drt/nf-drt-drtgetinstancenamesize) | <span data-ttu-id="91926-176">Devuelve el tamaño del nombre de la instancia de la tabla de enrutamiento distribuido.</span><span class="sxs-lookup"><span data-stu-id="91926-176">Returns the size of the Distributed Routing Table instance name.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="91926-177">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="91926-177">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="91926-178">Enumeraciones de tabla de enrutamiento distribuido</span><span class="sxs-lookup"><span data-stu-id="91926-178">Distributed Routing Table Enumerations</span></span>](distributed-routing-table-enumerations.md)
</dt> <dt>

[<span data-ttu-id="91926-179">Estructuras de tabla de enrutamiento distribuido</span><span class="sxs-lookup"><span data-stu-id="91926-179">Distributed Routing Table Structures</span></span>](distributed-routing-table-structures.md)
</dt> <dt>

[<span data-ttu-id="91926-180">Referencia de Table API de enrutamiento distribuido</span><span class="sxs-lookup"><span data-stu-id="91926-180">Distributed Routing Table API Reference</span></span>](distributed-routing-table-api-reference.md)
</dt> </dl>

 

 



