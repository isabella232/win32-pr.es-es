---
title: Sesiones secundarias
description: A partir de Windows Server 2012 y Windows 8, Escritorio remoto admite el concepto de una sesión secundaria, que es una sesión especial de bucle invertido Escritorio remoto que está asociada a la sesión existente de un usuario.
ms.assetid: 65B9DB67-4EE8-40B5-B465-CA425792C62B
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 788b36bf9799da9b0cb7486963f3154451ca5392
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104268311"
---
# <a name="child-sessions"></a><span data-ttu-id="5fdb9-103">Sesiones secundarias</span><span class="sxs-lookup"><span data-stu-id="5fdb9-103">Child Sessions</span></span>

<span data-ttu-id="5fdb9-104">A partir de Windows Server 2012 y Windows 8, Escritorio remoto admite el concepto de una *sesión secundaria*, que es una sesión especial de bucle invertido escritorio remoto que está asociada a la sesión existente de un usuario.</span><span class="sxs-lookup"><span data-stu-id="5fdb9-104">Beginning with Windows Server 2012 and Windows 8, Remote Desktop supports the concept of a *child session*, which is a special loopback Remote Desktop session that is tied to a user's existing session.</span></span>

<span data-ttu-id="5fdb9-105">Las sesiones secundarias no se admiten en los siguientes sistemas operativos:</span><span class="sxs-lookup"><span data-stu-id="5fdb9-105">Child sessions are not supported on the following operating systems:</span></span>

<dl> <span data-ttu-id="5fdb9-106">Windows RT</span><span class="sxs-lookup"><span data-stu-id="5fdb9-106">Windows RT</span></span>  
<span data-ttu-id="5fdb9-107">Opción de instalación Server Core de Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="5fdb9-107">Windows Server 2012 Server Core installation option</span></span>  
<span data-ttu-id="5fdb9-108">Microsoft Hyper-V Server 2012</span><span class="sxs-lookup"><span data-stu-id="5fdb9-108">Microsoft Hyper-V Server 2012</span></span>  
</dl>

<span data-ttu-id="5fdb9-109">Un sistema solo puede tener una sesión secundaria activa y conectada en un momento dado.</span><span class="sxs-lookup"><span data-stu-id="5fdb9-109">A system can only have one active and connected child session at any given time.</span></span>

<span data-ttu-id="5fdb9-110">La sesión secundaria se puede finalizar cerrando la sesión directamente de la misma o se terminará cuando finalice la sesión principal.</span><span class="sxs-lookup"><span data-stu-id="5fdb9-110">The child session can be terminated by logging off directly from it, or it will be terminated when its parent session terminates.</span></span>

<span data-ttu-id="5fdb9-111">Antes de poder usar las sesiones secundarias en un sistema, debe habilitar la funcionalidad de la sesión secundaria mediante una llamada a la función [**WTSEnableChildSessions**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsenablechildsessions) .</span><span class="sxs-lookup"><span data-stu-id="5fdb9-111">Before child sessions can be used on a system, you must enable the child session functionality by calling the [**WTSEnableChildSessions**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsenablechildsessions) function.</span></span> <span data-ttu-id="5fdb9-112">También puede determinar si las sesiones secundarias se han habilitado mediante la función [**WTSIsChildSessionsEnabled**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsischildsessionsenabled) .</span><span class="sxs-lookup"><span data-stu-id="5fdb9-112">You can also determine if child sessions have been enabled by using the [**WTSIsChildSessionsEnabled**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsischildsessionsenabled) function.</span></span>

