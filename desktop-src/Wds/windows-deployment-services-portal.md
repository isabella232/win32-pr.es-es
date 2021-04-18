---
title: Servicios de implementación de Windows
description: Implementar sistemas operativos Windows. Configure nuevos clientes con una instalación basada en red sin necesidad de que los administradores visiten cada equipo o instalen directamente desde un CD o DVD.
ms.assetid: 790abc27-03cc-4f93-bf04-a4eb37e614bb
keywords:
- Servicios de implementación de Windows servicios de implementación de Windows
- Servicios de implementación de Windows servicios de implementación de Windows, Página principal
- servicios de implementación servicios de implementación de Windows
- Servicios de implementación de Windows WDS véase servicios de implementación de Windows
- Servicios de instalación remota servicios de implementación de Windows ver servicios de implementación de Windows
- Servicios de implementación de Windows de RIS, vea servicios de implementación de Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b35bebb000b383552f12d259ca17552165e9247f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105705021"
---
# <a name="windows-deployment-services"></a><span data-ttu-id="22158-110">Servicios de implementación de Windows</span><span class="sxs-lookup"><span data-stu-id="22158-110">Windows Deployment Services</span></span>

## <a name="purpose"></a><span data-ttu-id="22158-111">Propósito</span><span class="sxs-lookup"><span data-stu-id="22158-111">Purpose</span></span>

<span data-ttu-id="22158-112">Servicios de implementación de Windows (WDS) es la versión revisada de los servicios de instalación remota (RIS).</span><span class="sxs-lookup"><span data-stu-id="22158-112">Windows Deployment Services (WDS) is the revised version of Remote Installation Services (RIS).</span></span> <span data-ttu-id="22158-113">WDS permite la implementación de sistemas operativos Windows.</span><span class="sxs-lookup"><span data-stu-id="22158-113">WDS enables the deployment of Windows operating systems.</span></span> <span data-ttu-id="22158-114">Puede usar WDS para configurar nuevos clientes con una instalación basada en red sin necesidad de que los administradores visiten cada equipo o instalen directamente desde un CD o DVD.</span><span class="sxs-lookup"><span data-stu-id="22158-114">You can use WDS to set up new clients with a network-based installation without requiring that administrators visit each computer or install directly from CD or DVD media.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="22158-115">Audiencia de desarrolladores</span><span class="sxs-lookup"><span data-stu-id="22158-115">Developer audience</span></span>

<span data-ttu-id="22158-116">La audiencia principal del desarrollador de la API de WDS es para los grupos que desarrollan herramientas y procesos personalizados para ti y otros grupos de administración de equipos.</span><span class="sxs-lookup"><span data-stu-id="22158-116">The primary developer audience of the WDS API is for groups that develop custom tools and processes for IT and other computer administration groups.</span></span> <span data-ttu-id="22158-117">En entornos donde no se puede usar la solución estándar de servicios de implementación de Windows (WDS), la API de WDS permite el acceso mediante programación a algunos componentes de WDS.</span><span class="sxs-lookup"><span data-stu-id="22158-117">In environments where the standard Windows Deployment Services (WDS) solution cannot be used, the WDS API enables programmatic access to some WDS components.</span></span>

<span data-ttu-id="22158-118">Los fabricantes de equipos originales (OEM), los ensambladores de equipos y los profesionales de TI de la empresa que buscan información sobre cómo implementar Windows en equipos nuevos, deben ver la información acerca de la solución de servicios de implementación de Windows (WDS) estándar en la [Guía paso a paso de actualización](/previous-versions/windows/it-pro/windows-vista/cc766320(v=ws.10)) de los servicios de implementación de Windows y el [Kit de instalación automatizada de Windows (WAIK)](https://www.microsoft.com/download/details.aspx?id=10333).</span><span class="sxs-lookup"><span data-stu-id="22158-118">Original Equipment Manufacturers (OEMs), system builders, and corporate IT professionals looking for information on how to deploy Windows onto new computers, should see the information about the standard Windows Deployment Services (WDS) solution in the [Windows Deployment Services Update Step-by-Step Guide](/previous-versions/windows/it-pro/windows-vista/cc766320(v=ws.10)) and the [Windows Automated Installation Kit (WAIK)](https://www.microsoft.com/download/details.aspx?id=10333).</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="22158-119">Requisitos de tiempo de ejecución</span><span class="sxs-lookup"><span data-stu-id="22158-119">Run-time requirements</span></span>

<span data-ttu-id="22158-120">WDS está disponible como complemento para Windows Server 2003 con Service Pack 1 (SP1) y se incluye en el sistema operativo a partir de Windows Server 2003 con Service Pack 2 (SP2) y Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="22158-120">WDS is available as an add-on for Windows Server 2003 with Service Pack 1 (SP1) and is included in the operating system starting with Windows Server 2003 with Service Pack 2 (SP2) and Windows Server 2008.</span></span> <span data-ttu-id="22158-121">La API del servidor PXE PXE requiere el rol de servidor de WDS en el servidor para implementar proveedores de PXE personalizados.</span><span class="sxs-lookup"><span data-stu-id="22158-121">The WDS PXE Server API requires the WDS server role on the server to implement custom PXE providers.</span></span> <span data-ttu-id="22158-122">La API de cliente de WDS requiere la fase de Microsoft Entorno de preinstalación de Windows (Windows PE 2,0) del proceso de instalación.</span><span class="sxs-lookup"><span data-stu-id="22158-122">The WDS Client API requires the Microsoft Windows Preinstallation Environment (Windows PE 2.0) phase of setup processing.</span></span> <span data-ttu-id="22158-123">Una imagen de arranque de RAMDISK de Windows PE 2,0 en. El formato WIM se debe descargar como parte del proceso de arranque de red para implementar clientes WDS personalizados.</span><span class="sxs-lookup"><span data-stu-id="22158-123">A RAMDISK bootable image of Windows PE 2.0 in the .WIM format must be downloaded as part of the network boot process to implement custom WDS clients.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="22158-124">En esta sección</span><span class="sxs-lookup"><span data-stu-id="22158-124">In this section</span></span>



| <span data-ttu-id="22158-125">Tema</span><span class="sxs-lookup"><span data-stu-id="22158-125">Topic</span></span>                                                                                                 | <span data-ttu-id="22158-126">Descripción</span><span class="sxs-lookup"><span data-stu-id="22158-126">Description</span></span>                                                                    |
|-------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [<span data-ttu-id="22158-127">Acerca de la API de servicios de implementación de Windows</span><span class="sxs-lookup"><span data-stu-id="22158-127">About the Windows Deployment Services API</span></span>](about-the-windows-deployment-services-api.md)<br/> | <span data-ttu-id="22158-128">Información general sobre la API del servidor WDS y la API de cliente de WDS.</span><span class="sxs-lookup"><span data-stu-id="22158-128">General information about the WDS Server API and WDS Client API.</span></span><br/>    |
| [<span data-ttu-id="22158-129">Referencia de servicios de implementación de Windows</span><span class="sxs-lookup"><span data-stu-id="22158-129">Windows Deployment Services Reference</span></span>](windows-deployment-services-reference.md)<br/>         | <span data-ttu-id="22158-130">Describe las funciones y estructuras de servicios de implementación de Windows.</span><span class="sxs-lookup"><span data-stu-id="22158-130">Describes the Windows Deployment Services functions and structures.</span></span><br/> |



 

 

