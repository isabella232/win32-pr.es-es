---
description: Tipos de subprocesos del dispensador de recursos COM+
ms.assetid: 3ab67adb-311f-404c-a3ca-d274af53f91c
title: Tipos de subprocesos del dispensador de recursos COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 761d85edc3105785ded904fd2dc6083a9aea30cd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423276"
---
# <a name="com-resource-dispenser-thread-types"></a>Tipos de subprocesos del dispensador de recursos COM+

Las llamadas a un dispensador de recursos COM+ pueden originarse en uno de los siguientes tipos de subprocesos:

-   Subproceso de apartamento (STA)
-   Subproceso libre (MTA)
-   Subproceso no COM (subproceso de recolector de elementos no utilizados del [Administrador de dispensadores](com--dispenser-manager.md) )

Si un dispensador de recursos no es un objeto COM, debe ser capaz de controlar las llamadas que llegan desde cualquier subproceso en cualquier momento. Si un dispensador de recursos es un objeto COM, el objeto COM se debe registrar con un modelo de subprocesos de **ambos**. Esto permite a los subprocesos STA o MTA crear y usar el dispensador de recursos sin un conmutador de subprocesos.

Si un dispensador de recursos crea y usa otro objeto COM (por ejemplo, un administrador de recursos fuera de proceso), es posible que el dispensador de recursos tenga que mantener varios servidores proxy en este otro objeto COM y asegurarse de que las llamadas al objeto se realizan utilizando el proxy adecuado para el subproceso que realiza la llamada. Cuando el dispensador de recursos crea este objeto, calcula las referencias y guarda la referencia. Antes de volver a llamar al objeto, se debe anular la serialización para crear un proxy para el subproceso que realiza la llamada.

Podría ser más eficaz almacenar en caché estos proxies por subproceso manteniendo una asignación del identificador de subproceso a un puntero proxy. Esta asignación se expande a medida que se usan nuevos subprocesos en el proceso.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Conceptos del dispensador de recursos COM+](com--resource-dispenser-concepts.md)
</dt> </dl>

 

 



