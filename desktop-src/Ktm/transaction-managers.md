---
description: Un administrador de transacciones (TM) es una instancia de un registro. En KTM, los objetos de TM especifican el registro y algunas de las funciones de TM. Normalmente hay muchos objetos TM en un nodo determinado. Los administradores de recursos (RMs) deben estar asociados a un TM específico.
ms.assetid: 8d43977a-84cf-4109-b7db-f9c94a226c5d
title: Administradores de transacciones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 313215816642201c75ae5f0facae3bf98799c8d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677692"
---
# <a name="transaction-managers"></a>Administradores de transacciones

Un administrador de transacciones (TM) es una instancia de un registro. En KTM, los objetos de TM especifican el registro y algunas de las funciones de TM. Normalmente hay muchos objetos TM en un nodo determinado. Los administradores de recursos (RMs) deben estar asociados a un TM específico. Hay tres tipos de TM:

-   TM volátil, que no tiene ningún registro.
-   TM normal, que tiene un registro y se utiliza para coordinar las transacciones de uno o más RMs.
-   Un administrador de transacciones superior.

## <a name="volatile-transaction-managers"></a>Administradores de transacciones volátiles

Un TM volátil es un TM para RMs de solo lectura o volátil. No tiene un registro y no conserva el estado de las transacciones a través de los reinicios del sistema.

## <a name="transaction-managers"></a>Administradores de transacciones

Las TM tienen un registro, uno o más RMs duradero o volátil, o ambos. El TM mantendrá el estado de una transacción a través de los reinicios del sistema hasta que se completen las transacciones. Se utiliza un modelo de anulación de la operación, por lo que las transacciones que estaban activas pero no se prepararon cuando se apaga el objeto TM se revierten. Al abrir un TM por primera vez, debe recuperar el TM mediante una llamada a la función [**RecoverTransactionManager**](/windows/desktop/api/Ktmw32/nf-ktmw32-recovertransactionmanager) .

## <a name="superior-transaction-managers"></a>Administradores de transacciones superiores

Un TM superior es un TM para otras TM. Coordina las transacciones. También emite notificaciones de **\_ notificaciones de \_ preparación** para el administrador de transacciones de kernel (KTM). Un ejemplo de un TM superior es Microsoft Coordinador de transacciones distribuidas (DTC). Esta capacidad incluye una responsabilidad adicional en tiempo de recuperación. Durante la recuperación, el RM debe llamar primero a la función [**OpenEnlistment**](/windows/desktop/api/Ktmw32/nf-ktmw32-openenlistment) para volver a abrir la inscripción. También debe proporcionar (o volver a proporcionar) el resultado de la transacción si se confirmó la transacción. es gratuito proporcionar un resultado llamando a la función [**CommitTransaction**](/windows/desktop/api/Ktmw32/nf-ktmw32-committransaction) o a la función [**RollbackTransaction**](/windows/desktop/api/Ktmw32/nf-ktmw32-rollbacktransaction) . Esta obligación no finaliza hasta que se ha recibido un evento de notificación de **\_ \_ confirmación \_** completa de transacción asociada o de notificaciones de **\_ \_ reversión \_** completa. Si un TM superior no puede realizar estas operaciones en el momento de la recuperación, el KTM limpiará las transacciones que no hayan recibido resultados al final de la fase de recuperación. Sin embargo, esto puede dar lugar a resultados incoherentes en las transacciones.

## <a name="transaction-manager-functions"></a>Funciones del administrador de transacciones

Las siguientes funciones se usan con administradores de transacciones.



| Función                                                                            | Descripción                                                                                    |
|-------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [**CreateTransactionManager**](/windows/desktop/api/Ktmw32/nf-ktmw32-createtransactionmanager)                        | Crea un nuevo objeto de administrador de transacciones (TM) y devuelve un identificador con el acceso especificado.  |
| [**GetCurrentClockTransactionManager**](/windows/desktop/api/Ktmw32/nf-ktmw32-getcurrentclocktransactionmanager) | Obtiene un valor de reloj virtual de un administrador de transacciones.                                      |
| [**GetTransactionManagerId**](/windows/desktop/api/Ktmw32/nf-ktmw32-gettransactionmanagerid)                          | Obtiene un identificador para el administrador de transacciones especificado.                                   |
| [**OpenTransactionManager**](/windows/desktop/api/Ktmw32/nf-ktmw32-opentransactionmanager)                            | Abre un administrador de transacciones existente.                                                         |
| [**RecoverTransactionManager**](/windows/desktop/api/Ktmw32/nf-ktmw32-recovertransactionmanager)                      | Recupera el estado de un administrador de transacciones desde su archivo de registro.                                      |
| [**RollforwardTransactionManager**](/windows/desktop/api/KtmW32/nf-ktmw32-rollforwardtransactionmanager)              | Recupera el estado de un administrador de transacciones desde su archivo de registro hasta el valor de reloj virtual especificado. |



 

 

 