<span data-ttu-id="5fdb9-113">Una sesión secundaria solo se puede crear desde dentro de una sesión de usuario existente mediante el [escritorio remoto control ActiveX](remote-desktop-activex-control.md) y estableciendo la propiedad "ConnectToChildSession" con [**IMsRdpExtendedSettings. Property**](imsrdpextendedsettings-property.md) antes de la conexión.</span><span class="sxs-lookup"><span data-stu-id="5fdb9-113">A child session can only be created from within an existing user's session by using the [Remote Desktop ActiveX control](remote-desktop-activex-control.md) and setting the "ConnectToChildSession" property with [**IMsRdpExtendedSettings.Property**](imsrdpextendedsettings-property.md) prior to connecting.</span></span> <span data-ttu-id="5fdb9-114">Cuando se llama al método [**IMsTscAx. Connect**](imstscax-connect.md) , el control ActiveX escritorio remoto iniciará sesión automáticamente en la sesión secundaria sin pedir credenciales, excepto cuando el usuario haya iniciado sesión en la sesión primaria con una tarjeta inteligente.</span><span class="sxs-lookup"><span data-stu-id="5fdb9-114">When the [**IMsTscAx.Connect**](imstscax-connect.md) method is called, the Remote Desktop ActiveX control will automatically log on to the child session without prompting for credentials, except when the user is logged into the parent session using a smart card.</span></span> <span data-ttu-id="5fdb9-115">A diferencia de una sesión de Escritorio remoto normal, un usuario no necesita el derecho interactivo remoto para iniciar sesión en la sesión secundaria, ya que se trata de una sesión de bucle invertido.</span><span class="sxs-lookup"><span data-stu-id="5fdb9-115">Unlike a regular Remote Desktop session, a user does not need the Remote Interactive right to log on to the child session because this is a loopback session.</span></span>

<span data-ttu-id="5fdb9-116">No se puede bloquear una sesión secundaria.</span><span class="sxs-lookup"><span data-stu-id="5fdb9-116">A child session cannot be locked.</span></span> <span data-ttu-id="5fdb9-117">No tendrá ningún protector de pantalla ni ninguna pantalla de inicio de sesión.</span><span class="sxs-lookup"><span data-stu-id="5fdb9-117">It will have no screen saver and no logon screen.</span></span> <span data-ttu-id="5fdb9-118">Además, a diferencia de una sesión normal, si se establece la Directiva de texto de inicio de sesión de WinLogon, el texto de inicio de sesión no se mostrará en esta sesión secundaria.</span><span class="sxs-lookup"><span data-stu-id="5fdb9-118">Also, unlike a regular session, if the WinLogon logon text policy is set, the logon text will not be displayed in this child session.</span></span> <span data-ttu-id="5fdb9-119">Además, no habrá ningún efecto de Conexión a Escritorio remoto directivas de grupo de tiempo de espera en la sesión secundaria si se establecen estas directivas.</span><span class="sxs-lookup"><span data-stu-id="5fdb9-119">Also, there will be no effect of Remote Desktop Connection Timeout Group policies on the child session if these policies are set.</span></span>

<span data-ttu-id="5fdb9-120">Las siguientes API se usan junto con las sesiones secundarias:</span><span class="sxs-lookup"><span data-stu-id="5fdb9-120">The following APIs are used in conjunction with child sessions:</span></span>

-   [<span data-ttu-id="5fdb9-121">**WTSEnableChildSessions**</span><span class="sxs-lookup"><span data-stu-id="5fdb9-121">**WTSEnableChildSessions**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsenablechildsessions)
-   [<span data-ttu-id="5fdb9-122">**WTSIsChildSessionsEnabled**</span><span class="sxs-lookup"><span data-stu-id="5fdb9-122">**WTSIsChildSessionsEnabled**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsischildsessionsenabled)
-   [<span data-ttu-id="5fdb9-123">**WTSGetChildSessionId**</span><span class="sxs-lookup"><span data-stu-id="5fdb9-123">**WTSGetChildSessionId**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsgetchildsessionid)
-   <span data-ttu-id="5fdb9-124">Propiedad "ConnectToChildSession" en [ **IMsRdpExtendedSettings. Property**](imsrdpextendedsettings-property.md)</span><span class="sxs-lookup"><span data-stu-id="5fdb9-124">"ConnectToChildSession" property in [**IMsRdpExtendedSettings.Property**](imsrdpextendedsettings-property.md)</span></span>

 

 




