---
description: Estados de recursos agrupados disponibles para el dispensador de recursos COM+
ms.assetid: 5037f11c-d113-49b0-b26f-0e3bc59ae8b3
title: Estados de recursos agrupados disponibles para el dispensador de recursos COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b0f28a54a85ed134bf95a8150b5bb4b9cb0d2fda15a16b0b96238ac8c2da18f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118305624"
---
# <a name="pooled-resource-states-available-to-com-resource-dispenser"></a>Estados de recursos agrupados disponibles para el dispensador de recursos COM+

En cualquier momento, un recurso está en uso o no en uso y se ha inscrito o no en una transacción. Esto produce cuatro posibles estados de recursos, como se indica a continuación:

-   **Recursos del inventario no publicado.** Un recurso que no está en uso por un objeto y que no está inscrito en una transacción está en un inventario no inscrito. Hay un recurso en el inventario general disponible para la asignación.

-   **Recursos del inventario inscrito.** Un recurso que no está en uso por un objeto pero que está inscrito en una transacción está en el inventario inscrito. Este recurso solo está disponible para su asignación a objetos que se ejecutan en la misma transacción. Un recurso pasa del inventario inscrito al inventario no inscrito cuando COM+ notifica al administrador del dispensador que la transacción se ha completado.

-   **Recursos en uso no publicado.** Si un recurso se asigna a un objeto y la instancia no se ejecuta en una transacción o el dispensador de recursos ha identificado el recurso como no transaccional, este recurso está en uso no publicado.

-   **Recursos en uso inscrito.** Si se asigna un recurso a un objeto, la instancia se ejecuta en una transacción y el dispensador de recursos ha dado de alta correctamente el recurso en la transacción, este recurso se encuentra en uso dado de alta.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Conceptos del dispensador de recursos com+](com--resource-dispenser-concepts.md)
</dt> <dt>

[Registro de un recurso en una transacción](enlisting-a-resource-in-a-transaction.md)
</dt> </dl>

 

 



