---
description: La función CreateTimerQueue crea una cola para los temporizadores.
ms.assetid: ee85a6c3-3a1d-4f94-9112-cb8247b2a189
title: Colas de temporizador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80ad2f94612c234b3ec0d1d75fa723c4e86e6fc0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667506"
---
# <a name="timer-queues"></a><span data-ttu-id="1c126-103">Colas de temporizador</span><span class="sxs-lookup"><span data-stu-id="1c126-103">Timer Queues</span></span>

<span data-ttu-id="1c126-104">La función [**CreateTimerQueue**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-createtimerqueue) crea una cola para los temporizadores.</span><span class="sxs-lookup"><span data-stu-id="1c126-104">The [**CreateTimerQueue**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-createtimerqueue) function creates a queue for timers.</span></span> <span data-ttu-id="1c126-105">Los temporizadores de esta cola, conocidos como *temporizadores de cola de temporizador*, son objetos ligeros que permiten especificar una función de devolución de llamada a la que se llamará cuando llegue el momento de vencimiento especificado.</span><span class="sxs-lookup"><span data-stu-id="1c126-105">Timers in this queue, known as *timer-queue timers*, are lightweight objects that enable you to specify a callback function to be called when the specified due time arrives.</span></span> <span data-ttu-id="1c126-106">Un subproceso del [grupo de subprocesos](../procthread/thread-pooling.md)realiza la operación de espera.</span><span class="sxs-lookup"><span data-stu-id="1c126-106">The wait operation is performed by a thread in the [thread pool](../procthread/thread-pooling.md).</span></span>

<span data-ttu-id="1c126-107">Para agregar un temporizador a la cola, llame a la función [**CreateTimerQueueTimer**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-createtimerqueuetimer) .</span><span class="sxs-lookup"><span data-stu-id="1c126-107">To add a timer to the queue, call the [**CreateTimerQueueTimer**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-createtimerqueuetimer) function.</span></span> <span data-ttu-id="1c126-108">Para actualizar un temporizador de cola de temporizador, llame a la función [**ChangeTimerQueueTimer**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-changetimerqueuetimer) .</span><span class="sxs-lookup"><span data-stu-id="1c126-108">To update a timer-queue timer, call the [**ChangeTimerQueueTimer**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-changetimerqueuetimer) function.</span></span> <span data-ttu-id="1c126-109">Puede especificar una función de devolución de llamada que va a ejecutar un subproceso de trabajo desde el grupo de subprocesos cuando expire el temporizador.</span><span class="sxs-lookup"><span data-stu-id="1c126-109">You can specify a callback function to be executed by a worker thread from the thread pool when the timer expires.</span></span>

<span data-ttu-id="1c126-110">Para cancelar un temporizador pendiente, llame a la función [**DeleteTimerQueueTimer**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-deletetimerqueuetimer) .</span><span class="sxs-lookup"><span data-stu-id="1c126-110">To cancel a pending timer, call the [**DeleteTimerQueueTimer**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-deletetimerqueuetimer) function.</span></span> <span data-ttu-id="1c126-111">Cuando haya terminado con la cola de temporizadores, llame a la función [**DeleteTimerQueueEx**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-deletetimerqueueex) para eliminar la cola del temporizador.</span><span class="sxs-lookup"><span data-stu-id="1c126-111">When you are finished with the queue of timers, call the [**DeleteTimerQueueEx**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-deletetimerqueueex) function to delete the timer queue.</span></span> <span data-ttu-id="1c126-112">Los temporizadores pendientes de la cola se cancelan y se eliminan.</span><span class="sxs-lookup"><span data-stu-id="1c126-112">Any pending timers in the queue are canceled and deleted.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1c126-113">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="1c126-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1c126-114">Usar colas de temporizador</span><span class="sxs-lookup"><span data-stu-id="1c126-114">Using Timer Queues</span></span>](using-timer-queues.md)
</dt> </dl>

 

 
