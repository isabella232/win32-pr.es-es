---
description: Describe la configuración de la Directiva de energía que constituye un plan de energía.
ms.assetid: cd515cd6-67f4-45d0-b769-3abc7a56faa8
title: Configuración de la Directiva de energía
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f490c758a890faf314be1ddffe9ac7a503bd473
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103813787"
---
# <a name="power-policy-settings"></a><span data-ttu-id="08cac-103">Configuración de la Directiva de energía</span><span class="sxs-lookup"><span data-stu-id="08cac-103">Power Policy Settings</span></span>

<span data-ttu-id="08cac-104">Los planes de energía y los esquemas constan de preferencias y configuraciones de directiva.</span><span class="sxs-lookup"><span data-stu-id="08cac-104">Power plans and schemes consist of preferences and policy settings.</span></span>

<span data-ttu-id="08cac-105">Un plan de energía consta de un grupo de preferencias de configuración de energía.</span><span class="sxs-lookup"><span data-stu-id="08cac-105">A power plan consists of a group of power setting preferences.</span></span> <span data-ttu-id="08cac-106">Estas preferencias se componen de un valor de AC y DC para cada una de las configuraciones de energía.</span><span class="sxs-lookup"><span data-stu-id="08cac-106">These preferences consist of both an AC and DC value for each of the power settings.</span></span> <span data-ttu-id="08cac-107">Cada plan de energía se identifica mediante un **GUID** único y un nombre descriptivo.</span><span class="sxs-lookup"><span data-stu-id="08cac-107">Each power plan is identified through a unique **GUID** as well as a friendly name.</span></span> <span data-ttu-id="08cac-108">Windows Vista tiene tres planes de energía predeterminados: economizador de energía, equilibrado y alto rendimiento.</span><span class="sxs-lookup"><span data-stu-id="08cac-108">Windows Vista has three default power plans: Power Saver, Balanced, and High Performance.</span></span> <span data-ttu-id="08cac-109">Estos planes se pueden personalizar y se pueden crear planes adicionales.</span><span class="sxs-lookup"><span data-stu-id="08cac-109">These plans can be customized, and additional plans can be created.</span></span> <span data-ttu-id="08cac-110">Todos los planes de energía tienen un atributo de personalidad que indica el comportamiento de ahorro de energía general del plan.</span><span class="sxs-lookup"><span data-stu-id="08cac-110">All power plans have a personality attribute that indicates the overall power savings behavior of the plan.</span></span>

<span data-ttu-id="08cac-111">En la tabla siguiente se muestran los tres personalidades del plan de energía.</span><span class="sxs-lookup"><span data-stu-id="08cac-111">The following table shows the three power plan personalities.</span></span> 

| <span data-ttu-id="08cac-112">Nombre para mostrar</span><span class="sxs-lookup"><span data-stu-id="08cac-112">Display name</span></span>     | <span data-ttu-id="08cac-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="08cac-113">Description</span></span>                                                                   | <span data-ttu-id="08cac-114">**GUID**</span><span class="sxs-lookup"><span data-stu-id="08cac-114">**GUID**</span></span>                             |
|------------------|-------------------------------------------------------------------------------|--------------------------------------|
| <span data-ttu-id="08cac-115">Economizador de energía</span><span class="sxs-lookup"><span data-stu-id="08cac-115">Power Saver</span></span>      | <span data-ttu-id="08cac-116">Ofrece un rendimiento reducido que puede aumentar el ahorro de energía.</span><span class="sxs-lookup"><span data-stu-id="08cac-116">Delivers reduced performance which may increase power savings.</span></span>                | <span data-ttu-id="08cac-117">a1841308-3541-4fab-bc81-f71556f20b4a</span><span class="sxs-lookup"><span data-stu-id="08cac-117">a1841308-3541-4fab-bc81-f71556f20b4a</span></span> |
| <span data-ttu-id="08cac-118">Equilibrada</span><span class="sxs-lookup"><span data-stu-id="08cac-118">Balanced</span></span>         | <span data-ttu-id="08cac-119">Equilibra automáticamente el rendimiento y el consumo de energía en función de la demanda.</span><span class="sxs-lookup"><span data-stu-id="08cac-119">Automatically balances performance and power consumption according to demand.</span></span> | <span data-ttu-id="08cac-120">381b4222-f694-41f0-9685-ff5bb260df2e</span><span class="sxs-lookup"><span data-stu-id="08cac-120">381b4222-f694-41f0-9685-ff5bb260df2e</span></span> |
| <span data-ttu-id="08cac-121">Alto rendimiento</span><span class="sxs-lookup"><span data-stu-id="08cac-121">High Performance</span></span> | <span data-ttu-id="08cac-122">Ofrece un rendimiento máximo a costa de un mayor consumo energético.</span><span class="sxs-lookup"><span data-stu-id="08cac-122">Delivers maximum performance at the expense of higher power consumption.</span></span>      | <span data-ttu-id="08cac-123">8c5e7fda-e8bf-4a96-9a85-a6e23a8c635c</span><span class="sxs-lookup"><span data-stu-id="08cac-123">8c5e7fda-e8bf-4a96-9a85-a6e23a8c635c</span></span> |



 

