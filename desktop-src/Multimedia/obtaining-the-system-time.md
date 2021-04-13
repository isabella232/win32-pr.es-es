---
title: Obtener la hora del sistema
description: Obtener la hora del sistema
ms.assetid: 33dfcd56-11d9-45b9-b983-8354526101a7
keywords:
- temporizadores multimedia, hora del sistema
- temporizadores, hora del sistema
- hora del sistema
- timeGetTime función)
- timeGetSystemTime función)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89fdcc905569a500afe689658676137c460d19d8
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104487571"
---
# <a name="obtaining-the-system-time"></a><span data-ttu-id="b3ee9-108">Obtener la hora del sistema</span><span class="sxs-lookup"><span data-stu-id="b3ee9-108">Obtaining the System Time</span></span>

<span data-ttu-id="b3ee9-109">Normalmente, antes de que una aplicación empiece a usar los servicios de temporizador multimedia, recupera la *hora actual del sistema*.</span><span class="sxs-lookup"><span data-stu-id="b3ee9-109">Typically, before an application begins using the multimedia timer services, it retrieves the current *system time*.</span></span> <span data-ttu-id="b3ee9-110">La hora del sistema es el tiempo, en milisegundos, transcurrido desde que se inició el sistema operativo Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="b3ee9-110">The system time is the time, in milliseconds, since the Microsoft Windows operating system was started.</span></span> <span data-ttu-id="b3ee9-111">Puede usar la función [**timeGetTime**](/windows/desktop/api/TimeAPI/nf-timeapi-timegettime) o [**timeGetSystemTime**](/windows/desktop/api/TimeAPI/nf-timeapi-timegetsystemtime) para recuperar la hora del sistema.</span><span class="sxs-lookup"><span data-stu-id="b3ee9-111">You can use the [**timeGetTime**](/windows/desktop/api/TimeAPI/nf-timeapi-timegettime) or [**timeGetSystemTime**](/windows/desktop/api/TimeAPI/nf-timeapi-timegetsystemtime) function to retrieve the system time.</span></span> <span data-ttu-id="b3ee9-112">Estas dos funciones son muy similares: **timeGetTime** devuelve la hora del sistema y **timeGetSystemTime** rellena una estructura [**MMTIME**](/previous-versions//dd757347(v=vs.85)) con la hora del sistema.</span><span class="sxs-lookup"><span data-stu-id="b3ee9-112">These two functions are very similar: **timeGetTime** returns the system time, and **timeGetSystemTime** fills an [**MMTIME**](/previous-versions//dd757347(v=vs.85)) structure with the system time.</span></span>

 

 