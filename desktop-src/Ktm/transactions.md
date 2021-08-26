---
description: Una transacción es un objeto que define una unidad lógica de trabajo.
ms.assetid: 29661a58-ada9-4b7c-8d85-ab65b824c7cd
title: Transacciones (Administrador de transacciones de kernel)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 471d2ece52d510c1a77baa59ee3af980c4e4630a17d0911fdcbe590bad78903f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119913894"
---
# <a name="transactions"></a>Transacciones

Una transacción es un objeto que define una unidad lógica de trabajo. La transacción está activa siempre que haya un identificador que haga referencia a la transacción y se considere activa si la transacción aún no se ha confirmado o revertido. Si se crea una transacción y todos los identificadores se han cerrado antes de que se produzca una confirmación o reversión, la transacción se revertirá.

Tenga en cuenta el caso de un cliente transaccional en modo de usuario que crea una transacción para el ámbito de sus operaciones y, a continuación, realiza actualizaciones en uno o varios administradores de recursos. Ocurre lo siguiente:

1.  El cliente llama a la [**función CreateTransaction**](/windows/desktop/api/KtmW32/nf-ktmw32-createtransaction) para crear la transacción y recibe un identificador para esa transacción como valor devuelto.

    La transacción se puede abrir o heredar mediante cualquier número de procesos; Por lo tanto, cada proceso está implicado en la transacción. El error de cualquiera de estos procesos hará que la transacción se anule.

    Es posible que esta transacción aún no sea persistente. Solo las transacciones que han alcanzado el estado preparado deben recuperarse a través de errores del sistema si la transacción usa el registro de supuesto anulación.

2.  El cliente debe pasar explícitamente una transacción al administrador de recursos.
3.  El cliente realiza todas sus operaciones transaccionales con uno o varios RMs, como los sistemas de archivos con transacciones.
4.  El cliente llama a la [**función CommitTransaction.**](/windows/desktop/api/Ktmw32/nf-ktmw32-committransaction)
5.  El administrador de recursos recibe notificaciones de KTM para preparar y confirmar sus datos.

## <a name="transactions-and-threads"></a>Transacciones y subprocesos

Las transacciones no son iguales que los subprocesos. Varios subprocesos o procesos pueden formar parte de una única transacción. Por el contrario, un subproceso puede formar parte de varias transacciones diferentes en momentos diferentes.

## <a name="transaction-functions"></a>Funciones de transacción

Las siguientes funciones se usan con transacciones.



| Función                                                            | Descripción                                                                                   |
|---------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [**CommitTransaction**](/windows/desktop/api/Ktmw32/nf-ktmw32-committransaction)                      | Solicita que se confirma la transacción especificada.                                         |
| [**CommitTransactionAsync**](/windows/desktop/api/Ktmw32/nf-ktmw32-committransactionasync)            | Solicita que se confirma la transacción especificada.                                         |
| [**CreateTransaction**](/windows/desktop/api/KtmW32/nf-ktmw32-createtransaction)                      | Crea un nuevo objeto de transacción.                                                             |
| [**GetTransactionInformation**](/windows/desktop/api/Ktmw32/nf-ktmw32-gettransactioninformation) | Devuelve la información solicitada sobre la transacción especificada.                            |
| [**OpenTransaction**](/windows/desktop/api/Ktmw32/nf-ktmw32-opentransaction)                          | Abre una transacción existente.                                                                |
| [**RollbackTransaction**](/windows/desktop/api/Ktmw32/nf-ktmw32-rollbacktransaction)                  | Solicita que se revierte la transacción especificada.                                       |
| [**RollbackTransactionAsync**](/windows/desktop/api/Ktmw32/nf-ktmw32-rollbacktransactionasync)        | Solicita que se revierte la transacción especificada. Esta función devuelve de forma asincrónica. |
| [**SetTransactionInformation**](/windows/desktop/api/Ktmw32/nf-ktmw32-settransactioninformation)      | Establece la información de transacción para la transacción especificada.                               |



 

 

 



