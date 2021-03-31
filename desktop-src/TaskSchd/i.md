---
title: I (Programador de tareas)
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 84a58712-72fb-47c6-8d92-e2a0ebfccaca
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8492f707a171c6811b4702d2a07de47d29482a8
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "104533645"
---
# <a name="i-task-scheduler"></a>I (Programador de tareas)

A B C D [E](e.md) F G H I J K L M N o [p](p.md) Q R [s](s.md) [T](t.md) U V [W](w.md) X Y Z

<dl> <dt>

<span id="_msb_idle_conditions_gly"></span><span id="_MSB_IDLE_CONDITIONS_GLY"></span>**condiciones de inactividad**
</dt> <dd>

Un período de tiempo en el que no hay ninguna entrada de usuario en el equipo. Las condiciones de inactividad están asociadas a la hora de inicio programada para la tarea.

Estas condiciones se establecen mediante una llamada a [**IScheduledWorkItem:: SetFlags**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-setflags).

</dd> <dt>

<span id="_msb_idle_triggers_gly"></span><span id="_MSB_IDLE_TRIGGERS_GLY"></span>**desencadenadores inactivos**
</dt> <dd>

Desencadenador basado en eventos que se desencadena cuando el equipo pasa a estar inactivo durante un período de tiempo específico.

Los desencadenadores inactivos se crean estableciendo \_ el \_ miembro de tipo de desencadenador de tarea de la estructura del [**\_ desencadenador de tarea**](/windows/desktop/api/Mstask/ns-mstask-task_trigger) \_ \_ en desencadenador \_ de evento de tarea en \_ inactivo.

</dd> <dt>

<span id="_msb_idle_wait_time_gly"></span><span id="_MSB_IDLE_WAIT_TIME_GLY"></span>**tiempo de espera de inactividad**
</dt> <dd>

Intervalo de tiempo (en minutos) utilizado por un desencadenador inactivo o una condición de inactividad. Los desencadenadores inactivos son desencadenadores basados en eventos que no están asociados a una hora programada. Las condiciones de inactividad están asociadas a la hora de inicio programada para la tarea.

El tiempo de inactividad se establece mediante una llamada a [**IScheduledWorkItem:: SetIdleWait**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-setidlewait).

</dd> </dl>

 

 




