---
title: Enumerar tareas y Mostrar información de tareas
description: La visualización de información acerca de una tarea, como el nombre de la tarea, el estado o la última vez que se ejecutó la tarea, se realiza mediante la enumeración de tareas en ejecución o las tareas de una carpeta de tareas y la visualización de la información deseada.
ms.assetid: a0305089-89ff-42b7-b3f1-99a6484d2e5e
keywords:
- enumerar tareas Programador de tareas
- Programador de tareas ejemplos Programador de tareas, enumerar tareas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58e4c1bbad0a1fa8892e38a001ff54e665f0c144
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103772816"
---
# <a name="enumerating-tasks-and-displaying-task-information"></a><span data-ttu-id="e2710-105">Enumerar tareas y Mostrar información de tareas</span><span class="sxs-lookup"><span data-stu-id="e2710-105">Enumerating Tasks and Displaying Task Information</span></span>

<span data-ttu-id="e2710-106">La visualización de información acerca de una tarea, como el nombre de la tarea, el estado o la última vez que se ejecutó la tarea, se realiza mediante la enumeración de tareas en ejecución o las tareas de una carpeta de tareas y la visualización de la información deseada.</span><span class="sxs-lookup"><span data-stu-id="e2710-106">Displaying information about a task, such as the task name, state, or the last time the task was run, is done by enumerating through running tasks or the tasks in a task folder and displaying the desired information.</span></span>

## <a name="accessing-properties-of-registered-tasks"></a><span data-ttu-id="e2710-107">Obtener acceso a las propiedades de las tareas registradas</span><span class="sxs-lookup"><span data-stu-id="e2710-107">Accessing Properties of Registered Tasks</span></span>

<span data-ttu-id="e2710-108">Para mostrar el valor de la propiedad de una tarea registrada, debe conectarse al servicio de Programador de tareas y, a continuación, obtener una instancia de la carpeta de tareas que contenga las tareas sobre las que desea obtener información.</span><span class="sxs-lookup"><span data-stu-id="e2710-108">To display a registered task's property value, you must connect to the Task Scheduler service, and then get an instance of the task folder that contains the tasks you want information about.</span></span> <span data-ttu-id="e2710-109">A continuación, obtiene una colección de todas las tareas registradas en la carpeta de tareas.</span><span class="sxs-lookup"><span data-stu-id="e2710-109">You then get a collection of all the registered tasks in the task folder.</span></span> <span data-ttu-id="e2710-110">A continuación, se enumeran las tareas registradas y se obtiene y se muestra un valor de propiedad para cada tarea.</span><span class="sxs-lookup"><span data-stu-id="e2710-110">Then you enumerate through each registered task and get and display a property value for each task.</span></span>

## <a name="accessing-properties-of-running-tasks"></a><span data-ttu-id="e2710-111">Obtener acceso a las propiedades de las tareas en ejecución</span><span class="sxs-lookup"><span data-stu-id="e2710-111">Accessing Properties of Running Tasks</span></span>

<span data-ttu-id="e2710-112">Para mostrar el valor de la propiedad de una tarea en ejecución, debe conectarse al servicio Programador de tareas y, a continuación, obtener una colección de todas las tareas en ejecución (incluidas o excluidas las tareas ocultas).</span><span class="sxs-lookup"><span data-stu-id="e2710-112">To display a running task's property value, you must connect to the Task Scheduler service, and then get a collection of all the running tasks (including or excluding hidden tasks).</span></span> <span data-ttu-id="e2710-113">A continuación, se enumeran las tareas en ejecución y se obtiene y se muestra un valor de propiedad para cada tarea.</span><span class="sxs-lookup"><span data-stu-id="e2710-113">Then you enumerate through each running task and get and display a property value for each task.</span></span>

## <a name="example"></a><span data-ttu-id="e2710-114">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="e2710-114">Example</span></span>

<span data-ttu-id="e2710-115">En los siguientes ejemplos se enumeran las tareas y se muestra el nombre y el estado de las tareas:</span><span class="sxs-lookup"><span data-stu-id="e2710-115">The following examples enumerate tasks and display the name and state of the tasks:</span></span>

-   [<span data-ttu-id="e2710-116">Mostrar nombres de tarea y Estados (scripting)</span><span class="sxs-lookup"><span data-stu-id="e2710-116">Displaying Task Names and States (Scripting)</span></span>](displaying-task-names-and-state--scripting-.md)
-   [<span data-ttu-id="e2710-117">Mostrar nombres de tarea y estado (C++)</span><span class="sxs-lookup"><span data-stu-id="e2710-117">Displaying Task Names and State (C++)</span></span>](displaying-task-names-and-state--c---.md)

## <a name="related-topics"></a><span data-ttu-id="e2710-118">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e2710-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e2710-119">Usar el Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="e2710-119">Using the Task Scheduler</span></span>](using-the-task-scheduler.md)
</dt> </dl>

 

 




