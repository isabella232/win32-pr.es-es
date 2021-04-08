---
title: Independencia de otros componentes
description: Los datos de error extendidos son útiles incluso cuando el servidor o la aplicación a través de la que se ha pasado la cadena no reconoce los datos de error extendidos o no se aprovecha de él. Al final de esta sección se proporcionan enfoques recomendados para estas situaciones.
ms.assetid: 32c52afd-cd79-4df3-bf30-72a17ce22089
keywords:
- Independencia de otros componentes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ba20a47a5bb30d8e23c1a90d666bc6b957ebb98
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994517"
---
# <a name="independence-from-other-components"></a>Independencia de otros componentes

Los datos de error extendidos son útiles incluso cuando el servidor o la aplicación a través de la que se ha pasado la cadena no reconoce los datos de error extendidos o no se aprovecha de él. Al final de esta sección se proporcionan enfoques recomendados para estas situaciones.

Los datos de error extendidos son muy útiles cuando las aplicaciones o los servidores que usan RPC aprovechan la información de error extendida. Al investigar un código de error de RPC \_ S \_ \* y los servidores o las aplicaciones implicadas no hacen que los datos de error extendidos estén disponibles, tenga en cuenta los siguientes enfoques:

-   Realice un examen.

    Reproduzca el escenario mientras realiza el examen. El examen de la conexión contendrá los datos de error extendidos.

-   Examínelo desde el depurador.

    Si no funciona el examen del problema, porque la llamada es local o porque el error se origina localmente, asocia un depurador al proceso que devuelve el error y coloca un punto de interrupción inmediatamente después de la llamada RPC que genera el error. RPC suele indicar errores iniciando excepciones, por lo que si busca el error 1825 (error de paquete de RPC \_ s \_ \_ \_ ), habilite la excepción 1825 y cuando el depurador se interrumpa en esa excepción, examine la información de error extendida para el subproceso.

 

 




