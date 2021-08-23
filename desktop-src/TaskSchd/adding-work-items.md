---
title: Agregar elementos de trabajo
description: Hay dos maneras de agregar elementos de trabajo a la carpeta Tareas programadas. Puede crear un nuevo elemento de trabajo dentro de la carpeta o puede agregar un elemento de trabajo existente a la carpeta.
ms.assetid: fad5e813-a2e9-40af-97a9-4f92debf1808
keywords:
- elementos de trabajo Programador de tareas , agregar
- tareas Programador de tareas , agregar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc964b620a01b0f1114240dcb11f275fa8faffc37e8264d8854cb60191628943
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119621165"
---
# <a name="adding-work-items"></a>Agregar elementos de trabajo

Hay dos maneras de agregar [*elementos de trabajo*](w.md) a la carpeta Tareas [*programadas*](s.md). Puede crear un nuevo elemento de trabajo dentro de la carpeta o puede agregar un elemento de trabajo existente a la carpeta.

> [!Note]  
> Actualmente, solo se pueden agregar objetos de tarea a la carpeta Tareas programadas. Al agregar una tarea, debe conocer los identificadores de la clase de tarea y la interfaz de [**tarea ITask**](/windows/desktop/api/Mstask/nn-mstask-itask).

 

Para crear nuevos elementos de trabajo, llame al [**método ITaskScheduler::NewWorkItem.**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-newworkitem) Este método crea un nuevo objeto de elemento de trabajo con el nombre que proporcione y agrega el elemento de trabajo a la carpeta Tareas programadas. Al crear un nuevo elemento de trabajo, el Programador de tareas asigna la memoria necesaria para el nuevo objeto.

Para agregar elementos de trabajo existentes a la carpeta Scheduled Tasks, llame al [**método ITaskScheduler::AddWorkItem.**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-addworkitem) Al llamar a este método, debe crear el objeto .

Los nombres que proporcione para los elementos de trabajo deben ser únicos dentro de la carpeta Tareas programadas. Si ya existe un elemento de trabajo con el mismo nombre cuando se llama al método [**ITaskScheduler::NewWorkItem**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-newworkitem) o al método [**ITaskScheduler::AddWorkItem,**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-addworkitem) el método devuelve un **error ERROR FILE \_ \_ EXISTS.** Para obtener más información, vea [Creating a Task Using NewWorkItem Example](creating-a-task-using-newworkitem-example.md).

 

 




