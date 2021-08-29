---
description: Tipos de subprocesos de dispensador de recursos COM+
ms.assetid: 3ab67adb-311f-404c-a3ca-d274af53f91c
title: Tipos de subprocesos de dispensador de recursos COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f20f9fc25dd1811b401dd15998ddb3f8fb9b21e5964277cc94d0ab1797eae622
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119129057"
---
# <a name="com-resource-dispenser-thread-types"></a>Tipos de subprocesos de dispensador de recursos COM+

Las llamadas a un dispensador de recursos COM+ pueden originarse en uno de los siguientes tipos de subprocesos:

-   Subproceso de apartamento (STA)
-   Subproceso libre (MTA)
-   Subproceso que no es COM (aplicación o [el](com--dispenser-manager.md) subproceso recolector de elementos no utilizados del administrador del distribuidor)

Si un dispensador de recursos no es un objeto COM, debe ser capaz de controlar las llamadas que llegan desde cualquier subproceso en cualquier momento. Si un dispensador de recursos es un objeto COM, el objeto COM debe registrarse con un modelo de subprocesos **de Ambos**. Esto permite que los subprocesos STA o MTA creen y usen el dispensador de recursos sin un conmutador de subproceso.

Si un dispensador de recursos crea y usa otro objeto COM (por ejemplo, un administrador de recursos fuera de proceso), es posible que el distribuidor de recursos tenga que mantener varios servidores proxy para este otro objeto COM y asegurarse de que las llamadas al objeto se realizan mediante el proxy adecuado para el subproceso de llamada. Cuando el distribuidor de recursos crea este objeto, serializa y guarda la referencia. Antes de volver a llamar al objeto , debe deshacer la autenticación para crear un proxy para el subproceso que realiza la llamada.

Podría ser más eficaz almacenar en caché estos servidores proxy por subproceso manteniendo una asignación del identificador de subproceso a un puntero de proxy. Este mapa se expande a medida que se usan nuevos subprocesos en el proceso.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Conceptos del distribuidor de recursos com+](com--resource-dispenser-concepts.md)
</dt> </dl>

 

 



