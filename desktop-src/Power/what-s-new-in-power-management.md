---
description: Windows 10 ayuda a la aplicación a optimizar el consumo de energía cuando se ejecuta en un dispositivo móvil.
ms.assetid: a956b88c-8a75-4c1c-af27-53c69feb1596
title: Novedades de la administración de energía
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e6c8394c2e5e6750b5d01fd997d374a9f87e10d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677879"
---
# <a name="whats-new-in-power-management"></a><span data-ttu-id="bffbe-103">Novedades de la administración de energía (puede estar en inglés)</span><span class="sxs-lookup"><span data-stu-id="bffbe-103">What's New in Power Management</span></span>

<span data-ttu-id="bffbe-104">Windows 10 ayuda a la aplicación a optimizar el consumo de energía cuando se ejecuta en un dispositivo móvil.</span><span class="sxs-lookup"><span data-stu-id="bffbe-104">Windows 10 helps your application optimize power consumption when it's running on a mobile device.</span></span>

## <a name="battery-saver"></a><span data-ttu-id="bffbe-105">Ahorro de batería</span><span class="sxs-lookup"><span data-stu-id="bffbe-105">Battery saver</span></span>

<span data-ttu-id="bffbe-106">En esta versión, se puede notificar a la aplicación cuando el ahorro de batería está activado o desactivado.</span><span class="sxs-lookup"><span data-stu-id="bffbe-106">In this release, your application can be notified when battery saver is turned on or off.</span></span> <span data-ttu-id="bffbe-107">Al responder a las condiciones de energía cambiantes, la aplicación puede funcionar en concierto con el ahorro de batería para ahorrar energía y ayudar a ampliar la duración de la batería.</span><span class="sxs-lookup"><span data-stu-id="bffbe-107">By responding to changing power conditions, your application can work in concert with battery saver to save energy and help extend battery life.</span></span> <span data-ttu-id="bffbe-108">Para obtener información general sobre el ahorro de batería, consulte [ahorro de batería (en las instrucciones de componentes de hardware)](/windows-hardware/design/component-guidelines/battery-saver).</span><span class="sxs-lookup"><span data-stu-id="bffbe-108">For general information about battery saver, see [battery saver (in the hardware component guidelines)](/windows-hardware/design/component-guidelines/battery-saver).</span></span>

-   <span data-ttu-id="bffbe-109">[**GUID \_ de \_ \_ Estado de ahorro de energía**](power-setting-guids.md) : Use este nuevo GUID con la función [**PowerSettingRegisterNotification**](/windows/desktop/api/Powersetting/nf-powersetting-powersettingregisternotification) para recibir una notificación cuando el ahorro de batería esté activado o desactivado.</span><span class="sxs-lookup"><span data-stu-id="bffbe-109">[**GUID\_POWER\_SAVING\_STATUS**](power-setting-guids.md) : Use this new GUID with the [**PowerSettingRegisterNotification**](/windows/desktop/api/Powersetting/nf-powersetting-powersettingregisternotification) function to be notified when battery saver is turned on or off.</span></span>

-   <span data-ttu-id="bffbe-110">[**Del sistema \_ \_Estado de energía**](/windows/desktop/api/Winbase/ns-winbase-system_power_status) : esta estructura se ha actualizado para admitir el ahorro de batería.</span><span class="sxs-lookup"><span data-stu-id="bffbe-110">[**SYSTEM\_POWER\_STATUS**](/windows/desktop/api/Winbase/ns-winbase-system_power_status) : This structure has been updated to support battery saver.</span></span> <span data-ttu-id="bffbe-111">El cuarto miembro, **SystemStatusFlag** (anteriormente denominado **Reserved1**), ahora indica si el ahorro de batería está activado o no.</span><span class="sxs-lookup"><span data-stu-id="bffbe-111">The fourth member, **SystemStatusFlag** (previously named **Reserved1**), now indicates if battery saver is engaged or not.</span></span> <span data-ttu-id="bffbe-112">Utilice la función [**GetSystemPowerStatus**](/windows/desktop/api/Winbase/nf-winbase-getsystempowerstatus) para recuperar un puntero a esta estructura.</span><span class="sxs-lookup"><span data-stu-id="bffbe-112">Use the [**GetSystemPowerStatus**](/windows/desktop/api/Winbase/nf-winbase-getsystempowerstatus) function to retrieve a pointer to this structure.</span></span>

 

 
