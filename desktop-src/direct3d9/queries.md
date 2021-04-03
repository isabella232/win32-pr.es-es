---
description: Hay varios tipos de consultas que se han diseñado para consultar el estado de los recursos.
ms.assetid: 2c65d199-141d-43a7-b513-4cb4459d7c27
title: Consultas (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22f450aa7015d4b66ad28b6c4d0632b2995bedd7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103906324"
---
# <a name="queries-direct3d-9"></a><span data-ttu-id="5edd3-103">Consultas (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="5edd3-103">Queries (Direct3D 9)</span></span>

<span data-ttu-id="5edd3-104">Hay varios tipos de consultas que se han diseñado para consultar el estado de los recursos.</span><span class="sxs-lookup"><span data-stu-id="5edd3-104">There are several types of queries which are designed to query the status of resources.</span></span> <span data-ttu-id="5edd3-105">El estado de un recurso determinado incluye el estado de la unidad de procesamiento de gráficos (GPU), el estado del controlador o el estado en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="5edd3-105">The status of a given resource includes graphics processing unit (GPU) status, driver status, or runtime status.</span></span> <span data-ttu-id="5edd3-106">Para comprender la diferencia entre los distintos tipos de consulta, debe comprender los Estados de la consulta.</span><span class="sxs-lookup"><span data-stu-id="5edd3-106">To understand the difference between the different query types, you need to understand the query states.</span></span> <span data-ttu-id="5edd3-107">En el siguiente diagrama de transición de estado se explica cada uno de los Estados de la consulta.</span><span class="sxs-lookup"><span data-stu-id="5edd3-107">The following state transition diagram explains each of the query states.</span></span>

![diagrama que muestra las transiciones entre Estados de consulta](images/queries.png)

<span data-ttu-id="5edd3-109">En el diagrama se muestran tres Estados, cada uno definido por círculos.</span><span class="sxs-lookup"><span data-stu-id="5edd3-109">The diagram shows three states, each defined by circles.</span></span> <span data-ttu-id="5edd3-110">Cada una de las líneas sólidas son eventos controlados por la aplicación que causan una transición de estado.</span><span class="sxs-lookup"><span data-stu-id="5edd3-110">Each of the solid lines are application-driven events that cause a state transition.</span></span> <span data-ttu-id="5edd3-111">La línea discontinua es un evento controlado por recursos que cambia una consulta del estado emitido al estado señalado.</span><span class="sxs-lookup"><span data-stu-id="5edd3-111">The dashed line is a resource-driven event that switches a query from the issued state to the signaled state.</span></span> <span data-ttu-id="5edd3-112">Cada uno de estos Estados tiene un propósito diferente:</span><span class="sxs-lookup"><span data-stu-id="5edd3-112">Each of these states has a different purpose:</span></span>

-   <span data-ttu-id="5edd3-113">El estado señalado es como un estado de inactividad.</span><span class="sxs-lookup"><span data-stu-id="5edd3-113">The signaled state is like an idle state.</span></span> <span data-ttu-id="5edd3-114">El objeto de consulta se ha generado y está esperando a que la aplicación emita la consulta.</span><span class="sxs-lookup"><span data-stu-id="5edd3-114">The query object has been generated and is waiting for the application to issue the query.</span></span> <span data-ttu-id="5edd3-115">Una vez que se completa una consulta y se vuelve a pasar al estado señalado, se puede recuperar la respuesta a la consulta.</span><span class="sxs-lookup"><span data-stu-id="5edd3-115">Once a query has completed and transitioned back to the signaled state, the answer to the query can be retrieved.</span></span>
-   <span data-ttu-id="5edd3-116">El estado de creación es como un área de ensayo para una consulta.</span><span class="sxs-lookup"><span data-stu-id="5edd3-116">The building state is like a staging area for a query.</span></span> <span data-ttu-id="5edd3-117">Desde el estado de compilación, se ha emitido una consulta (llamando a [**D3DISSUE \_ Begin**](d3dissue-begin.md)) pero aún no ha pasado al estado emitido.</span><span class="sxs-lookup"><span data-stu-id="5edd3-117">From the building state, a query has been issued (by calling [**D3DISSUE\_BEGIN**](d3dissue-begin.md)) but has not yet transitioned to the issued state.</span></span> <span data-ttu-id="5edd3-118">Cuando una aplicación emite un final de consulta (mediante una llamada a [**D3DISSUE \_ End**](d3dissue-end.md)), la consulta pasa al estado emitido.</span><span class="sxs-lookup"><span data-stu-id="5edd3-118">When an application issues a query end (by calling [**D3DISSUE\_END**](d3dissue-end.md)), the query transitions to the issued state.</span></span>
-   <span data-ttu-id="5edd3-119">El estado emitido significa que el recurso que se consulta tiene el control de la consulta.</span><span class="sxs-lookup"><span data-stu-id="5edd3-119">The issued state means that the resource being queried has control of the query.</span></span> <span data-ttu-id="5edd3-120">Una vez que el recurso finaliza su trabajo, el recurso realiza la transición de la máquina de Estados al estado señalado.</span><span class="sxs-lookup"><span data-stu-id="5edd3-120">Once the resource finishes its work, the resource transitions the state machine to the signaled state.</span></span> <span data-ttu-id="5edd3-121">Durante el estado emitido, la aplicación debe sondear para detectar la transición al estado señalado.</span><span class="sxs-lookup"><span data-stu-id="5edd3-121">During the issued state, the application must poll to detect the transition to the signaled state.</span></span> <span data-ttu-id="5edd3-122">Una vez que se produce la transición al estado señalado, [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) devuelve el resultado de la consulta (a través de un argumento) a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="5edd3-122">Once the transition to the signaled state occurs, [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) returns the query result (through an argument) to the application.</span></span>

<span data-ttu-id="5edd3-123">En la tabla siguiente se enumeran los tipos de consulta disponibles.</span><span class="sxs-lookup"><span data-stu-id="5edd3-123">The following table lists the available query types.</span></span>



| <span data-ttu-id="5edd3-124">Tipo de consulta</span><span class="sxs-lookup"><span data-stu-id="5edd3-124">Query Type</span></span>        | <span data-ttu-id="5edd3-125">Evento Issue</span><span class="sxs-lookup"><span data-stu-id="5edd3-125">Issue Event</span></span>                                                                      | <span data-ttu-id="5edd3-126">Búfer GetData</span><span class="sxs-lookup"><span data-stu-id="5edd3-126">GetData buffer</span></span>                                                              | <span data-ttu-id="5edd3-127">Tiempo de ejecución</span><span class="sxs-lookup"><span data-stu-id="5edd3-127">Runtime</span></span>      | <span data-ttu-id="5edd3-128">Inicio implícito de la consulta</span><span class="sxs-lookup"><span data-stu-id="5edd3-128">Implicit beginning of query</span></span>                      |
|-------------------|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------|--------------|--------------------------------------------------|
| <span data-ttu-id="5edd3-129">BANDWIDTHTIMINGS</span><span class="sxs-lookup"><span data-stu-id="5edd3-129">BANDWIDTHTIMINGS</span></span>  | <span data-ttu-id="5edd3-130">[**D3DISSUE \_ Inicio**](d3dissue-begin.md), [ **D3DISSUE \_ End**](d3dissue-end.md)</span><span class="sxs-lookup"><span data-stu-id="5edd3-130">[**D3DISSUE\_BEGIN**](d3dissue-begin.md), [**D3DISSUE\_END**](d3dissue-end.md)</span></span> | [<span data-ttu-id="5edd3-131">**D3DDEVINFO \_ D3D9BANDWIDTHTIMINGS**</span><span class="sxs-lookup"><span data-stu-id="5edd3-131">**D3DDEVINFO\_D3D9BANDWIDTHTIMINGS**</span></span>](d3ddevinfo-d3d9bandwidthtimings.md) | <span data-ttu-id="5edd3-132">Venta directa/depuración</span><span class="sxs-lookup"><span data-stu-id="5edd3-132">Retail/Debug</span></span> | <span data-ttu-id="5edd3-133">N/D</span><span class="sxs-lookup"><span data-stu-id="5edd3-133">N/A</span></span>                                              |
| <span data-ttu-id="5edd3-134">CACHEUTILIZATION</span><span class="sxs-lookup"><span data-stu-id="5edd3-134">CACHEUTILIZATION</span></span>  | <span data-ttu-id="5edd3-135">[**D3DISSUE \_ Inicio**](d3dissue-begin.md), [ **D3DISSUE \_ End**](d3dissue-end.md)</span><span class="sxs-lookup"><span data-stu-id="5edd3-135">[**D3DISSUE\_BEGIN**](d3dissue-begin.md), [**D3DISSUE\_END**](d3dissue-end.md)</span></span> | [<span data-ttu-id="5edd3-136">**D3DDEVINFO \_ D3D9CACHEUTILIZATION**</span><span class="sxs-lookup"><span data-stu-id="5edd3-136">**D3DDEVINFO\_D3D9CACHEUTILIZATION**</span></span>](d3ddevinfo-d3d9cacheutilization.md) | <span data-ttu-id="5edd3-137">Venta directa/depuración</span><span class="sxs-lookup"><span data-stu-id="5edd3-137">Retail/Debug</span></span> | <span data-ttu-id="5edd3-138">N/D</span><span class="sxs-lookup"><span data-stu-id="5edd3-138">N/A</span></span>                                              |
| <span data-ttu-id="5edd3-139">CESO</span><span class="sxs-lookup"><span data-stu-id="5edd3-139">EVENT</span></span>             | [<span data-ttu-id="5edd3-140">**Final de D3DISSUE \_**</span><span class="sxs-lookup"><span data-stu-id="5edd3-140">**D3DISSUE\_END**</span></span>](d3dissue-end.md)                                            | <span data-ttu-id="5edd3-141">BOOL</span><span class="sxs-lookup"><span data-stu-id="5edd3-141">BOOL</span></span>                                                                        | <span data-ttu-id="5edd3-142">Venta directa/depuración</span><span class="sxs-lookup"><span data-stu-id="5edd3-142">Retail/Debug</span></span> | [<span data-ttu-id="5edd3-143">**CreateDevice**</span><span class="sxs-lookup"><span data-stu-id="5edd3-143">**CreateDevice**</span></span>](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice) |
| <span data-ttu-id="5edd3-144">INTERFACETIMINGS</span><span class="sxs-lookup"><span data-stu-id="5edd3-144">INTERFACETIMINGS</span></span>  | <span data-ttu-id="5edd3-145">[**D3DISSUE \_ Inicio**](d3dissue-begin.md), [ **D3DISSUE \_ End**](d3dissue-end.md)</span><span class="sxs-lookup"><span data-stu-id="5edd3-145">[**D3DISSUE\_BEGIN**](d3dissue-begin.md), [**D3DISSUE\_END**](d3dissue-end.md)</span></span> | [<span data-ttu-id="5edd3-146">**D3DDEVINFO \_ D3D9INTERFACETIMINGS**</span><span class="sxs-lookup"><span data-stu-id="5edd3-146">**D3DDEVINFO\_D3D9INTERFACETIMINGS**</span></span>](d3ddevinfo-d3d9interfacetimings.md) | <span data-ttu-id="5edd3-147">Venta directa/depuración</span><span class="sxs-lookup"><span data-stu-id="5edd3-147">Retail/Debug</span></span> | <span data-ttu-id="5edd3-148">N/D</span><span class="sxs-lookup"><span data-stu-id="5edd3-148">N/A</span></span>                                              |
| <span data-ttu-id="5edd3-149">OCULTO</span><span class="sxs-lookup"><span data-stu-id="5edd3-149">OCCLUSION</span></span>         | <span data-ttu-id="5edd3-150">[**D3DISSUE \_ Inicio**](d3dissue-begin.md), [ **D3DISSUE \_ End**](d3dissue-end.md)</span><span class="sxs-lookup"><span data-stu-id="5edd3-150">[**D3DISSUE\_BEGIN**](d3dissue-begin.md), [**D3DISSUE\_END**](d3dissue-end.md)</span></span> | <span data-ttu-id="5edd3-151">DWORD</span><span class="sxs-lookup"><span data-stu-id="5edd3-151">DWORD</span></span>                                                                       | <span data-ttu-id="5edd3-152">Venta directa/depuración</span><span class="sxs-lookup"><span data-stu-id="5edd3-152">Retail/Debug</span></span> | <span data-ttu-id="5edd3-153">N/D</span><span class="sxs-lookup"><span data-stu-id="5edd3-153">N/A</span></span>                                              |
| <span data-ttu-id="5edd3-154">PIPELINETIMINGS</span><span class="sxs-lookup"><span data-stu-id="5edd3-154">PIPELINETIMINGS</span></span>   | <span data-ttu-id="5edd3-155">[**D3DISSUE \_ Inicio**](d3dissue-begin.md), [ **D3DISSUE \_ End**](d3dissue-end.md)</span><span class="sxs-lookup"><span data-stu-id="5edd3-155">[**D3DISSUE\_BEGIN**](d3dissue-begin.md), [**D3DISSUE\_END**](d3dissue-end.md)</span></span> | [<span data-ttu-id="5edd3-156">**D3DDEVINFO \_ D3D9PIPELINETIMINGS**</span><span class="sxs-lookup"><span data-stu-id="5edd3-156">**D3DDEVINFO\_D3D9PIPELINETIMINGS**</span></span>](d3ddevinfo-d3d9pipelinetimings.md)   | <span data-ttu-id="5edd3-157">Venta directa/depuración</span><span class="sxs-lookup"><span data-stu-id="5edd3-157">Retail/Debug</span></span> | <span data-ttu-id="5edd3-158">N/D</span><span class="sxs-lookup"><span data-stu-id="5edd3-158">N/A</span></span>                                              |
| <span data-ttu-id="5edd3-159">RESOURCEMANAGER</span><span class="sxs-lookup"><span data-stu-id="5edd3-159">RESOURCEMANAGER</span></span>   | [<span data-ttu-id="5edd3-160">**Final de D3DISSUE \_**</span><span class="sxs-lookup"><span data-stu-id="5edd3-160">**D3DISSUE\_END**</span></span>](d3dissue-end.md)                                            | [<span data-ttu-id="5edd3-161">**D3DDEVINFO \_ ResourceManager**</span><span class="sxs-lookup"><span data-stu-id="5edd3-161">**D3DDEVINFO\_ResourceManager**</span></span>](d3ddevinfo-resourcemanager.md)           | <span data-ttu-id="5edd3-162">Solo depuración</span><span class="sxs-lookup"><span data-stu-id="5edd3-162">Debug only</span></span>   | [<span data-ttu-id="5edd3-163">**Presente**</span><span class="sxs-lookup"><span data-stu-id="5edd3-163">**Present**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present)     |
| <span data-ttu-id="5edd3-164">timestamp</span><span class="sxs-lookup"><span data-stu-id="5edd3-164">TIMESTAMP</span></span>         | [<span data-ttu-id="5edd3-165">**Final de D3DISSUE \_**</span><span class="sxs-lookup"><span data-stu-id="5edd3-165">**D3DISSUE\_END**</span></span>](d3dissue-end.md)                                            | <span data-ttu-id="5edd3-166">UINT64</span><span class="sxs-lookup"><span data-stu-id="5edd3-166">UINT64</span></span>                                                                      | <span data-ttu-id="5edd3-167">Venta directa/depuración</span><span class="sxs-lookup"><span data-stu-id="5edd3-167">Retail/Debug</span></span> | <span data-ttu-id="5edd3-168">N/D</span><span class="sxs-lookup"><span data-stu-id="5edd3-168">N/A</span></span>                                              |
| <span data-ttu-id="5edd3-169">TIMESTAMPDISJOINT</span><span class="sxs-lookup"><span data-stu-id="5edd3-169">TIMESTAMPDISJOINT</span></span> | <span data-ttu-id="5edd3-170">[**D3DISSUE \_ Inicio**](d3dissue-begin.md), [ **D3DISSUE \_ End**](d3dissue-end.md)</span><span class="sxs-lookup"><span data-stu-id="5edd3-170">[**D3DISSUE\_BEGIN**](d3dissue-begin.md), [**D3DISSUE\_END**](d3dissue-end.md)</span></span> | <span data-ttu-id="5edd3-171">BOOL</span><span class="sxs-lookup"><span data-stu-id="5edd3-171">BOOL</span></span>                                                                        | <span data-ttu-id="5edd3-172">Venta directa/depuración</span><span class="sxs-lookup"><span data-stu-id="5edd3-172">Retail/Debug</span></span> | <span data-ttu-id="5edd3-173">N/D</span><span class="sxs-lookup"><span data-stu-id="5edd3-173">N/A</span></span>                                              |
| <span data-ttu-id="5edd3-174">TIMESTAMPFREQ</span><span class="sxs-lookup"><span data-stu-id="5edd3-174">TIMESTAMPFREQ</span></span>     | [<span data-ttu-id="5edd3-175">**Final de D3DISSUE \_**</span><span class="sxs-lookup"><span data-stu-id="5edd3-175">**D3DISSUE\_END**</span></span>](d3dissue-end.md)                                            | <span data-ttu-id="5edd3-176">UINT64</span><span class="sxs-lookup"><span data-stu-id="5edd3-176">UINT64</span></span>                                                                      | <span data-ttu-id="5edd3-177">Venta directa/depuración</span><span class="sxs-lookup"><span data-stu-id="5edd3-177">Retail/Debug</span></span> | <span data-ttu-id="5edd3-178">N/D</span><span class="sxs-lookup"><span data-stu-id="5edd3-178">N/A</span></span>                                              |
| <span data-ttu-id="5edd3-179">VCACHE</span><span class="sxs-lookup"><span data-stu-id="5edd3-179">VCACHE</span></span>            | [<span data-ttu-id="5edd3-180">**Final de D3DISSUE \_**</span><span class="sxs-lookup"><span data-stu-id="5edd3-180">**D3DISSUE\_END**</span></span>](d3dissue-end.md)                                            | [<span data-ttu-id="5edd3-181">**D3DDEVINFO \_ VCACHE**</span><span class="sxs-lookup"><span data-stu-id="5edd3-181">**D3DDEVINFO\_VCACHE**</span></span>](d3ddevinfo-vcache.md)                             | <span data-ttu-id="5edd3-182">Venta directa/depuración</span><span class="sxs-lookup"><span data-stu-id="5edd3-182">Retail/Debug</span></span> | [<span data-ttu-id="5edd3-183">**CreateDevice**</span><span class="sxs-lookup"><span data-stu-id="5edd3-183">**CreateDevice**</span></span>](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice) |
| <span data-ttu-id="5edd3-184">VERTEXSTATS</span><span class="sxs-lookup"><span data-stu-id="5edd3-184">VERTEXSTATS</span></span>       | [<span data-ttu-id="5edd3-185">**Final de D3DISSUE \_**</span><span class="sxs-lookup"><span data-stu-id="5edd3-185">**D3DISSUE\_END**</span></span>](d3dissue-end.md)                                            | [<span data-ttu-id="5edd3-186">**D3DDEVINFO \_ D3DVERTEXSTATS**</span><span class="sxs-lookup"><span data-stu-id="5edd3-186">**D3DDEVINFO\_D3DVERTEXSTATS**</span></span>](d3ddevinfo-d3dvertexstats.md)             | <span data-ttu-id="5edd3-187">Solo depuración</span><span class="sxs-lookup"><span data-stu-id="5edd3-187">Debug only</span></span>   | [<span data-ttu-id="5edd3-188">**Presente**</span><span class="sxs-lookup"><span data-stu-id="5edd3-188">**Present**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present)     |
| <span data-ttu-id="5edd3-189">VERTEXTIMINGS</span><span class="sxs-lookup"><span data-stu-id="5edd3-189">VERTEXTIMINGS</span></span>     | <span data-ttu-id="5edd3-190">[**D3DISSUE \_ Inicio**](d3dissue-begin.md), [ **D3DISSUE \_ End**](d3dissue-end.md)</span><span class="sxs-lookup"><span data-stu-id="5edd3-190">[**D3DISSUE\_BEGIN**](d3dissue-begin.md), [**D3DISSUE\_END**](d3dissue-end.md)</span></span> | [<span data-ttu-id="5edd3-191">**D3DDEVINFO \_ D3D9STAGETIMINGS**</span><span class="sxs-lookup"><span data-stu-id="5edd3-191">**D3DDEVINFO\_D3D9STAGETIMINGS**</span></span>](d3ddevinfo-d3d9stagetimings.md)         | <span data-ttu-id="5edd3-192">Venta directa/depuración</span><span class="sxs-lookup"><span data-stu-id="5edd3-192">Retail/Debug</span></span> | <span data-ttu-id="5edd3-193">N/D</span><span class="sxs-lookup"><span data-stu-id="5edd3-193">N/A</span></span>                                              |



 

<span data-ttu-id="5edd3-194">Algunas de las consultas requieren un evento Begin y end, mientras que otras solo requieren un evento End.</span><span class="sxs-lookup"><span data-stu-id="5edd3-194">Some of the queries require a begin and end event, while others only require an end event.</span></span> <span data-ttu-id="5edd3-195">Las consultas que solo requieren un evento End comienzan cuando se produce otro evento implícito (que aparece en la tabla).</span><span class="sxs-lookup"><span data-stu-id="5edd3-195">The queries that only require an end event begin when another implicit event occurs (which is listed in the table).</span></span> <span data-ttu-id="5edd3-196">Todas las consultas devuelven una respuesta, excepto la consulta de eventos cuya respuesta siempre es **true**.</span><span class="sxs-lookup"><span data-stu-id="5edd3-196">All queries return an answer, except the event query whose answer is always **TRUE**.</span></span> <span data-ttu-id="5edd3-197">Una aplicación utiliza el estado de la consulta o el código de retorno de [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata).</span><span class="sxs-lookup"><span data-stu-id="5edd3-197">An application uses either the state of the query or the return code of [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata).</span></span>

## <a name="create-a-query"></a><span data-ttu-id="5edd3-198">Crear una consulta</span><span class="sxs-lookup"><span data-stu-id="5edd3-198">Create a Query</span></span>

<span data-ttu-id="5edd3-199">Antes de crear una consulta, puede comprobar si el tiempo de ejecución admite consultas llamando a [**CreateQuery**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createquery) con un puntero **nulo** como este:</span><span class="sxs-lookup"><span data-stu-id="5edd3-199">Before you create a query, you can check to see if the runtime supports queries by calling [**CreateQuery**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createquery) with a **NULL** pointer like this:</span></span>


```
IDirect3DQuery9* pEventQuery;

// Create a device pointer m_pd3dDevice

// Create a query object
HRESULT hr = m_pd3dDevice->CreateQuery(D3DQUERYTYPE_EVENT, NULL);
```



<span data-ttu-id="5edd3-200">Este método devuelve un código de operación correcta si se puede crear una consulta; en caso contrario, devuelve un código de error.</span><span class="sxs-lookup"><span data-stu-id="5edd3-200">This method returns a success code if a query can be created; otherwise it returns an error code.</span></span> <span data-ttu-id="5edd3-201">Una vez que [**CreateQuery**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createquery) se ejecute correctamente, puede crear un objeto de consulta similar al siguiente:</span><span class="sxs-lookup"><span data-stu-id="5edd3-201">Once [**CreateQuery**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createquery) succeeds, you can create a query object like this:</span></span>


```
IDirect3DQuery9* pEventQuery;
m_pd3dDevice->CreateQuery(D3DQUERYTYPE_EVENT, &pEventQuery);
```



<span data-ttu-id="5edd3-202">Si la llamada se realiza correctamente, se crea un objeto de consulta.</span><span class="sxs-lookup"><span data-stu-id="5edd3-202">If this call succeeds, a query object is created.</span></span> <span data-ttu-id="5edd3-203">La consulta está esencialmente inactiva en el estado señalado (con una respuesta no inicializada) en espera de ser emitida.</span><span class="sxs-lookup"><span data-stu-id="5edd3-203">The query is essentially idle in the signaled state (with an uninitialized answer) waiting to be issued.</span></span> <span data-ttu-id="5edd3-204">Cuando haya terminado con la consulta, suéltelo como cualquier otra interfaz.</span><span class="sxs-lookup"><span data-stu-id="5edd3-204">When you are finished with the query, release it like any other interface.</span></span>

## <a name="issue-a-query"></a><span data-ttu-id="5edd3-205">Emisión de una consulta</span><span class="sxs-lookup"><span data-stu-id="5edd3-205">Issue a Query</span></span>

<span data-ttu-id="5edd3-206">Una aplicación cambia el estado de una consulta mediante la emisión de una consulta.</span><span class="sxs-lookup"><span data-stu-id="5edd3-206">An application changes a query state by issuing a query.</span></span> <span data-ttu-id="5edd3-207">Este es un ejemplo de la emisión de una consulta:</span><span class="sxs-lookup"><span data-stu-id="5edd3-207">Here is an example of issuing a query:</span></span>


```
IDirect3DQuery9* pEventQuery;
m_pD3DDevice->CreateQuery(D3DQUERYTYPE_EVENT, &pEventQuery);

// Issue a Begin event
pEventQuery->Issue(D3DISSUE_BEGIN);

or

// Issue an End event
pEventQuery->Issue(D3DISSUE_END);
```



<span data-ttu-id="5edd3-208">Una consulta en el estado señalado pasará a ser similar a la siguiente cuando se emita:</span><span class="sxs-lookup"><span data-stu-id="5edd3-208">A query in the signaled state will transition like this when issued:</span></span>



| <span data-ttu-id="5edd3-209">Tipo de problema</span><span class="sxs-lookup"><span data-stu-id="5edd3-209">Issue Type</span></span>                                | <span data-ttu-id="5edd3-210">Las transiciones de consulta a.</span><span class="sxs-lookup"><span data-stu-id="5edd3-210">Query Transitions to the .</span></span> <span data-ttu-id="5edd3-211">.</span><span class="sxs-lookup"><span data-stu-id="5edd3-211">.</span></span> <span data-ttu-id="5edd3-212">.</span><span class="sxs-lookup"><span data-stu-id="5edd3-212">.</span></span> |
|-------------------------------------------|--------------------------------|
| [<span data-ttu-id="5edd3-213">**Inicio de D3DISSUE \_**</span><span class="sxs-lookup"><span data-stu-id="5edd3-213">**D3DISSUE\_BEGIN**</span></span>](d3dissue-begin.md) | <span data-ttu-id="5edd3-214">Estado de compilación.</span><span class="sxs-lookup"><span data-stu-id="5edd3-214">Building state.</span></span>                |
| [<span data-ttu-id="5edd3-215">**Final de D3DISSUE \_**</span><span class="sxs-lookup"><span data-stu-id="5edd3-215">**D3DISSUE\_END**</span></span>](d3dissue-end.md)     | <span data-ttu-id="5edd3-216">Estado emitido.</span><span class="sxs-lookup"><span data-stu-id="5edd3-216">Issued state.</span></span>                  |



 

<span data-ttu-id="5edd3-217">Una consulta en el estado de creación cambiará de este modo cuando se emita:</span><span class="sxs-lookup"><span data-stu-id="5edd3-217">A query in the building state will transition like this when issued:</span></span>



| <span data-ttu-id="5edd3-218">Tipo de problema</span><span class="sxs-lookup"><span data-stu-id="5edd3-218">Issue Type</span></span>                                | <span data-ttu-id="5edd3-219">Las transiciones de consulta a.</span><span class="sxs-lookup"><span data-stu-id="5edd3-219">Query Transitions to the .</span></span> <span data-ttu-id="5edd3-220">.</span><span class="sxs-lookup"><span data-stu-id="5edd3-220">.</span></span> <span data-ttu-id="5edd3-221">.</span><span class="sxs-lookup"><span data-stu-id="5edd3-221">.</span></span>                                            |
|-------------------------------------------|---------------------------------------------------------------------------|
| [<span data-ttu-id="5edd3-222">**Inicio de D3DISSUE \_**</span><span class="sxs-lookup"><span data-stu-id="5edd3-222">**D3DISSUE\_BEGIN**</span></span>](d3dissue-begin.md) | <span data-ttu-id="5edd3-223">(Ninguna transición permanece en el estado de compilación.</span><span class="sxs-lookup"><span data-stu-id="5edd3-223">(No transition, stays in the building state.</span></span> <span data-ttu-id="5edd3-224">Reinicia el corchete de consulta).</span><span class="sxs-lookup"><span data-stu-id="5edd3-224">Restarts the query bracket.)</span></span> |
| [<span data-ttu-id="5edd3-225">**Final de D3DISSUE \_**</span><span class="sxs-lookup"><span data-stu-id="5edd3-225">**D3DISSUE\_END**</span></span>](d3dissue-end.md)     | <span data-ttu-id="5edd3-226">Estado emitido.</span><span class="sxs-lookup"><span data-stu-id="5edd3-226">Issued state.</span></span>                                                             |



 

<span data-ttu-id="5edd3-227">Una consulta en el estado emitido se realizará una transición similar a la siguiente cuando se emita:</span><span class="sxs-lookup"><span data-stu-id="5edd3-227">A query in the issued state will transition like this when issued:</span></span>



| <span data-ttu-id="5edd3-228">Tipo de problema</span><span class="sxs-lookup"><span data-stu-id="5edd3-228">Issue Type</span></span>                                | <span data-ttu-id="5edd3-229">Las transiciones de consulta a.</span><span class="sxs-lookup"><span data-stu-id="5edd3-229">Query Transitions to the .</span></span> <span data-ttu-id="5edd3-230">.</span><span class="sxs-lookup"><span data-stu-id="5edd3-230">.</span></span> <span data-ttu-id="5edd3-231">.</span><span class="sxs-lookup"><span data-stu-id="5edd3-231">.</span></span>                    |
|-------------------------------------------|---------------------------------------------------|
| [<span data-ttu-id="5edd3-232">**Inicio de D3DISSUE \_**</span><span class="sxs-lookup"><span data-stu-id="5edd3-232">**D3DISSUE\_BEGIN**</span></span>](d3dissue-begin.md) | <span data-ttu-id="5edd3-233">Compilar el estado y reinicia el corchete de consulta.</span><span class="sxs-lookup"><span data-stu-id="5edd3-233">Building state and restarts the query bracket.</span></span>    |
| [<span data-ttu-id="5edd3-234">**Final de D3DISSUE \_**</span><span class="sxs-lookup"><span data-stu-id="5edd3-234">**D3DISSUE\_END**</span></span>](d3dissue-end.md)     | <span data-ttu-id="5edd3-235">Estado emitido después de abandonar la consulta existente.</span><span class="sxs-lookup"><span data-stu-id="5edd3-235">Issued state after abandoning the existing query.</span></span> |



 

## <a name="check-the-query-state-and-get-the-answer-to-the-query"></a><span data-ttu-id="5edd3-236">Comprobar el estado de la consulta y obtener la respuesta a la consulta</span><span class="sxs-lookup"><span data-stu-id="5edd3-236">Check the Query State and Get the Answer to the Query</span></span>

<span data-ttu-id="5edd3-237">[**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) hace dos cosas:</span><span class="sxs-lookup"><span data-stu-id="5edd3-237">[**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) does two things:</span></span>

1.  <span data-ttu-id="5edd3-238">Devuelve el estado de la consulta en el código de retorno.</span><span class="sxs-lookup"><span data-stu-id="5edd3-238">Returns the query state in the return code.</span></span>
2.  <span data-ttu-id="5edd3-239">Devuelve la respuesta a la consulta en *pdata*.</span><span class="sxs-lookup"><span data-stu-id="5edd3-239">Returns the answer to the query in *pData*.</span></span>

<span data-ttu-id="5edd3-240">En cada uno de los tres Estados de la consulta, estos son los códigos de retorno [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) :</span><span class="sxs-lookup"><span data-stu-id="5edd3-240">From each of the three query states, here are the [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) return codes:</span></span>



| <span data-ttu-id="5edd3-241">Estado de la consulta</span><span class="sxs-lookup"><span data-stu-id="5edd3-241">Query State</span></span> | <span data-ttu-id="5edd3-242">Código de retorno GetData</span><span class="sxs-lookup"><span data-stu-id="5edd3-242">GetData return code</span></span> |
|-------------|---------------------|
| <span data-ttu-id="5edd3-243">Señalado</span><span class="sxs-lookup"><span data-stu-id="5edd3-243">Signaled</span></span>    | <span data-ttu-id="5edd3-244">S \_ correcto</span><span class="sxs-lookup"><span data-stu-id="5edd3-244">S\_OK</span></span>               |
| <span data-ttu-id="5edd3-245">Compilación</span><span class="sxs-lookup"><span data-stu-id="5edd3-245">Building</span></span>    | <span data-ttu-id="5edd3-246">Código de error</span><span class="sxs-lookup"><span data-stu-id="5edd3-246">Error code</span></span>          |
| <span data-ttu-id="5edd3-247">Emitido</span><span class="sxs-lookup"><span data-stu-id="5edd3-247">Issued</span></span>      | <span data-ttu-id="5edd3-248">S \_ false</span><span class="sxs-lookup"><span data-stu-id="5edd3-248">S\_FALSE</span></span>            |



 

<span data-ttu-id="5edd3-249">Por ejemplo, cuando una consulta está en el estado emitido y la respuesta a la consulta no está disponible, [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) devuelve S \_ false.</span><span class="sxs-lookup"><span data-stu-id="5edd3-249">For example, when a query is in the issued state and the answer to the query is not available, [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) returns S\_FALSE.</span></span> <span data-ttu-id="5edd3-250">Cuando el recurso finaliza su trabajo y la aplicación ha emitido un fin de consulta, el recurso realiza la transición de la consulta al estado señalado.</span><span class="sxs-lookup"><span data-stu-id="5edd3-250">When the resource finishes its work and the application has issued a query end, the resource transitions the query to the signaled state.</span></span> <span data-ttu-id="5edd3-251">En el estado señalado, **GetData** devuelve S, \_ lo que significa que la respuesta a la consulta también se devuelve en *pdata*.</span><span class="sxs-lookup"><span data-stu-id="5edd3-251">From the signaled state, **GetData** returns S\_OK which means that the answer to the query is also returned in *pData*.</span></span> <span data-ttu-id="5edd3-252">Por ejemplo, esta es la secuencia de eventos para devolver el número de píxeles dibujados en una secuencia de representación:</span><span class="sxs-lookup"><span data-stu-id="5edd3-252">For instance, here is the sequence of events to return the number of pixels drawn in a render sequence:</span></span>

-   <span data-ttu-id="5edd3-253">Crear la consulta.</span><span class="sxs-lookup"><span data-stu-id="5edd3-253">Create the query.</span></span>
-   <span data-ttu-id="5edd3-254">Emita un evento Begin.</span><span class="sxs-lookup"><span data-stu-id="5edd3-254">Issue a begin event.</span></span>
-   <span data-ttu-id="5edd3-255">Dibuje algo.</span><span class="sxs-lookup"><span data-stu-id="5edd3-255">Draw something.</span></span>
-   <span data-ttu-id="5edd3-256">Emite un evento de finalización.</span><span class="sxs-lookup"><span data-stu-id="5edd3-256">Issue an end event.</span></span>

<span data-ttu-id="5edd3-257">A continuación se encuentra la secuencia de código correspondiente:</span><span class="sxs-lookup"><span data-stu-id="5edd3-257">The following is the corresponding sequence of code:</span></span>


```
IDirect3DQuery9* pOcclusionQuery;
DWORD numberOfPixelsDrawn;

m_pD3DDevice->CreateQuery(D3DQUERYTYPE_OCCLUSION, &pOcclusionQuery);

// Add an end marker to the command buffer queue.
pOcclusionQuery->Issue(D3DISSUE_BEGIN);

// API render loop
...
Draw(...)
...

// Add an end marker to the command buffer queue.
pOcclusionQuery->Issue(D3DISSUE_END);

// Force the driver to execute the commands from the command buffer.
// Empty the command buffer and wait until the GPU is idle.
while(S_FALSE == pOcclusionQuery->GetData( &numberOfPixelsDrawn, 
                                  sizeof(DWORD), D3DGETDATA_FLUSH ))
    ;
```



<span data-ttu-id="5edd3-258">Estas líneas de código hacen varias cosas:</span><span class="sxs-lookup"><span data-stu-id="5edd3-258">These lines of code do several things:</span></span>

-   <span data-ttu-id="5edd3-259">Llame a [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) para devolver el número de píxeles dibujados.</span><span class="sxs-lookup"><span data-stu-id="5edd3-259">Call [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) to return the number of pixels drawn.</span></span>
-   <span data-ttu-id="5edd3-260">Especifique [**el \_ vaciado de D3DGETDATA**](d3dgetdata-flush.md) para permitir que el recurso pase la consulta al estado señalado.</span><span class="sxs-lookup"><span data-stu-id="5edd3-260">Specify [**D3DGETDATA\_FLUSH**](d3dgetdata-flush.md) to enable the resource to transition the query to the signaled state.</span></span>
-   <span data-ttu-id="5edd3-261">Sondee el recurso de consulta mediante una llamada a [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) desde un bucle.</span><span class="sxs-lookup"><span data-stu-id="5edd3-261">Poll the query resource by calling [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) from a loop.</span></span> <span data-ttu-id="5edd3-262">Siempre que **GetData** devuelva S \_ , esto significa que el recurso aún no ha devuelto la respuesta.</span><span class="sxs-lookup"><span data-stu-id="5edd3-262">As long as **GetData** returns S\_FALSE, this means the resource has not returned the answer yet.</span></span>

<span data-ttu-id="5edd3-263">En esencia, el valor devuelto por [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) indica en qué estado se encuentra la consulta.</span><span class="sxs-lookup"><span data-stu-id="5edd3-263">The return value of [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) essentially tells you in what state the query is.</span></span> <span data-ttu-id="5edd3-264">Los valores posibles son \_ OK, s \_ false y un error.</span><span class="sxs-lookup"><span data-stu-id="5edd3-264">Possible values are S\_OK, S\_FALSE, and an error.</span></span> <span data-ttu-id="5edd3-265">No llame a **GetData** en una consulta que se encuentra en el estado de compilación.</span><span class="sxs-lookup"><span data-stu-id="5edd3-265">Do not call **GetData** on a query that is in the building state.</span></span>

-   <span data-ttu-id="5edd3-266">S \_ correcto significa que el recurso (GPU o controlador o tiempo de ejecución) ha finalizado.</span><span class="sxs-lookup"><span data-stu-id="5edd3-266">S\_OK means the resource (GPU or driver, or runtime) is finished.</span></span> <span data-ttu-id="5edd3-267">La consulta devuelve el estado señalado.</span><span class="sxs-lookup"><span data-stu-id="5edd3-267">The query is returning to the signaled state.</span></span> <span data-ttu-id="5edd3-268">La respuesta (si existe) la devuelve [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata).</span><span class="sxs-lookup"><span data-stu-id="5edd3-268">The answer (if any) is being returned by [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata).</span></span>
-   <span data-ttu-id="5edd3-269">S \_ false significa que el recurso (GPU o controlador o tiempo de ejecución) no puede devolver una respuesta todavía.</span><span class="sxs-lookup"><span data-stu-id="5edd3-269">S\_FALSE means the resource (GPU or driver, or runtime) cannot return an answer yet.</span></span> <span data-ttu-id="5edd3-270">Esto puede deberse a que la GPU no se ha terminado o no ha detectado aún el trabajo.</span><span class="sxs-lookup"><span data-stu-id="5edd3-270">This could be because the GPU is not finished or has not seen the work yet.</span></span>
-   <span data-ttu-id="5edd3-271">Un error significa que la consulta ha generado un error del que no se puede recuperar.</span><span class="sxs-lookup"><span data-stu-id="5edd3-271">An error means that the query has generated an error from which it cannot recover.</span></span> <span data-ttu-id="5edd3-272">Este podría ser el caso si se pierde el dispositivo durante una consulta.</span><span class="sxs-lookup"><span data-stu-id="5edd3-272">This could be the case if the device is lost during a query.</span></span> <span data-ttu-id="5edd3-273">Una vez que una consulta ha generado un error (distinto de S \_ false), se debe volver a crear la consulta, lo que reiniciará la secuencia de consulta desde el estado señalado.</span><span class="sxs-lookup"><span data-stu-id="5edd3-273">Once a query has generated an error (other than S\_FALSE), the query must be recreated which will restart the query sequence from the signaled state.</span></span>

<span data-ttu-id="5edd3-274">En lugar de especificar el [**\_ vaciado de D3DGETDATA**](d3dgetdata-flush.md), que proporciona información más actualizada, puede proporcionar cero, que es una comprobación más ligera si la consulta está en el estado emitido.</span><span class="sxs-lookup"><span data-stu-id="5edd3-274">Instead of specifying [**D3DGETDATA\_FLUSH**](d3dgetdata-flush.md), which provides more up-to-date information, you could supply zero which is a more light-weight check if the query is in the issued state.</span></span> <span data-ttu-id="5edd3-275">Si se proporciona cero, [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) no vaciará el búfer de comandos.</span><span class="sxs-lookup"><span data-stu-id="5edd3-275">Supplying zero will cause [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) to not flush the command buffer.</span></span> <span data-ttu-id="5edd3-276">Por este motivo, se debe tener cuidado para evitar los bucles infinate (consulte **GetData** para obtener más detalles).</span><span class="sxs-lookup"><span data-stu-id="5edd3-276">For this reason, care must be taken to avoid infinate loops (see **GetData** for details).</span></span> <span data-ttu-id="5edd3-277">Dado que el Runtime pone en cola el trabajo en el búfer de comandos, **D3DGETDATA \_ Flush** es un mecanismo para vaciar el búfer de comandos en el controlador (y, por lo tanto, la GPU; consulte generación de perfiles de llamadas de la [API de Direct3D con precisión (Direct3D 9)](accurately-profiling-direct3d-api-calls.md)).</span><span class="sxs-lookup"><span data-stu-id="5edd3-277">Since the runtime queues up work in the command buffer, **D3DGETDATA\_FLUSH** is a mechanism for flushing the command buffer to the driver (and hence the GPU; see [Accurately Profiling Direct3D API Calls (Direct3D 9)](accurately-profiling-direct3d-api-calls.md)).</span></span> <span data-ttu-id="5edd3-278">Durante el vaciado del búfer de comandos, una consulta puede pasar al estado señalado.</span><span class="sxs-lookup"><span data-stu-id="5edd3-278">During the command buffer flush, a query may transition to the signaled state.</span></span>

## <a name="example-an-event-query"></a><span data-ttu-id="5edd3-279">Ejemplo: una consulta de evento</span><span class="sxs-lookup"><span data-stu-id="5edd3-279">Example: An Event Query</span></span>

<span data-ttu-id="5edd3-280">Una consulta de evento no admite un evento Begin.</span><span class="sxs-lookup"><span data-stu-id="5edd3-280">An event query does not support a begin event.</span></span>

-   <span data-ttu-id="5edd3-281">Crear la consulta.</span><span class="sxs-lookup"><span data-stu-id="5edd3-281">Create the query.</span></span>
-   <span data-ttu-id="5edd3-282">Emite un evento de finalización.</span><span class="sxs-lookup"><span data-stu-id="5edd3-282">Issue an end event.</span></span>
-   <span data-ttu-id="5edd3-283">Sondear hasta que la GPU esté inactiva.</span><span class="sxs-lookup"><span data-stu-id="5edd3-283">Poll until the GPU is idle.</span></span>
-   <span data-ttu-id="5edd3-284">Emite un evento de finalización.</span><span class="sxs-lookup"><span data-stu-id="5edd3-284">Issue an end event.</span></span>


```
IDirect3DQuery9* pEventQuery = NULL;
m_pD3DDevice->CreateQuery(D3DQUERYTYPE_EVENT, &pEventQuery);

// Add an end marker to the command buffer queue.
pEventQuery->Issue(D3DISSUE_END);

// Empty the command buffer and wait until the GPU is idle.
while(S_FALSE == pEventQuery->GetData( NULL, 0, D3DGETDATA_FLUSH ))
    ;

... // API calls

// Add an end marker to the command buffer queue.
pEventQuery->Issue(D3DISSUE_END);

// Force the driver to execute the commands from the command buffer.
// Empty the command buffer and wait until the GPU is idle.
while(S_FALSE == pEventQuery->GetData( NULL, 0, D3DGETDATA_FLUSH ))
    ;
```



<span data-ttu-id="5edd3-285">Esta es la secuencia de comandos que usa una consulta de eventos para generar perfiles de llamadas de la interfaz de programación de aplicaciones (API) (consulte generación de perfiles de llamadas de la [API de Direct3D (Direct3D 9) con precisión](accurately-profiling-direct3d-api-calls.md).</span><span class="sxs-lookup"><span data-stu-id="5edd3-285">This is the sequence of commands an event query uses to profile application programming interface (API) calls (see [Accurately Profiling Direct3D API Calls (Direct3D 9)](accurately-profiling-direct3d-api-calls.md)).</span></span> <span data-ttu-id="5edd3-286">Esta secuencia usa marcadores para ayudar a controlar la cantidad de trabajo en el búfer de comandos.</span><span class="sxs-lookup"><span data-stu-id="5edd3-286">This sequence uses markers to help control the amount of work in the command buffer.</span></span>

<span data-ttu-id="5edd3-287">Tenga en cuenta que las aplicaciones deben prestar especial atención al gran costo asociado con el vaciado del búfer de comandos, ya que esto hace que el sistema operativo cambie al modo kernel, lo que incurre en una penalización de rendimiento considerable.</span><span class="sxs-lookup"><span data-stu-id="5edd3-287">Note that applications should pay special attention to the large cost associated with flushing the command buffer because this causes the operating system to switch into kernel mode, thus incurring a sizeable performance penalty.</span></span> <span data-ttu-id="5edd3-288">Las aplicaciones también deben tener en cuenta la pérdida de ciclos de CPU al esperar a que se completen las consultas.</span><span class="sxs-lookup"><span data-stu-id="5edd3-288">Applications should also be aware of wasting CPU cycles by waiting for queries to complete.</span></span>

<span data-ttu-id="5edd3-289">Las consultas son una optimización que se va a utilizar durante la representación para aumentar el rendimiento.</span><span class="sxs-lookup"><span data-stu-id="5edd3-289">Queries are an optimization to be used during rendering to increase performance.</span></span> <span data-ttu-id="5edd3-290">Por lo tanto, no es beneficioso dedicar tiempo a esperar a que finalice una consulta.</span><span class="sxs-lookup"><span data-stu-id="5edd3-290">Therefore, it is not beneficial to spend time waiting for a query to finish.</span></span> <span data-ttu-id="5edd3-291">Si se emite una consulta y los resultados aún no están listos en el momento en que la aplicación los comprueba, el intento de optimización no se realizó correctamente y la representación debería continuar de la forma habitual.</span><span class="sxs-lookup"><span data-stu-id="5edd3-291">If a query is issued and if the results are not yet ready by the time the application checks for them, the attempt at optimizing did not succeed and rendering should continue as normal.</span></span>

<span data-ttu-id="5edd3-292">El ejemplo clásico es durante la selección de la oclusión.</span><span class="sxs-lookup"><span data-stu-id="5edd3-292">The classic example of this is during Occlusion Culling.</span></span> <span data-ttu-id="5edd3-293">En lugar del bucle **While** anterior, una aplicación que usa consultas puede implementar la selección de la oclusión para comprobar si una consulta ha finalizado en el momento en que necesita el resultado.</span><span class="sxs-lookup"><span data-stu-id="5edd3-293">Instead of the **while** loop above, an application using queries can implement occlusion culling to check to see if a query had finished by the time it needs the result.</span></span> <span data-ttu-id="5edd3-294">Si la consulta no ha finalizado, continúe (como un escenario en el peor de los casos) como si el objeto que se está probando no es ocluidos (es decir, es visible) y lo representa.</span><span class="sxs-lookup"><span data-stu-id="5edd3-294">If the query has not finished, continue (as a worst-case scenario) as if the object being tested against is not occluded (i.e. it is visible) and render it.</span></span> <span data-ttu-id="5edd3-295">El código tendría un aspecto similar al siguiente.</span><span class="sxs-lookup"><span data-stu-id="5edd3-295">The code would look similar to the following.</span></span>


```
IDirect3DQuery9* pOcclusionQuery = NULL;
m_pD3DDevice->CreateQuery( D3DQUERYTYPE_OCCLUSION, &pOcclusionQuery );

// Add a begin marker to the command buffer queue.
pOcclusionQuery->Issue( D3DISSUE_BEGIN );

... // API calls

// Add an end marker to the command buffer queue.
pOcclusionQuery->Issue( D3DISSUE_END );

// Avoid flushing and letting the CPU go idle by not using a while loop.
// Check if queries are finished:
DWORD dwOccluded = 0;
if( S_FALSE == pOcclusionQuery->GetData( &dwOccluded, sizeof(DWORD), 0 ) )
{
    // Query is not done yet or object not occluded; avoid flushing/wait by continuing with worst-case scenario
    pSomeComplexMesh->Render();
}
else if( dwOccluded != 0 )
{
    // Query is done and object is not occluded.
    pSomeComplexMesh->Render();
}
```



## <a name="related-topics"></a><span data-ttu-id="5edd3-296">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="5edd3-296">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5edd3-297">Temas avanzados</span><span class="sxs-lookup"><span data-stu-id="5edd3-297">Advanced Topics</span></span>](advanced-topics.md)
</dt> </dl>

 

 
