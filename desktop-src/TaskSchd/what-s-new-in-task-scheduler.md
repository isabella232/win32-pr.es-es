---
title: Novedades de Programador de tareas
description: Lista de nuevas funcionalidades introducidas por diferentes versiones de Programador de tareas.
ms.assetid: 43fbbbd2-6e97-4ba5-9474-23c5e2b33612
keywords:
- Programador de tareas Programador de tareas , novedades
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5245ab4e681af937924cfbd217095009d80d6a11
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127474633"
---
# <a name="whats-new-in-task-scheduler"></a>Novedades de Programador de tareas

Los siguientes cambios resumen las novedades de las distintas versiones de Programador de tareas.

## <a name="windows-10-and-windows-server-2016"></a>Windows 10 (y Windows Server 2016)

Los siguientes Programador de tareas cambios se presentan en Windows 10.

-   Cuando ahorro de batería está activado, Windows Programador de tareas tareas se desencadenan solo si la tarea es:

    -   No se establece en Iniciar la tarea solo si el equipo **está inactivo...** (la tarea no usa [**IdleSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_idlesettings))
    -   No se establece para ejecutarse durante el mantenimiento automático (la tarea no usa [**MaintenanceSettings**](/windows/desktop/api/Taskschd/nf-taskschd-itasksettings3-get_maintenancesettings))
    -   Se establece en **Ejecutar solo cuando el usuario ha iniciado sesión** (la tarea [**LogonType**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_logontype) es **TASK LOGON INTERACTIVE \_ \_ \_ TOKEN** o **TASK LOGON \_ \_ GROUP**)

    Todos los demás desencadenadores se retrasan hasta ahorro de batería está desactivado. Para obtener más información sobre cómo acceder ahorro de batería estado de la aplicación, vea [**SYSTEM \_ POWER \_ STATUS**](/windows/desktop/api/winbase/ns-winbase-system_power_status). Para obtener información general sobre ahorro de batería, [vea ahorro de batería (en las directrices de componentes de hardware).](/windows-hardware/design/component-guidelines/battery-saver)

-   Por motivos de seguridad, un usuario que no es administrador no puede ver ni administrar una Windows Programador de tareas que creó otro usuario.

## <a name="windows-8"></a>Windows 8

Los siguientes Programador de tareas cambios de la versión 2.0 se presentan en Windows 8:

-   Compatibilidad con PowerShell: los usuarios pueden administrar (crear, eliminar, modificar, iniciar, detener explícitamente, etc.) Windows Programador de tareas tareas mediante el módulo de PowerShell ScheduledTasks.
-   Contraseñas administradas: los administradores pueden usar Active Directory cuentas de contraseña administradas como entidades de seguridad de tarea. Estas tareas ya no requieren una directiva de restablecimiento de contraseña aplicada.
-   Cambios en la API: se han introducido dos nuevas opciones de configuración de tareas con la [**interfaz ITaskSettings3.**](/windows/desktop/api/taskschd/nn-taskschd-itasksettings3)
    -   [**MaintenanceSettings:**](/windows/desktop/api/Taskschd/nf-taskschd-itasksettings3-get_maintenancesettings)las tareas que usan esta configuración se tratan como un nuevo tipo de tareas programadas que se invocan durante el tiempo de mantenimiento automático del sistema operativo, según la periodicidad y la fecha límite especificadas.
    -   [**Volatile:**](/windows/desktop/api/Taskschd/nf-taskschd-itasksettings3-get_volatile)las tareas que se establecen como volátiles siempre se deshabilitan en un arranque del sistema operativo y se deben volver a habilitar explícitamente cuando sea necesario. Los clústeres de conmutación por error usan las tareas volátiles para asegurarse de que solo se programa una instancia de tarea en un clúster a la vez.
-   El motor de programación unificado ahora admite las siguientes características:
    -   Tipo de inicio de sesión S4U, a través del [**elemento LogonType.**](taskschedulerschema-logontype-principaltype-element.md)
    -   Valores de consulta XPath para desencadenadores de eventos, a través [**del elemento ValueQueries.**](taskschedulerschema-valuequeries-eventtriggertype-element.md)
    -   No permita que la tarea finalice de forma dura, a través [**del elemento AllowHardTerminate.**](taskschedulerschema-allowhardterminate-settingstype-element.md)
