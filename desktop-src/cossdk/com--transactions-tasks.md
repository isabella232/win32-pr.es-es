---
description: Tareas de transacciones de COM+
ms.assetid: fe4374f1-2452-4316-be57-b866c438404d
title: Tareas de transacciones de COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70aaebd3e788e1ff12e86b7831979f055367fea7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153264"
---
# <a name="com-transactions-tasks"></a>Tareas de transacciones de COM+

Aunque el procesamiento automático de transacciones en COM+ le permite dedicar tiempo de desarrollo más productivo a la creación y configuración de objetos que desea que participen en transacciones automáticas, hay algunas tareas de programación que puede realizar para adaptar el comportamiento de las transacciones a los requisitos de la aplicación.

En los temas siguientes se describen las opciones de programación específicas relacionadas con el procesamiento de transacciones.



| Tema                                                                                             | Descripción                                                                                        |
|---------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| [Establecer el atributo de transacción](setting-the-transaction-attribute.md)<br/>             | Describe cómo establecer los valores de atributo de transacción para los objetos de transacción.<br/>         |
| [Establecer el nivel de aislamiento de la transacción](setting-the-transaction-isolation-level.md)<br/> | Describe cómo establecer los niveles de aislamiento de transacción para los objetos de transacción.<br/>     |
| [Establecer el tiempo de espera de la transacción](setting-the-transaction-time-out.md)<br/>               | Describe cómo establecer intervalos de tiempo de espera para las transacciones.<br/>                          |
| [Establecimiento de las marcas coherente y realizada](setting-the-consistent-and-done-flags.md)<br/>     | Muestra cómo utilizar las marcas coherente y completada para controlar el resultado de una transacción.<br/> |
| [Crear objetos de transacciones](creating-byot-objects.md)<br/>                                     | Describe cómo crear objetos para que pueda llevar su propia transacción (transacciones).<br/>           |



 

> [!Note]  
> Como norma general, cualquier componente que actualice el estado persistente debe admitir transacciones. Los componentes que combinan las operaciones de dos o más objetos en una sola tarea deben usar transacciones para simplificar la recuperación de errores. Además, para liberar recursos, como las conexiones de base de datos, las transacciones en COM+ deben ser tan cortas como se puedan hacer.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Conceptos de transacciones de COM+](com--transactions-concepts.md)
</dt> </dl>

 

 




