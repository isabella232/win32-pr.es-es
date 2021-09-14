---
description: Describe la introducción de la priorización de indexación y los eventos de conjunto de filas para Windows 7.
ms.assetid: 6cdfb7d3-f849-432c-960f-912e5024c583
title: Indexación de eventos de priorización y conjunto de filas en Windows 7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6610500a3c2fcd359f346e5239507fb15ad896d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127363207"
---
# <a name="indexing-prioritization-and-rowset-events-in-windows-7"></a>Indexación de eventos de priorización y conjunto de filas en Windows 7

En este tema se describe la introducción de la priorización de indexación y los eventos de conjunto de filas Windows 7.

Este tema se organiza de la siguiente manera:

-   [Indexación de priorización y eventos de conjunto de filas](#indexing-prioritization-and-rowset-events)
    -   [Ejemplos de IRowsetPriorization](#irowsetpriorization-examples)
    -   [Eventos IRowsetPrioritization](#indexing-prioritization-and-rowset-events-in-windows-7)
-   [Recursos adicionales](#additional-resources)
-   [Temas relacionados](#related-topics)

## <a name="indexing-prioritization-and-rowset-events"></a>Indexación de priorización y eventos de conjunto de filas

En Windows 7? y versiones posteriores, hay una pila de prioridad en la que el contexto de cualquier consulta determinada, el cliente puede solicitar que los ámbitos usados en esa consulta se prioricen por encima del de los elementos normales.

Esta pila de priorización tiene las siguientes características:

-   Los elementos de la pila pueden tener prioridad en primer plano, alta o baja:
    -   **Primer** plano: la lógica de deserción se omite y la indexación continúa tan rápido como permite la máquina.
    -   **Alto:** se ha solicitado la priorización con reprobación.
    -   **Bajo:** se ha solicitado la priorización, no a costa de otros ámbitos de la pila, sino por encima de la indexación sin prioridad.
-   Cualquier solicitud de prioridad alta o en primer plano hace que la consulta solicitante se suba automáticamente a la parte superior de la pila.
-   Solo el elemento de la parte superior de la pila puede tener prioridad de primer plano.
-   Una consulta con prioridad en primer plano que se encuentra en orden de prioridad recibe un evento que le notifica que ha perdido la prioridad de primer plano y que se ha convertido en una prioridad alta con reenviamiento.

La pila de prioridad establece una prioridad general de los elementos que se procesan en el indexador de la siguiente manera:

-   Las notificaciones de prioridad alta no tienen ningún respaldo y normalmente solo se envían para un número reducido de elementos. Por ejemplo, Windows Explorer usa esta prioridad para las operaciones de motor de copia pequeños.
-   Priority Stack es la parte superior de la pila, tiene un reenlazamiento y es la última consulta de prioridad solicitada.
-   Segunda consulta de la pila.
-   Tercera consulta de la pila.
-   Cuarta consulta de la pila, etc.
-   Elementos de prioridad normal.
-   Elementos eliminados.
    > [!Note]  
    > Los elementos dentro de cada grupo se priorizan internamente a través de la semántica anterior por elemento.

     

### <a name="irowsetpriorization-examples"></a>Ejemplos de IRowsetPriorization

La API principal para el trabajo de priorización está disponible a través de la siguiente interfaz, a la que se puede llamar consultando el conjunto de filas devuelto:


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



La priorización de conjuntos de filas funciona de la siguiente manera:

1.  [**IRowsetPrioritization**](/windows/desktop/api/Searchapi/nn-searchapi-irowsetprioritization) se adquiere con [el método IUnknown::QueryInterface en](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) un conjunto de filas de indexador. **DBPROP \_ ENABLEROWSETEVENTS** debe establecerse en **TRUE** con OLE DB [método ICommandProperties::SetProperties](/previous-versions/windows/desktop/ms711497(v=vs.85)) antes de ejecutar la consulta para usar la priorización de conjuntos de filas.
2.  [**IRowsetPrioritization::SetScopePriority**](/windows/desktop/api/Searchapi/nf-searchapi-irowsetprioritization-setscopepriority) establece la priorización de los ámbitos que pertenecen a la consulta y el intervalo en el que se genera el evento de estadísticas de ámbito cuando hay documentos pendientes que se van a indexar dentro de los ámbitos de consulta. Este evento se genera si el nivel de prioridad está establecido en el valor predeterminado.
3.  [**IRowsetPrioritization::GetScopeStatistics**](/windows/desktop/api/Searchapi/nf-searchapi-irowsetprioritization-getscopestatistics) se puede usar para obtener el número de elementos indexados en el ámbito, el número de documentos pendientes que se van a agregar en el ámbito y el número de documentos que se deben volver a indexar dentro de este ámbito.

### <a name="irowsetprioritization-events"></a>Eventos IRowsetPrioritization

Hay tres eventos de conjunto de filas [**en IRowsetEvents::OnRowsetEvent en**](/windows/desktop/api/Searchapi/nf-searchapi-irowsetevents-onrowsetevent) la [**enumeración ROWSETEVENT \_ TYPE:**](/windows/win32/api/searchapi/ne-searchapi-rowsetevent_type)


```
    // This method allows for future notifications of various actions about your rowset or items within
    // eventType:                               - An identifier of the particular event being sent
    // pVarEventData:                           - The expected value of the EventData for each event type
    //      ROWSETEVENT_TYPE_DATAEXPIRED        - VT_EMPTY
    //      ROWSETEVENT_TYPE_FOREGROUNDLOST     - VT_EMPTY
    //      ROWSETEVENT_TYPE_SCOPESTATISTICS    - VT_VECTOR | VT_UI4 - 3 elements (0 = indexed items, 1 = outstanding adds, 2 = oustanding modifies)

    HRESULT OnRowsetEvent( [in] ROWSETEVENT_TYPE eventType, [in] REFPROPVARIANT eventData );
```



Los eventos de conjunto de filas son los siguientes:

-   El **evento ROWSETEVENT \_ TYPE \_ DATAEXPIRED** indica que los datos que copian el conjunto de filas han expirado y que se debe solicitar un nuevo conjunto de filas.
-   El evento **ROWSET \_ TYPE \_ FOREGROUNDLOST** indica que se ha degradado un elemento que tenía prioridad de primer plano en la pila de priorización, porque otra persona se priorizó por delante de esta consulta.
-   El evento **ROWSETEVENT \_ TYPE \_ SCOPESTATISTICS** proporciona la misma información disponible en la llamada al método [**IRowsetPrioritization::GetScopeStatistics,**](/windows/desktop/api/Searchapi/nf-searchapi-irowsetprioritization-getscopestatistics) pero a través de una mecánica de inserción, como se muestra a continuación:
    -   El evento surge si se ha usado la API de priorización para solicitar un nivel de priorización no predeterminado y una frecuencia de eventos de estadísticas distinto de cero.
    -   El evento solo se produce cuando las estadísticas cambian realmente y el intervalo especificado en [**IRowsetPrioritization**](/windows/desktop/api/Searchapi/nn-searchapi-irowsetprioritization) ha transcurrido (el intervalo no garantiza la frecuencia del evento).
    -   Se garantiza que este evento genera un estado "bounce zero" (cero elementos que quedan por agregar, cero modifica el resto), siempre que se haya producido un evento distinto de cero.
    -   El indexador puede procesar elementos sin enviar este evento, si la cola se vacía antes de la frecuencia de eventos de estadísticas.

## <a name="additional-resources"></a>Recursos adicionales

Consulte los siguientes recursos relacionados con la priorización y los conjuntos de filas:

-   Interfaces:
    -   [**IRowsetEvents**](/windows/desktop/api/Searchapi/nn-searchapi-irowsetevents)
    -   [**IRowsetPrioritization**](/windows/desktop/api/Searchapi/nn-searchapi-irowsetprioritization)
-   Enumeraciones:
    -   [**PRIORIZAR \_ MARCAS**](/windows/win32/api/searchapi/ne-searchapi-tagprioritize_flags)
    -   [**NIVEL DE \_ PRIORIDAD**](/windows/win32/api/searchapi/ne-searchapi-priority_level)
    -   [**ROWSETEVENT \_ ITEMSTATE**](/windows/win32/api/searchapi/ne-searchapi-rowsetevent_itemstate)
    -   [**TIPO \_ ROWSETEVENT**](/windows/win32/api/searchapi/ne-searchapi-rowsetevent_type)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Windows 7 Search](./-search-3x-wds-overview.md)
</dt> <dt>

[Novedades de Windows 7 Search](new-for-windows-7-search.md)
</dt> <dt>

[Windows Bibliotecas de shell en Windows 7](-search-win7-development-scenarios.md)
</dt> </dl>

 

 