-   Características en desuso en esta versión
    -   Acción: [**sendEmail**](taskschedulerschema-sendemail-actiongroup-element.md) (puede usar [**IExecAction**](/windows/desktop/api/taskschd/nn-taskschd-iexecaction) con [el](https://technet.microsoft.com/library/bb978526.aspx)cmdlet [Windows PowerShell Send-MailMessage](/powershell/module/microsoft.powershell.utility/send-mailmessage?view=powershell-7&preserve-view=true) como solución alternativa).
    -   Acción: [**showMessage**](taskschedulerschema-showmessage-actiongroup-element.md).
    -   AT.exe cmdline

## <a name="windows-7"></a>Windows 7

En Programador de tareas 7 se presentan los siguientes Windows 2.0:

-   Uso del motor de programación unificado proporcionado por el sistema operativo subyacente.
-   Capacidad de rechazar las tareas de inicio en sesiones de Aplicaciones remotas integradas localmente (RAIL).
-   Protección de la seguridad de tareas (solo para tareas que se ejecutan como "SERVICIO DE RED" o "SERVICIO LOCAL"):

    -   Capacidad de asignar un tipo de identificador de seguridad de token de proceso (SID) (por ejemplo, sin restricciones o ninguno) a una tarea.
    -   Permitir que los desarrolladores de tareas soliciten el conjunto exacto de privilegios que requiere su tarea.

-   Cambios en la API:

    -   Compatibilidad con la protección de la seguridad de tareas: la nueva característica de protección de la seguridad de tareas se presenta con la nueva interfaz IPrincipal2.
    -   Se han introducido dos nuevas opciones de configuración de tareas con la nueva interfaz ITaskSettings2.

        -   DisallowStartOnRemoteAppSession: la nueva configuración DisallowStartOnRemoteAppSession puede rechazar un inicio de tarea si se desencadena en sesiones de Aplicaciones remotas integradas [localmente (RAIL).](/openspecs/windows_protocols/MS-WINPROTLP/df36f95e-6a6b-48d6-a3ae-35a17674f546)
        -   UseUnifiedSchedulingEngine: el uso de la configuración UseUnifiedSchedulingEngine proporciona un comportamiento coherente para Windows Tasks and Services porque se administra de forma uniforme mediante un motor de programación común de todo el sistema. Aunque se recomienda usar un motor unificado, no admite algunas de las características Programador de tareas motor. Si la combinación de propiedades no permitirá la ejecución de la tarea en un motor unificado, se rechazará el registro de este tipo.
        -   Las características de tareas que no son compatibles con el motor de programación unificado incluyen:

            -   Tipos de inicio de sesión:

                -   [TOKEN \_ INTERACTIVO O CONTRASEÑA DE INICIO DE SESIÓN DE \_ \_ \_ \_ TAREA](./taskschedulerschema-logontype-principaltype-element.md)

            -   Directiva de varias instancias:

                -   [**INSTANCIAS \_ DE TAREA STOP \_ \_ EXISTING**](taskschedulerschema-multipleinstancespolicy-settingstype-element.md)

            -   Acciones:

                -   [Enviar correo electrónico](./taskschedulerschema-sendemail-actiongroup-element.md)
                -   [Mensaje para mostrar](./taskschedulerschema-showmessage-actiongroup-element.md)

            -   Configuración:

                -   [Configuración de red de tareas](./taskschedulerschema-networksettings-settingstype-element.md)
                -   [No permitir la terminación de tareas](./taskschedulerschema-allowhardterminate-settingstype-element.md)

            -   Desencadenadores:

                -   [Límite de tiempo de ejecución del desencadenador](./taskschedulerschema-executiontimelimit-triggerbasetype-element.md)
                -   [Patrones de repetición para desencadenadores de calendario]( ./taskschedulerschema-repetition-triggerbasetype-element.md)
                -   [Valores de consulta XPath para desencadenadores de eventos]( ./taskschedulerschema-valuequeries-eventtriggertype-element.md)
                -   [Tipos de](./taskschedulerschema-schedulebymonth-calendartriggertype-element.md) desencadenador [mensual y mensual del día de la](./taskschedulerschema-schedulebymonthdayofweek-calendartriggertype-element.md) semana

## <a name="windows-vista"></a>Windows Vista

La API Programador de tareas 2.0 debe usarse en el desarrollo de aplicaciones que usan el servicio Programador de tareas en Windows Vista. Para obtener más información, [vea Programador de tareas y](task-scheduler-reference.md) Using the [Programador de tareas](using-the-task-scheduler.md).

## <a name="windows-2000-windows-xp-and-windows-server-2003"></a>Windows 2000, Windows XP y Windows Server 2003

La Programador de tareas API 2.0 no está disponible. Use Programador de tareas 1.0.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Programador de tareas](task-scheduler-start-page.md)
</dt> <dt>

[Acerca de la Programador de tareas](about-the-task-scheduler.md)
</dt> </dl>

 

 
