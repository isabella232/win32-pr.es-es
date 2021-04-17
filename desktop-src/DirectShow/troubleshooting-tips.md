---
description: Sugerencias para la solución de problemas
ms.assetid: e87ad3bd-07ae-4b9d-b465-2ce4688bdd83
title: Sugerencias para la solución de problemas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c0280702c7ce2131d1252ec75b8bee4be231e29
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667638"
---
# <a name="troubleshooting-tips"></a><span data-ttu-id="d40c4-103">Sugerencias para la solución de problemas</span><span class="sxs-lookup"><span data-stu-id="d40c4-103">Troubleshooting Tips</span></span>

<span data-ttu-id="d40c4-104">Las siguientes sugerencias le ayudarán a evitar interbloqueos o bloqueos en la aplicación de DirectShow.</span><span class="sxs-lookup"><span data-stu-id="d40c4-104">This following tips will help you to avoid deadlocks or crashes in your DirectShow application.</span></span>

<span data-ttu-id="d40c4-105">**Objetos globales**</span><span class="sxs-lookup"><span data-stu-id="d40c4-105">**Global Objects**</span></span>

<span data-ttu-id="d40c4-106">Un objeto de C++ global no debe crear objetos de DirectShow en su método de constructor ni publicarlos en su método de destructor.</span><span class="sxs-lookup"><span data-stu-id="d40c4-106">A global C++ object should not create DirectShow objects in its constructor method or release them in its destructor method.</span></span> <span data-ttu-id="d40c4-107">Esto puede hacer que la aplicación se bloquee indefinidamente, por el siguiente motivo:</span><span class="sxs-lookup"><span data-stu-id="d40c4-107">Doing so can cause the application to block indefinitely, for the following reason:</span></span>

<span data-ttu-id="d40c4-108">Los subprocesos no pueden salir mientras se encuentren dentro de la función de punto de entrada de un archivo DLL.</span><span class="sxs-lookup"><span data-stu-id="d40c4-108">Threads cannot exit while inside a DLL's entry-point function.</span></span> <span data-ttu-id="d40c4-109">El kernel 32 mantiene un bloqueo de proceso global durante la función de punto de entrada y el bloqueo impide que el subproceso se salga.</span><span class="sxs-lookup"><span data-stu-id="d40c4-109">Kernel 32 holds a global process lock during the entry-point function, and the lock prevents the thread from exiting.</span></span> <span data-ttu-id="d40c4-110">Dado que algunos objetos de DirectShow poseen subprocesos, se pueden bloquear si se liberan desde una función de punto de entrada de DLL.</span><span class="sxs-lookup"><span data-stu-id="d40c4-110">Because some DirectShow objects own threads, they can block if released from inside a DLL entry-point function.</span></span> <span data-ttu-id="d40c4-111">Si una aplicación tiene un objeto global de C++, la DLL en tiempo de ejecución de C llama al destructor del objeto cuando se descarga el archivo DLL.</span><span class="sxs-lookup"><span data-stu-id="d40c4-111">If an application has a global C++ object, the C runtime DLL calls the object's destructor when the DLL is unloaded.</span></span> <span data-ttu-id="d40c4-112">Si el destructor libera objetos de DirectShow, puede bloquearse como resultado.</span><span class="sxs-lookup"><span data-stu-id="d40c4-112">If the destructor releases DirectShow objects, it can block as a result.</span></span>

<span data-ttu-id="d40c4-113">Por motivos similares, un archivo DLL no debe crear ni liberar objetos de DirectShow en su rutina de punto de entrada.</span><span class="sxs-lookup"><span data-stu-id="d40c4-113">For similar reasons, a DLL should not create or release DirectShow objects in its entry point routine.</span></span>

<span data-ttu-id="d40c4-114">**Liberar interfaces**</span><span class="sxs-lookup"><span data-stu-id="d40c4-114">**Releasing Interfaces**</span></span>

<span data-ttu-id="d40c4-115">Debe liberar todos los punteros de la interfaz de DirectShow mientras la aplicación sigue procesando los mensajes antes de salir del bucle de mensajes.</span><span class="sxs-lookup"><span data-stu-id="d40c4-115">You should release all DirectShow interface pointers while your application is still processing messages, before it exits the message loop.</span></span> <span data-ttu-id="d40c4-116">De lo contrario, podría ver varias aserciones, porque algunos objetos de DirectShow envían mensajes durante sus rutinas de limpieza.</span><span class="sxs-lookup"><span data-stu-id="d40c4-116">Otherwise, you might see various asserts, because some DirectShow objects send messages during their clean-up routines.</span></span>

<span data-ttu-id="d40c4-117">(Como consecuencia, si usa la clase ATL **CWindowImpl** , no espere hasta que **OnFinalMessage** libere las interfaces.</span><span class="sxs-lookup"><span data-stu-id="d40c4-117">(As a corollary, if you are using the ATL **CWindowImpl** class, do not wait until **OnFinalMessage** to free the interfaces.</span></span> <span data-ttu-id="d40c4-118">En su lugar, libere al controlar el mensaje de \_ cierre de WM).</span><span class="sxs-lookup"><span data-stu-id="d40c4-118">Instead, free them when you handle the WM\_CLOSE message.)</span></span>

<span data-ttu-id="d40c4-119">**Recuentos de referencias**</span><span class="sxs-lookup"><span data-stu-id="d40c4-119">**Reference Counts**</span></span>

<span data-ttu-id="d40c4-120">Cuando se descarga la versión de depuración de Quartz.dll, comprueba si los objetos de DirectShow tienen recuentos de referencias que no se han liberado.</span><span class="sxs-lookup"><span data-stu-id="d40c4-120">When the debug version of Quartz.dll unloads, it checks whether any DirectShow objects have reference counts that were not released.</span></span> <span data-ttu-id="d40c4-121">Si es así, se produce una aserción:</span><span class="sxs-lookup"><span data-stu-id="d40c4-121">If so, it throws an assertion:</span></span>


```C++
g_cFGObjects == 0 
```



<span data-ttu-id="d40c4-122">Cuando se produce un error en esta aserción, significa que la aplicación ha perdido un recuento de referencias.</span><span class="sxs-lookup"><span data-stu-id="d40c4-122">When this assertion fails, it means your application has leaked a reference count.</span></span> <span data-ttu-id="d40c4-123">Revise el código y asegúrese de que libera todos los punteros de interfaz.</span><span class="sxs-lookup"><span data-stu-id="d40c4-123">Review your code and make sure that you release all interface pointers.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d40c4-124">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d40c4-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d40c4-125">Depurar en DirectShow</span><span class="sxs-lookup"><span data-stu-id="d40c4-125">Debugging in DirectShow</span></span>](debugging-in-directshow.md)
</dt> </dl>

 

 



