---
description: Un administrador de transacciones (TM) es una instancia de un registro. En KTM, los objetos TM especifican el registro y parte de la funcionalidad de TM. Normalmente hay muchos objetos TM en un nodo determinado. Los administradores de recursos (RMs) deben estar asociados a una TM específica.
ms.assetid: 8d43977a-84cf-4109-b7db-f9c94a226c5d
title: Administradores de transacciones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0ea492a3eb10d95002d4e0a61500e7f1e74e87da21bc90daf680a2899e3fa67
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119424445"
---
# <a name="transaction-managers"></a>Administradores de transacciones

Un administrador de transacciones (TM) es una instancia de un registro. En KTM, los objetos TM especifican el registro y parte de la funcionalidad de TM. Normalmente hay muchos objetos TM en un nodo determinado. Los administradores de recursos (RMs) deben estar asociados a una TM específica. Hay tres tipos de MÁQUINAS virtuales:

-   Una TM volátil, que no tiene ningún registro.
-   Una TM normal, que tiene un registro y se usa para coordinar las transacciones de uno o varios RMs.
-   Un administrador de transacciones superior.

## <a name="volatile-transaction-managers"></a>Administradores de transacciones volátiles

Una TM volátil es una TM para RMs volátiles o de solo lectura. No tiene un registro y no conserva el estado de las transacciones en los reinicios del sistema.

## <a name="transaction-managers"></a>Administradores de transacciones

Los TMs tienen un registro, uno o varios RMs duraderos o volátiles, o ambos. La TM conservará el estado de una transacción entre reinicios del sistema hasta que se completen las transacciones. Se usa un modelo de anulación supuesto, por lo que se revierte las transacciones que estaban activas pero no preparadas cuando se apaga el objeto TM. Al abrir una TM por primera vez, debe recuperar la TM llamando a la [**función RecoverTransactionManager.**](/windows/desktop/api/Ktmw32/nf-ktmw32-recovertransactionmanager)

## <a name="superior-transaction-managers"></a>Administradores de transacciones superiores

Una TM superior es una TM para otros TMs. Coordina las transacciones. También emite notificaciones **TRANSACTION \_ NOTIFY \_ PREPARE** al Administrador de transacciones de kernel (KTM). Un ejemplo de una TM superior es el Microsoft DTC (Coordinador de transacciones distribuidas) (DTC). Esta capacidad incluye una responsabilidad adicional de tiempo de recuperación. Durante la recuperación, rm debe llamar primero a la [**función OpenEnlistment**](/windows/desktop/api/Ktmw32/nf-ktmw32-openenlistment) para volver a abrir la lista. También debe entregar (o volver a entregar) el resultado de la transacción si se confirma la transacción. es gratuito entregar un resultado llamando a la función [**CommitTransaction**](/windows/desktop/api/Ktmw32/nf-ktmw32-committransaction) o [**a la función RollbackTransaction.**](/windows/desktop/api/Ktmw32/nf-ktmw32-rollbacktransaction) Esta obligación no finaliza hasta que haya recibido un evento de notificación **TRANSACTION \_ NOTIFY COMMIT \_ \_ COMPLETE** o **TRANSACTION NOTIFY \_ \_ ROLLBACK \_ COMPLETE** asociado. Si un TM superior no puede realizar estas operaciones en tiempo de recuperación, KTM limpiará las transacciones que no han recibido resultados al final de la fase de recuperación. Sin embargo, esto puede dar lugar a resultados de transacción incoherentes.

## <a name="transaction-manager-functions"></a>Funciones del Administrador de transacciones

Las siguientes funciones se usan con administradores de transacciones.



| Función                                                                            | Descripción                                                                                    |
|-------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [**CreateTransactionManager**](/windows/desktop/api/Ktmw32/nf-ktmw32-createtransactionmanager)                        | Crea un nuevo objeto de administrador de transacciones (TM) y devuelve un identificador con el acceso especificado.  |
| [**GetCurrentClockTransactionManager**](/windows/desktop/api/Ktmw32/nf-ktmw32-getcurrentclocktransactionmanager) | Obtiene un valor de reloj virtual de un administrador de transacciones.                                      |
| [**GetTransactionManagerId**](/windows/desktop/api/Ktmw32/nf-ktmw32-gettransactionmanagerid)                          | Obtiene un identificador para el administrador de transacciones especificado.                                   |
| [**OpenTransactionManager**](/windows/desktop/api/Ktmw32/nf-ktmw32-opentransactionmanager)                            | Abre un administrador de transacciones existente.                                                         |
| [**RecoverTransactionManager**](/windows/desktop/api/Ktmw32/nf-ktmw32-recovertransactionmanager)                      | Recupera el estado de un administrador de transacciones de su archivo de registro.                                      |
| [**RollforwardTransactionManager**](/windows/desktop/api/KtmW32/nf-ktmw32-rollforwardtransactionmanager)              | Recupera el estado de un administrador de transacciones de su archivo de registro al valor de reloj virtual especificado. |



 

 

 



