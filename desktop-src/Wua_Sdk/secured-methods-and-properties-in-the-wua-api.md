---
description: Cuando WUA detecta que un llamador no tiene permiso para obtener acceso a una interfaz, método o propiedad, \_ se devuelve el ACCESSDENIED HRESULT.
ms.assetid: 4535ce8d-c329-4335-8b0a-8f63c22f111d
title: Protección de interfaces, métodos y propiedades en la API de WUA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6680f616e1ca0596aba04edf4f7ddf7615e0c7f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696566"
---
# <a name="securing-interfaces-methods-and-properties-in-the-wua-api"></a><span data-ttu-id="a78d3-103">Protección de interfaces, métodos y propiedades en la API de WUA</span><span class="sxs-lookup"><span data-stu-id="a78d3-103">Securing Interfaces, Methods, and Properties in the WUA API</span></span>

<span data-ttu-id="a78d3-104">Algunas interfaces, métodos y propiedades de Windows Update Agent (WUA) son accesibles únicamente a los autores de llamadas que pertenecen a los siguientes grupos de seguridad de Windows:</span><span class="sxs-lookup"><span data-stu-id="a78d3-104">Some interfaces, methods, and properties of Windows Update Agent (WUA) are accessible only to callers who belong to the following Windows security groups:</span></span>

-   <span data-ttu-id="a78d3-105">Administrador</span><span class="sxs-lookup"><span data-stu-id="a78d3-105">Administrator</span></span>
-   <span data-ttu-id="a78d3-106">User (Usuario)</span><span class="sxs-lookup"><span data-stu-id="a78d3-106">User</span></span>
-   <span data-ttu-id="a78d3-107">Usuario avanzado</span><span class="sxs-lookup"><span data-stu-id="a78d3-107">Power User</span></span>

<span data-ttu-id="a78d3-108">Cuando WUA detecta que un llamador no tiene permiso para obtener acceso a una interfaz, método o propiedad,  \_ se devuelve el ACCESSDENIED HRESULT.</span><span class="sxs-lookup"><span data-stu-id="a78d3-108">When WUA detects that a caller does not have permission to access an interface, method, or property, the **HRESULT** E\_ACCESSDENIED is returned.</span></span>

<span data-ttu-id="a78d3-109">Las siguientes interfaces están disponibles para los grupos de seguridad de administrador, usuario y usuario avanzado:</span><span class="sxs-lookup"><span data-stu-id="a78d3-109">The following interfaces are available to the Administrator, User, and Power User security groups:</span></span>

-   [<span data-ttu-id="a78d3-110">**IAutomaticUpdates**</span><span class="sxs-lookup"><span data-stu-id="a78d3-110">**IAutomaticUpdates**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-iautomaticupdates)
-   [<span data-ttu-id="a78d3-111">**IAutomaticUpdatesSettings**</span><span class="sxs-lookup"><span data-stu-id="a78d3-111">**IAutomaticUpdatesSettings**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-iautomaticupdatessettings)
-   [<span data-ttu-id="a78d3-112">**IAutomaticUpdatesSettings2**</span><span class="sxs-lookup"><span data-stu-id="a78d3-112">**IAutomaticUpdatesSettings2**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-iautomaticupdatessettings2)
-   [<span data-ttu-id="a78d3-113">**ISystemInformation**</span><span class="sxs-lookup"><span data-stu-id="a78d3-113">**ISystemInformation**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-isysteminformation)
-   [<span data-ttu-id="a78d3-114">**IUpdateSearcher**</span><span class="sxs-lookup"><span data-stu-id="a78d3-114">**IUpdateSearcher**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesearcher)
-   <span data-ttu-id="a78d3-115">[**IUpdateSession**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesession) y [ **IUpdateSession2**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesession2)</span><span class="sxs-lookup"><span data-stu-id="a78d3-115">[**IUpdateSession**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesession) and [**IUpdateSession2**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesession2)</span></span>

> [!Note]  
> <span data-ttu-id="a78d3-116">Si se cumplen las condiciones siguientes, se produce un error en la búsqueda:</span><span class="sxs-lookup"><span data-stu-id="a78d3-116">If the following conditions are true, a search fails:</span></span>
>
> -   <span data-ttu-id="a78d3-117">Un usuario que no es administrador establece la [**propiedad UserLocale de la interfaz IUpdateSession2**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesession2-get_userlocale) en una configuración regional que corresponde a un idioma que no está instalado en el equipo.</span><span class="sxs-lookup"><span data-stu-id="a78d3-117">A user who is not an administrator sets the [**UserLocale property of the IUpdateSession2**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesession2-get_userlocale) interface to a locale that corresponds to a language that is not installed on the computer.</span></span>
> -   <span data-ttu-id="a78d3-118">La búsqueda usa un objeto UpdateSearch creado a partir del objeto UpdateSession.</span><span class="sxs-lookup"><span data-stu-id="a78d3-118">The search uses an UpdateSearch object created from the UpdateSession object.</span></span>

 

