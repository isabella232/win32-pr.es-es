---
description: Registro de un recurso en una transacción
ms.assetid: b41fe0aa-a4cf-4d4a-9543-8eb0b38f07a2
title: Registro de un recurso en una transacción
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db0a0bf93f373872c8be79054899dea4199dda7e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127465688"
---
# <a name="enlisting-a-resource-in-a-transaction"></a>Registro de un recurso en una transacción

Después de asignar un recurso, pero justo antes de devolver el recurso al dispensador de recursos, el administrador del dispensador comprueba con COM+ para ver si el objeto de llamada se ejecuta dentro de una transacción. Si el objeto de llamada se ejecuta dentro de una transacción, el administrador del dispensador vuelve a llamar al dispensador de recursos y le pide que inste al recurso en la transacción. A continuación, el recurso se devuelve al dispensador de recursos, que lo devuelve a la instancia de llamada.

El dispensador de recursos debe ser capaz de dar de alta en una transacción OLE con el Coordinador de transacciones distribuidas (DTC).

> [!Note]  
> La lista de transacciones es opcional cuando un dispensador de recursos dispensa recursos no transaccionales, como memoria o subprocesos.

 

Cuando se completa una transacción, COM+ notifica al administrador del dispensador si se ha confirmado o anulado. A continuación, el administrador del dispensador notifica al titular de cada dispensador de recursos que los recursos inscritos en esta transacción ahora se pueden mover al inventario general.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Conceptos del dispensador de recursos com+](com--resource-dispenser-concepts.md)
</dt> <dt>

[Estados de recursos agrupados disponibles para el dispensador de recursos COM+](pooled-resource-states-available-to-com--resource-dispenser.md)
</dt> <dt>

[Proceso de asignación de recursos del dispensador de recursos](resource-dispenser-resource-allocation-process.md)
</dt> </dl>

 

 



