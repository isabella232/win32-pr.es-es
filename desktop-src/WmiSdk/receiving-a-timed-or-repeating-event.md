---
description: Un evento de tiempo o repetición es un evento que se produce en una fecha y hora específicas, o repetidamente a intervalos regulares. Por ejemplo, un evento puede producirse a medianoche solo en el 2 de diciembre de 2015 o una vez cada semana los martes a las 2:31 P.M.
ms.assetid: 369bf2d7-8350-4089-8e11-28e2b641f792
ms.tgt_platform: multiple
title: Recibir un evento de tiempo o repetición
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c395f77bdc9295b394fdee3b6d48894e07b09cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276149"
---
# <a name="receiving-a-timed-or-repeating-event"></a><span data-ttu-id="be5e5-104">Recibir un evento de tiempo o repetición</span><span class="sxs-lookup"><span data-stu-id="be5e5-104">Receiving a Timed or Repeating Event</span></span>

<span data-ttu-id="be5e5-105">Un evento de tiempo o repetición es un evento que se produce en una fecha y hora específicas, o repetidamente a intervalos regulares.</span><span class="sxs-lookup"><span data-stu-id="be5e5-105">A timed or repeating event is an event that occurs at one specific time and date, or repeatedly at regular intervals.</span></span> <span data-ttu-id="be5e5-106">Por ejemplo, un evento puede producirse a medianoche solo en el 2 de diciembre de 2015 o una vez cada semana los martes a las 2:31 P.M.</span><span class="sxs-lookup"><span data-stu-id="be5e5-106">For example, an event can occur at midnight on only December 2, 2015, or one time each week on Tuesdays at 2:31 PM.</span></span>

<span data-ttu-id="be5e5-107">En la tabla siguiente se enumeran las distintas clases que se usan para crear un evento de tiempo o repetición.</span><span class="sxs-lookup"><span data-stu-id="be5e5-107">The following table lists the different classes that are used to create a timed or repeating event.</span></span>



| <span data-ttu-id="be5e5-108">Clase</span><span class="sxs-lookup"><span data-stu-id="be5e5-108">Class</span></span>                                                                                            | <span data-ttu-id="be5e5-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="be5e5-109">Description</span></span>                                                                                                                                                                                                         |
|--------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="be5e5-110">[**Win32 \_ LocalTime**](/previous-versions/windows/desktop/wmitimepprov/win32-localtime) o [ **Win32 \_ UTCTime**](/previous-versions/windows/desktop/wmitimepprov/win32-utctime)</span><span class="sxs-lookup"><span data-stu-id="be5e5-110">[**Win32\_LocalTime**](/previous-versions/windows/desktop/wmitimepprov/win32-localtime) or [**Win32\_UTCTime**](/previous-versions/windows/desktop/wmitimepprov/win32-utctime)</span></span> | <span data-ttu-id="be5e5-111">Modelo de eventos estándar de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="be5e5-111">Standard Microsoft event model.</span></span><br/> <span data-ttu-id="be5e5-112">Para obtener más información, vea [crear un evento de temporizador con Win32 \_ localtime o Win32 \_ UTCTime](creating-a-timer-event-with-win32-localtime-or-win32-utctime.md).</span><span class="sxs-lookup"><span data-stu-id="be5e5-112">For more information, see [Creating a Timer Event with Win32\_LocalTime or Win32\_UTCTime](creating-a-timer-event-with-win32-localtime-or-win32-utctime.md).</span></span><br/> |
| [<span data-ttu-id="be5e5-113">**\_\_TimerInstruction**</span><span class="sxs-lookup"><span data-stu-id="be5e5-113">**\_\_TimerInstruction**</span></span>](--timerinstruction.md)                                               | <span data-ttu-id="be5e5-114">Técnica heredada.</span><span class="sxs-lookup"><span data-stu-id="be5e5-114">Legacy technique.</span></span><br/> <span data-ttu-id="be5e5-115">Para obtener más información, vea [crear un evento de temporizador con \_ TimerInstruction](creating-a-timer-event-with---timerinstruction.md).</span><span class="sxs-lookup"><span data-stu-id="be5e5-115">For more information, see [Creating a Timer Event with \_TimerInstruction](creating-a-timer-event-with---timerinstruction.md).</span></span><br/>                                             |



 

<span data-ttu-id="be5e5-116">Si desea programar una tarea o un trabajo para que se produzca en un momento determinado o de forma repetida, utilice la clase [**Win32 \_ ScheduledJob**](/windows/desktop/CIMWin32Prov/win32-scheduledjob) y sus métodos.</span><span class="sxs-lookup"><span data-stu-id="be5e5-116">If you want to schedule a task or job to occur at a specific time or repeatedly, use the [**Win32\_ScheduledJob**](/windows/desktop/CIMWin32Prov/win32-scheduledjob) class and its methods.</span></span> <span data-ttu-id="be5e5-117">Esta clase representa un trabajo creado con el comando AT en una ventana de comandos desde el **Inicio** y después **Ejecutar**, o desde las **tareas programadas** del **Panel de control**.</span><span class="sxs-lookup"><span data-stu-id="be5e5-117">This class represents a job created with the AT command in a command window from **Start** and then **Run**, or from the **Scheduled Tasks** in **Control Panel**.</span></span>

 

