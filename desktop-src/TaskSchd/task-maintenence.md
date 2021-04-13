---
title: Mantenimiento automático (Programador de tareas)
description: La actividad de mantenimiento hace referencia a una aplicación o un proceso que ayuda a mantener el estado y el rendimiento de un equipo Windows.
ms.assetid: 1D38341B-15AA-422F-AED1-647FCDE69E2E
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 456383eeb75c3b29bf575357d4b17d5f8a66234b
ms.sourcegitcommit: 857e701bbd35004661bb047e1f24622af9ff1dd7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/19/2020
ms.locfileid: "104421562"
---
# <a name="automatic-maintenance"></a>Mantenimiento automático

La actividad de mantenimiento hace referencia a una aplicación o un proceso que ayuda a mantener el estado y el rendimiento de un equipo Windows. El mantenimiento incluye mantener actualizados el sistema operativo Windows (SO) y las aplicaciones, comprobar la seguridad y ejecutar exámenes de malware. La administración automática de Windows (WAM) es un conjunto de mejoras en la API de Programador de tareas que puede usar para vincular las aplicaciones a la programación de mantenimiento de Windows. En concreto, el WAM le permite agregar actividades que requieren una programación normal, pero que no tienen requisitos de tiempo exactos. En su lugar, WAM se basa en el sistema operativo para elegir el momento adecuado para activar la tarea a lo largo del día. El sistema elige esas horas en función de un impacto mínimo en el usuario, el rendimiento del equipo y la eficacia energética.

## <a name="how-scheduled-maintenance-works"></a>Cómo funciona el mantenimiento programado

Programador de tareas tareas de mantenimiento son tareas oportunistas que se ejecutan cuando el equipo está inactivo y con corriente alterna. Uno de los principales objetivos de las tareas de mantenimiento es minimizar el impacto en el equipo mediante la programación de mantenimiento solo cuando el equipo está conectado a la corriente alterna e inactivo (es decir, cuando no se usa o se aleja del equipo). Hoy en día, la idea del mantenimiento es que el equipo trabaje con la mínima interrupción para el usuario. Por lo tanto, la hora de mantenimiento de estilo anterior (hablaremos más sobre esto en la sección reactivación **&mdash; diaria de mantenimiento automático** más adelante en este tema) se ha mejorado con el fin de aprovechar estos períodos inactivos. Aunque se puede seguir aprovechando la hora de mantenimiento, la ejecución del mantenimiento oportunista es mejor para el mantenimiento del sistema.

Es posible que la tarea se encuentre en caso de que el equipo no dedique mucho tiempo a estar inactivos y con corriente alterna. Asegúrese de que el escenario seguirá proporcionando valor al usuario, incluso si se retrasa. Si el usuario está utilizando activamente el equipo, el sistema aplaza el mantenimiento hasta un momento posterior. El sistema también suspende cualquier tarea de mantenimiento en ejecución si el usuario vuelve a usar el equipo.

El sistema reinicia una tarea de mantenimiento suspendida durante el siguiente período de inactividad; sin embargo, el sistema no suspenderá ninguna tarea marcada como crítica. En su lugar, el sistema permite que se complete una tarea crítica, independientemente de la acción del usuario.

Debido a la naturaleza de la programación, es posible que algunas tareas programadas no finalicen: quizás haya demasiados eventos programados para caber en la ventana de mantenimiento de una hora, o quizás el equipo simplemente no esté encendido. En tales casos, puede definir una tarea con una fecha límite. Una fecha límite se define como un período de tiempo periódico en el que el sistema debe realizar correctamente la tarea al menos una vez.

Si una tarea pierde una fecha límite, el programador de mantenimiento seguirá intentando ejecutar la tarea durante la ventana de mantenimiento. Además, el programador no se limitará a un límite de tiempo de 1 hora normal. En su lugar, el programador amplía la duración de la ventana de mantenimiento para completar la tarea retrasada.

Una vez que el sistema completa la tarea (incluso con un código de error de error), el intento se considera correcto. Después de un intento correcto, Scheduler se restablece a la programación de mantenimiento normal e intentará realizar la tarea durante el siguiente período.

## <a name="automatic-maintenancemdashdaily-wakeup"></a>Activación diaria de mantenimiento automático &mdash;

En Windows 7, una tarea de mantenimiento se ejecuta exclusivamente durante la *hora de mantenimiento*, el valor predeterminado es 3 AM y se puede configurar mediante Directiva de grupo. El equipo se reactivará del modo de espera, ejecutará las tareas de mantenimiento y volverá a entrar en suspensión. Esta sesión diaria se limitó a una duración máxima de 1 hora por intento. Esto permitiría que el sistema realizara el mantenimiento diariamente, a partir de las 3 AM de forma predeterminada. Tenga en cuenta que el usuario puede volver a programar la hora a la que se desencadena el mantenimiento mediante la configuración de estas opciones.

