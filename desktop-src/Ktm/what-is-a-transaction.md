---
description: 'Una transacción es un grupo de operaciones que tienen las siguientes propiedades: atómicas, coherentes, aisladas y duraderas (ACID).'
ms.assetid: b3da52a3-1c52-4577-a997-7e72ebc03fa8
title: ¿Qué es una transacción?
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0c459462d3aee3d7eef556ce0951ede537e8109
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909182"
---
# <a name="what-is-a-transaction"></a>¿Qué es una transacción?

Una transacción es un grupo de operaciones que tienen las siguientes propiedades: atómicas, coherentes, aisladas y duraderas (ACID). La compatibilidad de las transacciones permite desarrollar nuevos tipos de aplicaciones, a la vez que simplifica el proceso de desarrollo y hace que la aplicación sea más sólida. En el resto de este tema se proporcionan escenarios que muestran la necesidad de estas propiedades y, a continuación, una tabla que define cada propiedad.

En un grupo *atómico* de operaciones, todas las operaciones del grupo deben realizarse correctamente o los efectos de todas ellas se deben deshacer (también conocido como *revertir*). Por ejemplo, una transferencia bancaria debe ser un conjunto atómico de dos operaciones: un débito de una cuenta y un crédito a otra cuenta. El débito y el crédito deben implementarse como un grupo atómico. Si estas dos operaciones no se realizan correctamente, la transferencia es equitativa en favor del Banco o del titular de la cuenta.

El requisito de *coherencia* significa que los datos son coherentes después de la transacción (suponiendo que comenzamos con un sistema coherente antes de la transacción). En el ejemplo de transferencia bancaria, la coherencia se puede definir teniendo en cuenta que el saldo combinado de cuentas de las dos cuentas es una constante. Para implementar la coherencia en el ejemplo de transferencia bancaria, las operaciones de débito y crédito simplemente deben ser para la misma cantidad de dinero.

Otro ejemplo de una transacción es una actualización de un sitio Web. Un sitio de comercio electrónico requiere que haya una nueva página de navegación por categoría de producto para que aparezca exactamente al mismo tiempo que las páginas de detalles de producto que describen los nuevos productos. En este caso, es necesario actualizar y agregar varias entradas de directorio bajo el control de una transacción. No solo es necesario que las actualizaciones sean atómicas, pero también es necesario que un cliente que está comprando actualmente no debe ver las actualizaciones en curso. Este es un ejemplo de la propiedad de *aislamiento* de las transacciones.

La propiedad de *durabilidad* requiere que, una vez finalizada una actualización, sus efectos persistan incluso si el sistema deja de responder. En el ejemplo anterior, la durabilidad se puede proporcionar simplemente asegurándose de la recuperación de datos adecuada para que todas las nuevas entradas del sistema de archivos que representan la adición de un nuevo producto al sitio aparezcan después de que un sistema deje de responder. Esto requiere un sistema con mecanismos de copia de seguridad, recuperación y alta disponibilidad de los datos.

La garantía de la atomicidad de una transacción, así como las demás propiedades, está presente en cualquier número de errores, incluidos los errores que se producen durante la fase de recuperación de un error anterior. Finalmente, el sistema llegará a uno de dos Estados: se han aplicado todas las operaciones o no se ha aplicado ninguna de las operaciones.

En la tabla siguiente se resumen las propiedades de una transacción.



| Término                                                                                                         | Descripción                                                                                                                       |
|--------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span id="Atomic"></span><span id="atomic"></span><span id="ATOMIC"></span>Elemental<br/>                 | Todas las operaciones de la transacción se realizan correctamente o ninguna de las operaciones persiste.<br/>                             |
| <span id="Consistent"></span><span id="consistent"></span><span id="CONSISTENT"></span>Ajusta<br/> | Si los datos son coherentes antes de que comience la transacción, serán coherentes después de que finalice la transacción.<br/> |
| <span id="Isolated_"></span><span id="isolated_"></span><span id="ISOLATED_"></span>Determinado <br/>     | Los efectos de una transacción en curso están ocultos en todas las demás transacciones.<br/>                               |
| <span id="Durable"></span><span id="durable"></span><span id="DURABLE"></span>Durabilidad<br/>             | Cuando una transacción finaliza, sus resultados son persistentes y sobreviven a un bloqueo del sistema.<br/>                               |



 

Estas propiedades garantizan que el software puede controlar errores inesperados, ya que simplemente puede anular una transacción cuando una situación inesperada evita una finalización correcta. La infraestructura de transacciones garantiza que todos los efectos de la transacción anulada se revierten y devuelven los datos a un estado coherente. Por lo tanto, un sistema transaccional permite una recuperación correcta de errores del sistema.

Para garantizar las propiedades ACID, un sistema que admita transacciones debe tener una capacidad de registro robusta que se puede usar para confirmar o revertir las transacciones según sea necesario. Para obtener más información, vea [sistema de archivos de registro común](/previous-versions/windows/desktop/clfs/common-log-file-system-portal).

 

