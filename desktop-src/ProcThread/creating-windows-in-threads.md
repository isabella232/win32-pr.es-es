---
description: Cualquier subproceso puede crear una ventana.
ms.assetid: 27f04f9f-52d9-46d6-8e06-9b032682b7c7
title: Crear ventanas en subprocesos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aebcde45ca37696b6dbc90e639f630a689498b04
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677863"
---
# <a name="creating-windows-in-threads"></a><span data-ttu-id="8b9b5-103">Crear ventanas en subprocesos</span><span class="sxs-lookup"><span data-stu-id="8b9b5-103">Creating Windows in Threads</span></span>

<span data-ttu-id="8b9b5-104">Cualquier subproceso puede crear una ventana.</span><span class="sxs-lookup"><span data-stu-id="8b9b5-104">Any thread can create a window.</span></span> <span data-ttu-id="8b9b5-105">El subproceso que crea la ventana es el propietario de la ventana y su cola de mensajes asociada.</span><span class="sxs-lookup"><span data-stu-id="8b9b5-105">The thread that creates the window owns the window and its associated message queue.</span></span> <span data-ttu-id="8b9b5-106">Por lo tanto, el subproceso debe proporcionar un bucle de mensajes para procesar los mensajes en su cola de mensajes.</span><span class="sxs-lookup"><span data-stu-id="8b9b5-106">Therefore, the thread must provide a message loop to process the messages in its message queue.</span></span> <span data-ttu-id="8b9b5-107">Además, debe usar [**MsgWaitForMultipleObjects**](/windows/desktop/api/winuser/nf-winuser-msgwaitformultipleobjects) o [**MsgWaitForMultipleObjectsEx**](/windows/desktop/api/winuser/nf-winuser-msgwaitformultipleobjectsex) en ese subproceso, en lugar de las demás [funciones de espera](/windows/desktop/Sync/wait-functions), para que pueda procesar los mensajes.</span><span class="sxs-lookup"><span data-stu-id="8b9b5-107">In addition, you must use [**MsgWaitForMultipleObjects**](/windows/desktop/api/winuser/nf-winuser-msgwaitformultipleobjects) or [**MsgWaitForMultipleObjectsEx**](/windows/desktop/api/winuser/nf-winuser-msgwaitformultipleobjectsex) in that thread, rather than the other [wait functions](/windows/desktop/Sync/wait-functions), so that it can process messages.</span></span> <span data-ttu-id="8b9b5-108">De lo contrario, se puede producir un interbloqueo del sistema cuando se envía un mensaje al subproceso mientras está esperando.</span><span class="sxs-lookup"><span data-stu-id="8b9b5-108">Otherwise, the system can become deadlocked when the thread is sent a message while it is waiting.</span></span>

<span data-ttu-id="8b9b5-109">La función [**AttachThreadInput**](/windows/desktop/api/Winuser/nf-winuser-attachthreadinput) se puede usar para permitir que un conjunto de subprocesos comparta el mismo estado de entrada.</span><span class="sxs-lookup"><span data-stu-id="8b9b5-109">The [**AttachThreadInput**](/windows/desktop/api/Winuser/nf-winuser-attachthreadinput) function can be used to allow a set of threads to share the same input state.</span></span> <span data-ttu-id="8b9b5-110">Al compartir el estado de entrada, los subprocesos comparten su concepto de la ventana activa.</span><span class="sxs-lookup"><span data-stu-id="8b9b5-110">By sharing input state, the threads share their concept of the active window.</span></span> <span data-ttu-id="8b9b5-111">Al hacerlo, un subproceso siempre puede activar la ventana de otro subproceso.</span><span class="sxs-lookup"><span data-stu-id="8b9b5-111">By doing this, one thread can always activate another thread's window.</span></span> <span data-ttu-id="8b9b5-112">Esta función también es útil para compartir el estado del foco, el estado de la captura del mouse, el estado del teclado y el estado del orden Z de la ventana entre las ventanas creadas por subprocesos diferentes cuyo estado de entrada es compartido.</span><span class="sxs-lookup"><span data-stu-id="8b9b5-112">This function is also useful for sharing focus state, mouse capture state, keyboard state, and window Z-order state among windows created by different threads whose input state is shared.</span></span>

<span data-ttu-id="8b9b5-113">Para obtener información sobre cómo crear ventanas, vea [clases de Windows](../winmsg/window-classes.md).</span><span class="sxs-lookup"><span data-stu-id="8b9b5-113">For information about creating windows, see [Windows Classes](../winmsg/window-classes.md).</span></span>

 

 
