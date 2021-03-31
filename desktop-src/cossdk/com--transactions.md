---
description: Transacciones COM+
ms.assetid: 40eccce1-a362-4adc-8060-f6923b9162c9
title: Transacciones COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aef51f4c8ed5e37101f64d36af385c93ac7e69ca
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423400"
---
# <a name="com-transactions"></a>Transacciones COM+

Al comprar un libro de una librería en línea, puede usar una tarjeta de crédito para el dinero de un libro. Después de enviar el pedido, una serie de operaciones relacionadas (validación de la tarjeta de crédito, comprobación de la disponibilidad del inventario, etc.) garantiza que obtendrá el libro y que la librería obtenga su dinero. Si se produce un error en una sola operación de la serie durante el intercambio, se produce un error en todo el intercambio. No se obtiene el libro y la librería no obtiene el dinero.

La tecnología responsable de la realización de este intercambio en línea con equilibrio y predicción se denomina *procesamiento de transacciones*. Mediante programación, una *transacción* es una unidad de trabajo en la que se producen una serie de operaciones. COM+ utiliza transacciones mediante programación para asegurarse de que los recursos no se actualizan de forma permanente a menos que todas las operaciones dentro de la transacción se completen correctamente. Al enlazar un conjunto de operaciones relacionadas en una transacción de COM+ que se completa o completa correctamente, puede simplificar enormemente la recuperación de errores.

En los siguientes temas se presenta la teoría general del procesamiento de transacciones, se ofrece una visión más detallada de las transacciones en COM+ y se presentan sugerencias prácticas para escribir componentes transaccionales.



| Tema                                                                   | Descripción                                                                    |
|-------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [Conceptos de transacciones de COM+](com--transactions-concepts.md)<br/> | Presenta términos y conceptos básicos.<br/>                                  |
| [Tareas de transacciones de COM+](com--transactions-tasks.md)<br/>       | Proporciona información práctica sobre la escritura de componentes transaccionales.<br/> |



 

 

 




