---
description: Puede optar por un equipo en el servicio de Microsoft Update y, a continuación, registrar ese servicio con Actualizaciones automáticas.
ms.assetid: d6f3d8ca-3b7e-409c-87b6-db247b7b68e4
title: Opt-In a Microsoft Update
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b149eb28024d77f66a08371827187adf05d4b78
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153823"
---
# <a name="opt-in-to-microsoft-update"></a><span data-ttu-id="456ba-103">Opt-In a Microsoft Update</span><span class="sxs-lookup"><span data-stu-id="456ba-103">Opt-In to Microsoft Update</span></span>

<span data-ttu-id="456ba-104">Puede optar por un equipo en el servicio de Microsoft Update y, a continuación, registrar ese servicio con Actualizaciones automáticas.</span><span class="sxs-lookup"><span data-stu-id="456ba-104">You can opt a computer in to the Microsoft Update service and then register that service with Automatic Updates.</span></span>

<span data-ttu-id="456ba-105">En el ejemplo de scripting de este tema se muestra cómo usar Windows Update Agent (WUA) para registrar el servicio de Microsoft Update con Actualizaciones automáticas.</span><span class="sxs-lookup"><span data-stu-id="456ba-105">The scripting sample in this topic shows you how to use Windows Update Agent (WUA) to register the Microsoft Update service with Automatic Updates.</span></span> <span data-ttu-id="456ba-106">Como alternativa, para registrar el servicio, el usuario puede visitar Microsoft Update.</span><span class="sxs-lookup"><span data-stu-id="456ba-106">Alternatively, to register the service, the user can visit Microsoft Update.</span></span>

<span data-ttu-id="456ba-107">Antes de intentar ejecutar este ejemplo, compruebe que la versión de WUA instalada en el equipo sea la versión 7.0.6000 o una versión posterior.</span><span class="sxs-lookup"><span data-stu-id="456ba-107">Before you attempt to run this sample, verify that the version of WUA that is installed on the computer is version 7.0.6000 or a later version.</span></span> <span data-ttu-id="456ba-108">Para obtener más información sobre cómo determinar la versión de WUA que está instalada, vea [determinar la versión actual de WUA](determining-the-current-version-of-wua.md).</span><span class="sxs-lookup"><span data-stu-id="456ba-108">For more information about how to determine the version of WUA that is installed, see [Determining the Current Version of WUA](determining-the-current-version-of-wua.md).</span></span>

## <a name="example"></a><span data-ttu-id="456ba-109">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="456ba-109">Example</span></span>

<span data-ttu-id="456ba-110">En el ejemplo de scripting siguiente se muestra cómo utilizar el agente de Windows Update (WUA) para registrar el servicio de Microsoft Update con Actualizaciones automáticas.</span><span class="sxs-lookup"><span data-stu-id="456ba-110">The following scripting sample shows you how to use the Windows Update Agent (WUA) to register the Microsoft Update service with Automatic Updates.</span></span> <span data-ttu-id="456ba-111">El ejemplo permite el procesamiento diferido o sin conexión si es necesario.</span><span class="sxs-lookup"><span data-stu-id="456ba-111">The sample allows deferred or offline processing if needed.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="456ba-112">Este script está pensado para demostrar el uso de las API del agente de Windows Update y proporcionar un ejemplo de cómo los desarrolladores pueden usar estas API para resolver los problemas.</span><span class="sxs-lookup"><span data-stu-id="456ba-112">This script is intended to demonstrate the use of the Windows Update Agent APIs, and provide an example of how developers can use these APIs to solve problems.</span></span> <span data-ttu-id="456ba-113">Este script no está pensado como código de producción y Microsoft no admite el propio script (aunque se admiten las API del agente de Windows Update subyacentes).</span><span class="sxs-lookup"><span data-stu-id="456ba-113">This script is not intended as production code, and the script itself is not supported by Microsoft (though the underlying Windows Update Agent APIs are supported).</span></span>

 


