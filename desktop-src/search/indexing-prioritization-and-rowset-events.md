---
description: Describe la introducción de la priorización de indización y los eventos de conjunto de filas para Windows 7.
ms.assetid: 6cdfb7d3-f849-432c-960f-912e5024c583
title: Indexación de los eventos de priorización y de conjunto de filas en Windows 7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6610500a3c2fcd359f346e5239507fb15ad896d
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "105678617"
---
# <a name="indexing-prioritization-and-rowset-events-in-windows-7"></a><span data-ttu-id="2c59d-103">Indexación de los eventos de priorización y de conjunto de filas en Windows 7</span><span class="sxs-lookup"><span data-stu-id="2c59d-103">Indexing Prioritization and Rowset Events in Windows 7</span></span>

<span data-ttu-id="2c59d-104">En este tema se describe la introducción de la priorización de indización y los eventos de conjunto de filas para Windows 7.</span><span class="sxs-lookup"><span data-stu-id="2c59d-104">This topic outlines the introduction of indexing prioritization and rowset events for Windows 7.</span></span>

<span data-ttu-id="2c59d-105">Este tema se organiza de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="2c59d-105">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="2c59d-106">Indexación de los eventos de priorización y de conjunto de filas</span><span class="sxs-lookup"><span data-stu-id="2c59d-106">Indexing Prioritization and Rowset Events</span></span>](#indexing-prioritization-and-rowset-events)
    -   [<span data-ttu-id="2c59d-107">Ejemplos de IRowsetPriorization</span><span class="sxs-lookup"><span data-stu-id="2c59d-107">IRowsetPriorization Examples</span></span>](#irowsetpriorization-examples)
    -   [<span data-ttu-id="2c59d-108">Eventos IRowsetPrioritization</span><span class="sxs-lookup"><span data-stu-id="2c59d-108">IRowsetPrioritization Events</span></span>](#indexing-prioritization-and-rowset-events-in-windows-7)
-   [<span data-ttu-id="2c59d-109">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="2c59d-109">Additional Resources</span></span>](#additional-resources)
-   [<span data-ttu-id="2c59d-110">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="2c59d-110">Related topics</span></span>](#related-topics)

## <a name="indexing-prioritization-and-rowset-events"></a><span data-ttu-id="2c59d-111">Indexación de los eventos de priorización y de conjunto de filas</span><span class="sxs-lookup"><span data-stu-id="2c59d-111">Indexing Prioritization and Rowset Events</span></span>

<span data-ttu-id="2c59d-112">En Windows 7? y versiones posteriores, hay una pila de prioridades dentro de la cual el contexto de una consulta determinada, el cliente puede solicitar que los ámbitos utilizados en esa consulta tengan prioridad sobre los elementos normales.</span><span class="sxs-lookup"><span data-stu-id="2c59d-112">In Windows 7?and later, there is a priority stack within which the context of any particular query, the client can request that the scopes used in that query be prioritized above that of normal items.</span></span>

<span data-ttu-id="2c59d-113">Esta pila de priorización tiene las siguientes características:</span><span class="sxs-lookup"><span data-stu-id="2c59d-113">This prioritization stack has the following characteristics:</span></span>

-   <span data-ttu-id="2c59d-114">Los elementos de la pila pueden tener una prioridad de primer plano, alta o baja:</span><span class="sxs-lookup"><span data-stu-id="2c59d-114">Items in the stack can have foreground, high, or low priority:</span></span>
    -   <span data-ttu-id="2c59d-115">**Foreground**: la lógica de retroceso se omite y la indexación continúa con la velocidad que permite el equipo.</span><span class="sxs-lookup"><span data-stu-id="2c59d-115">**Foreground**: Backoff logic is skipped and indexing proceeds as fast as the machine allows.</span></span>
    -   <span data-ttu-id="2c59d-116">**Alto**: se ha solicitado la priorización con el retroceso.</span><span class="sxs-lookup"><span data-stu-id="2c59d-116">**High**: Prioritization has been requested with backoff.</span></span>
    -   <span data-ttu-id="2c59d-117">**Bajo**: se ha solicitado la priorización, no a costa de otros ámbitos de la pila, sino por encima de la indización sin prioridad.</span><span class="sxs-lookup"><span data-stu-id="2c59d-117">**Low**: Prioritization has been requested, not at the expense of other scopes on the stack, but above non-prioritized indexing.</span></span>
-   <span data-ttu-id="2c59d-118">Las solicitudes de prioridad alta o de primer plano sobrepasan la consulta que se solicita a la parte superior de la pila automáticamente.</span><span class="sxs-lookup"><span data-stu-id="2c59d-118">Any request for high or foreground priority bumps the requesting query to the top of the stack automatically.</span></span>
-   <span data-ttu-id="2c59d-119">Solo el elemento de la parte superior de la pila puede tener prioridad de primer plano.</span><span class="sxs-lookup"><span data-stu-id="2c59d-119">Only the item on top of the stack can have foreground priority.</span></span>
-   <span data-ttu-id="2c59d-120">Una consulta con prioridad de primer plano desplazada por prioridad recibe un evento que le informa de que ha perdido la prioridad de primer plano y se ha convertido en una prioridad alta con el retroceso.</span><span class="sxs-lookup"><span data-stu-id="2c59d-120">A query with foreground priority that is bumped down in priority receives an event notifying it that it has lost foreground priority and has become a high priority with backoff.</span></span>

<span data-ttu-id="2c59d-121">La pila de prioridades establece una prioridad general de los elementos que se procesan en el indexador de la manera siguiente:</span><span class="sxs-lookup"><span data-stu-id="2c59d-121">The priority stack sets an overall priority of items that are processed in the indexer as follows:</span></span>

-   <span data-ttu-id="2c59d-122">Las notificaciones de prioridad alta no tienen ningún retroceso y normalmente se envían solo para un número reducido de elementos.</span><span class="sxs-lookup"><span data-stu-id="2c59d-122">High Priority notifications have no backoff, and are typically sent only for a small number of items.</span></span> <span data-ttu-id="2c59d-123">Por ejemplo, el explorador de Windows usa esta prioridad para las operaciones de motor de copia pequeño.</span><span class="sxs-lookup"><span data-stu-id="2c59d-123">For example, Windows Explorer uses this priority for small copy engine operations.</span></span>
-   <span data-ttu-id="2c59d-124">La pila de prioridades es la parte superior de la pila, tiene retroceso y es la última consulta de prioridad solicitada.</span><span class="sxs-lookup"><span data-stu-id="2c59d-124">Priority Stack is top of the stack, has backoff, and is the last requested priority query.</span></span>
-   <span data-ttu-id="2c59d-125">Segunda consulta de la pila.</span><span class="sxs-lookup"><span data-stu-id="2c59d-125">Second query in the stack.</span></span>
-   <span data-ttu-id="2c59d-126">Tercera consulta de la pila.</span><span class="sxs-lookup"><span data-stu-id="2c59d-126">Third query in the stack.</span></span>
-   <span data-ttu-id="2c59d-127">Cuarta consulta de la pila, etc.</span><span class="sxs-lookup"><span data-stu-id="2c59d-127">Fourth query in the stack, and so forth.</span></span>
-   <span data-ttu-id="2c59d-128">Elementos de prioridad normal.</span><span class="sxs-lookup"><span data-stu-id="2c59d-128">Normal Priority items.</span></span>
-   <span data-ttu-id="2c59d-129">Elementos eliminados.</span><span class="sxs-lookup"><span data-stu-id="2c59d-129">Deleted items.</span></span>
    > [!Note]  
    > <span data-ttu-id="2c59d-130">Los elementos de cada grupo se priorizan internamente a través de la semántica de cada elemento más antigua.</span><span class="sxs-lookup"><span data-stu-id="2c59d-130">Items within each group are prioritized internally through the older per-item semantics.</span></span>

     

### <a name="irowsetpriorization-examples"></a><span data-ttu-id="2c59d-131">Ejemplos de IRowsetPriorization</span><span class="sxs-lookup"><span data-stu-id="2c59d-131">IRowsetPriorization Examples</span></span>

<span data-ttu-id="2c59d-132">La API principal para el trabajo de priorización está disponible a través de la interfaz siguiente, a la que se puede llamar consultando el conjunto de filas devuelto:</span><span class="sxs-lookup"><span data-stu-id="2c59d-132">The primary API for prioritization work is available through the following interface, which can be called by querying the returned rowset:</span></span>


```
typedef [v1_enum] enum
{
    PRIORITY_LEVEL_FOREGROUND           = 0,    // process items in the scope first as quickly as possible
    PRIORITY_LEVEL_HIGH                 = 1,    // process items in the scope first at the normal rate
    PRIORITY_LEVEL_LOW                  = 2,    // process items in this scope before those at the normal rate, but after any other prioritization requests
    PRIORITY_LEVEL_DEFAULT              = 3     // process items at the normal indexer rate
} PRIORITY_LEVEL;


[
    object,
    uuid(IRowsetPrioritization_GUID),
    pointer_default(unique)
]
interface IRowsetPrioritization : IUnknown
{
    // Sets or retrieves the current indexer prioritization level for the scope specified by
    // this query.

    HRESULT SetScopePriority( [in] PRIORITY_LEVEL priority, [in] DWORD scopeStatisticsEventFrequency );
    HRESULT GetScopePriority( [out] PRIORITY_LEVEL * priority, [out] DWORD * scopeStatisticsEventFrequency );

    // Gets information describing the scope specified by this query:
    // indexedDocumentCount     -   The total number of documents currently indexed in the scope
    // oustandingAddCount       -   The total number of documents yet to be indexed in the scope (those not yet included in indexedDocumentCount)
    // oustandingModifyCount    -   The total number of documents indexed in the scope that need to be re-indexed (included in indexedDocumentCount)
    
    HRESULT GetScopeStatistics( [out] DWORD * indexedDocumentCount, [out] DWORD * oustandingAddCount, [out] DWORD * oustandingModifyCount );
};
```



<span data-ttu-id="2c59d-133">La priorización del conjunto de filas funciona de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="2c59d-133">Rowset prioritization works as follows:</span></span>

1.  <span data-ttu-id="2c59d-134">[**IRowsetPrioritization**](/windows/desktop/api/Searchapi/nn-searchapi-irowsetprioritization) se adquiere con el [método IUnknown:: QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) en un conjunto de filas de indexador.</span><span class="sxs-lookup"><span data-stu-id="2c59d-134">[**IRowsetPrioritization**](/windows/desktop/api/Searchapi/nn-searchapi-irowsetprioritization) is acquired with [IUnknown::QueryInterface Method](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) on an indexer rowset.</span></span> <span data-ttu-id="2c59d-135">**DBPROP \_ ENABLEROWSETEVENTS** debe establecerse en **true** con el método [ICommandProperties:: SetProperties](/previous-versions/windows/desktop/ms711497(v=vs.85)) de OLE DB antes de ejecutar la consulta para poder usar la priorización del conjunto de filas.</span><span class="sxs-lookup"><span data-stu-id="2c59d-135">**DBPROP\_ENABLEROWSETEVENTS** must be set to **TRUE** with the OLE DB [ICommandProperties::SetProperties](/previous-versions/windows/desktop/ms711497(v=vs.85)) method prior to executing the query in order to use rowset prioritization.</span></span>
2.  <span data-ttu-id="2c59d-136">[**IRowsetPrioritization:: SetScopePriority**](/windows/desktop/api/Searchapi/nf-searchapi-irowsetprioritization-setscopepriority) establece la priorización para los ámbitos que pertenecen a la consulta y el intervalo durante el que se generan los eventos de estadísticas de ámbito cuando hay documentos pendientes que se van a indizar en los ámbitos de la consulta.</span><span class="sxs-lookup"><span data-stu-id="2c59d-136">[**IRowsetPrioritization::SetScopePriority**](/windows/desktop/api/Searchapi/nf-searchapi-irowsetprioritization-setscopepriority) sets the prioritization for the scopes belonging to the query, and the interval the scope statistics event is raised when there are outstanding documents to be indexed within the query scopes.</span></span> <span data-ttu-id="2c59d-137">Este evento se desencadena si el nivel de prioridad se establece en el valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="2c59d-137">This event is raised if the priority level is set to default.</span></span>
3.  <span data-ttu-id="2c59d-138">[**IRowsetPrioritization:: GetScopeStatistics**](/windows/desktop/api/Searchapi/nf-searchapi-irowsetprioritization-getscopestatistics) se puede usar para obtener el número de elementos indizados en el ámbito, el número de documentos pendientes que se van a agregar en el ámbito y el número de documentos que se deben volver a indizar dentro de este ámbito.</span><span class="sxs-lookup"><span data-stu-id="2c59d-138">[**IRowsetPrioritization::GetScopeStatistics**](/windows/desktop/api/Searchapi/nf-searchapi-irowsetprioritization-getscopestatistics) can be used to get the number of indexed items in the scope, the number of outstanding documents to be added in the scope, and the number of documents that need to be re-indexed within this scope.</span></span>

### <a name="irowsetprioritization-events"></a><span data-ttu-id="2c59d-139">Eventos IRowsetPrioritization</span><span class="sxs-lookup"><span data-stu-id="2c59d-139">IRowsetPrioritization Events</span></span>

<span data-ttu-id="2c59d-140">Hay tres eventos de conjunto de filas en [**IRowsetEvents:: OnRowsetEvent**](/windows/desktop/api/Searchapi/nf-searchapi-irowsetevents-onrowsetevent) en la enumeración de [**\_ tipos ROWSETEVENT**](/windows/win32/api/searchapi/ne-searchapi-rowsetevent_type) :</span><span class="sxs-lookup"><span data-stu-id="2c59d-140">There are three rowset events in [**IRowsetEvents::OnRowsetEvent**](/windows/desktop/api/Searchapi/nf-searchapi-irowsetevents-onrowsetevent) in the [**ROWSETEVENT\_TYPE**](/windows/win32/api/searchapi/ne-searchapi-rowsetevent_type) enumeration:</span></span>


```
    // This method allows for future notifications of various actions about your rowset or items within
    // eventType:                               - An identifier of the particular event being sent
    // pVarEventData:                           - The expected value of the EventData for each event type
    //      ROWSETEVENT_TYPE_DATAEXPIRED        - VT_EMPTY
    //      ROWSETEVENT_TYPE_FOREGROUNDLOST     - VT_EMPTY
    //      ROWSETEVENT_TYPE_SCOPESTATISTICS    - VT_VECTOR | VT_UI4 - 3 elements (0 = indexed items, 1 = outstanding adds, 2 = oustanding modifies)

    HRESULT OnRowsetEvent( [in] ROWSETEVENT_TYPE eventType, [in] REFPROPVARIANT eventData );
```



<span data-ttu-id="2c59d-141">Los eventos de conjunto de filas son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="2c59d-141">The rowset events are as follows:</span></span>

-   <span data-ttu-id="2c59d-142">El evento **ROWSETEVENT \_ Type \_ Expired** indica que los datos que respaldan el conjunto de filas han expirado y que se debe solicitar un nuevo conjunto de filas.</span><span class="sxs-lookup"><span data-stu-id="2c59d-142">The **ROWSETEVENT\_TYPE\_DATAEXPIRED** event indicates that data backing the rowset has expired, and that a new rowset should be requested.</span></span>
-   <span data-ttu-id="2c59d-143">El **evento \_ \_ FOREGROUNDLOST del tipo de conjunto de filas** indica que se ha degradado un elemento que tenía prioridad de primer plano en la pila de priorización, ya que otra persona prioriza por sí misma antes de esta consulta.</span><span class="sxs-lookup"><span data-stu-id="2c59d-143">The **ROWSET\_TYPE\_FOREGROUNDLOST** event indicates that an item that did have foreground priority in the prioritization stack has been demoted, because someone else prioritized themselves ahead of this query.</span></span>
-   <span data-ttu-id="2c59d-144">El evento **ROWSETEVENT \_ Type \_ SCOPESTATISTICS** proporciona la misma información disponible desde la llamada al método [**IRowsetPrioritization:: GetScopeStatistics**](/windows/desktop/api/Searchapi/nf-searchapi-irowsetprioritization-getscopestatistics) , pero a través de un mecánico de extracción, como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="2c59d-144">The **ROWSETEVENT\_TYPE\_SCOPESTATISTICS** event gives you the same information available from the [**IRowsetPrioritization::GetScopeStatistics**](/windows/desktop/api/Searchapi/nf-searchapi-irowsetprioritization-getscopestatistics) method call, but through a push mechanic, as follows:</span></span>
    -   <span data-ttu-id="2c59d-145">El evento se produce si la API de priorización se ha usado para solicitar un nivel de priorización no predeterminado y una frecuencia de eventos de estadísticas que no son cero.</span><span class="sxs-lookup"><span data-stu-id="2c59d-145">The event arises if the prioritization API has been used to request a non-default prioritization level, and a non-zero statistics event frequency.</span></span>
    -   <span data-ttu-id="2c59d-146">El evento solo se produce cuando las estadísticas cambian realmente y el intervalo especificado en [**IRowsetPrioritization**](/windows/desktop/api/Searchapi/nn-searchapi-irowsetprioritization) ha transcurrido (el intervalo no garantiza la frecuencia del evento).</span><span class="sxs-lookup"><span data-stu-id="2c59d-146">The event arises only when statistics actually change, and the interval specified in the [**IRowsetPrioritization**](/windows/desktop/api/Searchapi/nn-searchapi-irowsetprioritization) has elapsed (the interval does not guarantee the frequency of the event).</span></span>
    -   <span data-ttu-id="2c59d-147">Se garantiza que este evento genera un estado "rebote cero" (no quedan elementos que se agreguen, cero modificaciones restantes), siempre que se haya producido un evento distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="2c59d-147">This event is guaranteed to raise a "bounce zero" state (zero items remaining to be added, zero modifies remaining), provided that a non-zero event has been raised.</span></span>
    -   <span data-ttu-id="2c59d-148">El indizador puede procesar elementos sin enviar este evento, si la cola se vacía antes de la frecuencia de eventos de estadísticas.</span><span class="sxs-lookup"><span data-stu-id="2c59d-148">The indexer may process items without sending this event, if the queue empties before the statistics event frequency.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2c59d-149">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="2c59d-149">Additional Resources</span></span>

<span data-ttu-id="2c59d-150">Vea los siguientes recursos relacionados con la priorización y los conjuntos de filas:</span><span class="sxs-lookup"><span data-stu-id="2c59d-150">See the following resources related to prioritization and rowsets:</span></span>

-   <span data-ttu-id="2c59d-151">Interfaces:</span><span class="sxs-lookup"><span data-stu-id="2c59d-151">Interfaces:</span></span>
    -   [<span data-ttu-id="2c59d-152">**IRowsetEvents**</span><span class="sxs-lookup"><span data-stu-id="2c59d-152">**IRowsetEvents**</span></span>](/windows/desktop/api/Searchapi/nn-searchapi-irowsetevents)
    -   [<span data-ttu-id="2c59d-153">**IRowsetPrioritization**</span><span class="sxs-lookup"><span data-stu-id="2c59d-153">**IRowsetPrioritization**</span></span>](/windows/desktop/api/Searchapi/nn-searchapi-irowsetprioritization)
-   <span data-ttu-id="2c59d-154">Enumeraciones:</span><span class="sxs-lookup"><span data-stu-id="2c59d-154">Enumerations:</span></span>
    -   [<span data-ttu-id="2c59d-155">**PRIORIZAr \_ marcas**</span><span class="sxs-lookup"><span data-stu-id="2c59d-155">**PRIORITIZE\_FLAGS**</span></span>](/windows/win32/api/searchapi/ne-searchapi-tagprioritize_flags)
    -   [<span data-ttu-id="2c59d-156">**nivel de prioridad \_**</span><span class="sxs-lookup"><span data-stu-id="2c59d-156">**PRIORITY\_LEVEL**</span></span>](/windows/win32/api/searchapi/ne-searchapi-priority_level)
    -   [<span data-ttu-id="2c59d-157">**ROWSETEVENT \_ ITEMSTATE**</span><span class="sxs-lookup"><span data-stu-id="2c59d-157">**ROWSETEVENT\_ITEMSTATE**</span></span>](/windows/win32/api/searchapi/ne-searchapi-rowsetevent_itemstate)
    -   [<span data-ttu-id="2c59d-158">**\_tipo ROWSETEVENT**</span><span class="sxs-lookup"><span data-stu-id="2c59d-158">**ROWSETEVENT\_TYPE**</span></span>](/windows/win32/api/searchapi/ne-searchapi-rowsetevent_type)

## <a name="related-topics"></a><span data-ttu-id="2c59d-159">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="2c59d-159">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2c59d-160">Búsqueda de Windows 7</span><span class="sxs-lookup"><span data-stu-id="2c59d-160">Windows 7 Search</span></span>](./-search-3x-wds-overview.md)
</dt> <dt>

[<span data-ttu-id="2c59d-161">Novedades de Windows 7 Search</span><span class="sxs-lookup"><span data-stu-id="2c59d-161">New for Windows 7 Search</span></span>](new-for-windows-7-search.md)
</dt> <dt>

[<span data-ttu-id="2c59d-162">Bibliotecas de Shell de Windows en Windows 7</span><span class="sxs-lookup"><span data-stu-id="2c59d-162">Windows Shell Libraries in Windows 7</span></span>](-search-win7-development-scenarios.md)
</dt> </dl>

 

 