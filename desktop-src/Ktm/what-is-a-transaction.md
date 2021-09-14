---
description: 'Una transacción es un grupo de operaciones que tienen las siguientes propiedades: atómicas, coherentes, aisladas y durables (ACID).'
ms.assetid: b3da52a3-1c52-4577-a997-7e72ebc03fa8
title: ¿Qué es una transacción?
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0c459462d3aee3d7eef556ce0951ede537e8109
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160018"
---
# <a name="what-is-a-transaction"></a>¿Qué es una transacción?

Una transacción es un grupo de operaciones que tienen las siguientes propiedades: atómicas, coherentes, aisladas y durables (ACID). La compatibilidad con transacciones permite desarrollar nuevos tipos de aplicaciones, a la vez que simplifica el proceso de desarrollo y hace que la aplicación sea más sólida. En el resto de este tema se proporcionan escenarios que muestran la necesidad de estas propiedades y, a continuación, una tabla que define cada propiedad.

En un *grupo atómico* de operaciones, todas las operaciones del grupo deben realizarse correctamente o los efectos de todas ellas deben deshacerse (también conocidas como revertir *).* Por ejemplo, una transferencia bancaria debe ser un conjunto atómico de dos operaciones: un adeudo de una cuenta y un crédito a otra cuenta. El débito y el crédito deben implementarse como un grupo atómico. Si esas dos operaciones no se realizaron correctamente, la transferencia se realiza de forma imparcial en favor del banco o del titular de la cuenta.

El requisito de *coherencia* significa que los datos son coherentes después de la transacción (suponiendo que se inició con un sistema coherente antes de la transacción). En el ejemplo de transferencia bancaria, la coherencia se puede definir como que el saldo de cuenta combinado de las dos cuentas sea una constante. Para implementar la coherencia en el ejemplo de transferencia bancaria, las operaciones de débito y crédito simplemente deben ser para la misma cantidad de dinero.

Otro ejemplo de transacción es una actualización de un sitio web. Un sitio de comercio electrónico requiere que una nueva página de navegación de categoría de producto aparezca exactamente al mismo tiempo que las páginas de detalles del producto que describen los nuevos productos. En este caso, es necesario actualizar y agregar varias entradas de directorio bajo el control de una transacción. No solo es necesario que las actualizaciones sean atómicas, sino que también es necesario que un cliente que está comprando actualmente no vea las actualizaciones en curso. Este es un ejemplo de la *propiedad de* aislamiento de las transacciones.

La propiedad de *durabilidad requiere* que una vez finalizada una actualización, sus efectos persistan incluso si el sistema deja de responder. En el ejemplo anterior, la durabilidad se puede proporcionar simplemente asegurándose de una recuperación de datos adecuada para que todas las nuevas entradas del sistema de archivos que representan la adición de un nuevo producto al sitio aparezcan después de que un sistema deje de responder. Esto requiere un sistema con mecanismos de copia de seguridad, recuperación y alta disponibilidad de datos.

La garantía de la atomicidad de una transacción, así como de las otras propiedades, está presente ante cualquier número de errores, incluidos los errores que se producen durante la fase de recuperación de un error anterior. Finalmente, el sistema alcanzará uno de estos dos estados: se han aplicado todas las operaciones o no se ha aplicado ninguna de las operaciones.

Las propiedades de una transacción se resumen en la tabla siguiente.



| Término                                                                                                         | Descripción                                                                                                                       |
|--------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span id="Atomic"></span><span id="atomic"></span><span id="ATOMIC"></span>Atómica<br/>                 | Todas las operaciones de la transacción se realizaron correctamente o ninguna de ellas persiste.<br/>                             |
| <span id="Consistent"></span><span id="consistent"></span><span id="CONSISTENT"></span>Consistente<br/> | Si los datos son coherentes antes de que comience la transacción, serán coherentes una vez que finalice la transacción.<br/> |
| <span id="Isolated_"></span><span id="isolated_"></span><span id="ISOLATED_"></span>Aislado <br/>     | Los efectos de una transacción que está en curso se ocultan a todas las demás transacciones.<br/>                               |
| <span id="Durable"></span><span id="durable"></span><span id="DURABLE"></span>Durable<br/>             | Cuando finaliza una transacción, sus resultados son persistentes y sobrevivirán a un bloqueo del sistema.<br/>                               |



 

Estas propiedades garantizan que el software pueda controlar errores inesperados, ya que simplemente puede anular una transacción cuando una situación inesperada impide una finalización correcta. La infraestructura de la transacción garantiza que todos los efectos de la transacción anulada se revierte, devolviendo los datos a un estado coherente. Por lo tanto, un sistema transaccional permite una recuperación correcta de errores del sistema.

Para garantizar las propiedades ACID, un sistema que admita transacciones debe tener una sólida funcionalidad de registro que se pueda usar para confirmar o revertir transacciones según sea necesario. Para obtener más información, [vea Sistema de archivos de registro común](/previous-versions/windows/desktop/clfs/common-log-file-system-portal).

 