<span data-ttu-id="a78d3-119">Las siguientes interfaces de descarga y métodos están disponibles para los grupos de administradores y usuarios avanzados:</span><span class="sxs-lookup"><span data-stu-id="a78d3-119">The following download interfaces and methods are available to the Administrator and Power User groups:</span></span>

-   [<span data-ttu-id="a78d3-120">**IUpdateDownloader**</span><span class="sxs-lookup"><span data-stu-id="a78d3-120">**IUpdateDownloader**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-iupdatedownloader)
-   [<span data-ttu-id="a78d3-121">**IUpdate::CopyFromCache**</span><span class="sxs-lookup"><span data-stu-id="a78d3-121">**IUpdate::CopyFromCache**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-copyfromcache)
-   [<span data-ttu-id="a78d3-122">**IAutomaticUpdatesSettings2::CheckPermission**</span><span class="sxs-lookup"><span data-stu-id="a78d3-122">**IAutomaticUpdatesSettings2::CheckPermission**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings2-checkpermission)
    > [!Note]  
    > <span data-ttu-id="a78d3-123">Los administradores, los usuarios y los usuarios avanzados pueden llamar a [**IAutomaticUpdatesSettings2:: CheckPermission**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings2-checkpermission).</span><span class="sxs-lookup"><span data-stu-id="a78d3-123">Administrators, users, and power users can call [**IAutomaticUpdatesSettings2::CheckPermission**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings2-checkpermission).</span></span>

     

<span data-ttu-id="a78d3-124">Las siguientes interfaces de instalación, métodos y propiedades están disponibles para los grupos de administradores:</span><span class="sxs-lookup"><span data-stu-id="a78d3-124">The following installation interfaces, methods, and properties are available to the Administrator groups:</span></span>

-   [<span data-ttu-id="a78d3-125">**IAutomaticUpdates::P ause**</span><span class="sxs-lookup"><span data-stu-id="a78d3-125">**IAutomaticUpdates::Pause**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdates-pause)
-   [<span data-ttu-id="a78d3-126">**IAutomaticUpdates:: resume**</span><span class="sxs-lookup"><span data-stu-id="a78d3-126">**IAutomaticUpdates::Resume**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdates-resume)
-   [<span data-ttu-id="a78d3-127">**IAutomaticUpdates::EnableService**</span><span class="sxs-lookup"><span data-stu-id="a78d3-127">**IAutomaticUpdates::EnableService**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdates-enableservice)
-   [<span data-ttu-id="a78d3-128">**IUpdateInstaller**</span><span class="sxs-lookup"><span data-stu-id="a78d3-128">**IUpdateInstaller**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-iupdateinstaller)
-   [<span data-ttu-id="a78d3-129">**Propiedad IsHidden de IUpdate**</span><span class="sxs-lookup"><span data-stu-id="a78d3-129">**IsHidden Property of IUpdate**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_ishidden)
    > [!Note]  
    > <span data-ttu-id="a78d3-130">Los administradores, los usuarios y los usuarios avanzados pueden recuperar los valores de la [**propiedad IsHidden de IUpdate**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_ishidden).</span><span class="sxs-lookup"><span data-stu-id="a78d3-130">Administrators, users, and power users can retrieve the values of the [**IsHidden Property of IUpdate**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_ishidden).</span></span> <span data-ttu-id="a78d3-131">Sin embargo, solo los administradores y los usuarios avanzados pueden establecer los valores.</span><span class="sxs-lookup"><span data-stu-id="a78d3-131">However, only administrators and power users can set the values.</span></span>

     

-   [<span data-ttu-id="a78d3-132">**IUpdate:: AcceptEula**</span><span class="sxs-lookup"><span data-stu-id="a78d3-132">**IUpdate::AcceptEula**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-accepteula)
    > [!Note]  
    > <span data-ttu-id="a78d3-133">Los administradores y los usuarios avanzados pueden llamar al [**método AcceptEula de IUpdate**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-accepteula).</span><span class="sxs-lookup"><span data-stu-id="a78d3-133">Administrators and power users can call the [**AcceptEula method of IUpdate**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-accepteula).</span></span>

     