Con la llegada de los equipos portátiles y el intenso enfoque en la duración de la batería, las máquinas ya no están configuradas para permitir la activación S3 en la mayoría de los casos y, por lo general, de Doze a S4 (hibernación) tan pronto como sea posible, para ahorrar batería. En respuesta a estos cambios, Programador de tareas (> Win7) ejecuta tareas de mantenimiento siempre que están pendientes y el equipo está inactivo y con corriente alterna.

Esta configuración se puede configurar en el panel de control.

Abra el **Panel**  >  **de control sistema y**  >  **seguridad de seguridad y** mantenimiento  >  **mantenimiento automático**.

Por lo tanto, en función de cómo se configuran las máquinas y las tareas, es posible que el comportamiento de la activación diaria no se produzca de la manera esperada debido a esta nueva configuración. En primer lugar, puede determinar si el equipo es compatible con S3 o compatible con CS (modo de espera conectado).
Para ello, abra un símbolo del sistema de Power Shell con privilegios elevados y ejecute el siguiente comando.

```console
powercfg /a
```

Hora de mantenimiento, si la máquina está configurada correctamente, sigue funcionando, pero si no es así,
  - Compruebe la configuración del BIOS para la configuración de reactivación. 
  - Compruebe si permitir temporizador de activación está habilitado en las opciones de energía.
    Vaya a **Panel de control**  >  opciones **de hardware y sonido**  >  **Opciones de energía**  >  **Editar configuración del plan**  >  **Cambiar configuración avanzada de energía** > haga clic en **suspender**  >  **permitir temporizador de activación**.
  - Compruebe si la tarea programada está configurada con lo siguiente.
      * MaintenanceSettings: la tarea debe configurarse con período, fecha límite.
      * Habilitada: la tarea debe estar habilitada.
      * WakeToRun: la tarea debe tener permiso para reactivar la máquina.
  - Para programar las reactivaciones desde CS, el equipo debe ser compatible con AOAC.
  - Para programar activaciones en máquinas S3,
      * Compruebe si el equipo entró en S3 con corriente alterna.
      * El sistema debe tener **habilitada la reactivación** en Directiva de grupo para el mantenimiento.
 
El modo de espera conectado es el estado del sistema que puede escribir un sistema compatible con AOAC.

Vea las diferencias entre el modo de espera moderno y S3 en el tema [modo de espera moderno frente a S3](/windows-hardware/design/device-experiences/modern-standby-vs-s3).

## <a name="defining-an-automatic-maintenance-task"></a>Definir una tarea de mantenimiento automática

Puede convertir cualquier Programador de tareas tarea en una tarea de mantenimiento. Para ello, debe confirmar que la aplicación se puede suspender. A continuación, debe extender la definición de tarea con los nuevos elementos [**MaintenanceSettings**](taskschedulerschema-maintenancesettings-maintenancesettingstype-element.md) y [**AllowStartOnDemand**](taskschedulerschema-allowstartondemand-settingstype-element.md) .

La principal preocupación de la creación de una tarea de mantenimiento es asegurarse de que el sistema puede suspender y reiniciar la tarea. Probablemente, el sistema suspenderá una tarea de mantenimiento varias veces; por lo tanto, debe asegurarse de que la aplicación pueda guardar su propio estado y, a continuación, reanudar en un momento arbitrario. Esto garantiza que el sistema no realiza la misma parte de la tarea varias veces.

Una vez que se haya asegurado de que la aplicación se puede suspender y reanudar correctamente, puede usar los elementos **MaintenanceSettings** y **AllowStartOnDemand** para definir la programación. **MaintenanceSettings** se define según el período, la fecha límite y la exclusividad.

-   El **período** es obligatorio y define la frecuencia con que se debe realizar la tarea. Normalmente, esto se define en términos de un ciclo de varios días, como "una vez cada 5 días". Un período debe ser al menos un día, lo que significa que no se puede programar una tarea para que se produzca varias veces en un día.
-   La **fecha límite** es opcional y define cuánto tiempo puede no realizarse el programador para completar la tarea antes de notificar al usuario o realizar el mantenimiento de emergencia. La fecha límite debe ser mayor que el período, lo que significa que el sistema debe tener la oportunidad de intentar la tarea al menos una vez antes de notificar al usuario.
-   Además, una tarea de mantenimiento se puede definir opcionalmente como *exclusiva*. Una tarea exclusiva se ejecuta de forma independiente de otras tareas de mantenimiento. Normalmente, una tarea exclusiva es aquella que usa una gran cantidad de recursos, como una gran cantidad de tiempo de CPU o acceso exclusivo a una base de datos. El sistema completa todas las tareas de mantenimiento no exclusivas antes de iniciar una tarea exclusiva. Por lo tanto, debe declarar una tarea como exclusiva solo cuando sea necesario.

En cambio, **AllowStartOnDemand** simplemente indica que el sistema o el usuario puede iniciar la tarea en cualquier momento. Esto permite al sistema iniciar la tarea durante el mantenimiento normal. De lo contrario, tendría que establecer un desencadenador único para la tarea.
