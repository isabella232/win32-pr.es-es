---
title: Elección del modelo de subprocesos
description: Elección del modelo de subprocesos
ms.assetid: e8a0286d-1831-454f-8549-1957fd794809
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2f0fdcd327bf05c0019a03ad171d41c1f1d95a1
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124369455"
---
# <a name="choosing-the-threading-model"></a>Elección del modelo de subprocesos

La elección del modelo de subprocesos para un objeto depende de la función del objeto. Un objeto que realiza una E/S extensa podría admitir el subprocesamiento libre para proporcionar la máxima respuesta a los clientes al permitir llamadas de interfaz durante la latencia de E/S. Por otro lado, un objeto que interactúa con el usuario podría admitir el subprocesamiento de apartamento para sincronizar las llamadas COM entrantes con sus operaciones de ventana.

Es más fácil admitir el subprocesamiento de apartamento en departamentos de un solo subproceso porque COM proporciona sincronización por llamada. La compatibilidad con el subprocesamiento libre es más difícil porque el objeto debe implementar la sincronización; sin embargo, la respuesta a los clientes puede ser mejor porque se puede implementar la sincronización para secciones de código más pequeñas.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acceso a interfaces entre departamentos](accessing-interfaces-across-apartments.md)
</dt> <dt>

[Departamentos multiproceso](multithreaded-apartments.md)
</dt> <dt>

[Problemas de subprocesos del servidor en proceso](in-process-server-threading-issues.md)
</dt> <dt>

[Procesos, subprocesos y departamentos](processes--threads--and-apartments.md)
</dt> <dt>

[Comunicación multiproceso y de subproceso único](single-threaded-and-multithreaded-communication.md)
</dt> <dt>

[Departamentos de un solo subproceso](single-threaded-apartments.md)
</dt> </dl>

 

 




