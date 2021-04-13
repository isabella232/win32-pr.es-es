---
description: Estados de recursos agrupados disponibles para el dispensador de recursos COM+
ms.assetid: 5037f11c-d113-49b0-b26f-0e3bc59ae8b3
title: Estados de recursos agrupados disponibles para el dispensador de recursos COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff0bc59dcc2b7e95e060c0d6e96a5880d09d26e3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496325"
---
# <a name="pooled-resource-states-available-to-com-resource-dispenser"></a>Estados de recursos agrupados disponibles para el dispensador de recursos COM+

En cualquier momento, un recurso está en uso o no está en uso y se da de alta o no se ha dado de alta en una transacción. Esto produce cuatro posibles estados de recursos, como se indica a continuación:

-   **Recursos en inventario dado de baja.** Un recurso que no está en uso por un objeto y que no está dado de alta en una transacción se encuentra en un inventario dado de baja. Un recurso de inventario general está disponible para su asignación.

-   **Recursos en inventario dado de alta.** Un recurso que no está en uso por un objeto pero está dado de alta en una transacción está en el inventario dado de alta. Este tipo de recurso solo está disponible para la asignación a objetos que se ejecutan en la misma transacción. Un recurso se desplaza desde el inventario dado de alta hasta el inventario de bajada cuando COM+ notifica al administrador dispensador de que la transacción se ha completado.

-   **Recursos en uso dado de baja.** Si un recurso se asigna a un objeto y la instancia no se está ejecutando en una transacción o el dispensador de recursos ha identificado el recurso como no transaccional, este recurso tiene el uso dado de baja.

-   **Recursos en uso dado de alta.** Si un recurso se asigna a un objeto, la instancia se está ejecutando en una transacción y el dispensador de recursos ha dado de alta correctamente el recurso en la transacción, el recurso está en uso dado de alta.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Conceptos del dispensador de recursos COM+](com--resource-dispenser-concepts.md)
</dt> <dt>

[Dar de alta un recurso en una transacción](enlisting-a-resource-in-a-transaction.md)
</dt> </dl>

 

 



