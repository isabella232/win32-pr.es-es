---
description: Para el usuario, la ventaja de la multitarea es la capacidad de tener varias aplicaciones abiertas y en funcionamiento al mismo tiempo. Por ejemplo, un usuario puede editar un archivo con una aplicación mientras otra aplicación vuelve a calcular una hoja de cálculo.
ms.assetid: 163291ce-78bd-43ee-98ca-564ce91c520c
title: Ventajas de la multitarea
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 119e327ba07a226a8422c61a100d6ff000b48ed9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677876"
---
# <a name="advantages-of-multitasking"></a><span data-ttu-id="73d78-104">Ventajas de la multitarea</span><span class="sxs-lookup"><span data-stu-id="73d78-104">Advantages of Multitasking</span></span>

<span data-ttu-id="73d78-105">Para el usuario, la ventaja de la multitarea es la capacidad de tener varias aplicaciones abiertas y en funcionamiento al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="73d78-105">To the user, the advantage of multitasking is the ability to have several applications open and working at the same time.</span></span> <span data-ttu-id="73d78-106">Por ejemplo, un usuario puede editar un archivo con una aplicación mientras otra aplicación vuelve a calcular una hoja de cálculo.</span><span class="sxs-lookup"><span data-stu-id="73d78-106">For example, a user can edit a file with one application while another application is recalculating a spreadsheet.</span></span>

<span data-ttu-id="73d78-107">Para el desarrollador de la aplicación, la ventaja de la multitarea es la capacidad de crear aplicaciones que usan más de un proceso y de crear procesos que usan más de un subproceso de ejecución.</span><span class="sxs-lookup"><span data-stu-id="73d78-107">To the application developer, the advantage of multitasking is the ability to create applications that use more than one process and to create processes that use more than one thread of execution.</span></span> <span data-ttu-id="73d78-108">Por ejemplo, un proceso puede tener un subproceso de interfaz de usuario que administra las interacciones con el usuario (entrada del teclado y del mouse) y los subprocesos de trabajo que realizan otras tareas mientras el subproceso de la interfaz de usuario espera a que los usuarios realicen la acción.</span><span class="sxs-lookup"><span data-stu-id="73d78-108">For example, a process can have a user interface thread that manages interactions with the user (keyboard and mouse input), and worker threads that perform other tasks while the user interface thread waits for user input.</span></span> <span data-ttu-id="73d78-109">Si asigna una prioridad más alta al subproceso de la interfaz de usuario, la aplicación tendrá mayor capacidad de respuesta al usuario, mientras que los subprocesos de trabajo usan el procesador de forma eficaz durante las ocasiones en las que no hay ninguna entrada de usuario.</span><span class="sxs-lookup"><span data-stu-id="73d78-109">If you give the user interface thread a higher priority, the application will be more responsive to the user, while the worker threads use the processor efficiently during the times when there is no user input.</span></span>

 

 



