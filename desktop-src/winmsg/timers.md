---
description: En este tema se describen los temporizadores. Un temporizador es una rutina interna que mide repetidamente un intervalo especificado, en milisegundos.
ms.assetid: vs|winui|~\winui\windowsuserinterface\windowing\timers.htm
title: Temporizadores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5fa44be05acc09eafed550a200ed6bc61f79daa2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105707225"
---
# <a name="timers"></a><span data-ttu-id="cf54a-104">Temporizadores</span><span class="sxs-lookup"><span data-stu-id="cf54a-104">Timers</span></span>

<span data-ttu-id="cf54a-105">Un temporizador es una rutina interna que mide repetidamente un intervalo especificado, en milisegundos.</span><span class="sxs-lookup"><span data-stu-id="cf54a-105">A timer is an internal routine that repeatedly measures a specified interval, in milliseconds.</span></span>

### <a name="in-this-section"></a><span data-ttu-id="cf54a-106">En esta sección</span><span class="sxs-lookup"><span data-stu-id="cf54a-106">In This Section</span></span>



| <span data-ttu-id="cf54a-107">Nombre</span><span class="sxs-lookup"><span data-stu-id="cf54a-107">Name</span></span>                                   | <span data-ttu-id="cf54a-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="cf54a-108">Description</span></span>                                                                                                               |
|----------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cf54a-109">Acerca de los temporizadores</span><span class="sxs-lookup"><span data-stu-id="cf54a-109">About Timers</span></span>](about-timers.md)       | <span data-ttu-id="cf54a-110">Describe cómo crear, identificar, establecer y eliminar temporizadores.</span><span class="sxs-lookup"><span data-stu-id="cf54a-110">Describes how to create, identify, set, and delete timers.</span></span><br/>                                                     |
| [<span data-ttu-id="cf54a-111">Usar temporizadores</span><span class="sxs-lookup"><span data-stu-id="cf54a-111">Using Timers</span></span>](using-timers.md)       | <span data-ttu-id="cf54a-112">Describe cómo crear y destruir temporizadores, y cómo usar un temporizador para interceptar la entrada del mouse a intervalos especificados.</span><span class="sxs-lookup"><span data-stu-id="cf54a-112">Discusses how to create and destroy timers, and how to use a timer to trap mouse input at specified intervals.</span></span><br/> |
| [<span data-ttu-id="cf54a-113">Referencia del temporizador</span><span class="sxs-lookup"><span data-stu-id="cf54a-113">Timer Reference</span></span>](timer-reference.md) | <span data-ttu-id="cf54a-114">Contiene la referencia de la API.</span><span class="sxs-lookup"><span data-stu-id="cf54a-114">Contains the API reference.</span></span><br/>                                                                                    |



 

### <a name="timer-functions"></a><span data-ttu-id="cf54a-115">Funciones de temporizador</span><span class="sxs-lookup"><span data-stu-id="cf54a-115">Timer Functions</span></span>



| <span data-ttu-id="cf54a-116">Nombre</span><span class="sxs-lookup"><span data-stu-id="cf54a-116">Name</span></span>                           | <span data-ttu-id="cf54a-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="cf54a-117">Description</span></span>                                                                                                                                                                                                                                                              |
|--------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cf54a-118">**KillTimer**</span><span class="sxs-lookup"><span data-stu-id="cf54a-118">**KillTimer**</span></span>](/windows/win32/api/winuser/nf-winuser-killtimer) | <span data-ttu-id="cf54a-119">Destruye el temporizador especificado.</span><span class="sxs-lookup"><span data-stu-id="cf54a-119">Destroys the specified timer.</span></span> <br/>                                                                                                                                                                                                                                |
| [<span data-ttu-id="cf54a-120">**SetTimer**</span><span class="sxs-lookup"><span data-stu-id="cf54a-120">**SetTimer**</span></span>](/windows/win32/api/winuser/nf-winuser-settimer)   | <span data-ttu-id="cf54a-121">Crea un temporizador con el valor de tiempo de espera especificado.</span><span class="sxs-lookup"><span data-stu-id="cf54a-121">Creates a timer with the specified time-out value.</span></span><br/>                                                                                                                                                                                                            |
| [<span data-ttu-id="cf54a-122">*TimerProc*</span><span class="sxs-lookup"><span data-stu-id="cf54a-122">*TimerProc*</span></span>](/windows/win32/api/winuser/nc-winuser-timerproc)   | <span data-ttu-id="cf54a-123">Función de devolución de llamada definida por la aplicación que procesa los mensajes [**\_ del temporizador de WM**](wm-timer.md) .</span><span class="sxs-lookup"><span data-stu-id="cf54a-123">An application-defined callback function that processes [**WM\_TIMER**](wm-timer.md) messages.</span></span> <span data-ttu-id="cf54a-124">El tipo **TIMERPROC** define un puntero a esta función de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="cf54a-124">The **TIMERPROC** type defines a pointer to this callback function.</span></span> <span data-ttu-id="cf54a-125">[*TimerProc*](/windows/win32/api/winuser/nc-winuser-timerproc) es un marcador de posición para el nombre de la función definida por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="cf54a-125">[*TimerProc*](/windows/win32/api/winuser/nc-winuser-timerproc) is a placeholder for the application-defined function name.</span></span> <br/> |



 

### <a name="timer-notifications"></a><span data-ttu-id="cf54a-126">Notificaciones del temporizador</span><span class="sxs-lookup"><span data-stu-id="cf54a-126">Timer Notifications</span></span>



| <span data-ttu-id="cf54a-127">Nombre</span><span class="sxs-lookup"><span data-stu-id="cf54a-127">Name</span></span>                          | <span data-ttu-id="cf54a-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="cf54a-128">Description</span></span>                                                                                                                                                                                     |
|-------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cf54a-129">**temporizador de WM \_**</span><span class="sxs-lookup"><span data-stu-id="cf54a-129">**WM\_TIMER**</span></span>](wm-timer.md) | <span data-ttu-id="cf54a-130">Se envía a la cola de mensajes del subproceso de instalación cuando expira un temporizador.</span><span class="sxs-lookup"><span data-stu-id="cf54a-130">Posted to the installing thread's message queue when a timer expires.</span></span> <span data-ttu-id="cf54a-131">El mensaje se expone mediante la función [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) o [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea) .</span><span class="sxs-lookup"><span data-stu-id="cf54a-131">The message is posted by the [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) or [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea) function.</span></span> <br/> |



 

 

 
