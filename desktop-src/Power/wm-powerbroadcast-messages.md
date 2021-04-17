---
description: El sistema difunde un mensaje a todas las aplicaciones y controladores instalables siempre que se produzca un evento de administración de energía.
ms.assetid: a64ed11a-43d6-41f7-aabd-5dca2a2b4a12
title: Mensajes de WM_POWERBROADCAST
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f70c5848ec5d71666c26fcd4b5b161e31465543
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677877"
---
# <a name="wm_powerbroadcast-messages"></a><span data-ttu-id="0d1cc-103">\_Mensajes POWERBROADCAST de WM</span><span class="sxs-lookup"><span data-stu-id="0d1cc-103">WM\_POWERBROADCAST Messages</span></span>

<span data-ttu-id="0d1cc-104">El sistema difunde un mensaje a todas las aplicaciones y controladores instalables siempre que se produzca un evento de administración de energía.</span><span class="sxs-lookup"><span data-stu-id="0d1cc-104">The system broadcasts a message to all applications and installable drivers whenever a power management event occurs.</span></span> <span data-ttu-id="0d1cc-105">El sistema difunde estos eventos a través del mensaje de [**\_ POWERBROADCAST de WM**](wm-powerbroadcast.md) , estableciendo el parámetro *wParam* en el evento de administración de energía adecuado.</span><span class="sxs-lookup"><span data-stu-id="0d1cc-105">The system broadcasts these events through the [**WM\_POWERBROADCAST**](wm-powerbroadcast.md) message, setting the *wParam* parameter to the appropriate power management event.</span></span> <span data-ttu-id="0d1cc-106">Por ejemplo, el evento [PBT \_ APMPOWERSTATUSCHANGE](pbt-apmpowerstatuschange.md) indica un cambio de estado de energía del sistema.</span><span class="sxs-lookup"><span data-stu-id="0d1cc-106">For example, the [PBT\_APMPOWERSTATUSCHANGE](pbt-apmpowerstatuschange.md) event indicates a system power status change.</span></span> <span data-ttu-id="0d1cc-107">Debe asegurarse de que la aplicación responde correctamente al mensaje de **\_ POWERBROADCAST de WM** .</span><span class="sxs-lookup"><span data-stu-id="0d1cc-107">You must ensure that your application responds properly to the **WM\_POWERBROADCAST** message.</span></span>

<span data-ttu-id="0d1cc-108">El sistema difunde un evento [PBT \_ APMSUSPEND](pbt-apmsuspend.md) inmediatamente antes de suspender la operación.</span><span class="sxs-lookup"><span data-stu-id="0d1cc-108">The system broadcasts a [PBT\_APMSUSPEND](pbt-apmsuspend.md) event immediately before suspending operation.</span></span> <span data-ttu-id="0d1cc-109">Esto proporciona a las aplicaciones y controladores una última oportunidad para prepararse para el evento.</span><span class="sxs-lookup"><span data-stu-id="0d1cc-109">This gives applications and drivers one last chance to prepare for the event.</span></span> <span data-ttu-id="0d1cc-110">En muchos casos, el sistema difunde estos mensajes sin solicitar permiso para hacerlo.</span><span class="sxs-lookup"><span data-stu-id="0d1cc-110">In many cases, the system broadcasts these messages without requesting permission to do so.</span></span> <span data-ttu-id="0d1cc-111">Esto sucede, por ejemplo, si una aplicación fuerza la suspensión con la función [**SetSuspendState**](/windows/desktop/api/PowrProf/nf-powrprof-setsuspendstate) .</span><span class="sxs-lookup"><span data-stu-id="0d1cc-111">This happens, for example, if an application forces suspension with the [**SetSuspendState**](/windows/desktop/api/PowrProf/nf-powrprof-setsuspendstate) function.</span></span>

<span data-ttu-id="0d1cc-112">El sistema difunde el evento [PBT \_ APMRESUMESUSPEND](pbt-apmresumesuspend.md) o [PBT \_ APMRESUMECRITICAL](pbt-apmresumecritical.md) cuando se ha restaurado la operación del sistema.</span><span class="sxs-lookup"><span data-stu-id="0d1cc-112">The system broadcasts the [PBT\_APMRESUMESUSPEND](pbt-apmresumesuspend.md) or [PBT\_APMRESUMECRITICAL](pbt-apmresumecritical.md) event when system operation has been restored.</span></span> <span data-ttu-id="0d1cc-113">Si una aplicación ha recibido un evento [PBT \_ APMSUSPEND](pbt-apmsuspend.md) antes de que se suspendiera el equipo, recibirá el \_ evento PBT APMRESUMESUSPEND.</span><span class="sxs-lookup"><span data-stu-id="0d1cc-113">If an application received a [PBT\_APMSUSPEND](pbt-apmsuspend.md) event before the computer was suspended, it will receive the PBT\_APMRESUMESUSPEND event.</span></span> <span data-ttu-id="0d1cc-114">De lo contrario, recibirá el \_ evento PBT APMRESUMECRITICAL.</span><span class="sxs-lookup"><span data-stu-id="0d1cc-114">Otherwise, it will receive the PBT\_APMRESUMECRITICAL event.</span></span>

<span data-ttu-id="0d1cc-115">El sistema envía un evento [PBT \_ POWERSETTINGCHANGE](pbt-powersettingchange.md) a las aplicaciones que se han registrado para el evento específico mediante [**RegisterPowerSettingNotification**](/windows/desktop/api/WinUser/nf-winuser-registerpowersettingnotification).</span><span class="sxs-lookup"><span data-stu-id="0d1cc-115">The system sends a [PBT\_POWERSETTINGCHANGE](pbt-powersettingchange.md) event to applications that have registered for the specific event using [**RegisterPowerSettingNotification**](/windows/desktop/api/WinUser/nf-winuser-registerpowersettingnotification).</span></span> <span data-ttu-id="0d1cc-116">Para obtener más información, consulte [registro de eventos de energía](registering-for-power-events.md).</span><span class="sxs-lookup"><span data-stu-id="0d1cc-116">For more information, see [Registering for Power Events](registering-for-power-events.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="0d1cc-117">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="0d1cc-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0d1cc-118">Acerca de la administración de energía</span><span class="sxs-lookup"><span data-stu-id="0d1cc-118">About Power Management</span></span>](about-power-management.md)
</dt> </dl>

 

 



