---
description: Transacciones COM+
ms.assetid: 40eccce1-a362-4adc-8060-f6923b9162c9
title: Transacciones COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f800f637a9faec7564d929f3fe7f638ba36d9556db138283c0e6ff3aee87a4f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120070805"
---
# <a name="com-transactions"></a>Transacciones COM+

Al comprar un libro en una tienda de libros en línea, se usa una tarjeta de crédito para intercambiar dinero por un libro. Después de enviar el pedido, una serie de operaciones relacionadas (validación de la tarjeta de crédito, comprobación de la disponibilidad del inventario, etc.) garantiza que obtiene el libro y que la tienda de libros obtiene su dinero. Si se produce un error en una sola operación de la serie durante el intercambio, se produce un error en todo el intercambio. No se obtiene el libro y la tienda de libros no obtiene su dinero.

La tecnología responsable de hacer que este intercambio en línea sea equilibrado y predecible se denomina *procesamiento de transacciones.* Mediante programación, *una transacción* es una unidad de trabajo en la que se produce una serie de operaciones. COM+ usa transacciones mediante programación para asegurarse de que los recursos no se actualizan permanentemente a menos que todas las operaciones dentro de la transacción se completen correctamente. Al enlazar un conjunto de operaciones relacionadas en una transacción COM+ que se realiza correctamente o que produce un error completo, puede simplificar enormemente la recuperación de errores.

En los temas siguientes se presenta la teoría general del procesamiento de transacciones, se proporciona un vistazo más de cerca a las transacciones en COM+, y se presentan sugerencias prácticas para escribir componentes transaccionales.



| Tema                                                                   | Descripción                                                                    |
|-------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [Conceptos de transacciones com+](com--transactions-concepts.md)<br/> | Presenta términos y conceptos básicos.<br/>                                  |
| [Tareas de transacciones COM+](com--transactions-tasks.md)<br/>       | Proporciona información práctica sobre cómo escribir componentes transaccionales.<br/> |



 

 

 




