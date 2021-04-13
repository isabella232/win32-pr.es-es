---
title: Protección de la seguridad de tareas
description: El uso de la característica de protección de seguridad de tareas permitirá a los propietarios de tareas ejecutar sus tareas con los privilegios mínimos necesarios.
ms.assetid: ba03add5-aa05-4bef-baec-684ca17363bd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ab70679d605a9ad56c6d26116245ae17d41a7a1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104268794"
---
# <a name="task-security-hardening"></a>Protección de la seguridad de tareas

El uso de la característica de protección de seguridad de tareas permitirá a los propietarios de tareas ejecutar sus tareas con los privilegios mínimos necesarios. Tenga en cuenta que esta característica está habilitada de forma predeterminada y los propietarios de tareas pueden realizar ajustes adicionales mediante el tipo de identificador de seguridad del token de proceso de tarea y la matriz de privilegios necesarios para la tarea.

## <a name="task-process-token-sid-type-and-task-required-privileges-array"></a>Tipo de SID de token de proceso de tarea y matriz de privilegios de tarea requerida

La especificación de **ProcessTokenSidType** en el nivel de definición de tarea permite a los propietarios de tareas solicitar un proceso de tarea para que se ejecute con el tipo de Sid "none" o el tipo de Sid "Unrestricted". Si el campo está presente en la definición de la tarea, la validación garantiza que UserId de la tarea contiene el nombre o la cadena SID correspondiente para una de esas cuentas de servicio integradas del sistema operativo: "servicio de red" o "servicio LOCAL".

El tipo de SID "none" significa que la tarea se ejecuta en un proceso que no contiene un SID de token de proceso (no se realizarán cambios en la lista de grupos de tokens de proceso). En ese caso, el SID de la cuenta principal de tarea (LocalService/NetworkService) tiene acceso completo al token del proceso.

El tipo de SID "Unrestricted" significa que un SID de tarea se derivará de la ruta de acceso completa de la tarea y se agregará a la lista de grupos de tokens de proceso. Por ejemplo, la \\ RACTask de Microsoft \\ Windows \\ RAC \\ que se ejecuta en la cuenta de servicio local, el SID de la tarea se deriva del nombre Microsoft-Windows-RAC-RACTask, donde un "-" se sustituye por " \\ ", ya que " \\ " es un carácter de nombre de usuario no válido. El nombre de grupo conocido para el SID de la tarea sería "tarea NT \\ <modified full task path> " (nombredominio \\ nombreDeUsuario Format). La lista de control de acceso discrecional (DACL) predeterminada del token de proceso también se modificará para permitir el control total del SID de la tarea y del SID del sistema local y de leer el control del SID de la cuenta de la entidad de seguridad de la tarea. "schtasks.exe/showsid/TN <full task path> " mostrará el SID de la tarea que corresponde a la tarea.

Cuando se inicia una acción de tarea no COM, el motor de programación registra en la cuenta de la entidad de seguridad de la tarea, obtiene el token del proceso y consulta la lista de privilegios que tiene el token y, a continuación, lo compara con la lista de privilegios especificada en RequiredPrivileges. Si no se especifica un privilegio en el último, se ha marcado como privilegio SE \_ \_ quitado. La acción ejecutable se iniciará con el identificador de token resultante mediante la API de CreateProcessAsUser.

Cuando se inicia una acción de tarea COM, debe activarse mediante el proceso de taskhost.exe. El motor de programación consulta el bloque de contexto de cada taskhost.exe en ejecución con la misma cuenta que la tarea de inicio. Si encuentra que un proceso de host se inició con un superconjunto de privilegios que la tarea de inicio necesita, esa tarea se hospeda en ese proceso. Si no encuentra este tipo de proceso, combina la información de protección de todas las tareas que se están ejecutando en el taskhosts en la cuenta de la entidad de seguridad de la tarea con la máscara RequiredPrivileges especificada y, a continuación, inicia una nueva instancia de taskhost.exe.

Si RequiredPrivileges no está presente en la definición de la tarea, los privilegios predeterminados de la cuenta de la entidad de seguridad de tareas sin SeImpersonatePrivilege se usarán para el proceso de la tarea. Si **ProcessTokenSidType** no está presente en la definición de la tarea, se utiliza "Unrestricted" como valor predeterminado.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Información de registro de tareas](task-registration-information.md)
</dt> <dt>

[Acerca del Programador de tareas](about-the-task-scheduler.md)
</dt> <dt>

[Contextos de seguridad para tareas](security-contexts-for-running-tasks.md)
</dt> </dl>

 

 




