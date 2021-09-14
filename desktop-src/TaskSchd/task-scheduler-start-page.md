---
title: Programador de tareas para desarrolladores
description: El Programador de tareas permite realizar automáticamente tareas rutinarias en un equipo elegido. Programador de tareas hace esto supervisando los criterios que elija (denominados desencadenadores) y, a continuación, ejecutando las tareas cuando se cumplen esos criterios.
ms.assetid: 15970a51-c139-48b8-b82b-605728d0f386
keywords:
- Programador de tareas para desarrolladores
- Programador de tareas desarrollo
- Desarrollo con Programador de tareas
- Programador de tareas, página del portal
ms.topic: article
ms.date: 09/09/2021
ms.openlocfilehash: cce9e1898be5de60517e4bb269df20e44f432b23
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127253400"
---
# <a name="task-scheduler-for-developers"></a>Programador de tareas para desarrolladores

> [!IMPORTANT]
> Este tema y los otros temas de esta sección son para un público desarrollador. Si desea usar el componente Programador de tareas en su capacidad como administrador o un administrador de TI Professional, consulte [Programador de tareas](/dynamics365/business-central/dev-itpro/developer/devenv-task-scheduler).

## <a name="about-the-task-scheduler"></a>Acerca de la Programador de tareas

El Programador de tareas permite realizar automáticamente tareas rutinarias en un equipo elegido. Programador de tareas hace esto supervisando los criterios que elija (denominados desencadenadores) y, a continuación, ejecutando las tareas cuando se cumplen esos criterios.

Puede usar el Programador de tareas para ejecutar tareas como iniciar una aplicación, enviar un mensaje de correo electrónico o mostrar un cuadro de mensaje. Las tareas se pueden programar para ejecutarse en respuesta a estos eventos o desencadenadores. 

- Cuando se produce un evento del sistema específico.
- En un momento específico.
- En un momento específico según una programación diaria.
- En un momento específico de una programación semanal.
- En un momento específico según una programación mensual.
- A una hora específica según una programación mensual del día de la semana.
- Cuando el equipo entra en un estado de inactividad.
- Cuando se registra la tarea.
- Cuando se inicia el sistema.
- Cuando un usuario inicia sesión.
- Cuando una sesión de Terminal Server cambia de estado.

## <a name="developers"></a>Desarrolladores

El Programador de tareas proporciona API en estos formularios.

- Programador de tareas 2.0: se proporcionan interfaces y objetos para C++ y para el desarrollo de scripting, respectivamente.
- Programador de tareas 1.0: se proporcionan interfaces para el desarrollo de C++.

## <a name="run-time-requirements"></a>Requisitos de tiempo de ejecución

El Programador de tareas requiere los siguientes sistemas operativos.

- Programador de tareas 2.0: el cliente requiere Windows Vista o superior. El servidor Windows Server 2008 o posterior.
- Programador de tareas 1.0: el cliente requiere Windows Vista o Windows XP. El servidor Windows Server 2008 o Windows Server 2003.

## <a name="in-this-section"></a>En esta sección

| Tema | Descripción |
|-|-|
| [Novedades de Programador de tareas](what-s-new-in-task-scheduler.md) | Resumen de la nueva funcionalidad introducida por el Programador de tareas. |
| [Acerca de la Programador de tareas](about-the-task-scheduler.md) | Información conceptual general sobre Programador de tareas API. |
| [Uso del Programador de tareas](using-the-task-scheduler.md) | Ejemplos de código que muestran cómo usar Programador de tareas API. |
| [Programador de tareas referencia](task-scheduler-reference.md) | Información de referencia detallada para Programador de tareas API y el esquema Programador de tareas datos. |