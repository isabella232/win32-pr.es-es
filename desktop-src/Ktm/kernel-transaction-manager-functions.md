---
description: Las siguientes funciones se usan con transacciones.
ms.assetid: e9704ea8-e67d-4278-b77e-1d4787224d52
title: Funciones del Administrador de transacciones de kernel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ce98208b6ac78795be95b7255e9f263971ad6f08237e75ac0ef661c38a0878a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119535286"
---
# <a name="kernel-transaction-manager-functions"></a>Funciones del Administrador de transacciones de kernel

Las siguientes funciones se usan con transacciones.



| Función                                                            | Descripción                                                                                     |
|---------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [**CommitTransaction**](/windows/desktop/api/Ktmw32/nf-ktmw32-committransaction)                      | Solicita que se confirma la transacción especificada.                                           |
| [**CommitTransactionAsync**](/windows/desktop/api/Ktmw32/nf-ktmw32-committransactionasync)            | Solicita que se confirma la transacción especificada.                                           |
| [**CreateTransaction**](/windows/desktop/api/KtmW32/nf-ktmw32-createtransaction)                      | Crea un nuevo objeto de transacción.                                                               |
| [**GetTransactionId**](/windows/desktop/api/Ktmw32/nf-ktmw32-gettransactionid)                        | Obtiene el identificador de la transacción especificada.                                                   |
| [**GetTransactionInformation**](/windows/desktop/api/Ktmw32/nf-ktmw32-gettransactioninformation) | Devuelve la información solicitada sobre la transacción especificada.                              |
| [**OpenTransaction**](/windows/desktop/api/Ktmw32/nf-ktmw32-opentransaction)                          | Abre una transacción existente.                                                                  |
| [**RollbackComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-rollbackcomplete)                        | Indica que el administrador de recursos (RM) ha completado correctamente la re rolling back a transaction. |
| [**RollbackTransaction**](/windows/desktop/api/Ktmw32/nf-ktmw32-rollbacktransaction)                  | Solicita que se revierte la transacción especificada.                                         |
| [**RollbackTransactionAsync**](/windows/desktop/api/Ktmw32/nf-ktmw32-rollbacktransactionasync)        | Solicita que se revierte la transacción especificada. Esta función devuelve de forma asincrónica.   |
| [**SetTransactionInformation**](/windows/desktop/api/Ktmw32/nf-ktmw32-settransactioninformation)      | Establece la información de transacción para la transacción especificada.                                 |



 

Las siguientes funciones se usan con las inscciones.



| Función                                                                          | Descripción                                                                                                                                                                                                                                                                                                                                                                          |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CommitComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-commitcomplete)                                          | Indica que un administrador de transacciones ha terminado de confirmar una transacción solicitada por el administrador de transacciones (TM).                                                                                                                                                                                                                                                                        |
| [**CommitEnlistment**](/windows/desktop/api/KtmW32/nf-ktmw32-commitenlistment)                                      | Confirma la transacción para la alta especificada.                                                                                                                                                                                                                                                                                                                                |
| [**GetEnlistmentId**](/windows/desktop/api/Ktmw32/nf-ktmw32-getenlistmentid)                                        | Obtiene el identificador de la suscripción especificada.                                                                                                                                                                                                                                                                                                                                         |
| [**CreateEnlistment**](/windows/desktop/api/KtmW32/nf-ktmw32-createenlistment)                                      | Crea una lista, establece su estado inicial y abre un identificador para la alta con el acceso especificado.                                                                                                                                                                                                                                                                       |
| [**GetEnlistmentRecoveryInformation**](/windows/desktop/api/Ktmw32/nf-ktmw32-getenlistmentrecoveryinformation) | Recupera una estructura opaca de datos de recuperación de KTM. La información de recuperación se almacena en un registro en nombre de un rm mediante una llamada a la [**función SetEnlistmentRecoveryInformation.**](/windows/desktop/api/Ktmw32/nf-ktmw32-setenlistmentrecoveryinformation) Después de un error, rm puede usar la [**función GetEnlistmentRecoveryInformation**](/windows/desktop/api/Ktmw32/nf-ktmw32-getenlistmentrecoveryinformation) para recuperar la información. |
| [**OpenEnlistment**](/windows/desktop/api/Ktmw32/nf-ktmw32-openenlistment)                                          | Abre un objeto de registro existente y devuelve un identificador a la lista.                                                                                                                                                                                                                                                                                                         |
| [**PrepareEnlistment**](/windows/desktop/api/KtmW32/nf-ktmw32-prepareenlistment)                                    | Lo llama tm superior para indicar que se ha completado su trabajo de preparación previa.                                                                                                                                                                                                                                                                                                   |
| [**PrePrepareEnlistment**](/windows/desktop/api/KtmW32/nf-ktmw32-preprepareenlistment)                              | Lo llama tm superior para indicar que se ha completado su trabajo de preparación previa.                                                                                                                                                                                                                                                                                                   |
| [**RecoverEnlistment**](/windows/desktop/api/Ktmw32/nf-ktmw32-recoverenlistment)                                    | Recupera el estado de una lista.                                                                                                                                                                                                                                                                                                                                                      |
| [**ReadOnlyEnlistment**](/windows/desktop/api/Ktmw32/nf-ktmw32-readonlyenlistment)                                  | Solicita que la lista especificada se convierta en una lista de solo lectura. Una alta de solo lectura no puede participar en el resultado de la transacción y no se registra de forma dura para la recuperación.                                                                                                                                                                                 |
| [**RollbackEnlistment**](/windows/desktop/api/Ktmw32/nf-ktmw32-rollbackenlistment)                                  | Revierte la transacción especificada que está asociada a una alta. No se puede llamar a esta función para las inselecciones de solo lectura.                                                                                                                                                                                                                                                |
| [**SetEnlistmentRecoveryInformation**](/windows/desktop/api/Ktmw32/nf-ktmw32-setenlistmentrecoveryinformation)      | Establece una estructura opaca definida por el usuario de los datos de recuperación de KTM. La información de recuperación se almacena en un registro en nombre de un rm mediante una llamada a [**SetEnlistmentRecoveryInformation**](/windows/desktop/api/Ktmw32/nf-ktmw32-setenlistmentrecoveryinformation). Después de un error, rm puede usar [**GetEnlistmentRecoveryInformation**](/windows/desktop/api/Ktmw32/nf-ktmw32-getenlistmentrecoveryinformation) para recuperar la información.                  |
| [**SinglePhaseReject**](/windows/desktop/api/Ktmw32/nf-ktmw32-singlephasereject)                                    | Indica que el rm está rechazando una solicitud de una sola fase. Cuando un TM recibe esta llamada, inicia una confirmación en dos fases y envía una solicitud de preparación a todos los RMs inscritos.                                                                                                                                                                                                             |



 

