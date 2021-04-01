---
title: Arquitectura de Administración remota de Windows
description: La arquitectura Administración remota de Windows consta de componentes en los equipos cliente y servidor.
ms.assetid: 82e67851-fe46-4bb0-8278-9718b5e0c7ae
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0f5576913c5e4a1f2a105fb77e2282dc682c6659
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103793041"
---
# <a name="windows-remote-management-architecture"></a><span data-ttu-id="da78f-103">Arquitectura de Administración remota de Windows</span><span class="sxs-lookup"><span data-stu-id="da78f-103">Windows Remote Management Architecture</span></span>

<span data-ttu-id="da78f-104">La arquitectura Administración remota de Windows consta de componentes en los equipos cliente y servidor.</span><span class="sxs-lookup"><span data-stu-id="da78f-104">The Windows Remote Management architecture consists of components on the client and server computers.</span></span> <span data-ttu-id="da78f-105">En la ilustración siguiente se muestran los componentes de ambos equipos, cómo interactúan los componentes con otros componentes y el protocolo que se usa para la comunicación entre los equipos.</span><span class="sxs-lookup"><span data-stu-id="da78f-105">The following illustration shows the components on both computers, how the components interact with other components, and the protocol that is used to communicate between the computers.</span></span>

![arquitectura de WinRM](images/winrm-architecture.png)

## <a name="requesting-client"></a><span data-ttu-id="da78f-107">Cliente solicitante</span><span class="sxs-lookup"><span data-stu-id="da78f-107">Requesting Client</span></span>

<span data-ttu-id="da78f-108">Los siguientes componentes de WinRM residen en el equipo que ejecuta el script que solicita los datos.</span><span class="sxs-lookup"><span data-stu-id="da78f-108">The following WinRM components reside on the computer that is running the script that requests data.</span></span>

