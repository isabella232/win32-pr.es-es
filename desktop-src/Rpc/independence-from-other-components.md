---
title: Independencia de otros componentes
description: Los datos de error extendidos son útiles incluso cuando el servidor o la aplicación a través de la que se pasa la cadena no reconoce los datos de error extendidos o no los aprovecha. Los enfoques recomendados para estas situaciones se proporcionan al final de esta sección.
ms.assetid: 32c52afd-cd79-4df3-bf30-72a17ce22089
keywords:
- Independencia de otros componentes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b8174ffa0469550d3a7b274fb28f2f30dd807314e6bd596b75469f717f5924a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120020455"
---
# <a name="independence-from-other-components"></a>Independencia de otros componentes

Los datos de error extendidos son útiles incluso cuando el servidor o la aplicación a través de la que se pasa la cadena no reconoce los datos de error extendidos o no los aprovecha. Los enfoques recomendados para estas situaciones se proporcionan al final de esta sección.

Los datos de error extendidos son más útiles cuando las aplicaciones o servidores que usan RPC aprovechan la información de error extendida. Al investigar un código de error de RPC S y los servidores o aplicaciones implicados no hacen que los datos de error extendidos estén disponibles, tenga en cuenta \_ \_ \* los siguientes enfoques:

-   Realizar un sniff.

    Reproduzca el escenario mientras se toma el sniff. El análisis de la conexión contendrá los datos de error extendidos.

-   Examinarlo desde el depurador.

    Si realizar un control del problema no funciona, porque la llamada es local o porque el error se origina localmente, adjunte un depurador al proceso que devuelve el error y coloque un punto de interrupción inmediatamente después de que la llamada RPC genere el error. RPC suele indicar errores iniciando excepciones, por lo que si busca el error 1825 (ERROR PKG de RPC S SEC), habilite la excepción \_ \_ \_ 1825 y, cuando el depurador se interrumpe en esa excepción, examine la información de error extendida para \_ el subproceso.

 

 




