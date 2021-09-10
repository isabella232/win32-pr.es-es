---
title: Single-Threaded multiproceso y comunicación multiproceso
description: Single-Threaded multiproceso y comunicación multiproceso
ms.assetid: 8d3a855c-b52d-48bb-9fdf-efbf8005c374
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6470ac398e6ae1c8a645fb076fbbf509d58b579
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124369488"
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

 

 