-   <span data-ttu-id="da78f-109">Aplicación WinRM</span><span class="sxs-lookup"><span data-stu-id="da78f-109">WinRM application</span></span>

    <span data-ttu-id="da78f-110">Esta es la herramienta de línea de comandos de **WinRM** o script que usa la API de scripting de WinRM para realizar llamadas para solicitar datos o para ejecutar métodos.</span><span class="sxs-lookup"><span data-stu-id="da78f-110">This is the script or **Winrm** command-line tool that uses the WinRM scripting API to make calls to request data or to execute methods.</span></span> <span data-ttu-id="da78f-111">Para obtener más información, consulte la [API de scripting de WinRM](winrm-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="da78f-111">For more information, see the [WinRM Scripting API](winrm-scripting-api.md).</span></span>

-   <span data-ttu-id="da78f-112">WSMAuto.dll</span><span class="sxs-lookup"><span data-stu-id="da78f-112">WSMAuto.dll</span></span>

    <span data-ttu-id="da78f-113">Nivel de automatización que proporciona compatibilidad con scripting.</span><span class="sxs-lookup"><span data-stu-id="da78f-113">The Automation layer that provides scripting support.</span></span>

-   <span data-ttu-id="da78f-114">WsmCL.dll</span><span class="sxs-lookup"><span data-stu-id="da78f-114">WsmCL.dll</span></span>

    <span data-ttu-id="da78f-115">Nivel de la API de C dentro del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="da78f-115">C API layer within the operating system.</span></span>

-   <span data-ttu-id="da78f-116">API DE HTTP</span><span class="sxs-lookup"><span data-stu-id="da78f-116">HTTP API</span></span>

    <span data-ttu-id="da78f-117">WinRM requiere compatibilidad con el transporte HTTP y HTTPS.</span><span class="sxs-lookup"><span data-stu-id="da78f-117">WinRM requires support for HTTP and HTTPS transport.</span></span>

## <a name="responding-server"></a><span data-ttu-id="da78f-118">Servidor que responde</span><span class="sxs-lookup"><span data-stu-id="da78f-118">Responding Server</span></span>

<span data-ttu-id="da78f-119">Los siguientes componentes de WinRM residen en el equipo que responde.</span><span class="sxs-lookup"><span data-stu-id="da78f-119">The following WinRM components reside on the responding computer.</span></span>

-   <span data-ttu-id="da78f-120">API DE HTTP</span><span class="sxs-lookup"><span data-stu-id="da78f-120">HTTP API</span></span>

    <span data-ttu-id="da78f-121">WinRM requiere compatibilidad con el transporte HTTP y HTTPS.</span><span class="sxs-lookup"><span data-stu-id="da78f-121">WinRM requires support for HTTP and HTTPS transport.</span></span>

-   <span data-ttu-id="da78f-122">WSMAuto.dll</span><span class="sxs-lookup"><span data-stu-id="da78f-122">WSMAuto.dll</span></span>

    <span data-ttu-id="da78f-123">Nivel de automatización que proporciona compatibilidad con scripting.</span><span class="sxs-lookup"><span data-stu-id="da78f-123">The Automation layer that provides scripting support.</span></span>

-   <span data-ttu-id="da78f-124">WsmCL.dll</span><span class="sxs-lookup"><span data-stu-id="da78f-124">WsmCL.dll</span></span>

    <span data-ttu-id="da78f-125">Nivel de la API de C dentro del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="da78f-125">C API layer within the operating system.</span></span>

-   <span data-ttu-id="da78f-126">WsmSvc.dll</span><span class="sxs-lookup"><span data-stu-id="da78f-126">WsmSvc.dll</span></span>

    <span data-ttu-id="da78f-127">Servicio de [*escucha*](windows-remote-management-glossary.md) de WinRM.</span><span class="sxs-lookup"><span data-stu-id="da78f-127">WinRM [*listener*](windows-remote-management-glossary.md) service.</span></span>

-   <span data-ttu-id="da78f-128">WsmProv.dll</span><span class="sxs-lookup"><span data-stu-id="da78f-128">WsmProv.dll</span></span>

    <span data-ttu-id="da78f-129">Subsistema del proveedor.</span><span class="sxs-lookup"><span data-stu-id="da78f-129">Provider subsystem.</span></span>

-   <span data-ttu-id="da78f-130">WsmRes.dll</span><span class="sxs-lookup"><span data-stu-id="da78f-130">WsmRes.dll</span></span>

    <span data-ttu-id="da78f-131">Archivo de recursos.</span><span class="sxs-lookup"><span data-stu-id="da78f-131">Resource file.</span></span>

-   <span data-ttu-id="da78f-132">WsmWmiPl.dll</span><span class="sxs-lookup"><span data-stu-id="da78f-132">WsmWmiPl.dll</span></span>

    <span data-ttu-id="da78f-133">[*Complemento WMI*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="da78f-133">[*WMI plug-in*](windows-remote-management-glossary.md).</span></span> <span data-ttu-id="da78f-134">Esto le permite obtener datos de WMI a través de WinRM.</span><span class="sxs-lookup"><span data-stu-id="da78f-134">This allows you to obtain WMI data through WinRM.</span></span>

-   <span data-ttu-id="da78f-135">Controlador de interfaz de administración de plataforma inteligente (IPMI) y proveedor IPMI de WMI</span><span class="sxs-lookup"><span data-stu-id="da78f-135">Intelligent Platform Management Interface (IPMI) driver and WMI IPMI provider</span></span>

    <span data-ttu-id="da78f-136">Estos componentes proporcionan los datos de hardware solicitados mediante las clases de IPMI.</span><span class="sxs-lookup"><span data-stu-id="da78f-136">These components supply any hardware data that is requested using the IPMI classes.</span></span> <span data-ttu-id="da78f-137">Para obtener más información, consulte [proveedor IPMI](/previous-versions/windows/desktop/ipmiprv/ipmi-provider).</span><span class="sxs-lookup"><span data-stu-id="da78f-137">For more information, see [IPMI Provider](/previous-versions/windows/desktop/ipmiprv/ipmi-provider).</span></span> <span data-ttu-id="da78f-138">El SMBIOS debe haber detectado hardware de BMC o el dispositivo creado manualmente cargando el controlador.</span><span class="sxs-lookup"><span data-stu-id="da78f-138">BMC hardware must have been detected by the SMBIOS or the device created manually by loading the driver.</span></span> <span data-ttu-id="da78f-139">Para obtener más información, vea [instalación y configuración de administración remota de Windows](installation-and-configuration-for-windows-remote-management.md).</span><span class="sxs-lookup"><span data-stu-id="da78f-139">For more information, see [Installation and Configuration for Windows Remote Management](installation-and-configuration-for-windows-remote-management.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="da78f-140">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="da78f-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="da78f-141">Acerca de Administración remota de Windows</span><span class="sxs-lookup"><span data-stu-id="da78f-141">About Windows Remote Management</span></span>](about-windows-remote-management.md)
</dt> </dl>

 

 