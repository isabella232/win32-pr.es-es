---
title: Single-Threaded y comunicación multiproceso
description: Single-Threaded y comunicación multiproceso
ms.assetid: 8d3a855c-b52d-48bb-9fdf-efbf8005c374
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6470ac398e6ae1c8a645fb076fbbf509d58b579
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104356929"
---
# <a name="single-threaded-and-multithreaded-communication"></a>Single-Threaded y comunicación multiproceso

Un cliente o servidor que admita apartamentos de un solo subproceso y multiproceso tendrá un apartamento multiproceso, que contiene todos los subprocesos inicializados como de subprocesamiento libre y uno o más apartamentos de un solo subproceso. Se deben calcular las referencias de los punteros de interfaz entre apartamentos, pero se pueden usar sin serialización dentro de un contenedor. COM sincronizará las llamadas a los objetos de un contenedor uniproceso. COM no sincronizará las llamadas a los objetos del apartamento multiproceso.

Toda la información sobre apartamentos de un solo subproceso se aplica a los subprocesos marcados como modelo de apartamento y toda la información sobre apartamentos multiproceso se aplica a todos los subprocesos marcados como de subproceso libre. Las reglas de subprocesos de apartamento se aplican a la comunicación entre apartamentos, que requiere que se calculen las referencias de los punteros de interfaz entre apartamentos con llamadas a [**CoMarshalInterThreadInterfaceInStream**](/windows/desktop/api/combaseapi/nf-combaseapi-comarshalinterthreadinterfaceinstream) y [**CoGetInterfaceAndReleaseStream**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetinterfaceandreleasestream), tal y como se describe en [apartamentos de un solo subproceso](single-threaded-apartments.md).

> [!Note]  
> Se aplican algunas consideraciones especiales cuando se trabaja con servidores en proceso. Para obtener más información, vea [problemas de subprocesos de servidor en proceso](in-process-server-threading-issues.md).

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acceso a interfaces entre apartamentos](accessing-interfaces-across-apartments.md)
</dt> <dt>

[Elegir el modelo de subprocesos](choosing-the-threading-model.md)
</dt> <dt>

[Apartamentos multiproceso](multithreaded-apartments.md)
</dt> <dt>

[Problemas de subprocesos de servidor en proceso](in-process-server-threading-issues.md)
</dt> <dt>

[Procesos, subprocesos y apartamentos](processes--threads--and-apartments.md)
</dt> <dt>

[Apartamentos de un solo subproceso](single-threaded-apartments.md)
</dt> </dl>

 

 




