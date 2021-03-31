---
description: Las siguientes funciones se usan con transacciones.
ms.assetid: e9704ea8-e67d-4278-b77e-1d4787224d52
title: Funciones del administrador de transacciones de kernel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 221bcc13bb1cfb1f8cc67eb4d16f40a27799b921
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913094"
---
# <a name="kernel-transaction-manager-functions"></a>Funciones del administrador de transacciones de kernel

Las siguientes funciones se usan con transacciones.



| Función                                                            | Descripción                                                                                     |
|---------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [**CommitTransaction**](/windows/desktop/api/Ktmw32/nf-ktmw32-committransaction)                      | Solicita que se confirme la transacción especificada.                                           |
| [**CommitTransactionAsync**](/windows/desktop/api/Ktmw32/nf-ktmw32-committransactionasync)            | Solicita que se confirme la transacción especificada.                                           |
| [**CreateTransaction**](/windows/desktop/api/KtmW32/nf-ktmw32-createtransaction)                      | Crea un nuevo objeto de transacción.                                                               |
| [**GetTransactionId**](/windows/desktop/api/Ktmw32/nf-ktmw32-gettransactionid)                        | Obtiene el identificador de la transacción especificada.                                                   |
| [**GetTransactionInformation**](/windows/desktop/api/Ktmw32/nf-ktmw32-gettransactioninformation) | Devuelve la información solicitada sobre la transacción especificada.                              |
| [**OpenTransaction**](/windows/desktop/api/Ktmw32/nf-ktmw32-opentransaction)                          | Abre una transacción existente.                                                                  |
| [**RollbackComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-rollbackcomplete)                        | Indica que el administrador de recursos (RM) ha completado correctamente la reversión de una transacción. |
| [**RollbackTransaction**](/windows/desktop/api/Ktmw32/nf-ktmw32-rollbacktransaction)                  | Solicita que se revierta la transacción especificada.                                         |
| [**RollbackTransactionAsync**](/windows/desktop/api/Ktmw32/nf-ktmw32-rollbacktransactionasync)        | Solicita que se revierta la transacción especificada. Esta función devuelve de forma asincrónica.   |
| [**SetTransactionInformation**](/windows/desktop/api/Ktmw32/nf-ktmw32-settransactioninformation)      | Establece la información de transacción para la transacción especificada.                                 |



 

Las siguientes funciones se usan con inscritos.



| Función                                                                          | Descripción                                                                                                                                                                                                                                                                                                                                                                          |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CommitComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-commitcomplete)                                          | Indica que un RM ha terminado de confirmar una transacción solicitada por el administrador de transacciones (TM).                                                                                                                                                                                                                                                                        |
| [**CommitEnlistment**](/windows/desktop/api/KtmW32/nf-ktmw32-commitenlistment)                                      | Confirma la transacción para la inscripción especificada.                                                                                                                                                                                                                                                                                                                                |
| [**GetEnlistmentId**](/windows/desktop/api/Ktmw32/nf-ktmw32-getenlistmentid)                                        | Obtiene el identificador de la inscripción especificada.                                                                                                                                                                                                                                                                                                                                         |
| [**CreateEnlistment**](/windows/desktop/api/KtmW32/nf-ktmw32-createenlistment)                                      | Crea una inscripción, establece su estado inicial y abre un identificador para la inscripción con el acceso especificado.                                                                                                                                                                                                                                                                       |
| [**GetEnlistmentRecoveryInformation**](/windows/desktop/api/Ktmw32/nf-ktmw32-getenlistmentrecoveryinformation) | Recupera una estructura opaca de datos de recuperación de KTM. La información de recuperación se almacena en un inicio de sesión en nombre de un RM mediante una llamada a la función [**SetEnlistmentRecoveryInformation**](/windows/desktop/api/Ktmw32/nf-ktmw32-setenlistmentrecoveryinformation) . Después de un error, el RM puede usar la función [**GetEnlistmentRecoveryInformation**](/windows/desktop/api/Ktmw32/nf-ktmw32-getenlistmentrecoveryinformation) para recuperar la información. |
| [**OpenEnlistment**](/windows/desktop/api/Ktmw32/nf-ktmw32-openenlistment)                                          | Abre un objeto de inscripción existente y devuelve un identificador a la inscripción.                                                                                                                                                                                                                                                                                                         |
| [**PrepareEnlistment**](/windows/desktop/api/KtmW32/nf-ktmw32-prepareenlistment)                                    | Lo llama el TM superior para indicar que se ha completado el trabajo de preparaciones previas.                                                                                                                                                                                                                                                                                                   |
| [**PrePrepareEnlistment**](/windows/desktop/api/KtmW32/nf-ktmw32-preprepareenlistment)                              | Lo llama el TM superior para indicar que se ha completado el trabajo de preparaciones previas.                                                                                                                                                                                                                                                                                                   |
| [**RecoverEnlistment**](/windows/desktop/api/Ktmw32/nf-ktmw32-recoverenlistment)                                    | Recupera el estado de una inscripción.                                                                                                                                                                                                                                                                                                                                                      |
| [**ReadOnlyEnlistment**](/windows/desktop/api/Ktmw32/nf-ktmw32-readonlyenlistment)                                  | Solicita que la inscripción especificada se convierta en una inscripción de solo lectura. Una inscripción de solo lectura no puede participar en el resultado de la transacción y no se registra de forma duradera para la recuperación.                                                                                                                                                                                 |
| [**RollbackEnlistment**](/windows/desktop/api/Ktmw32/nf-ktmw32-rollbackenlistment)                                  | Revierte la transacción especificada que está asociada a una inscripción. No se puede llamar a esta función para las inlistas de solo lectura.                                                                                                                                                                                                                                                |
| [**SetEnlistmentRecoveryInformation**](/windows/desktop/api/Ktmw32/nf-ktmw32-setenlistmentrecoveryinformation)      | Establece una estructura opaca definida por el usuario de los datos de recuperación de KTM. La información de recuperación se almacena en un inicio de sesión en nombre de un RM mediante una llamada a [**SetEnlistmentRecoveryInformation**](/windows/desktop/api/Ktmw32/nf-ktmw32-setenlistmentrecoveryinformation). Después de un error, el RM puede usar [**GetEnlistmentRecoveryInformation**](/windows/desktop/api/Ktmw32/nf-ktmw32-getenlistmentrecoveryinformation) para recuperar la información.                  |
| [**SinglePhaseReject**](/windows/desktop/api/Ktmw32/nf-ktmw32-singlephasereject)                                    | Indica que el RM está rechazando una solicitud de una sola fase. Cuando un TM recibe esta llamada, inicia una confirmación en dos fases y envía una solicitud de preparación a todos los RMs que se han dado de alta.                                                                                                                                                                                                             |



 

