---
title: Operaciones de eventos de temporizador
description: Operaciones de eventos de temporizador
ms.assetid: a2b75e84-4da8-449f-b02a-4ffc4846eef5
keywords:
- temporizadores multimedia, eventos
- temporizadores, eventos
- timeSetEvent función)
- timeKillEvent función)
- iniciar eventos de temporizador
- eventos de temporizador único
- eventos de temporizador periódicos
- Cancelando eventos de temporizador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1d4329a6d6c55e9e8dd6c56fab5d1e3ca938833
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103789748"
---
# <a name="timer-event-operations"></a><span data-ttu-id="b4eac-111">Operaciones de eventos de temporizador</span><span class="sxs-lookup"><span data-stu-id="b4eac-111">Timer Event Operations</span></span>

<span data-ttu-id="b4eac-112">Una vez establecida la resolución del temporizador de la aplicación, puede iniciar los eventos del temporizador mediante la función [**timeSetEvent**](/previous-versions//dd757634(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="b4eac-112">After you have established your application's timer resolution, you can start timer events by using the [**timeSetEvent**](/previous-versions//dd757634(v=vs.85)) function.</span></span> <span data-ttu-id="b4eac-113">Esta función devuelve un identificador de temporizador que se puede usar para detener o identificar eventos de temporizador.</span><span class="sxs-lookup"><span data-stu-id="b4eac-113">This function returns a timer identifier that can be used to stop or identify timer events.</span></span> <span data-ttu-id="b4eac-114">Uno de los parámetros de la función es la dirección de una función de devolución de llamada [**TimeProc**](/previous-versions//dd757631(v=vs.85)) a la que se llama cuando tiene lugar el evento del temporizador.</span><span class="sxs-lookup"><span data-stu-id="b4eac-114">One of the function's parameters is the address of a [**TimeProc**](/previous-versions//dd757631(v=vs.85)) callback function that is called when the timer event takes place.</span></span>

<span data-ttu-id="b4eac-115">Hay dos tipos de eventos de temporizador: *único* y *periódico*.</span><span class="sxs-lookup"><span data-stu-id="b4eac-115">There are two types of timer events: *single* and *periodic*.</span></span> <span data-ttu-id="b4eac-116">Un solo evento de temporizador se produce una vez, después de un número de milisegundos especificado.</span><span class="sxs-lookup"><span data-stu-id="b4eac-116">A single timer event occurs once, after a specified number of milliseconds.</span></span> <span data-ttu-id="b4eac-117">Un evento de temporizador periódico se produce cada vez que transcurre un número especificado de milisegundos.</span><span class="sxs-lookup"><span data-stu-id="b4eac-117">A periodic timer event occurs every time a specified number of milliseconds elapses.</span></span> <span data-ttu-id="b4eac-118">El intervalo entre eventos periódicos se denomina *retraso de evento*.</span><span class="sxs-lookup"><span data-stu-id="b4eac-118">The interval between periodic events is called an *event delay*.</span></span> <span data-ttu-id="b4eac-119">Los eventos de temporizador periódicos con un retraso de evento de 10 milisegundos o menos consumen una parte significativa de los recursos de CPU.</span><span class="sxs-lookup"><span data-stu-id="b4eac-119">Periodic timer events with an event delay of 10 milliseconds or less consume a significant portion of CPU resources.</span></span>

<span data-ttu-id="b4eac-120">La relación entre la resolución de un evento de temporizador y la duración del retraso de evento es importante en los eventos de temporizador.</span><span class="sxs-lookup"><span data-stu-id="b4eac-120">The relationship between the resolution of a timer event and the length of the event delay is important in timer events.</span></span> <span data-ttu-id="b4eac-121">Por ejemplo, si especifica una resolución de 5 y un retraso de evento de 100, los servicios de temporizador notifican a la función de devolución de llamada después de un intervalo comprendido entre 95 y 105 milisegundos.</span><span class="sxs-lookup"><span data-stu-id="b4eac-121">For example, if you specify a resolution of 5 and an event delay of 100, the timer services notify the callback function after an interval ranging from 95 to 105 milliseconds.</span></span>

<span data-ttu-id="b4eac-122">Puede cancelar un evento de temporizador activo en cualquier momento mediante la función [**timeKillEvent**](/previous-versions//dd757630(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="b4eac-122">You can cancel an active timer event at any time by using the [**timeKillEvent**](/previous-versions//dd757630(v=vs.85)) function.</span></span> <span data-ttu-id="b4eac-123">Asegúrese de cancelar los temporizadores pendientes antes de liberar la memoria que contiene la función de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="b4eac-123">Be sure to cancel any outstanding timers before freeing the memory containing the callback function.</span></span>

> [!Note]  
> <span data-ttu-id="b4eac-124">El temporizador multimedia se ejecuta en su propio subproceso.</span><span class="sxs-lookup"><span data-stu-id="b4eac-124">The multimedia timer runs in its own thread.</span></span>

 

 

 