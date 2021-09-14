---
title: Mantenimiento automático (Programador de tareas)
description: La actividad de mantenimiento hace referencia a una aplicación o proceso que ayuda a mantener el estado y el rendimiento de un Windows equipo.
ms.assetid: 1D38341B-15AA-422F-AED1-647FCDE69E2E
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 456383eeb75c3b29bf575357d4b17d5f8a66234b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126886465"
---
# <a name="automatic-maintenance"></a>Mantenimiento automático

La actividad de mantenimiento hace referencia a una aplicación o proceso que ayuda a mantener el estado y el rendimiento de un Windows equipo. El mantenimiento incluye mantener actualizados Windows sistema operativo (SO) y aplicaciones, comprobar la seguridad y ejecutar exámenes de malware. Windows La administración automática (WAM) es un conjunto de mejoras en la API de Programador de tareas que puede usar para vincular las aplicaciones a la programación de mantenimiento Windows aplicaciones. En concreto, WAM permite agregar actividades que requieren programación periódica, pero que no tienen requisitos de tiempo exactos. En su lugar, WAM se basa en el sistema operativo para elegir la hora adecuada para activar la tarea a lo largo del día. El sistema elige esas horas en función del impacto mínimo en el usuario, el rendimiento del equipo y la eficiencia energética.

## <a name="how-scheduled-maintenance-works"></a>Funcionamiento del mantenimiento programado

Programador de tareas tareas de mantenimiento son tareas oportunistas que se ejecutan cuando la máquina está inactiva y con alimentación de CA. Uno de los principales objetivos de las tareas de mantenimiento es minimizar el impacto en el equipo mediante la programación del mantenimiento solo cuando el equipo está conectado a la alimentación de CA e inactivo (es decir, cuando no usa o ha salido de la máquina). En la actualidad, la idea de mantenimiento es que la máquina funcione con la menor interrupción para el usuario. Por lo tanto, la hora de mantenimiento **&mdash;** de estilo antiguo (se habla más sobre esto en la sección Reactivación diaria de mantenimiento automático más adelante en este tema) se ha mejorado para aprovechar estos períodos de inactividad. Aunque todavía se puede aprovechar la hora de mantenimiento, la ejecución del mantenimiento oportunista es mejor para el estado del sistema.

Es posible que la tarea se haya quedado inactiva si una máquina no pasa mucho tiempo inactiva y con alimentación de CA. Asegúrese de que el escenario seguirá proporcionando valor al usuario, aunque se retrase. Si el usuario usa activamente la máquina, el sistema aplaza el mantenimiento hasta un momento posterior. El sistema también suspende cualquier tarea de mantenimiento en ejecución si el usuario vuelve a usar el equipo.

El sistema reinicia una tarea de mantenimiento suspendida durante el siguiente período de inactividad. sin embargo, el sistema no suspenderá ninguna tarea marcada como crítica. En su lugar, el sistema permite que se complete una tarea crítica, independientemente de la acción del usuario.

Debido a la naturaleza de la programación, es posible que algunas tareas programadas no finalicen: quizás haya demasiados eventos programados para caber en la ventana de mantenimiento de una hora o quizás el equipo simplemente no se haya activado. En tales casos, puede definir una tarea con una fecha límite. Una fecha límite se define como un período de tiempo periódico en el que el sistema debe realizar correctamente la tarea al menos una vez.

Si una tarea no cumple una fecha límite, el programador de mantenimiento seguirá intentando ejecutar la tarea durante la ventana de mantenimiento. Además, el programador no se limitará al límite de tiempo normal de 1 hora. En su lugar, el programador amplía la duración de la ventana de mantenimiento para completar la tarea retrasada.

Una vez que el sistema completa la tarea (incluso con un código de error), el intento se considera correcto. Después de un intento correcto, el programador se restablece a la programación de mantenimiento normal e intentará realizar la tarea durante el siguiente período.

## <a name="automatic-maintenancemdashdaily-wakeup"></a>Reactivación diaria &mdash; de mantenimiento automático

En Windows 7, una tarea de mantenimiento se ejecuta exclusivamente durante la hora de mantenimiento *,* de forma predeterminada a las 3 a. m., y se puede configurar a través de directiva de grupo. La máquina se reactivaría de modo de espera, ejecutaría tareas de mantenimiento y volvería a suspensión. Esta sesión diaria se limitó a una duración máxima de 1 hora por intento. Esto permitiría que el sistema realizara tareas de mantenimiento diariamente, empezando a las 3 a. m. de forma predeterminada. Tenga en cuenta que el usuario puede volver a programar la hora a la que se desencadena el mantenimiento mediante la configuración de estas opciones.

