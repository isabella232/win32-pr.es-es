---
title: Recuperar información
description: RTMv2 permite a un cliente recuperar la información a la que hace referencia un identificador determinado mediante las funciones RtmGetEntityInfo, RtmGetDestInfo, RtmGetRouteInfo y RtmGetNextHopInfo.
ms.assetid: a3fc2020-eac4-40a1-9a6e-6eaa2bcc582c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51958fccc8a07e8846705945d9210f4259dfd89b1e3cefccd65d57dd0f033757
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120028025"
---
# <a name="retrieving-information"></a>Recuperar información

RTMv2 permite a un cliente recuperar la información a la que hace referencia un identificador determinado mediante las funciones [**RtmGetEntityInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetentityinfo), [**RtmGetDestInfo,**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetdestinfo) [**RtmGetRouteInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetrouteinfo)y [**RtmGetNextHopInfo.**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetnexthopinfo)

Estas llamadas de función tienen las funciones correspondientes ([**RtmReleaseEntityInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleaseentityinfo), [**RtmReleaseDestInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleasedestinfo), [**RtmReleaseRouteInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleaserouteinfo), [**RtmReleaseNextHopInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleasenexthopinfo)) para liberar los identificadores asociados a la estructura de información devuelta por el administrador de tablas de enrutamiento.

> [!Note]  
> La información de los clientes solo está disponible en la familia de direcciones y la instancia actual.

 

Para obtener código de ejemplo que muestra cómo usar estas funciones, vea [Buscar la mejor ruta.](search-for-the-best-route.md)

## <a name="using-rtmgetexactmatchroute-and-rtmgetexactmatchdestination"></a>Uso de RtmGetExactMatchRoute y RtmGetExactMatchDestination

Los clientes usan las funciones [**RtmGetExactMatchRoute**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetexactmatchroute) y [**RtmGetExactMatchDestination**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetexactmatchdestination) para buscar una ruta o un destino específicos. Estas funciones ahorran tiempo realizando el trabajo de comparación para el cliente.

Por ejemplo, cuando RIP actualiza una ruta, RIP debe conservar la información de métrica antigua. RIP busca la ruta y su información. A continuación, RIP puede copiar la información y actualizar la ruta.

## <a name="using-rtmgetmostspecificdestination"></a>Usar RtmGetMostSpecificDestination

La [**función RtmGetMostSpecificDestination**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetmostspecificdestination) se usa para buscar el destino que mejor coincida con el prefijo de red especificado.

Por ejemplo, el administrador de grupos de multidifusión usa esta función para realizar una comprobación de reenvío de ruta de acceso inversa (RPF) en una sola dirección. La función también se puede usar para buscar el próximo salto local para un próximo salto remoto determinado.

Para obtener código de ejemplo que muestra cómo usar estas funciones, vea [Buscar rutas](search-for-routes-using-rtmgetmostspecificdestination-and-rtmgetlessspecificdestination.md) mediante un árbol de prefijos y [Buscar la mejor ruta.](search-for-the-best-route.md)

## <a name="using-rtmgetlessspecificdestination"></a>Uso de RtmGetLessSpecificDestination

La [**función RtmGetLessSpecificDestination**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetlessspecificdestination) se usa para buscar el destino que es la siguiente mejor coincidencia para el prefijo de red especificado. Se puede llamar a esta función repetidamente para devolver la siguiente coincidencia sucesiva menos específica, hasta que no coincidan más destinos.

Se llama a esta función después de una llamada a [**RtmGetMostSpecificDestination**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetmostspecificdestination).

Para obtener código de ejemplo que muestra cómo usar estas funciones, vea [Buscar rutas mediante un árbol de prefijos.](search-for-routes-using-rtmgetmostspecificdestination-and-rtmgetlessspecificdestination.md)

## <a name="using-rtmisbestroute"></a>Uso de RtmIsBestRoute

La [**función RtmIsBestRoute**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmisbestroute) permite a un cliente averiguar rápidamente si una ruta determinada es o no la mejor ruta a un destino. Por ejemplo, un cliente puede necesitar almacenar una ruta determinada solo si es la mejor. Por lo tanto, el cliente puede llamar a esta función, en lugar de enumerar todas las rutas y realizar la propia comparación.

 

 




