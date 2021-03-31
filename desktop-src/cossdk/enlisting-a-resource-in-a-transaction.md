---
description: Dar de alta un recurso en una transacción
ms.assetid: b41fe0aa-a4cf-4d4a-9543-8eb0b38f07a2
title: Dar de alta un recurso en una transacción
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db0a0bf93f373872c8be79054899dea4199dda7e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423496"
---
# <a name="enlisting-a-resource-in-a-transaction"></a>Dar de alta un recurso en una transacción

Una vez que se asigna un recurso, pero justo antes de devolver el recurso al dispensador de recursos, el administrador dispensador comprueba con COM+ si el objeto que realiza la llamada se ejecuta dentro de una transacción. Si el objeto que realiza la llamada se ejecuta dentro de una transacción, el administrador dispensador vuelve a llamar al dispensador de recursos y le pide que dé de alta el recurso en la transacción. Después, el recurso se devuelve al dispensador de recursos, que, a continuación, lo devuelve a la instancia de que realiza la llamada.

El dispensador de recursos debe ser capaz de dar de alta en una transacción OLE con el Coordinador de transacciones distribuidas (DTC).

> [!Note]  
> La inscripción de transacciones es opcional cuando un dispensador de recursos dispensado en recursos no transaccionales, como la memoria o los subprocesos.

 

Cuando se completa una transacción, COM+ notifica al administrador del dispensado si se ha confirmado o anulado. A continuación, el administrador del dispensador notifica a cada titular de recursos que los recursos que se hayan dado de alta en esta transacción se pueden pasar ahora a inventario general.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Conceptos del dispensador de recursos COM+](com--resource-dispenser-concepts.md)
</dt> <dt>

[Estados de recursos agrupados disponibles para el dispensador de recursos COM+](pooled-resource-states-available-to-com--resource-dispenser.md)
</dt> <dt>

[Proceso de asignación de recursos del dispensador de recursos](resource-dispenser-resource-allocation-process.md)
</dt> </dl>

 

 



