---
title: Single-Threaded multiproceso y comunicación multiproceso
description: Single-Threaded multiproceso y comunicación multiproceso
ms.assetid: 8d3a855c-b52d-48bb-9fdf-efbf8005c374
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1096ff2cd5916bf16b00a746c2e6de6ce22008258c6e200c2858c0430cb3f96
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119129837"
---
# <a name="single-threaded-and-multithreaded-communication"></a>Single-Threaded multiproceso y comunicación multiproceso

Un cliente o servidor que admita los departamentos de un solo subproceso y multiproceso tendrá un apartamento multiproceso, que contiene todos los subprocesos inicializados como subprocesos libres y uno o varios departamentos de un solo subproceso. Los punteros de interfaz se deben serializar entre los departamentos, pero se pueden usar sin serializar dentro de un apartamento. COM sincronizará las llamadas a objetos de un solo subproceso. COM no sincronizará las llamadas a los objetos del apartamento multiproceso.

Toda la información sobre los departamentos de un solo subproceso se aplica a los subprocesos marcados como modelo de apartamento, y toda la información sobre los departamentos multiproceso se aplica a todos los subprocesos marcados como de subproceso libre. Las reglas de subprocesos de apartamento se aplican a la comunicación entre departamentos, lo que requiere que los punteros de interfaz se serializan entre los departamentos con llamadas a [**CoMarshalInterThreadInterfaceInStream**](/windows/desktop/api/combaseapi/nf-combaseapi-comarshalinterthreadinterfaceinstream) y [**CoGetInterfaceAndReleaseStream**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetinterfaceandreleasestream), tal y como se describe en [Single-Threaded Apartment](single-threaded-apartments.md).

> [!Note]  
> Se aplican algunas consideraciones especiales al tratar con servidores en proceso. Para obtener más información, vea [In-Process Server Threading Issues](in-process-server-threading-issues.md).

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acceso a interfaces entre departamentos](accessing-interfaces-across-apartments.md)
</dt> <dt>

[Elección del modelo de subprocesos](choosing-the-threading-model.md)
</dt> <dt>

[Departamentos multiproceso](multithreaded-apartments.md)
</dt> <dt>

[Problemas de subprocesos del servidor en proceso](in-process-server-threading-issues.md)
</dt> <dt>

[Procesos, subprocesos y departamentos](processes--threads--and-apartments.md)
</dt> <dt>

[Departamentos de un solo subproceso](single-threaded-apartments.md)
</dt> </dl>

 

 




