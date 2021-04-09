---
title: Programador de tareas para desarrolladores
description: El Programador de tareas permite realizar automáticamente las tareas rutinarias en un equipo seleccionado. Programador de tareas lo hace mediante la supervisión de los criterios que elija (denominados desencadenadores) y la ejecución de las tareas cuando se cumplan esos criterios.
ms.assetid: 15970a51-c139-48b8-b82b-605728d0f386
keywords:
- Programador de tareas para desarrolladores
- Programador de tareas para el desarrollo
- Desarrollo con Programador de tareas
- Programador de tareas, página del portal
ms.topic: article
ms.date: 10/18/2019
ms.openlocfilehash: dfbfb76145e38003e7c501b98c817f4aaca3ff09
ms.sourcegitcommit: 087843ef08ddcd8bce9ed647b610035925da2b3e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/19/2019
ms.locfileid: "104148865"
---
# <a name="task-scheduler-for-developers"></a>Programador de tareas para desarrolladores

> [!IMPORTANT]
> Este tema y los otros temas de esta sección son para un público del desarrollador. Si desea usar el componente de Programador de tareas en su capacidad como administrador o como profesional de ti, consulte [programador de tareas](/dynamics365/business-central/dev-itpro/developer/devenv-task-scheduler).

## <a name="about-the-task-scheduler"></a>Acerca del Programador de tareas

El Programador de tareas permite realizar automáticamente las tareas rutinarias en un equipo seleccionado. Programador de tareas lo hace mediante la supervisión de los criterios que elija (denominados desencadenadores) y la ejecución de las tareas cuando se cumplan esos criterios.

Puede utilizar la Programador de tareas para ejecutar tareas como el inicio de una aplicación, el envío de un mensaje de correo electrónico o la presentación de un cuadro de mensaje. Las tareas se pueden programar para que se ejecuten en respuesta a estos eventos o desencadenadores. 

- Cuando se produce un evento de sistema específico.
- En un momento dado.
- A una hora específica en una programación diaria.
- En un momento específico según una programación semanal.
- A una hora específica en una programación mensual.
- A una hora específica de una programación mensual de día de la semana.
- Cuando el equipo entra en un estado de inactividad.
- Cuando se registra la tarea.
- Cuando se arranca el sistema.
- Cuando un usuario inicia sesión.
- Cuando una sesión de Terminal Server cambia de estado.

## <a name="developers"></a>Desarrolladores

El Programador de tareas proporciona las API de estos formatos.

- Programador de tareas 2,0: se proporcionan interfaces y objetos para C++ y para el desarrollo de scripting, respectivamente.
- Programador de tareas 1,0: se proporcionan interfaces para el desarrollo de C++.

## <a name="run-time-requirements"></a>Requisitos de tiempo de ejecución

El Programador de tareas requiere los siguientes sistemas operativos.

- Programador de tareas 2,0: el cliente requiere Windows Vista o posterior. El servidor requiere Windows Server 2008 o posterior.
- Programador de tareas 1,0: el cliente requiere Windows Vista o Windows XP. El servidor requiere Windows Server 2008 o Windows Server 2003.

## <a name="in-this-section"></a>En esta sección

| Tema | Descripción |
|-|-|
| [Novedades de Programador de tareas](what-s-new-in-task-scheduler.md) | Resumen de las nuevas funciones introducidas por el Programador de tareas. |
| [Acerca del Programador de tareas](about-the-task-scheduler.md) | Información conceptual general sobre la API de Programador de tareas. |
| [Usar el Programador de tareas](using-the-task-scheduler.md) | Ejemplos de código que muestran cómo usar las API de Programador de tareas. |
| [Referencia de Programador de tareas](task-scheduler-reference.md) | Información de referencia detallada sobre las API de Programador de tareas y el esquema de Programador de tareas. |