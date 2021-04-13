---
title: Funciones de registro de MDM
description: El registro de MDM usa las siguientes funciones.
ms.assetid: 1b063a56-f59f-4b02-949f-c8b6bbf45a13
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 821e08d9c6631bbb300a86ab6b9c480a3af0c25b
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/08/2020
ms.locfileid: "104359465"
---
# <a name="mdm-registration-functions"></a><span data-ttu-id="e7ec7-103">Funciones de registro de MDM</span><span class="sxs-lookup"><span data-stu-id="e7ec7-103">MDM Registration Functions</span></span>

<span data-ttu-id="e7ec7-104">El registro de MDM usa las siguientes funciones.</span><span class="sxs-lookup"><span data-stu-id="e7ec7-104">The following functions are used by MDM Registration.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="e7ec7-105">En esta sección</span><span class="sxs-lookup"><span data-stu-id="e7ec7-105">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="e7ec7-106">**DiscoverManagementService**</span><span class="sxs-lookup"><span data-stu-id="e7ec7-106">**DiscoverManagementService**</span></span>](/windows/desktop/api/MDMRegistration/nf-mdmregistration-discovermanagementservice)
</dt> <dd>

<span data-ttu-id="e7ec7-107">Detecta el servicio MDM.</span><span class="sxs-lookup"><span data-stu-id="e7ec7-107">Discovers the MDM service.</span></span>

</dd> <dt>

[<span data-ttu-id="e7ec7-108">**DiscoverManagementServiceEx**</span><span class="sxs-lookup"><span data-stu-id="e7ec7-108">**DiscoverManagementServiceEx**</span></span>](/windows/desktop/api/MDMRegistration/nf-mdmregistration-discovermanagementserviceex)
</dt> <dd>

<span data-ttu-id="e7ec7-109">Detecta el servicio MDM mediante un servidor candidato.</span><span class="sxs-lookup"><span data-stu-id="e7ec7-109">Discovers the MDM service using a candidate server.</span></span>

</dd> <dt>

[<span data-ttu-id="e7ec7-110">**GetDeviceRegistrationInfo**</span><span class="sxs-lookup"><span data-stu-id="e7ec7-110">**GetDeviceRegistrationInfo**</span></span>](/windows/desktop/api/MDMRegistration/nf-mdmregistration-getdeviceregistrationinfo)
</dt> <dd>

<span data-ttu-id="e7ec7-111">Recupera la información de registro del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e7ec7-111">Retrieves the device registration information.</span></span>

</dd> <dt>

[<span data-ttu-id="e7ec7-112">**GetManagementAppHyperlink**</span><span class="sxs-lookup"><span data-stu-id="e7ec7-112">**GetManagementAppHyperlink**</span></span>](/windows/desktop/api/MDMRegistration/nf-mdmregistration-getmanagementapphyperlink)
</dt> <dd>

<span data-ttu-id="e7ec7-113">Recupera el hipervínculo de la aplicación de administración asociado al servicio MDM.</span><span class="sxs-lookup"><span data-stu-id="e7ec7-113">Retrieves the management app hyperlink associated with the MDM service.</span></span>

</dd> <dt>

[<span data-ttu-id="e7ec7-114">**IsDeviceRegisteredWithManagement**</span><span class="sxs-lookup"><span data-stu-id="e7ec7-114">**IsDeviceRegisteredWithManagement**</span></span>](/windows/desktop/api/MDMRegistration/nf-mdmregistration-isdeviceregisteredwithmanagement)
</dt> <dd>

<span data-ttu-id="e7ec7-115">Comprueba si el dispositivo está registrado con un servicio MDM.</span><span class="sxs-lookup"><span data-stu-id="e7ec7-115">Checks whether the device is registered with an MDM service.</span></span>

</dd> <dt>

[<span data-ttu-id="e7ec7-116">**IsManagementRegistrationAllowed**</span><span class="sxs-lookup"><span data-stu-id="e7ec7-116">**IsManagementRegistrationAllowed**</span></span>](/windows/desktop/api/MDMRegistration/nf-mdmregistration-ismanagementregistrationallowed)
</dt> <dd>

<span data-ttu-id="e7ec7-117">Comprueba si la directiva local permite el registro de MDM.</span><span class="sxs-lookup"><span data-stu-id="e7ec7-117">Checks whether MDM registration is allowed by local policy.</span></span>

</dd> <dt>

[<span data-ttu-id="e7ec7-118">**RegisterDeviceWithManagement**</span><span class="sxs-lookup"><span data-stu-id="e7ec7-118">**RegisterDeviceWithManagement**</span></span>](/windows/desktop/api/MDMRegistration/nf-mdmregistration-registerdevicewithmanagement)
</dt> <dd>

<span data-ttu-id="e7ec7-119">Registra un dispositivo con un servicio MDM mediante el protocolo de [ \[ inscripción MS-MDE \] : dispositivos móviles](/openspecs/windows_protocols/ms-mde/5c841535-042e-489e-913c-9d783d741267).</span><span class="sxs-lookup"><span data-stu-id="e7ec7-119">Registers a device with a MDM service, using the [\[MS-MDE\]: Mobile Device Enrollment Protocol](/openspecs/windows_protocols/ms-mde/5c841535-042e-489e-913c-9d783d741267).</span></span>

</dd> <dt>

[<span data-ttu-id="e7ec7-120">**RegisterDeviceWithManagementUsingAADCredentials**</span><span class="sxs-lookup"><span data-stu-id="e7ec7-120">**RegisterDeviceWithManagementUsingAADCredentials**</span></span>](/windows/desktop/api/MDMRegistration/nf-mdmregistration-registerdevicewithmanagementusingaadcredentials)
</dt> <dd>

<span data-ttu-id="e7ec7-121">Registra un dispositivo con un servicio MDM mediante credenciales Azure Active Directory (AAD).</span><span class="sxs-lookup"><span data-stu-id="e7ec7-121">Registers a device with a MDM service, using Azure Active Directory (AAD) credentials.</span></span>

</dd> <dt>

[<span data-ttu-id="e7ec7-122">**SetManagedExternally**</span><span class="sxs-lookup"><span data-stu-id="e7ec7-122">**SetManagedExternally**</span></span>](/windows/desktop/api/MDMRegistration/nf-mdmregistration-setmanagedexternally)
</dt> <dd>

<span data-ttu-id="e7ec7-123">Indica al agente MDM que el dispositivo se administra externamente y no se va a registrar con un servicio MDM.</span><span class="sxs-lookup"><span data-stu-id="e7ec7-123">Indicates to the MDM agent that the device is managed externally and is not to be registered with an MDM service.</span></span>

</dd> <dt>

[<span data-ttu-id="e7ec7-124">**UnregisterDeviceWithManagement**</span><span class="sxs-lookup"><span data-stu-id="e7ec7-124">**UnregisterDeviceWithManagement**</span></span>](/windows/desktop/api/MDMRegistration/nf-mdmregistration-unregisterdevicewithmanagement)
</dt> <dd>

<span data-ttu-id="e7ec7-125">Anula el registro de un dispositivo con el servicio MDM</span><span class="sxs-lookup"><span data-stu-id="e7ec7-125">Unregisters a device with the MDM service</span></span>

</dd> </dl>

 

 