Las siguientes funciones se usan con los administradores de recursos.



| Función                                                                           | Descripción                                                                                                                                                      |
|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CreateResourceManager (**](/windows/desktop/api/Ktmw32/nf-ktmw32-createresourcemanager)                             | Crea un nuevo objeto RM y asocia el RM con un administrador de transacciones (TM).                                                                                  |
| [**GetNotificationResourceManager**](/windows/desktop/api/KtmW32/nf-ktmw32-getnotificationresourcemanager)           | Solicita y recibe una notificación para RM. El registro de RM usa esta función para recibir notificaciones cuando una transacción cambia de estado.                 |
| [**GetNotificationResourceManagerAsync**](/windows/desktop/api/KtmW32/nf-ktmw32-getnotificationresourcemanagerasync) | Solicita y recibe la notificación asincrónica de un RM. El RM usa esta función para registrarse para recibir notificaciones cuando una transacción cambia el estado. |
| [**OpenResourceManager**](/windows/desktop/api/Ktmw32/nf-ktmw32-openresourcemanager)                                 | Abre un RM existente.                                                                                                                                            |
| [**PrepareComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-preparecomplete)                                         | Indica que el RM ha completado todo el procesamiento necesario para garantizar que una operación de confirmación o anulación se realizará correctamente para la transacción especificada.           |
| [**PrePrepareComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-prepreparecomplete)                                   | Indica que este RM ha completado su trabajo de prepreparación, de modo que otro RMs puede comenzar ahora sus operaciones de preparación.                                                |
| [**RecoverResourceManager**](/windows/desktop/api/Ktmw32/nf-ktmw32-recoverresourcemanager)                           | Recupera el estado de RM del archivo de registro.                                                                                                                         |
| [**SetResourceManagerCompletionPort**](/windows/desktop/api/Ktmw32/nf-ktmw32-setresourcemanagercompletionport)       | Asocia el puerto de finalización de e/s especificado con el RM especificado. Este puerto recibe todas las notificaciones para el RM.                                             |



 

Las siguientes funciones se usan con administradores de transacciones.



| Función                                                                            | Descripción                                                                 |
|-------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| [**CreateTransactionManager**](/windows/desktop/api/Ktmw32/nf-ktmw32-createtransactionmanager)                        | Crea un nuevo objeto TM y devuelve un identificador con el acceso especificado.     |
| [**GetCurrentClockTransactionManager**](/windows/desktop/api/Ktmw32/nf-ktmw32-getcurrentclocktransactionmanager) | Obtiene un valor de reloj virtual de un TM.                                    |
| [**GetTransactionManagerId**](/windows/desktop/api/Ktmw32/nf-ktmw32-gettransactionmanagerid)                          | Obtiene un identificador para el TM especificado.                                 |
| [**OpenTransactionManager**](/windows/desktop/api/Ktmw32/nf-ktmw32-opentransactionmanager)                            | Abre un TM existente.                                                       |
| [**OpenTransactionManagerById**](/windows/desktop/api/Ktmw32/nf-ktmw32-opentransactionmanagerbyid)                    | Abre un TM existente.                                                       |
| [**RecoverTransactionManager**](/windows/desktop/api/Ktmw32/nf-ktmw32-recovertransactionmanager)                      | Recupera el estado de TM del archivo de registro.                                    |
| [**RenameTransactionManager**](/windows/desktop/api/KtmW32/nf-ktmw32-renametransactionmanager)                        | Cambia el nombre de un TM.                                                               |
| [**RollforwardTransactionManager**](/windows/desktop/api/KtmW32/nf-ktmw32-rollforwardtransactionmanager)              | Recupera el estado de TM del archivo de registro en el valor de reloj virtual especificado. |



 

 

 