> [!Note]  
> <span data-ttu-id="08cac-124">Los dispositivos que admiten el modo de [espera moderno](/windows-hardware/design/device-experiences/modern-standby) solo permiten el plan de energía **equilibrado** .</span><span class="sxs-lookup"><span data-stu-id="08cac-124">Devices that support [Modern Standby](/windows-hardware/design/device-experiences/modern-standby) mode only allow the **Balanced** power plan.</span></span> <span data-ttu-id="08cac-125">El **modo de espera moderno** es la solución más reciente y más simplificada para la administración de la configuración de energía.</span><span class="sxs-lookup"><span data-stu-id="08cac-125">**Modern Standby** is the newer, more streamlined solution to power settings management.</span></span>

 

<span data-ttu-id="08cac-126">Cada equipo tiene un plan de energía único y activo.</span><span class="sxs-lookup"><span data-stu-id="08cac-126">Each computer has a single, active power plan.</span></span> <span data-ttu-id="08cac-127">De forma predeterminada, los usuarios sin privilegios pueden acceder a la configuración de energía del sistema.</span><span class="sxs-lookup"><span data-stu-id="08cac-127">By default, nonprivileged users are able to access system power settings.</span></span> <span data-ttu-id="08cac-128">Se puede controlar el acceso a toda la configuración de energía o a través de las ACL en la configuración de energía o a través de directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="08cac-128">Access to all or individual power settings can be controlled through ACLs on the power settings or through Group Policy.</span></span> <span data-ttu-id="08cac-129">Las aplicaciones deben llamar a [**PowerSettingAccessCheck**](/windows/desktop/api/PowrProf/nf-powrprof-powersettingaccesscheck) para determinar si el usuario tiene acceso a la configuración de energía.</span><span class="sxs-lookup"><span data-stu-id="08cac-129">Applications should call [**PowerSettingAccessCheck**](/windows/desktop/api/PowrProf/nf-powrprof-powersettingaccesscheck) to determine if the user has access to the power setting.</span></span>

<span data-ttu-id="08cac-130">Cada configuración de energía se identifica mediante un **GUID** único e incluye un nombre descriptivo, una descripción, valores permitidos y valores predeterminados para AC y DC.</span><span class="sxs-lookup"><span data-stu-id="08cac-130">Each power setting is identified by a unique **GUID** and includes a friendly name, description, allowable values, and default values for AC and DC.</span></span> <span data-ttu-id="08cac-131">La configuración de energía personalizada se puede crear con la función [**PowerCreateSetting**](/windows/desktop/api/PowrProf/nf-powrprof-powercreatesetting) .</span><span class="sxs-lookup"><span data-stu-id="08cac-131">Custom power settings can be created using the [**PowerCreateSetting**](/windows/desktop/api/PowrProf/nf-powrprof-powercreatesetting) function.</span></span>

## <a name="related-topics"></a><span data-ttu-id="08cac-132">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="08cac-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="08cac-133">Planes de energía</span><span class="sxs-lookup"><span data-stu-id="08cac-133">Power Schemes</span></span>](power-schemes.md)
</dt> </dl>

 

 
