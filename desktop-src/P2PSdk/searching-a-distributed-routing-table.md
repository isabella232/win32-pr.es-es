---
description: Para que una aplicación pueda buscar en la tabla de enrutamiento distribuido (DRT), se debe crear una consulta de búsqueda.
ms.assetid: b3403a64-128c-461e-9384-8e62c03322e1
title: Búsqueda de una tabla de enrutamiento distribuido
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c9977ca395393cef09198182fb8790738d2b00c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127473660"
---
# <a name="searching-a-distributed-routing-table"></a>Búsqueda de una tabla de enrutamiento distribuido

Para que una aplicación pueda buscar en la tabla de enrutamiento distribuido (DRT), se debe crear una consulta de búsqueda. La aplicación especifica el valor de clave deseado cuando se llama a la función [**DrtStartSearch.**](/windows/desktop/api/drt/nf-drt-drtstartsearch) El comportamiento de la búsqueda viene determinado por la información especificada por la aplicación en la [**estructura DRT \_ SEARCH \_ INFO.**](/windows/desktop/api/drt/ns-drt-drt_search_info)

Normalmente, se señala un evento de aplicación cuando la búsqueda detecta resultados y otro al finalizar la búsqueda. Sin embargo, si **fIterative** se establece en [**DRT \_ SEARCH \_ INFO,**](/windows/desktop/api/drt/ns-drt-drt_search_info)se puede señalar un evento de aplicación cuando se realiza un contacto con cada nodo a lo largo del proceso.

Una vez señalado un evento, la aplicación llama a la [**función DrtGetSearchResult**](/windows/desktop/api/drt/nf-drt-drtgetsearchresult) para obtener los resultados. Si el código devuelto es **S \_ OK**, los resultados se apuntan a en la estructura [**DRT \_ SEARCH \_ RESULT**](/windows/desktop/api/drt/ns-drt-drt_search_result) devuelta por la API. Los resultados devueltos entran en el intervalo de valores especificado en [**DRT \_ SEARCH \_ INFO**](/windows/desktop/api/drt/ns-drt-drt_search_info). En caso de que la búsqueda no encuentre ninguna coincidencia, solo se devolverá el valor **DRT \_ E NO \_ \_ MORE** al finalizar la devolución del resultado.

La siguiente información detalla cómo los miembros contenidos en [**DRT \_ SEARCH \_ INFO**](/windows/desktop/api/drt/ns-drt-drt_search_info) permiten a una aplicación dictar específicamente el comportamiento de búsqueda de la infraestructura de DRT:

## <a name="fallowcurrentinstancematch"></a>fAllowCurrentInstanceMatch

De forma predeterminada, los resultados de la búsqueda de DRT incluyen solo las coincidencias encontradas fuera del nodo local. Al **establecer fAllowCurrentInstanceMatch,** se especifica que los resultados de la búsqueda también incluyen coincidencias encontradas en la instancia de DRT local.

## <a name="cmaxendpoints"></a>cMaxEndpoints

La aplicación especifica la cantidad y el intervalo de los resultados devueltos por la búsqueda con los valores **cMaxEndpoints** (quantity) y **pMinimumKey** y **pMaximumKey** (range) y se hace referencia a ellos mediante [**DRT \_ SEARCH \_ INFO.**](/windows/desktop/api/drt/ns-drt-drt_search_info)

Cuando **cMaxEndpoints = 1**, la infraestructura de DRT busca una clave y devuelve una coincidencia dentro del intervalo especificado por los valores **pMinimumKey** y **pMaximumKey** en [**DRT \_ SEARCH \_ INFO**](/windows/desktop/api/drt/ns-drt-drt_search_info). Esta coincidencia puede ser una coincidencia exacta o la coincidencia más cercana dentro del intervalo. Si no se encuentra una coincidencia, **se devuelve DRT \_ E NO \_ \_ MORE.**

Si **cMaxEndpoints > 1**, la infraestructura de DRT devolverá coincidencias dentro del intervalo hasta el valor de **cMaxEndpoints**. Las coincidencias devueltas pueden contener una coincidencia exacta o los resultados de coincidencia más cercanos dentro del intervalo. Además, si **pMinimumKey** y **pMaximumKey** se establecen en el mismo valor, se realiza una búsqueda solo para ese valor, devolviendo **DRT \_ E NO \_ \_ MORE** si no se encuentra.

## <a name="fanymatchinrange"></a>fAnyMatchInRange

El **miembro fAnyMatchInRange** indica si la búsqueda se detendrá después de que la primera coincidencia se encuentra dentro del intervalo especificado, o si la búsqueda continuará para la coincidencia más cercana a la clave especificada en la API [**DrtStartSearch.**](/windows/desktop/api/drt/nf-drt-drtstartsearch) Cuando se establece **fAnyMatchInRange,** la búsqueda se lleva a cabo con **cMaxEndpoints = 1 independientemente** del valor especificado de **cMaxEndpoints** en [**DRT \_ SEARCH \_ INFO**](/windows/desktop/api/drt/ns-drt-drt_search_info).

## <a name="fiterative"></a>fIterative

El **miembro fIterative** especifica si cada nodo contactado por la infraestructura de DRT durante la búsqueda tendrá los datos de clave o punto de conexión asociados a él puestos a disposición de la aplicación a través de [**DRT SEARCH \_ \_ RESULT**](/windows/desktop/api/drt/ns-drt-drt_search_result). Al establecer **fIterative** en **TRUE**, se forzará el valor de **cMaxEndpoints = 1.** Cuando **fIterative se** establece en **TRUE dentro** de una consulta de búsqueda para drt, se llama a la aplicación después de ponerse en contacto con cada nodo o "salto". Cada resultado de salto contiene una clave que indica qué nodo buscará el DRT a continuación. Un resultado de salto se devuelve a [**través de DrtGetSearchResult como**](/windows/desktop/api/drt/nf-drt-drtgetsearchresult) resultado DE COINCIDENCIA INTERMEDIA **\_ \_ de DRT.**

## <a name="pminimumkey-and-pmaximumkey"></a>pMinimumKey y pMaximumKey

Los **miembros pMinimumKey** y **pMaximumKey** se pueden usar para buscar claves que se encuentran dentro de un intervalo. Si el miembro **fAnyMatchInRange** se establece en **FALSE,** el DRT devolverá las claves más cercanas al destino de búsqueda (especificado mediante el argumento pKey pasado en la función [**DrtStartSearch)**](/windows/desktop/api/drt/nf-drt-drtstartsearch) dentro del intervalo. Tenga en cuenta que el *argumento pKey* pasado a **DrtStartSearch** debe estar dentro del intervalo definido por **pMinimumKey** y **pMaximumKey.** Para buscar una clave precisa, establezca **pMinimumKey**, **pMaximumKey** y *pKey* en el mismo valor.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Registro y anulación del registro de claves](registering-and-deregistering-keys.md)
</dt> <dt>

[Acerca de las tablas de enrutamiento distribuido](about-distributed-routing-tables.md)
</dt> <dt>

[Referencia de Table API enrutamiento distribuido](distributed-routing-table-api-reference.md)
</dt> </dl>

 

 



