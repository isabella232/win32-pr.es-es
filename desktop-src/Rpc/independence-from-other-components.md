---
title: Independencia de otros componentes
description: Los datos de error extendidos son útiles incluso cuando el servidor o la aplicación a través de la que se pasa la cadena no reconoce los datos de error extendidos o no los aprovecha. Los enfoques recomendados para estas situaciones se proporcionan al final de esta sección.
ms.assetid: 32c52afd-cd79-4df3-bf30-72a17ce22089
keywords:
- Independencia de otros componentes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ba20a47a5bb30d8e23c1a90d666bc6b957ebb98
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127244617"
---
# <a name="independence-from-other-components"></a>Independencia de otros componentes

Los datos de error extendidos son útiles incluso cuando el servidor o la aplicación a través de la que se pasa la cadena no reconoce los datos de error extendidos o no los aprovecha. Los enfoques recomendados para estas situaciones se proporcionan al final de esta sección.

Los datos de error extendidos son más útiles cuando las aplicaciones o servidores que usan RPC aprovechan la información de error extendida. Al investigar un código de error RPC S y los servidores o aplicaciones implicados no hacen que los datos de error extendidos estén disponibles, tenga en cuenta \_ \_ \* los enfoques siguientes:

-   Realizar un esniff.

    Reproduzca el escenario mientras toma el sniff. El análisis de la conexión contendrá los datos de error extendidos.

-   Examinarlo desde el depurador.

    Si realizar un control del problema no funciona, porque la llamada es local o porque el error se origina localmente, adjunte un depurador al proceso que devuelve el error y coloque un punto de interrupción inmediatamente después de que la llamada RPC genere el error. RPC a menudo indica errores iniciando excepciones, por lo que si busca el error 1825 (RPC S SEC PKG ERROR), habilite la excepción \_ \_ \_ 1825 y, cuando el depurador se interrumpe en esa excepción, examine la información de error extendida para \_ el subproceso.

 

 




