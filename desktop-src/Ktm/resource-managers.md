---
description: Administradores de recursos
ms.assetid: c717b731-cf0b-45cb-bbff-695410fcf6ce
title: Administradores de recursos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b2ea9b1cd834daf3bfbca49bf37d3f2c0956344
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687394"
---
# <a name="resource-managers"></a>Administradores de recursos

Un administrador de recursos utiliza el registro del administrador de transacciones para realizar el seguimiento del estado de la transacción. La acción del administrador de recursos al procesar una transacción es la siguiente:

-   El cliente pasa una transacción al RM explícitamente.
-   El RM se da de alta en la transacción mediante [**CreateEnlistment**](/windows/desktop/api/KtmW32/nf-ktmw32-createenlistment).
-   Después, el usuario puede continuar para realizar cualquier operación.
-   Cuando el usuario llama a CommitTransaction, KTM envía una notificación de preparación de \_ la transacción al RM. En este momento, el RM se vacía en el disco en cualquier cambio que sea necesario para confirmar la transacción, pero podría producirse un error. Si estas operaciones se realizan correctamente, el RM indica que ha finalizado con la operación de preparación llamando a [**PrepareComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-preparecomplete). Si se produce un error en estas operaciones, el RM responde llamando a [**RollBackEnlistment**](/windows/desktop/api/Ktmw32/nf-ktmw32-rollbackenlistment).
-   El administrador de recursos recibe una notificación de preparación.
-   El administrador de recursos vacía los datos asociados a la transacción en su archivo de registro de servicios de registro comunes.
-   El administrador de recursos llama a la función [**PrepareComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-preparecomplete) y espera recibir el resultado de la transacción del KTM.
-   Dependiendo del resultado de la transacción, el administrador de recursos recibe un evento de notificación commit o ROLLBACK. Si el administrador de recursos recibe una notificación de confirmación, hace que los cambios sean permanentes e informa al KTM mediante una llamada a la función [**CommitComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-commitcomplete) . Si el administrador de recursos recibe una notificación de reversión, descarta todos los cambios y vuelve al estado que existía antes de cualquiera de los cambios de transacción e informa al KTM mediante una llamada a [**RollbackComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-rollbackcomplete).

## <a name="resource-manager-functions"></a>Funciones de Administrador de recursos

Las siguientes funciones se usan con los administradores de recursos.



| Función                                                                           | Descripción                                                                                                                                                                      |
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CreateResourceManager (**](/windows/desktop/api/Ktmw32/nf-ktmw32-createresourcemanager)                             | Crea un nuevo objeto de Resource Manager (RM) y asocia el RM con un administrador de transacciones (TM).                                                                               |
| [**GetNotificationResourceManager**](/windows/desktop/api/KtmW32/nf-ktmw32-getnotificationresourcemanager)           | Solicita y recibe una notificación para un administrador de recursos (RM). El registro de RM usa esta función para recibir notificaciones cuando una transacción cambia de estado.            |
| [**GetNotificationResourceManagerAsync**](/windows/desktop/api/KtmW32/nf-ktmw32-getnotificationresourcemanagerasync) | Solicita y recibe notificaciones asincrónicas de un administrador de recursos (RM). El registro de RM usa esta función para recibir notificaciones cuando una transacción cambia de estado. |
| [**OpenResourceManager**](/windows/desktop/api/Ktmw32/nf-ktmw32-openresourcemanager)                                 | Abre un administrador de recursos (RM) existente.                                                                                                                                         |
| [**PrepareComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-preparecomplete)                                         | Indica que el administrador de recursos (RM) ha completado todo el procesamiento necesario para garantizar que una operación de confirmación o anulación se realizará correctamente para la transacción especificada.        |
| [**PrePrepareComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-prepreparecomplete)                                   | Indica que este administrador de recursos ha completado su trabajo de prepreparación, de modo que otros administradores de recursos puedan comenzar ahora sus operaciones de preparación.                                    |
| [**SetResourceManagerCompletionPort**](/windows/desktop/api/Ktmw32/nf-ktmw32-setresourcemanagercompletionport)       | Asocia el puerto de finalización de e/s especificado al administrador de recursos (RM) especificado. Este puerto recibe todas las notificaciones para el RM.                                          |



 

 

 



