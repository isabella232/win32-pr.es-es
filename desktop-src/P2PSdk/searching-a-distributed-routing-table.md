---
description: Para que una aplicación pueda buscar en la tabla de enrutamiento distribuida (DRT), se debe crear una consulta de búsqueda.
ms.assetid: b3403a64-128c-461e-9384-8e62c03322e1
title: Buscar una tabla de enrutamiento distribuida
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c9977ca395393cef09198182fb8790738d2b00c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668058"
---
# <a name="searching-a-distributed-routing-table"></a>Buscar una tabla de enrutamiento distribuida

Para que una aplicación pueda buscar en la tabla de enrutamiento distribuida (DRT), se debe crear una consulta de búsqueda. La aplicación especifica el valor de clave deseado cuando se llama a la función [**DrtStartSearch**](/windows/desktop/api/drt/nf-drt-drtstartsearch) . El comportamiento de la búsqueda viene determinado por la información especificada por la aplicación en la estructura de [**\_ \_ información de búsqueda de DRT**](/windows/desktop/api/drt/ns-drt-drt_search_info) .

Normalmente, un evento de aplicación se señaliza cuando la búsqueda detecta los resultados y otro al final de la búsqueda. Sin embargo, si se establece **fIterative** en la [**información de \_ búsqueda \_ de DRT**](/windows/desktop/api/drt/ns-drt-drt_search_info), se puede señalar un evento de aplicación cuando se realiza el contacto con cada nodo durante el proceso.

Después de señalar un evento, la aplicación llama a la función [**DrtGetSearchResult**](/windows/desktop/api/drt/nf-drt-drtgetsearchresult) para obtener los resultados. Si el código devuelto **es \_ correcto**, los resultados se señalan en la estructura del resultado de la [**\_ búsqueda \_ de DRT**](/windows/desktop/api/drt/ns-drt-drt_search_result) devuelta por la API. Los resultados devueltos se encuentran en el intervalo de valores especificado en [**\_ \_ información de búsqueda de DRT**](/windows/desktop/api/drt/ns-drt-drt_search_info). En caso de que la búsqueda no encuentre ninguna coincidencia, solo se devolverá el valor de **DRT \_ E \_ no \_ más** al final de las devoluciones de resultados.

La siguiente información detalla cómo los miembros contenidos en [**la \_ \_ información de búsqueda de DRT**](/windows/desktop/api/drt/ns-drt-drt_search_info) permiten a una aplicación dictar específicamente el comportamiento de búsqueda de la infraestructura de DRT:

## <a name="fallowcurrentinstancematch"></a>fAllowCurrentInstanceMatch

De forma predeterminada, los resultados de búsqueda de DRT incluyen solo las coincidencias encontradas fuera del nodo local. Establecer **fAllowCurrentInstanceMatch** especifica que los resultados de la búsqueda también incluyen las coincidencias encontradas en la instancia de DRT local.

## <a name="cmaxendpoints"></a>cMaxEndpoints

La cantidad y el rango de los resultados devueltos por la búsqueda se especifican mediante la aplicación con los valores **cMaxEndpoints** (quantity) y **pMinimumKey** y **pMaximumKey** (Range) y a los que hace referencia la [**información de \_ búsqueda \_ de DRT**](/windows/desktop/api/drt/ns-drt-drt_search_info).

Cuando **cMaxEndpoints = 1**, la infraestructura de DRT busca una clave y devuelve una coincidencia en el intervalo especificado por los valores **pMinimumKey** y **pMaximumKey** de [**la \_ \_ información de búsqueda de DRT**](/windows/desktop/api/drt/ns-drt-drt_search_info). Esta coincidencia puede ser una coincidencia exacta o la coincidencia más cercana dentro del intervalo. Si no se encuentra ninguna coincidencia, se devuelve **DRT \_ E \_ no \_ More** .

Si **cMaxEndpoints > 1**, la infraestructura de DRT devolverá coincidencias en el intervalo hasta el valor de **cMaxEndpoints**. Las coincidencias devueltas pueden contener una coincidencia exacta o los resultados de coincidencia más cercanos dentro del intervalo. Además, si **pMinimumKey** y **pMaximumKey** se establecen en el mismo valor, se realiza una búsqueda solo para ese valor, devolviendo **DRT \_ E \_ no \_ More** si no se encuentra.

## <a name="fanymatchinrange"></a>fAnyMatchInRange

El miembro **fAnyMatchInRange** indica si la búsqueda se detendrá una vez que la primera coincidencia se encuentra dentro del intervalo especificado, o si la búsqueda continuará para la coincidencia más cercana a la clave especificada en la API de [**DrtStartSearch**](/windows/desktop/api/drt/nf-drt-drtstartsearch) . Cuando se establece **fAnyMatchInRange** , la búsqueda se realiza con **cMaxEndpoints = 1** , independientemente del valor de **cMaxEndpoints** especificado en la [**\_ \_ información de búsqueda de DRT**](/windows/desktop/api/drt/ns-drt-drt_search_info).

## <a name="fiterative"></a>fIterative

El miembro **fIterative** especifica si cada nodo que se pone en contacto con la infraestructura de DRT durante la búsqueda tendrá los datos de la clave/extremo asociados a él disponibles para la aplicación a través del resultado de la [**\_ búsqueda \_ de DRT**](/windows/desktop/api/drt/ns-drt-drt_search_result). Si establece **fIterative** en **true**, se forzará el valor de **cMaxEndpoints = 1** . Cuando **fIterative** se establece en **true** en una consulta de búsqueda para DRT, se vuelve a llamar a la aplicación después del contacto con cada nodo o "salto". Cada resultado de salto contiene una clave que indica el nodo que la DRT buscará a continuación. Un resultado de salto se devuelve a través de [**DrtGetSearchResult**](/windows/desktop/api/drt/nf-drt-drtgetsearchresult) como un resultado **intermedio de \_ coincidencia \_ de DRT** .

## <a name="pminimumkey-and-pmaximumkey"></a>pMinimumKey y pMaximumKey

Los miembros **pMinimumKey** y **pMaximumKey** se pueden usar para buscar claves dentro de un intervalo. Si el miembro **fAnyMatchInRange** se establece en **false**, DRT devolverá las claves más próximas al destino de búsqueda (especificado mediante el argumento pKey pasado en la función [**DrtStartSearch**](/windows/desktop/api/drt/nf-drt-drtstartsearch) ) que se encuentran dentro del intervalo. Tenga en cuenta que el argumento *pKey* pasado a **DrtStartSearch** debe estar dentro del intervalo definido por **pMinimumKey** y **pMaximumKey**. Para buscar una clave precisa, establezca **pMinimumKey**, **pMaximumKey** y *pKey* en el mismo valor.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Registrar y anular el registro de claves](registering-and-deregistering-keys.md)
</dt> <dt>

[Acerca de las tablas de enrutamiento distribuido](about-distributed-routing-tables.md)
</dt> <dt>

[Referencia de Table API de enrutamiento distribuido](distributed-routing-table-api-reference.md)
</dt> </dl>

 

 



