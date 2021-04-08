---
description: El dispositivo Power API facilita la determinación de los dispositivos que pueden reactivar el sistema desde un estado de suspensión y los Estados de suspensión en los que los dispositivos admiten la activación. Para obtener más información acerca de los Estados de suspensión, consulte Estados de energía del sistema.
ms.assetid: aaa776e5-3fc2-41bd-a805-6c09ef73807b
title: Administración de energía de dispositivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0982b7de23f7b7d8cf39686c854d64f284d1ce2f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001960"
---
# <a name="device-power-management"></a><span data-ttu-id="91e77-104">Administración de energía de dispositivos</span><span class="sxs-lookup"><span data-stu-id="91e77-104">Device Power Management</span></span>

<span data-ttu-id="91e77-105">El dispositivo Power API facilita la determinación de los dispositivos que pueden reactivar el sistema desde un estado de suspensión y los Estados de suspensión en los que los dispositivos admiten la activación.</span><span class="sxs-lookup"><span data-stu-id="91e77-105">The Device Power API makes it easy to determine which devices are able to wake the system from a sleep state, and which sleep states those devices support waking from.</span></span> <span data-ttu-id="91e77-106">Para obtener más información acerca de los Estados de suspensión, consulte [Estados de energía del sistema](system-power-states.md).</span><span class="sxs-lookup"><span data-stu-id="91e77-106">For more information about sleep states, see [System Power States](system-power-states.md).</span></span>

<span data-ttu-id="91e77-107">La función [**DevicePowerEnumDevices**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowerenumdevices) se puede usar para buscar los dispositivos que coinciden con los criterios especificados en la lista de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="91e77-107">The [**DevicePowerEnumDevices**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowerenumdevices) function can be used to search the device list for devices that match specified criteria.</span></span> <span data-ttu-id="91e77-108">Los criterios pueden incluir la capacidad del dispositivo para admitir un estado del sistema o reactivar desde ese estado.</span><span class="sxs-lookup"><span data-stu-id="91e77-108">The criteria may include the device's ability to support a system state, or wake from that state.</span></span> <span data-ttu-id="91e77-109">Las marcas admitidas actualmente se pueden encontrar en Winnt. h y DevPower. h.</span><span class="sxs-lookup"><span data-stu-id="91e77-109">Currently supported flags can be found in WinNT.h and DevPower.h.</span></span>

<span data-ttu-id="91e77-110">La función [**DevicePowerSetDeviceState**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowersetdevicestate) habilita o deshabilita el dispositivo especificado para que no reactiva el sistema desde un estado de suspensión.</span><span class="sxs-lookup"><span data-stu-id="91e77-110">The [**DevicePowerSetDeviceState**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowersetdevicestate) function enables or disables a specified device from waking the system from a sleep state.</span></span>

<span data-ttu-id="91e77-111">El dispositivo Power API permite a los desarrolladores crear una mejor experiencia de usuario, ya que proporciona al usuario más información sobre lo que está haciendo el sistema y más control sobre los dispositivos del sistema.</span><span class="sxs-lookup"><span data-stu-id="91e77-111">The Device Power API allows developers to create a better user experience by giving the user more information about what the system is doing, and more control over the devices in the system.</span></span> <span data-ttu-id="91e77-112">La potencia del dispositivo es útil en situaciones en las que el consumo de energía es crítico, como en dispositivos portátiles que se ejecutan con baterías.</span><span class="sxs-lookup"><span data-stu-id="91e77-112">Device Power is useful in situations where power consumption is critical, such as in portable devices running on batteries.</span></span> <span data-ttu-id="91e77-113">Por ejemplo, el esquema de administración de energía que se usa en un equipo de escritorio puede no ser el esquema óptimo para un equipo portátil, por lo que es posible que el usuario desee deshabilitar la activación de determinados dispositivos.</span><span class="sxs-lookup"><span data-stu-id="91e77-113">For example, the power management scheme used in a desktop computer may not be the optimal scheme for a laptop computer, so the user may want to disable certain devices from waking the system.</span></span> <span data-ttu-id="91e77-114">Esto puede ahorrar energía porque los dispositivos deshabilitados no reproducirán energía mientras el sistema está en modo de suspensión.</span><span class="sxs-lookup"><span data-stu-id="91e77-114">This can conserve energy because the disabled devices will not draw power while the system is in sleep mode.</span></span>

<span data-ttu-id="91e77-115">Para ver un ejemplo, consulte [uso de la API de energía de dispositivos](using-the-device-power-api.md).</span><span class="sxs-lookup"><span data-stu-id="91e77-115">For an example, see [Using the Device Power API](using-the-device-power-api.md).</span></span>

 

 



