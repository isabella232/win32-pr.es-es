---
description: Administradores de recursos
ms.assetid: c717b731-cf0b-45cb-bbff-695410fcf6ce
title: Administradores de recursos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33d32d697d58705760002065d005f5927717055f235358c12fd0629de86e14b4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119870025"
---
# <a name="resource-managers"></a>Administradores de recursos

Un administrador de recursos usa el registro del administrador de transacciones para realizar el seguimiento del estado de la transacción. La acción del administrador de recursos al procesar una transacción es la siguiente:

-   El cliente pasa una transacción al rm explícitamente.
-   Rm se alista en la transacción mediante [**CreateEnlistment**](/windows/desktop/api/KtmW32/nf-ktmw32-createenlistment).
-   A continuación, el usuario puede continuar para realizar cualquier operación.
-   Cuando el usuario llama a CommitTransaction, KTM envía una notificación PREPARE \_ TRANSACTION al administrador de transacciones. En este momento, el rm vacía en el disco los cambios que serían necesarios para confirmar la transacción, pero podría producir un error. Si estas operaciones se realizaron correctamente, rm indica que ha finalizado con la operación de preparación mediante una llamada [**a PrepareComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-preparecomplete). Si se producirá un error en estas operaciones, rm responderá llamando a [**RollBackEnlistment**](/windows/desktop/api/Ktmw32/nf-ktmw32-rollbackenlistment).
-   El administrador de recursos recibe una notificación de preparación.
-   El administrador de recursos vacía los datos asociados a la transacción en su archivo de registro de Common Log Services.
-   El administrador de recursos llama [**a la función PrepareComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-preparecomplete) y espera a recibir el resultado de la transacción de KTM.
-   En función del resultado de la transacción, el administrador de recursos recibe un evento de notificación de confirmación o reversión. Si el administrador de recursos recibe una notificación de confirmación, hace que los cambios se realicen de forma permanente e informa a KTM mediante una llamada a [**la función CommitComplete.**](/windows/desktop/api/Ktmw32/nf-ktmw32-commitcomplete) Si el administrador de recursos recibe una notificación de reversión, descarta todos los cambios y revierte al estado que existía antes de cualquiera de los cambios de transacción e informa a KTM mediante una llamada a [**RollbackComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-rollbackcomplete).

## <a name="resource-manager-functions"></a>Resource Manager Functions

Las siguientes funciones se usan con administradores de recursos.



| Función                                                                           | Descripción                                                                                                                                                                      |
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CreateResourceManager**](/windows/desktop/api/Ktmw32/nf-ktmw32-createresourcemanager)                             | Crea un nuevo objeto de Resource Manager (RM) y asocia el rm con un administrador de transacciones (TM).                                                                               |
| [**GetNotificationResourceManager**](/windows/desktop/api/KtmW32/nf-ktmw32-getnotificationresourcemanager)           | Solicita y recibe una notificación para un administrador de recursos (RM). El registro de RM usa esta función para recibir notificaciones cuando una transacción cambia de estado.            |
| [**GetNotificationResourceManagerAsync**](/windows/desktop/api/KtmW32/nf-ktmw32-getnotificationresourcemanagerasync) | Solicita y recibe una notificación asincrónica para un administrador de recursos (RM). El registro de RM usa esta función para recibir notificaciones cuando una transacción cambia de estado. |
| [**OpenResourceManager**](/windows/desktop/api/Ktmw32/nf-ktmw32-openresourcemanager)                                 | Abre un administrador de recursos (RM) existente.                                                                                                                                         |
| [**PrepareComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-preparecomplete)                                         | Indica que el administrador de recursos (RM) ha completado todo el procesamiento necesario para garantizar que una operación de confirmación o anulación se realizará correctamente para la transacción especificada.        |
| [**PrePrepareComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-prepreparecomplete)                                   | Indica que este administrador de recursos ha completado su trabajo de preparación, por lo que otros administradores de recursos ahora pueden comenzar sus operaciones de preparación.                                    |
| [**SetResourceManagerCompletionPort**](/windows/desktop/api/Ktmw32/nf-ktmw32-setresourcemanagercompletionport)       | Asocia el puerto de finalización de E/S especificado al administrador de recursos (RM) especificado. Este puerto recibe todas las notificaciones para el rm.                                          |



 

 

 



