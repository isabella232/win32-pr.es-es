---
title: Novedades de Programador de tareas
description: Lista de nuevas funcionalidades introducidas por versiones diferentes de Programador de tareas.
ms.assetid: 43fbbbd2-6e97-4ba5-9474-23c5e2b33612
keywords:
- Programador de tareas Programador de tareas, novedades
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5245ab4e681af937924cfbd217095009d80d6a11
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677247"
---
# <a name="whats-new-in-task-scheduler"></a>Novedades de Programador de tareas

Los cambios siguientes resumen las novedades de las distintas versiones de Programador de tareas.

## <a name="windows-10-and-windows-server-2016"></a>Windows 10 (y Windows Server 2016)

Los siguientes cambios de Programador de tareas se introdujeron en Windows 10.

-   Cuando el ahorro de batería está activado, las tareas de Windows Programador de tareas se desencadenan solo si la tarea es:

    -   No está configurado para **iniciar la tarea solo si el equipo está inactivo... (la** tarea no usa [**IdleSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_idlesettings))
    -   No está configurado para ejecutarse durante el mantenimiento automático (la tarea no usa [**MaintenanceSettings**](/windows/desktop/api/Taskschd/nf-taskschd-itasksettings3-get_maintenancesettings))
    -   Está configurado para **ejecutarse solo cuando el usuario ha iniciado sesión** (la tarea [**LogonType**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_logontype) es el **\_ \_ \_ token interactivo interactivo de inicio** de sesión de tarea o el **grupo de inicio de \_ sesión \_ de tareas**)

    El resto de los desencadenadores se retrasa hasta que el ahorro de batería está desactivado. Para obtener más información sobre el acceso al estado del ahorro de batería en la aplicación, consulte [**\_ \_ Estado de la energía del sistema**](/windows/desktop/api/winbase/ns-winbase-system_power_status). Para obtener información general sobre el ahorro de batería, consulte [ahorro de batería (en las instrucciones de componentes de hardware)](/windows-hardware/design/component-guidelines/battery-saver).

-   Por motivos de seguridad, un usuario que no es administrador no puede ver ni administrar una tarea de Programador de tareas de Windows creada por otro usuario.

## <a name="windows-8"></a>Windows 8

En Windows 8 se introdujeron los siguientes cambios Programador de tareas 2,0:

-   Compatibilidad con PowerShell: los usuarios pueden administrar (crear, eliminar, modificar, iniciar explícitamente, detener, etc.) Windows Programador de tareas tareas mediante el módulo de PowerShell ScheduledTasks.
-   Contraseñas administradas: los administradores pueden usar el Active Directory cuentas de contraseña administradas como entidades de seguridad de tareas. Estas tareas ya no requieren una directiva de restablecimiento de contraseña forzada.
-   Cambios de la API: se introdujeron dos nuevas configuraciones de tarea con la interfaz [**ITaskSettings3**](/windows/desktop/api/taskschd/nn-taskschd-itasksettings3) .
    -   [**MaintenanceSettings**](/windows/desktop/api/Taskschd/nf-taskschd-itasksettings3-get_maintenancesettings): las tareas que usan estos valores se tratan como un nuevo tipo de tareas programadas que se invocan durante el tiempo de mantenimiento automático del sistema operativo, de acuerdo con la periodicidad y la fecha límite especificadas.
    -   [**Volatile**](/windows/desktop/api/Taskschd/nf-taskschd-itasksettings3-get_volatile): las tareas que se establecen en volatile siempre están deshabilitadas en un arranque del sistema operativo y se deben volver a habilitar explícitamente cuando sea necesario. Los clústeres de conmutación por error usan las tareas volátiles para asegurarse de que solo se programa una instancia de tarea en un clúster a la vez.
-   El motor de programación unificado ahora admite las siguientes características:
    -   Tipo de inicio de sesión S4U, mediante el elemento [**LogonType**](taskschedulerschema-logontype-principaltype-element.md) .
    -   Valores de consulta XPath para desencadenadores de eventos, a través del elemento [**ValueQueries**](taskschedulerschema-valuequeries-eventtriggertype-element.md) .
    -   No permita que finalice la tarea a través del elemento [**AllowHardTerminate**](taskschedulerschema-allowhardterminate-settingstype-element.md) .