```VB
Set ServiceManager = CreateObject("Microsoft.Update.ServiceManager")
ServiceManager.ClientApplicationID = "My App"

'add the Microsoft Update Service, GUID
Set NewUpdateService = ServiceManager.AddService2("7971f918-a847-4430-9279-4a52d1efe18d",7,"")

```



<span data-ttu-id="456ba-114">En versiones anteriores de WUA (una versión de WUA mínima de 7.0.6000), puede simplificar el proceso de participación mediante una configuración del registro.</span><span class="sxs-lookup"><span data-stu-id="456ba-114">In earlier versions of WUA (a minimum WUA version of 7.0.6000), you can simplify the opt-in process by using a registry setting.</span></span> <span data-ttu-id="456ba-115">Una vez configurados los valores y la clave del registro, el proceso de participación en el Microsoft Update se produce la próxima vez que WUA realiza una búsqueda.</span><span class="sxs-lookup"><span data-stu-id="456ba-115">After the registry key and values are configured, the Microsoft Update opt-in process occurs the next time WUA performs a search.</span></span> <span data-ttu-id="456ba-116">El proceso de participación puede ser desencadenado por Actualizaciones automáticas o por un llamador de la API.</span><span class="sxs-lookup"><span data-stu-id="456ba-116">The opt-in process may be triggered by Automatic Updates or by an API caller.</span></span>

<span data-ttu-id="456ba-117">Por ejemplo, la ruta de acceso completa de la clave del registro y los valores que se establecen para el proceso de participación son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="456ba-117">For example, the full path of the registry key and values to set for the opt-in process are as follows:</span></span>

<span data-ttu-id="456ba-118">**HKLM** \\ **Software** \\ de **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Windowsupdate** \\ **PendingServiceRegistration** \\ **7971f918-A847-4430-9279-4a52d1efe18d**</span><span class="sxs-lookup"><span data-stu-id="456ba-118">**HKLM**\\**Software**\\**Microsoft**\\**Windows**\\**CurrentVersion**\\**WindowsUpdate**\\**PendingServiceRegistration**\\**7971f918-a847-4430-9279-4a52d1efe18d**</span></span>

<span data-ttu-id="456ba-119">**ClientApplicationID** = mi aplicación</span><span class="sxs-lookup"><span data-stu-id="456ba-119">**ClientApplicationID** = My App</span></span>

<span data-ttu-id="456ba-120">**RegisterWithAU** = 1</span><span class="sxs-lookup"><span data-stu-id="456ba-120">**RegisterWithAU** = 1</span></span>

> [!Note]
>
> <span data-ttu-id="456ba-121">La clave del registro se respeta una vez solo cuando WUA se actualiza desde una versión anterior a la versión 7.0.6000 a la versión 7.0.6000 o a una versión posterior.</span><span class="sxs-lookup"><span data-stu-id="456ba-121">The registry key is respected once only when WUA is updated from a version that is earlier than version 7.0.6000 to version 7.0.6000 or to a later version.</span></span> <span data-ttu-id="456ba-122">Recomendamos que se sobrescriban los valores del registro existentes, ya que si se sobrescriben los valores, se puede cambiar el resultado de una solicitud de registro del servicio anterior.</span><span class="sxs-lookup"><span data-stu-id="456ba-122">We recommend discretion when overwriting existing registry values because overwriting the values may change the result of an earlier service registration request.</span></span>
>
> <span data-ttu-id="456ba-123">La creación de esta clave del registro requiere credenciales administrativas.</span><span class="sxs-lookup"><span data-stu-id="456ba-123">Creating this registry key requires administrative credentials.</span></span> <span data-ttu-id="456ba-124">En Windows Vista, el autor de la llamada debe crear la clave del registro en un proceso con privilegios elevados.</span><span class="sxs-lookup"><span data-stu-id="456ba-124">For Windows Vista, the caller must create the registry key in an elevated process.</span></span>

 

 

 