Con la llegada de los portátiles y el enfoque pesado en la duración de la batería, las máquinas ya no están configuradas para permitir la reactivación S3 en la mayoría de las circunstancias y, por lo general, Doze-To-S4 (hibernar) lo antes posible, para ahorrar batería. En respuesta a estos cambios, Programador de tareas (> Win7) ejecuta tareas de mantenimiento cada vez que se les debe, y la máquina está inactiva y con alimentación de CA.

Esta configuración se puede configurar en Panel de control.

Abra **Panel de control**  >  **sistema y seguridad**  >  **Seguridad y mantenimiento**  >  **Mantenimiento automático**.

Por lo tanto, en función de cómo estén configuradas las máquinas y las tareas, es posible que el comportamiento de reactivación diaria no se produzca hoy como se esperaba debido a esta nueva configuración. En primer lugar, puede determinar si la máquina es compatible con S3 o con CS (espera conectada).
Para ello, abra un símbolo del sistema de Power Shell con privilegios elevados y ejecute el siguiente comando.

```console
powercfg /a
```

La hora de mantenimiento, si la máquina está configurada correctamente, sigue funcionando, pero si no es así,
  - Compruebe la configuración del BIOS para wake settings (Configuración de reactivación). 
  - Compruebe si Permitir temporizador de reactivación está habilitado en Opciones de energía.
    Vaya a **Panel de control** Hardware and Sound Opciones de energía Edit Plan Configuración Change advanced power settings (Cambiar configuración avanzada de energía) > haga clic en Sleep Allow Wake Timer (Permitir temporizador  >    >    >    >     >  **de reactivación de suspensión).**
  - Compruebe si la tarea programada está configurada con lo siguiente.
      * MaintenanceSettings: la tarea debe configurarse con Período, Fecha límite.
      * Habilitado: la tarea debe estar habilitada.
      * WakeToRun: la tarea debe tener permiso para reactivar la máquina.
  - Para programar reactivaciones desde CS, la máquina debe ser compatible con AOAC.
  - Para programar reactivaciones en máquinas S3,
      * Compruebe si la máquina entró en S3 en la alimentación de ca.
      * El sistema debe tener **Wake Enabled en** directiva de grupo para mantenimiento.
 
Espera conectada es el estado del sistema que puede especificar un sistema compatible con AOAC.

Vea las diferencias entre modern standby y S3 en el tema [Modern Standby vs S3](/windows-hardware/design/device-experiences/modern-standby-vs-s3).

## <a name="defining-an-automatic-maintenance-task"></a>Definición de una Mantenimiento automático tarea

Puede convertir cualquier tarea Programador de tareas en una tarea de mantenimiento. Para ello, debe confirmar que la aplicación se puede suspender. A continuación, debe extender la definición de tarea con los [**nuevos elementos MaintenanceSettings**](taskschedulerschema-maintenancesettings-maintenancesettingstype-element.md) [**y AllowStartOnDemand.**](taskschedulerschema-allowstartondemand-settingstype-element.md)

La principal preocupación con la creación de una tarea de mantenimiento es asegurarse de que el sistema puede suspender y reiniciar la tarea. Es probable que el sistema suspenda varias veces una tarea de mantenimiento. Por lo tanto, debe asegurarse de que la aplicación pueda guardar su propio estado y, a continuación, reanudarla en un momento arbitrario. Esto garantiza que el sistema no realiza la misma parte de la tarea repetidamente.

Una vez que haya asegurado que la aplicación se puede suspender y reanudar correctamente, puede usar los elementos **MaintenanceSettings** y **AllowStartOnDemand** para definir la programación. **MaintenanceSettings** se define según el período, la fecha límite y la exclusividad.

-   El **período** es obligatorio y define la frecuencia con la que se debe producir la tarea. Normalmente, esto se define en términos de un ciclo de varios días, como "una vez cada 5 días". Un período debe ser al menos un día, lo que significa que no se puede programar que una tarea se produzca varias veces al día.
-   La **fecha límite** es opcional y define cuánto tiempo el programador puede no completar la tarea antes de notificar al usuario o realizar un mantenimiento de emergencia. La fecha límite debe ser mayor que el período, lo que significa que el sistema debe tener la oportunidad de intentar la tarea al menos una vez antes de notificar al usuario.
-   Además, una tarea de mantenimiento se puede definir opcionalmente como *exclusiva.* Una tarea exclusiva se ejecuta independiente de otras tareas de mantenimiento. Normalmente, una tarea exclusiva es aquella que usa una gran cantidad de recursos, como una gran cantidad de tiempo de CPU o acceso exclusivo a una base de datos. El sistema completa todas las tareas de mantenimiento no exclusivas antes de iniciar una tarea exclusiva. Por lo tanto, debe declarar una tarea como exclusiva solo cuando sea necesario.

En cambio, **AllowStartOnDemand** simplemente indica que el sistema o el usuario pueden iniciar la tarea en cualquier momento. Esto permite al sistema iniciar la tarea durante el mantenimiento normal. De lo contrario, tendría que establecer un desencadenador único para la tarea.
