---
title: Agregar elementos de trabajo
description: Hay dos maneras de agregar elementos de trabajo al Tasksfolder programado. Puede crear un nuevo elemento de trabajo dentro de la carpeta o puede Agregar un elemento de trabajo existente a la carpeta.
ms.assetid: fad5e813-a2e9-40af-97a9-4f92debf1808
keywords:
- Programador de tareas de elementos de trabajo, agregar
- tareas Programador de tareas, agregar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 722f776fd36933995cfd9b5a85612b52dae63f7b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105676201"
---
# <a name="adding-work-items"></a>Agregar elementos de trabajo

Hay dos maneras de agregar [*elementos de trabajo*](w.md) al [*Tasksfolder programado*](s.md). Puede crear un nuevo elemento de trabajo dentro de la carpeta o puede Agregar un elemento de trabajo existente a la carpeta.

> [!Note]  
> Actualmente, solo se pueden agregar objetos de tarea a la carpeta tareas programadas. Al agregar una tarea, debe conocer los identificadores de la clase de tarea y la interfaz de tarea [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask).

 

Cree nuevos elementos de trabajo llamando al método [**ITaskScheduler:: NewWorkItem**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-newworkitem) . Este método crea un nuevo objeto de elemento de trabajo con el nombre que se proporciona y agrega el elemento de trabajo a la carpeta tareas programadas. Cuando se crea un nuevo elemento de trabajo, el Programador de tareas asigna la memoria necesaria para el nuevo objeto.

Para agregar elementos de trabajo existentes a la carpeta tareas programadas, llame al método [**ITaskScheduler:: AddWorkItem**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-addworkitem) . Cuando llame a este método, debe crear el objeto.

Los nombres que proporcione para los elementos de trabajo deben ser únicos en la carpeta tareas programadas. Si ya existe un elemento de trabajo con el mismo nombre cuando se llama al método [**ITaskScheduler:: NewWorkItem**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-newworkitem) o al método [**ITaskScheduler:: AddWorkItem**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-addworkitem) , el método devuelve un error de **\_ archivo \_ de error** . Para obtener más información, vea [crear una tarea mediante el ejemplo de NewWorkItem](creating-a-task-using-newworkitem-example.md).

 

 




