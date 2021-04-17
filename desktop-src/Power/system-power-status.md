---
description: El estado de alimentación del sistema indica si el origen de energía de un equipo es una batería de sistema o corriente alterna. En el caso de los equipos que usan baterías, el estado de alimentación del sistema también indica la duración de la batería y si la batería se está cargando.
ms.assetid: b9a5e7de-a603-4bd9-b854-1e58572c3b2b
title: Estado de la alimentación del sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e221142b5d39a4cb5bc49dbe85271c99837d0a20
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677886"
---
# <a name="system-power-status"></a><span data-ttu-id="64f6e-104">Estado de la alimentación del sistema</span><span class="sxs-lookup"><span data-stu-id="64f6e-104">System Power Status</span></span>

<span data-ttu-id="64f6e-105">El estado de alimentación del sistema indica si el origen de energía de un equipo es una batería de sistema o corriente alterna.</span><span class="sxs-lookup"><span data-stu-id="64f6e-105">The system power status indicates whether the source of power for a computer is a system battery or AC power.</span></span> <span data-ttu-id="64f6e-106">En el caso de los equipos que usan baterías, el estado de alimentación del sistema también indica la duración de la batería y si la batería se está cargando.</span><span class="sxs-lookup"><span data-stu-id="64f6e-106">For computers that use batteries, the system power status also indicates how much battery life remains and whether the battery is charging.</span></span>

<span data-ttu-id="64f6e-107">La información de energía se recupera registrando las notificaciones de configuración de energía a través de la función [**RegisterPowerSettingNotification**](/windows/desktop/api/WinUser/nf-winuser-registerpowersettingnotification) .</span><span class="sxs-lookup"><span data-stu-id="64f6e-107">Power information is retrieved by registering for power setting notifications through the [**RegisterPowerSettingNotification**](/windows/desktop/api/WinUser/nf-winuser-registerpowersettingnotification) function.</span></span> <span data-ttu-id="64f6e-108">Esta función permite a las aplicaciones registrarse para una configuración de energía específica y recibir una notificación cuando cambien.</span><span class="sxs-lookup"><span data-stu-id="64f6e-108">This function allows applications to register for specific power settings and be notified when they change.</span></span>

> [!Note]  
> <span data-ttu-id="64f6e-109">Para consultar la información de estado de energía sin notificaciones, use [**CallNtPowerInformation**](/windows/desktop/api/Powerbase/nf-powerbase-callntpowerinformation).</span><span class="sxs-lookup"><span data-stu-id="64f6e-109">To query for power status information without notifications, use [**CallNtPowerInformation**](/windows/desktop/api/Powerbase/nf-powerbase-callntpowerinformation).</span></span>

 

<span data-ttu-id="64f6e-110">Las aplicaciones y los controladores instalables normalmente usan el estado de alimentación del sistema para determinar si la operación continua es viable.</span><span class="sxs-lookup"><span data-stu-id="64f6e-110">Applications and installable drivers typically use the system power status to determine whether continued operation is feasible.</span></span> <span data-ttu-id="64f6e-111">Por ejemplo, antes de que una aplicación realice operaciones en segundo plano, como comprimir o paginar un archivo, debe comprobar si el sistema tiene baterías.</span><span class="sxs-lookup"><span data-stu-id="64f6e-111">For example, before an application performs background operations such as compressing or paginating a file, it should check whether the system is on batteries.</span></span> <span data-ttu-id="64f6e-112">Otro ejemplo: una aplicación que inicia una operación larga debe comprobar el estado para determinar si existe suficiente energía de la batería para completar la operación.</span><span class="sxs-lookup"><span data-stu-id="64f6e-112">As another example, an application that is beginning a lengthy operation should check the status to determine whether enough battery power exists to complete the operation.</span></span>

<span data-ttu-id="64f6e-113">De forma predeterminada, el sistema no consulta las aplicaciones o los controladores durante las transiciones de suspensión.</span><span class="sxs-lookup"><span data-stu-id="64f6e-113">By default, the system does not query applications or drivers during sleep transitions.</span></span>

> [!Note]  
> <span data-ttu-id="64f6e-114">Si la alimentación es baja, una aplicación puede solicitar la intervención del usuario o solicitar que el sistema se suspenda.</span><span class="sxs-lookup"><span data-stu-id="64f6e-114">If power is low, an application can request user intervention or request that the system suspend itself.</span></span> <span data-ttu-id="64f6e-115">Puede suspender el funcionamiento del sistema mediante la función [**SetSuspendState**](/windows/desktop/api/PowrProf/nf-powrprof-setsuspendstate) .</span><span class="sxs-lookup"><span data-stu-id="64f6e-115">You can suspend system operation by using the [**SetSuspendState**](/windows/desktop/api/PowrProf/nf-powrprof-setsuspendstate) function.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="64f6e-116">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="64f6e-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="64f6e-117">Acerca de la administración de energía</span><span class="sxs-lookup"><span data-stu-id="64f6e-117">About Power Management</span></span>](about-power-management.md)
</dt> </dl>

 

 



