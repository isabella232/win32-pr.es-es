---
description: Al quitar o desconectar una sesión se termina la comunicación. La aplicación tiene la opción de enviar información de usuario de usuario en el momento de la desconexión, si el proveedor de servicios lo admite.
ms.assetid: dc348bb2-d564-40f8-afe3-5473c5769fa4
title: Anular
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a9bf3705d9b104b8816ce4b493ec6b188c5fe1c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001030"
---
# <a name="drop"></a><span data-ttu-id="1b444-104">Anular</span><span class="sxs-lookup"><span data-stu-id="1b444-104">Drop</span></span>

<span data-ttu-id="1b444-105">Al quitar o desconectar una sesión se termina la comunicación.</span><span class="sxs-lookup"><span data-stu-id="1b444-105">Dropping or disconnecting a session terminates communication.</span></span> <span data-ttu-id="1b444-106">La aplicación tiene la opción de enviar información de usuario de usuario en el momento de la desconexión, si el proveedor de servicios lo admite.</span><span class="sxs-lookup"><span data-stu-id="1b444-106">The application has the option of sending user-user information at the time of the disconnect, if the service provider supports it.</span></span>

<span data-ttu-id="1b444-107">Las razones habituales para quitar una sesión es que un usuario ha solicitado una desconexión o se ha quitado el otro extremo de la sesión.</span><span class="sxs-lookup"><span data-stu-id="1b444-107">The usual reasons for dropping a session is a user has requested a disconnect or the other end of the session has dropped.</span></span> <span data-ttu-id="1b444-108">También se puede llamar a una operación Drop cuando TAPI ofrece una sesión a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="1b444-108">A drop operation may also be called when TAPI offers a session to the application.</span></span> <span data-ttu-id="1b444-109">Si el proveedor de servicios lo admite, el efecto es que la aplicación rechaza la llamada.</span><span class="sxs-lookup"><span data-stu-id="1b444-109">If the service provider supports this, the effect is that the application rejects the call.</span></span>

<span data-ttu-id="1b444-110">Al invocar una operación de colocar, las sesiones relacionadas a veces también pueden verse afectadas.</span><span class="sxs-lookup"><span data-stu-id="1b444-110">When invoking a drop operation, related sessions can sometimes be affected as well.</span></span> <span data-ttu-id="1b444-111">Por ejemplo, quitar una llamada de conferencia puede quitar todos los participantes individuales.</span><span class="sxs-lookup"><span data-stu-id="1b444-111">For example, dropping a conference call can drop all individual participants.</span></span> <span data-ttu-id="1b444-112">Los mensajes de cambio de estado se envían a la aplicación para todas las llamadas cuyo estado se ve afectado.</span><span class="sxs-lookup"><span data-stu-id="1b444-112">State change messages are sent to the application for all calls whose state is affected.</span></span>

<span data-ttu-id="1b444-113">En varias configuraciones puente o de línea de entidad cuando hay varias entidades en la llamada, es posible que una operación de colocar no borre realmente la llamada.</span><span class="sxs-lookup"><span data-stu-id="1b444-113">In various bridged or party-line configurations when multiple parties are on the call, a drop operation may not actually clear the call.</span></span> <span data-ttu-id="1b444-114">Por ejemplo, en una situación de puente, es posible que la llamada no se quite porque el estado de otras estaciones de la llamada puede regir.</span><span class="sxs-lookup"><span data-stu-id="1b444-114">For example, in a bridged situation, the call may not be dropped because the status of other stations on the call may govern.</span></span> <span data-ttu-id="1b444-115">En su lugar, la llamada simplemente se puede cambiar al estado inactivo mientras está conectado en otras estaciones.</span><span class="sxs-lookup"><span data-stu-id="1b444-115">Instead, the call may simply be changed to the inactive state while remaining connected at other stations.</span></span>

<span data-ttu-id="1b444-116">Después de una operación de colocar, el identificador de sesión y la mayoría de los recursos asociados a la sesión seguirán siendo utilizables para la mayoría de las operaciones de consulta.</span><span class="sxs-lookup"><span data-stu-id="1b444-116">Following a drop operation, the session identifier and most resources associated with the session will remain usable for most query operations.</span></span> <span data-ttu-id="1b444-117">Cuando una aplicación ya no requiere estos recursos, debe [finalizar la sesión](terminate-a-session-ovr.md) para evitar pérdidas de memoria.</span><span class="sxs-lookup"><span data-stu-id="1b444-117">When an application no longer requires these resources, it must [terminate the session](terminate-a-session-ovr.md) in order to avoid memory leaks.</span></span>

<span data-ttu-id="1b444-118">**TAPI 2. x:** Vea [**lineDrop**](/windows/win32/api/tapi/nf-tapi-linedrop).</span><span class="sxs-lookup"><span data-stu-id="1b444-118">**TAPI 2.x:** See [**lineDrop**](/windows/win32/api/tapi/nf-tapi-linedrop).</span></span>

<span data-ttu-id="1b444-119">**TAPI 3. x:** Vea [**ITBasicCallControl::D Ulta**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-disconnect).</span><span class="sxs-lookup"><span data-stu-id="1b444-119">**TAPI 3.x:** See [**ITBasicCallControl::Disconnect**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-disconnect).</span></span>

 

 
