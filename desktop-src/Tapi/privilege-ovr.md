---
description: El privilegio se refiere a si una aplicación es propietaria o está supervisando la sesión.
ms.assetid: 0c02a88a-370f-4eb9-ba64-07a382bd2e87
title: Privilegio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc2f773edb05afc029a8f9fb6b014cd8a737eef0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688143"
---
# <a name="privilege"></a><span data-ttu-id="8ec35-103">Privilegio</span><span class="sxs-lookup"><span data-stu-id="8ec35-103">Privilege</span></span>

<span data-ttu-id="8ec35-104">El privilegio se refiere a si una aplicación es propietaria o está supervisando la sesión.</span><span class="sxs-lookup"><span data-stu-id="8ec35-104">Privilege refers to whether an application owns or is monitoring the session.</span></span> <span data-ttu-id="8ec35-105">Si la aplicación es propietaria de la sesión, se le permite realizar una serie de operaciones de sesión.</span><span class="sxs-lookup"><span data-stu-id="8ec35-105">If the application owns the session, it is allowed to perform a variety of session operations.</span></span> <span data-ttu-id="8ec35-106">Si la aplicación solo está supervisando, recibirá mensajes de estado y podrá tener acceso a la información de la sesión, pero cualquier intento de realizar la mayoría de las operaciones producirá un error.</span><span class="sxs-lookup"><span data-stu-id="8ec35-106">If the application is only monitoring, it will receive state messages and it can access session information, but any attempt to perform most operations will result in an error.</span></span>

<span data-ttu-id="8ec35-107">Durante la inicialización, una aplicación indica a TAPI qué nivel de privilegios requiere en qué direcciones.</span><span class="sxs-lookup"><span data-stu-id="8ec35-107">During initialization, an application tells TAPI which privilege level it requires on which addresses.</span></span> <span data-ttu-id="8ec35-108">TAPI ofrece sesiones entrantes únicamente a las aplicaciones que se han registrado para los privilegios de propietario, de propietario y de supervisión.</span><span class="sxs-lookup"><span data-stu-id="8ec35-108">TAPI offers incoming sessions only to applications that have registered for either owner or owner and monitor privilege.</span></span>

<span data-ttu-id="8ec35-109">El privilegio de una aplicación en una sesión que crea siempre es el propietario.</span><span class="sxs-lookup"><span data-stu-id="8ec35-109">An application's privilege on a session it creates is always owner.</span></span>

<span data-ttu-id="8ec35-110">**TAPI 2. x:** Vea [**lineGetCallStatus**](/windows/win32/api/tapi/nf-tapi-linegetcallstatus), miembro **dwCallPrivilege** de [**LINECALLSTATUS**](/windows/win32/api/tapi/ns-tapi-linecallstatus), [**lineSetCallPrivilege**](/windows/win32/api/tapi/nf-tapi-linesetcallprivilege).</span><span class="sxs-lookup"><span data-stu-id="8ec35-110">**TAPI 2.x:** See [**lineGetCallStatus**](/windows/win32/api/tapi/nf-tapi-linegetcallstatus), **dwCallPrivilege** member of [**LINECALLSTATUS**](/windows/win32/api/tapi/ns-tapi-linecallstatus), [**lineSetCallPrivilege**](/windows/win32/api/tapi/nf-tapi-linesetcallprivilege).</span></span>

<span data-ttu-id="8ec35-111">**TAPI 3. x:** Vea [**ITCallInfo:: get \_ Privilege**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_privilege), [**ITCallInfo:: get \_ CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong), llamado con el miembro **CIL \_ NUMBEROFOWNERS** o **CIL \_ NUMBEROFMONITORS** de [**CALLINFO \_ Long**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long).</span><span class="sxs-lookup"><span data-stu-id="8ec35-111">**TAPI 3.x:** See [**ITCallInfo::get\_Privilege**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_privilege), [**ITCallInfo::get\_CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong), called with the **CIL\_NUMBEROFOWNERS** or **CIL\_NUMBEROFMONITORS** member of [**CALLINFO\_LONG**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long).</span></span>

 

 
