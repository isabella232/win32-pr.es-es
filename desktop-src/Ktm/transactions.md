---
description: Una transacción es un objeto que define una unidad lógica de trabajo.
ms.assetid: 29661a58-ada9-4b7c-8d85-ab65b824c7cd
title: Transacciones (Administrador de transacciones de kernel)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bff77ae0d89f5e334319ea0b7b73c27a4b34b57e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677691"
---
# <a name="transactions"></a>Transacciones

Una transacción es un objeto que define una unidad lógica de trabajo. La transacción está activa siempre que haya un identificador que haga referencia a la transacción y se considere activo si aún no se ha confirmado o revertido la transacción. Si se crea una transacción y se cierran todos los identificadores antes de que se produzca una confirmación o una reversión, la transacción se revertirá.

Considere el caso de un cliente transaccional en modo de usuario que crea una transacción para el ámbito de sus operaciones y, a continuación, realiza actualizaciones en uno o varios administradores de recursos. Ocurre lo siguiente:

1.  El cliente llama a la función [**CreateTransaction**](/windows/desktop/api/KtmW32/nf-ktmw32-createtransaction) para crear la transacción y recibe un identificador a esa transacción como el valor devuelto.

    La transacción se puede abrir o heredar en cualquier número de procesos; por tanto, cada proceso está implicado en la transacción. Si se produce un error en cualquiera de estos procesos, se anulará la transacción.

    Es posible que esta transacción aún no sea persistente. Solo las transacciones que han alcanzado el estado preparado deben recuperarse en los errores del sistema si la transacción utiliza el registro supuesto que se ha anulado.

2.  El cliente debe pasar una transacción al administrador de recursos explícitamente.
3.  El cliente realiza todas las operaciones transaccionales con uno o más RMs, como los sistemas de archivos de transacciones.
4.  El cliente llama a la función [**CommitTransaction**](/windows/desktop/api/Ktmw32/nf-ktmw32-committransaction) .
5.  El administrador de recursos recibe notificaciones de KTM para preparar y confirmar sus datos.

## <a name="transactions-and-threads"></a>Transacciones y subprocesos

Las transacciones no son las mismas que los subprocesos. Varios subprocesos o procesos pueden formar parte de una única transacción. Por el contrario, un subproceso puede formar parte de varias transacciones diferentes en momentos diferentes.

## <a name="transaction-functions"></a>Funciones de transacción

Las siguientes funciones se usan con transacciones.



| Función                                                            | Descripción                                                                                   |
|---------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [**CommitTransaction**](/windows/desktop/api/Ktmw32/nf-ktmw32-committransaction)                      | Solicita que se confirme la transacción especificada.                                         |
| [**CommitTransactionAsync**](/windows/desktop/api/Ktmw32/nf-ktmw32-committransactionasync)            | Solicita que se confirme la transacción especificada.                                         |
| [**CreateTransaction**](/windows/desktop/api/KtmW32/nf-ktmw32-createtransaction)                      | Crea un nuevo objeto de transacción.                                                             |
| [**GetTransactionInformation**](/windows/desktop/api/Ktmw32/nf-ktmw32-gettransactioninformation) | Devuelve la información solicitada sobre la transacción especificada.                            |
| [**OpenTransaction**](/windows/desktop/api/Ktmw32/nf-ktmw32-opentransaction)                          | Abre una transacción existente.                                                                |
| [**RollbackTransaction**](/windows/desktop/api/Ktmw32/nf-ktmw32-rollbacktransaction)                  | Solicita que se revierta la transacción especificada.                                       |
| [**RollbackTransactionAsync**](/windows/desktop/api/Ktmw32/nf-ktmw32-rollbacktransactionasync)        | Solicita que se revierta la transacción especificada. Esta función devuelve de forma asincrónica. |
| [**SetTransactionInformation**](/windows/desktop/api/Ktmw32/nf-ktmw32-settransactioninformation)      | Establece la información de transacción para la transacción especificada.                               |



 

 

 



