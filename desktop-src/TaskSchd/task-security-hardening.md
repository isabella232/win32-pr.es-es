---
title: Protección de seguridad de tareas
description: El uso de la característica de protección de seguridad de tareas permitirá a los propietarios de tareas ejecutar sus tareas con los privilegios mínimos necesarios.
ms.assetid: ba03add5-aa05-4bef-baec-684ca17363bd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e41117b5317d4cd625ad991db1fdab1428d8748e86f372b2fc5c6e189112a1b7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118858746"
---
# <a name="task-security-hardening"></a>Protección de seguridad de tareas

El uso de la característica de protección de seguridad de tareas permitirá a los propietarios de tareas ejecutar sus tareas con los privilegios mínimos necesarios. Tenga en cuenta que esta característica está habilitada de forma predeterminada y los propietarios de tareas pueden realizar ajustes adicionales mediante el tipo de identificador de seguridad del token de proceso de tarea y la matriz de privilegios necesarios para la tarea.

## <a name="task-process-token-sid-type-and-task-required-privileges-array"></a>Tipo de SID del token de proceso de tarea y matriz de privilegios necesarios para tareas

La especificación de **ProcessTokenSidType** en el nivel de definición de tarea permite a los propietarios de tareas solicitar que un proceso de tarea se ejecute con el tipo DE SID "ninguno" o el tipo DE SID "sin restricciones". Si el campo está presente en la definición de tarea, la validación garantiza que la tarea UserId contiene el nombre o la cadena de SID correspondiente para una de esas cuentas de servicio integradas del sistema operativo: "NETWORK SERVICE" o "LOCAL SERVICE".

El tipo de SID "none" significa que la tarea se ejecuta en un proceso que no contiene un SID de token de proceso (no se realizarán cambios en la lista de grupos de tokens de proceso). En ese caso, el SID de la cuenta de entidad de seguridad de tarea (LocalService/NetworkService) tiene acceso total al token de proceso.

El tipo de SID "sin restricciones" significa que un SID de tarea se derivará de la ruta de acceso de tarea completa y se agregará a la lista de grupos de tokens de proceso. Por ejemplo, la RACTask de Microsoft Windows RAC que se ejecuta en la cuenta de servicio local, el SID de tarea se deriva del nombre \\ \\ \\ \\ Microsoft-Windows-RAC-RACTask, donde "-" se sustituye por \\ " " \\ porque " " es un carácter de nombre de usuario no válido. El nombre de grupo conocido para el SID de tarea sería "NT \\ <modified full task path> TASK" (formato de nombre de usuario \\ de nombre de dominio). La lista de control de acceso discrecional (DACL) predeterminada del token de proceso también se modificará para permitir el control total para el SID de la tarea y el SID del sistema local solo y el control de lectura en el SID de la cuenta de entidad de seguridad de la tarea. "schtasks.exe /showsid /tn" mostrará el SID de <full task path> tarea correspondiente a la tarea.

Cuando se inicia una acción de tarea que no es COM, el motor de programación inicia sesión en la cuenta de entidad de seguridad de tarea, obtiene el token de proceso y consulta la lista de privilegios que tiene el token y, a continuación, lo compara con la lista de privilegios especificada en RequiredPrivileges. Si no se especifica un privilegio en este último, se marca como SE \_ PRIVILEGE \_ REMOVED. A continuación, la acción ejecutable se inicia con el identificador de token resultante mediante la API CreateProcessAsUser.

Cuando se inicia una acción de tarea COM, el proceso de taskhost.exe activarla. El motor de programación consulta el bloque de contexto de cada taskhost.exe con la misma cuenta que la tarea de inicio. Si encuentra que un proceso de host se inició con un superconjunto de privilegios que necesita la tarea de inicio, esa tarea se hospeda en ese proceso. Si no encuentra este proceso, combina la información de seguridad de todas las tareas que se ejecutan en los host de tareas en la cuenta de entidad de seguridad de tarea con la máscara RequiredPrivileges especificada y, a continuación, inicia una nueva instancia de taskhost.exe.

Si RequiredPrivileges no está presente en la definición de tarea, los privilegios predeterminados de la cuenta de entidad de seguridad de tarea sin SeImpersonatePrivilege se usarán para el proceso de tarea. Si **ProcessTokenSidType** no está presente en la definición de tarea, se usa "unrestricted" como valor predeterminado.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Información de registro de tareas](task-registration-information.md)
</dt> <dt>

[Acerca de la Programador de tareas](about-the-task-scheduler.md)
</dt> <dt>

[Contextos de seguridad para tareas](security-contexts-for-running-tasks.md)
</dt> </dl>

 

 