-   [<span data-ttu-id="a78d3-134">**IAutomaticUpdatesSettings:: Save**</span><span class="sxs-lookup"><span data-stu-id="a78d3-134">**IAutomaticUpdatesSettings::Save**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-save)
-   [<span data-ttu-id="a78d3-135">**Propiedad NotificationLevel de IAutomaticUpdatesSettings**</span><span class="sxs-lookup"><span data-stu-id="a78d3-135">**NotificationLevel Property of IAutomaticUpdatesSettings**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_notificationlevel)
    > [!Note]  
    > <span data-ttu-id="a78d3-136">Los administradores, los usuarios y los usuarios avanzados pueden recuperar los valores de la [**propiedad NotificationLevel de IAutomaticUpdatesSettings**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_notificationlevel).</span><span class="sxs-lookup"><span data-stu-id="a78d3-136">Administrators, users, and power users can retrieve the values of the [**NotificationLevel Property of IAutomaticUpdatesSettings**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_notificationlevel).</span></span> <span data-ttu-id="a78d3-137">Sin embargo, solo los administradores pueden establecer los valores.</span><span class="sxs-lookup"><span data-stu-id="a78d3-137">However, only administrators can set the values.</span></span>

     

-   [<span data-ttu-id="a78d3-138">**Propiedad ScheduledInstallationDay de IAutomaticUpdatesSettings**</span><span class="sxs-lookup"><span data-stu-id="a78d3-138">**ScheduledInstallationDay Property of IAutomaticUpdatesSettings**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_scheduledinstallationday)
    > [!Note]  
    > <span data-ttu-id="a78d3-139">Los administradores, los usuarios y los usuarios avanzados pueden recuperar los valores de la [**propiedad ScheduledInstallationDay de IAutomaticUpdatesSettings**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_scheduledinstallationday).</span><span class="sxs-lookup"><span data-stu-id="a78d3-139">Administrators, users, and power users can retrieve the values of the [**ScheduledInstallationDay Property of IAutomaticUpdatesSettings**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_scheduledinstallationday).</span></span> <span data-ttu-id="a78d3-140">Sin embargo, solo los administradores pueden establecer los valores.</span><span class="sxs-lookup"><span data-stu-id="a78d3-140">However, only administrators can set the values.</span></span>

     

-   [<span data-ttu-id="a78d3-141">**Propiedad ScheduledInstallationTime de IAutomaticUpdatesSettings**</span><span class="sxs-lookup"><span data-stu-id="a78d3-141">**ScheduledInstallationTime Property of IAutomaticUpdatesSettings**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_scheduledinstallationtime)
    > [!Note]  
    > <span data-ttu-id="a78d3-142">Los administradores, los usuarios y los usuarios avanzados pueden recuperar los valores de la [**propiedad ScheduledInstallationTime de IAutomaticUpdatesSettings**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_scheduledinstallationtime).</span><span class="sxs-lookup"><span data-stu-id="a78d3-142">Administrators, users, and power users can retrieve the values of the [**ScheduledInstallationTime Property of IAutomaticUpdatesSettings**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_scheduledinstallationtime).</span></span> <span data-ttu-id="a78d3-143">Sin embargo, solo los administradores pueden establecer los valores.</span><span class="sxs-lookup"><span data-stu-id="a78d3-143">However, only administrators can set the values.</span></span>

     

-   [<span data-ttu-id="a78d3-144">**Propiedad IncludeRecommendedUpdates de IAutomaticUpdatesSettings2**</span><span class="sxs-lookup"><span data-stu-id="a78d3-144">**IncludeRecommendedUpdates Property of IAutomaticUpdatesSettings2**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings2-get_includerecommendedupdates)
    > [!Note]  
    > <span data-ttu-id="a78d3-145">Los administradores, los usuarios y los usuarios avanzados pueden recuperar los valores de la [**propiedad IncludeRecommendedUpdates de IAutomaticUpdatesSettings2**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings2-get_includerecommendedupdates).</span><span class="sxs-lookup"><span data-stu-id="a78d3-145">Administrators, users, and power users can retrieve the values of the [**IncludeRecommendedUpdates Property of IAutomaticUpdatesSettings2**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings2-get_includerecommendedupdates).</span></span> <span data-ttu-id="a78d3-146">Sin embargo, solo los administradores pueden establecer los valores.</span><span class="sxs-lookup"><span data-stu-id="a78d3-146">However, only administrators can set the values.</span></span>

     

 

 



