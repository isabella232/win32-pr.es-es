---
description: Tareas de transacciones com+
ms.assetid: fe4374f1-2452-4316-be57-b866c438404d
title: Tareas de transacciones com+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 102b0ec6ae54430be5499c67b5041ee26035eb077e27b1b860377cd728e3e42d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118307595"
---
# <a name="com-transactions-tasks"></a>Tareas de transacciones com+

Aunque el procesamiento automático de transacciones en COM+ permite dedicar un tiempo de desarrollo más productivo a la creación y configuración de objetos que desea participar en transacciones automáticas, hay algunas tareas de programación que puede realizar para adaptar el comportamiento de las transacciones a los requisitos de la aplicación.

En los temas siguientes se tratan opciones de programación específicas relacionadas con el procesamiento de transacciones.



| Tema                                                                                             | Descripción                                                                                        |
|---------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| [Establecer el atributo de transacción](setting-the-transaction-attribute.md)<br/>             | Describe cómo establecer valores de atributo de transacción para los objetos de transacción.<br/>         |
| [Establecer el nivel de aislamiento de la transacción](setting-the-transaction-isolation-level.md)<br/> | Describe cómo establecer los niveles de aislamiento de transacción para los objetos de transacción.<br/>     |
| [Establecer el tiempo de espera de la transacción](setting-the-transaction-time-out.md)<br/>               | Describe cómo establecer intervalos de tiempo de espera para las transacciones.<br/>                          |
| [Establecimiento de las marcas Coherente y Listo](setting-the-consistent-and-done-flags.md)<br/>     | Muestra cómo usar las marcas coherentes y realizadas para controlar el resultado de una transacción.<br/> |
| [Creación de objetos BYOT](creating-byot-objects.md)<br/>                                     | Describe cómo crear objetos para que pueda aportar su propia transacción (BYOT).<br/>           |



 

> [!Note]  
> Como regla general, cualquier componente que actualice el estado persistente debe admitir transacciones. Los componentes que combinan las operaciones de dos o más objetos en una sola tarea deben usar transacciones para simplificar la recuperación de errores. Además, para liberar recursos, como las conexiones de base de datos, las transacciones en COM+ deben ser tan cortas como se puedan hacer.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Conceptos de transacciones de COM+](com--transactions-concepts.md)
</dt> </dl>

 

 




