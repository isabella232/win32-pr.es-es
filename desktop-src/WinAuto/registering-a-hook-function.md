---
title: Registro de una función de enlace
description: Las aplicaciones cliente reciben WinEvents en una función de devolución de llamada WinEventProc. La aplicación define las acciones realizadas por la función de devolución de llamada, pero la sintaxis debe ser como se especifica en el prototipo.
ms.assetid: 7e999335-6a41-4d22-82ef-1a8dd6cb656e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5b1f39a535b366af72b1034cc9344171d253ea0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903291"
---
# <a name="registering-a-hook-function"></a><span data-ttu-id="5336a-104">Registro de una función de enlace</span><span class="sxs-lookup"><span data-stu-id="5336a-104">Registering a Hook Function</span></span>

<span data-ttu-id="5336a-105">Las aplicaciones cliente reciben WinEvents en una función de devolución de llamada [*WinEventProc*](/windows/desktop/api/Winuser/nc-winuser-wineventproc) .</span><span class="sxs-lookup"><span data-stu-id="5336a-105">Client applications receive WinEvents in a [*WinEventProc*](/windows/desktop/api/Winuser/nc-winuser-wineventproc) callback function.</span></span> <span data-ttu-id="5336a-106">La aplicación define las acciones realizadas por la función de devolución de llamada, pero la sintaxis debe ser como se especifica en el prototipo.</span><span class="sxs-lookup"><span data-stu-id="5336a-106">The actions performed by the callback function are defined by the application, but the syntax must be as specified in the prototype.</span></span>

<span data-ttu-id="5336a-107">Antes de poder recibir eventos, la función se debe registrar llamando a [**SetWinEventHook**](/windows/desktop/api/Winuser/nf-winuser-setwineventhook).</span><span class="sxs-lookup"><span data-stu-id="5336a-107">Before it can receive events, the function must be registered by calling [**SetWinEventHook**](/windows/desktop/api/Winuser/nf-winuser-setwineventhook).</span></span> <span data-ttu-id="5336a-108">El cliente puede llamar a **SetWinEventHook** más de una vez para registrar distintas funciones de enlace o para establecer eventos adicionales para una función de enlace registrada previamente.</span><span class="sxs-lookup"><span data-stu-id="5336a-108">The client can call **SetWinEventHook** more than once to register different hook functions, or to set additional events for a previously registered hook function.</span></span>

<span data-ttu-id="5336a-109">Al llamar a [**SetWinEventHook**](/windows/desktop/api/Winuser/nf-winuser-setwineventhook) , el cliente especifica qué eventos se van a recibir y cómo recibirlos.</span><span class="sxs-lookup"><span data-stu-id="5336a-109">When calling [**SetWinEventHook**](/windows/desktop/api/Winuser/nf-winuser-setwineventhook) the client specifies which events to receive and how to receive them.</span></span> <span data-ttu-id="5336a-110">El cliente puede elegir:</span><span class="sxs-lookup"><span data-stu-id="5336a-110">The client can choose to:</span></span>

-   <span data-ttu-id="5336a-111">Recibir todos los eventos o un conjunto específico de eventos.</span><span class="sxs-lookup"><span data-stu-id="5336a-111">Receive all events or a specific set of events.</span></span>
-   <span data-ttu-id="5336a-112">Recibir eventos de todos los subprocesos o de un subproceso específico.</span><span class="sxs-lookup"><span data-stu-id="5336a-112">Receive events from all threads or from a specific thread.</span></span>
-   <span data-ttu-id="5336a-113">Recibir eventos de todos los procesos o de un proceso específico.</span><span class="sxs-lookup"><span data-stu-id="5336a-113">Receive events from all processes or from a specific process.</span></span>
-   <span data-ttu-id="5336a-114">Controlar eventos en proceso o fuera de proceso.</span><span class="sxs-lookup"><span data-stu-id="5336a-114">Handle events in process or out of process.</span></span>

<span data-ttu-id="5336a-115">Cuando se genera un evento que coincide con los criterios especificados, el sistema llama a la función de devolución de llamada de [*WinEventProc*](/windows/desktop/api/Winuser/nc-winuser-wineventproc) del cliente (o al "procedimiento de enlace").</span><span class="sxs-lookup"><span data-stu-id="5336a-115">When an event is generated that matches the specified criteria, the system calls the client's [*WinEventProc*](/windows/desktop/api/Winuser/nc-winuser-wineventproc) callback function (or "hook procedure").</span></span> <span data-ttu-id="5336a-116">Los parámetros que recibe la función de enlace indican al cliente sobre la ventana, el objeto y el posible elemento secundario que generó el evento.</span><span class="sxs-lookup"><span data-stu-id="5336a-116">The parameters that the hook function receives tell the client about the window, object, and possible child element that generated the event.</span></span> <span data-ttu-id="5336a-117">Un cliente usa estos parámetros en una llamada de recuperación de objeto, como [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent).</span><span class="sxs-lookup"><span data-stu-id="5336a-117">A client uses these parameters in an object retrieval call, such as [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent).</span></span>

 

 




