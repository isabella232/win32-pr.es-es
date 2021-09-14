---
description: Tipos de subprocesos de dispensador de recursos COM+
ms.assetid: 3ab67adb-311f-404c-a3ca-d274af53f91c
title: Tipos de subprocesos de dispensador de recursos COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 761d85edc3105785ded904fd2dc6083a9aea30cd
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126973536"
---
# <a name="com-resource-dispenser-thread-types"></a>Tipos de subprocesos de dispensador de recursos COM+

Las llamadas a un dispensador de recursos COM+ pueden originarse en uno de los siguientes tipos de subproceso:

-   Subproceso de apartamento (STA)
-   Subproceso libre (MTA)
-   Subproceso no COM (aplicación o el [subproceso](com--dispenser-manager.md) del recolector de elementos no utilizados del administrador de dispensadores)

Si un dispensador de recursos no es un objeto COM, debe ser capaz de controlar las llamadas que llegan desde cualquier subproceso en cualquier momento. Si un dispensador de recursos es un objeto COM, el objeto COM debe registrarse con un modelo de subprocesos **de ambos**. Esto permite que los subprocesos STA o MTA creen y usen el dispensador de recursos sin un conmutador de subproceso.

Si un dispensador de recursos crea y usa otro objeto COM (por ejemplo, un administrador de recursos fuera de proceso), es posible que el dispensador de recursos tenga que mantener varios servidores proxy a este otro objeto COM y asegurarse de que las llamadas al objeto se realizan mediante el proxy adecuado para el subproceso de llamada. Cuando el dispensador de recursos crea este objeto, serializa y guarda la referencia. Antes de volver a llamar al objeto , debe deshacer la desmarshal para crear un proxy para el subproceso que realiza la llamada.

Podría ser más eficaz almacenar en caché estos servidores proxy por subproceso manteniendo una asignación del identificador de subproceso a un puntero de proxy. Este mapa se expande a medida que se usan nuevos subprocesos en el proceso.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Conceptos del dispensador de recursos com+](com--resource-dispenser-concepts.md)
</dt> </dl>

 

 