Las siguientes funciones se usan con administradores de recursos.



| Función                                                                           | Descripción                                                                                                                                                      |
|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CreateResourceManager**](/windows/desktop/api/Ktmw32/nf-ktmw32-createresourcemanager)                             | Crea un nuevo objeto rm y asocia el rm con un administrador de transacciones (TM).                                                                                  |
| [**GetNotificationResourceManager**](/windows/desktop/api/KtmW32/nf-ktmw32-getnotificationresourcemanager)           | Solicita y recibe una notificación para RM. El registro de RM usa esta función para recibir notificaciones cuando una transacción cambia de estado.                 |
| [**GetNotificationResourceManagerAsync**](/windows/desktop/api/KtmW32/nf-ktmw32-getnotificationresourcemanagerasync) | Solicita y recibe una notificación asincrónica para un rm. El rm usa esta función para registrarse y recibir notificaciones cuando cambia el estado de una transacción. |
| [**OpenResourceManager**](/windows/desktop/api/Ktmw32/nf-ktmw32-openresourcemanager)                                 | Abre un RM existente.                                                                                                                                            |
| [**PrepareComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-preparecomplete)                                         | Indica que el rm ha completado todo el procesamiento necesario para garantizar que una operación de confirmación o anulación se realizará correctamente para la transacción especificada.           |
| [**PrePrepareComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-prepreparecomplete)                                   | Indica que este rm ha completado su trabajo de preparación, de modo que otros RM ahora puedan comenzar sus operaciones de preparación.                                                |
| [**RecoverResourceManager**](/windows/desktop/api/Ktmw32/nf-ktmw32-recoverresourcemanager)                           | Recupera el estado de un rm a partir de su archivo de registro.                                                                                                                         |
| [**SetResourceManagerCompletionPort**](/windows/desktop/api/Ktmw32/nf-ktmw32-setresourcemanagercompletionport)       | Asocia el puerto de finalización de E/S especificado con el RM especificado. Este puerto recibe todas las notificaciones para el rm.                                             |



 

Las siguientes funciones se usan con administradores de transacciones.



| Función                                                                            | Descripción                                                                 |
|-------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| [**CreateTransactionManager**](/windows/desktop/api/Ktmw32/nf-ktmw32-createtransactionmanager)                        | Crea un nuevo objeto TM y devuelve un identificador con el acceso especificado.     |
| [**GetCurrentClockTransactionManager**](/windows/desktop/api/Ktmw32/nf-ktmw32-getcurrentclocktransactionmanager) | Obtiene un valor de reloj virtual de una TM.                                    |
| [**GetTransactionManagerId**](/windows/desktop/api/Ktmw32/nf-ktmw32-gettransactionmanagerid)                          | Obtiene un identificador para la TM especificada.                                 |
| [**OpenTransactionManager**](/windows/desktop/api/Ktmw32/nf-ktmw32-opentransactionmanager)                            | Abre una TM existente.                                                       |
| [**OpenTransactionManagerById**](/windows/desktop/api/Ktmw32/nf-ktmw32-opentransactionmanagerbyid)                    | Abre una TM existente.                                                       |
| [**RecoverTransactionManager**](/windows/desktop/api/Ktmw32/nf-ktmw32-recovertransactionmanager)                      | Recupera el estado de una TM de su archivo de registro.                                    |
| [**RenameTransactionManager**](/windows/desktop/api/KtmW32/nf-ktmw32-renametransactionmanager)                        | Cambia el nombre de una TM.                                                               |
| [**RollforwardTransactionManager**](/windows/desktop/api/KtmW32/nf-ktmw32-rollforwardtransactionmanager)              | Recupera el estado de TM de su archivo de registro al valor de reloj virtual especificado. |



 

 

 