-   Características desusadas en esta versión
    -   Acción: [**sendEmail**](taskschedulerschema-sendemail-actiongroup-element.md) (puede usar [**IExecAction**](/windows/desktop/api/taskschd/nn-taskschd-iexecaction) con el cmdlet [send-MailMessage](/powershell/module/microsoft.powershell.utility/send-mailmessage?view=powershell-7&preserve-view=true) de [Windows PowerShell](https://technet.microsoft.com/library/bb978526.aspx)como solución alternativa).
    -   Acción: [**ShowMessage**](taskschedulerschema-showmessage-actiongroup-element.md).
    -   AT.exe utilidad cmdline

## <a name="windows-7"></a>Windows 7

En Windows 7 se introdujeron los siguientes cambios Programador de tareas 2,0:

-   Usar el motor de programación unificado proporcionado por el sistema operativo subyacente.
-   Capacidad de rechazar las tareas iniciales en las sesiones remotas integradas (ferrocarril).
-   Protección de la seguridad de tareas (solo para tareas que se ejecutan como "servicio de red" o "servicio LOCAL"):

    -   Capacidad de asignar un tipo de identificador de seguridad (SID) de token de proceso (por ejemplo, Unrestricted o None) a una tarea.
    -   Permita que los desarrolladores de tareas soliciten el conjunto exacto de privilegios que requiere su tarea.

-   Cambios de la API:

    -   Compatibilidad con la protección de la seguridad de tareas: la nueva característica de protección de la seguridad de tareas se presenta con la nueva interfaz IPrincipal2.
    -   Se introdujeron dos nuevas configuraciones de tarea con la nueva interfaz ITaskSettings2.

        -   DisallowStartOnRemoteAppSession: el nuevo valor de DisallowStartOnRemoteAppSession puede rechazar un inicio de tarea si se desencadena en [las sesiones remotas integradas localmente (ferrocarril)](/openspecs/windows_protocols/MS-WINPROTLP/df36f95e-6a6b-48d6-a3ae-35a17674f546) .
        -   UseUnifiedSchedulingEngine: el uso del valor de UseUnifiedSchedulingEngine proporciona un comportamiento cohesivo para tareas y servicios de Windows, ya que se administra de forma uniforme mediante un motor de programación común para todo el sistema. Aunque se recomienda usar un motor unificado, no es compatible con algunas de las características Programador de tareas. Si la combinación de propiedades no permite la ejecución de la tarea en un motor unificado, se rechazará el registro de este.
        -   Las características de la tarea que no son compatibles con el motor de programación unificado incluyen:

            -   Tipos de inicio de sesión:

                -   [\_ \_ \_ contraseña o token interactivo \_ de inicio de sesión de \_ tareas](./taskschedulerschema-logontype-principaltype-element.md)

            -   Directiva de varias instancias:

                -   [**instancias de tarea \_ \_ detener \_ existentes**](taskschedulerschema-multipleinstancespolicy-settingstype-element.md)

            -   Acciones:

                -   [Enviar correo electrónico](./taskschedulerschema-sendemail-actiongroup-element.md)
                -   [Mensaje para mostrar](./taskschedulerschema-showmessage-actiongroup-element.md)

            -   Configuración:

                -   [Configuración de red de tareas](./taskschedulerschema-networksettings-settingstype-element.md)
                -   [No permitir finalizar la tarea](./taskschedulerschema-allowhardterminate-settingstype-element.md)

            -   Desencadenadores:

                -   [Límite de tiempo de ejecución del desencadenador](./taskschedulerschema-executiontimelimit-triggerbasetype-element.md)
                -   [Patrones de repetición para desencadenadores de calendario]( ./taskschedulerschema-repetition-triggerbasetype-element.md)
                -   [Valores de consulta XPath para desencadenadores de eventos]( ./taskschedulerschema-valuequeries-eventtriggertype-element.md)
                -   Tipos de desencadenador [de día de la semana](./taskschedulerschema-schedulebymonthdayofweek-calendartriggertype-element.md) [mensual](./taskschedulerschema-schedulebymonth-calendartriggertype-element.md) y mensual

## <a name="windows-vista"></a>Windows Vista

La API Programador de tareas 2,0 se debe usar en el desarrollo de aplicaciones que usan el servicio Programador de tareas en Windows Vista. Para obtener más información, vea [referencia de programador de tareas](task-scheduler-reference.md) y [usar el programador de tareas](using-the-task-scheduler.md).

## <a name="windows-2000-windows-xp-and-windows-server-2003"></a>Windows 2000, Windows XP y Windows Server 2003

La API Programador de tareas 2,0 no está disponible. Use Programador de tareas 1,0.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Programador de tareas](task-scheduler-start-page.md)
</dt> <dt>

[Acerca del Programador de tareas](about-the-task-scheduler.md)
</dt> </dl>

 

 
