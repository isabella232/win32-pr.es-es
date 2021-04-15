---
title: Elegir el modelo de subprocesos
description: Elegir el modelo de subprocesos
ms.assetid: e8a0286d-1831-454f-8549-1957fd794809
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2f0fdcd327bf05c0019a03ad171d41c1f1d95a1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104419101"
---
# <a name="choosing-the-threading-model"></a>Elegir el modelo de subprocesos

La elección del modelo de subprocesos para un objeto depende de la función del objeto. Un objeto que realiza operaciones de e/s extensas podría admitir el subprocesamiento libre para proporcionar la respuesta máxima a los clientes al permitir llamadas de interfaz durante la latencia de e/s. Por otro lado, un objeto que interactúe con el usuario podría admitir el subprocesamiento de apartamento para sincronizar las llamadas COM entrantes con sus operaciones de ventana.

Es más fácil admitir el subprocesamiento de apartamento en apartamentos de un solo subproceso, ya que COM proporciona la sincronización por cada llamada. Admitir el subprocesamiento libre es más difícil porque el objeto debe implementar la sincronización; sin embargo, la respuesta a los clientes puede ser mejor porque la sincronización se puede implementar para secciones de código más pequeñas.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acceso a interfaces entre apartamentos](accessing-interfaces-across-apartments.md)
</dt> <dt>

[Apartamentos multiproceso](multithreaded-apartments.md)
</dt> <dt>

[Problemas de subprocesos de servidor en proceso](in-process-server-threading-issues.md)
</dt> <dt>

[Procesos, subprocesos y apartamentos](processes--threads--and-apartments.md)
</dt> <dt>

[Comunicación multiproceso y de un solo subproceso](single-threaded-and-multithreaded-communication.md)
</dt> <dt>

[Apartamentos de un solo subproceso](single-threaded-apartments.md)
</dt> </dl>

 

 




