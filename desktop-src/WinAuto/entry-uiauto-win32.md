---
title: Automatización de la interfaz de usuario
description: La automatización de la interfaz de usuario de Microsoft es un marco de accesibilidad que permite que las aplicaciones Windows proporcionen y consuman información mediante programación sobre las interfaces de usuario (IUS).
ms.assetid: 700ca38d-ff40-472b-a95a-11fa94c3bc1d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8006c79299cc1f736dc43555968443f634d4a51
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103904728"
---
# <a name="ui-automation"></a><span data-ttu-id="8072a-103">Automatización de la interfaz de usuario</span><span class="sxs-lookup"><span data-stu-id="8072a-103">UI Automation</span></span>

<span data-ttu-id="8072a-104">La automatización de la interfaz de usuario de Microsoft es un marco de accesibilidad que permite que las aplicaciones Windows proporcionen y consuman información mediante programación sobre las interfaces de usuario (IUS).</span><span class="sxs-lookup"><span data-stu-id="8072a-104">Microsoft UI Automation is an accessibility framework that enables Windows applications to provide and consume programmatic information about user interfaces (UIs).</span></span> <span data-ttu-id="8072a-105">Proporciona acceso mediante programación a la mayoría de los elementos de la interfaz de usuario en el escritorio.</span><span class="sxs-lookup"><span data-stu-id="8072a-105">It provides programmatic access to most UI elements on the desktop.</span></span> <span data-ttu-id="8072a-106">Permite productos de tecnología de asistencia, como lectores de pantalla, para proporcionar información sobre la interfaz de usuario a los usuarios finales y manipular la interfaz de usuario por medios distintos de la entrada estándar.</span><span class="sxs-lookup"><span data-stu-id="8072a-106">It enables assistive technology products, such as screen readers, to provide information about the UI to end users and to manipulate the UI by means other than standard input.</span></span> <span data-ttu-id="8072a-107">UI Automation también permite que los scripts de pruebas automatizadas interactúen con la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="8072a-107">UI Automation also allows automated test scripts to interact with the UI.</span></span>

-   [<span data-ttu-id="8072a-108">Cuando proceda</span><span class="sxs-lookup"><span data-stu-id="8072a-108">Where Applicable</span></span>](#where-applicable)
-   [<span data-ttu-id="8072a-109">Audiencia para desarrolladores</span><span class="sxs-lookup"><span data-stu-id="8072a-109">Developer Audience</span></span>](#developer-audience)
-   [<span data-ttu-id="8072a-110">Requisitos de tiempo de ejecución</span><span class="sxs-lookup"><span data-stu-id="8072a-110">Run-Time Requirements</span></span>](#run-time-requirements)
-   [<span data-ttu-id="8072a-111">Compatibilidad con sistemas operativos de nivel inferior</span><span class="sxs-lookup"><span data-stu-id="8072a-111">Support for Down-level Operating Systems</span></span>](#support-for-down-level-operating-systems)

## <a name="where-applicable"></a><span data-ttu-id="8072a-112">Dónde se puede aplicar</span><span class="sxs-lookup"><span data-stu-id="8072a-112">Where Applicable</span></span>

<span data-ttu-id="8072a-113">Mediante la automatización de la interfaz de usuario y las siguientes prácticas de diseño accesibles, los desarrolladores pueden hacer que las aplicaciones que se ejecutan en Windows sean más accesibles para muchas personas con discapacidades visuales, auditivas o de movimiento.</span><span class="sxs-lookup"><span data-stu-id="8072a-113">By using UI Automation and following accessible design practices, developers can make applications running on Windows more accessible to many people with vision, hearing, or motion disabilities.</span></span> <span data-ttu-id="8072a-114">Además, la automatización de la interfaz de usuario está diseñada específicamente para proporcionar una sólida funcionalidad para escenarios de pruebas automatizadas.</span><span class="sxs-lookup"><span data-stu-id="8072a-114">Also, UI Automation is specifically designed to provide robust functionality for automated testing scenarios.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="8072a-115">Audiencia de los desarrolladores</span><span class="sxs-lookup"><span data-stu-id="8072a-115">Developer Audience</span></span>

<span data-ttu-id="8072a-116">La automatización de la interfaz de usuario está diseñada para desarrolladores de C/C++ con experiencia.</span><span class="sxs-lookup"><span data-stu-id="8072a-116">UI Automation is designed for experienced C/C++ developers.</span></span> <span data-ttu-id="8072a-117">En general, los desarrolladores necesitan un nivel moderado de conocimiento sobre objetos e interfaces COM (modelo de objetos componentes), Unicode y programación de la API de Windows.</span><span class="sxs-lookup"><span data-stu-id="8072a-117">In general, developers need a moderate level of understanding about Component Object Model (COM) objects and interfaces, Unicode, and Windows API programming.</span></span>

<span data-ttu-id="8072a-118">Para obtener información sobre la automatización de la interfaz de usuario para código administrado, vea [accesibilidad](/dotnet/framework/ui-automation/) en la sección Guía del desarrollador de .NET Framework de MSDN.</span><span class="sxs-lookup"><span data-stu-id="8072a-118">For information about UI Automation for managed code, please see [Accessibility](/dotnet/framework/ui-automation/) in the .NET Framework Developer's Guide section of MSDN.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="8072a-119">Requisitos del tiempo de ejecución</span><span class="sxs-lookup"><span data-stu-id="8072a-119">Run-Time Requirements</span></span>

<span data-ttu-id="8072a-120">La automatización de la interfaz de usuario es compatible con los siguientes sistemas operativos: Windows XP, Windows Server 2003, Windows Server 2003 R2, Windows Vista, Windows 7, Windows 10, Windows Server 2008, Windows Server 2008 R2, Windows Server 2012, Windows Server 2012 R2, Windows Server 2016 y Windows Server 2019.</span><span class="sxs-lookup"><span data-stu-id="8072a-120">UI Automation is supported on the following operating systems: Windows XP, Windows Server 2003, Windows Server 2003 R2, Windows Vista, Windows 7, Windows 10, Windows Server 2008, Windows Server 2008 R2, Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, and Windows Server 2019.</span></span>

> [!Note]  
> <span data-ttu-id="8072a-121">Windows XP y Windows Server 2003 también requieren Microsoft .NET Framework 3,0.</span><span class="sxs-lookup"><span data-stu-id="8072a-121">Windows XP and Windows Server 2003 also require Microsoft .NET Framework 3.0.</span></span>

 

## <a name="support-for-down-level-operating-systems"></a><span data-ttu-id="8072a-122">Compatibilidad con sistemas operativos de nivel inferior</span><span class="sxs-lookup"><span data-stu-id="8072a-122">Support for Down-level Operating Systems</span></span>

<span data-ttu-id="8072a-123">La actualización de la plataforma para Windows Vista es un conjunto de bibliotecas en tiempo de ejecución que permite a los desarrolladores destinar aplicaciones a Windows 7 y a sistemas operativos de nivel inferior.</span><span class="sxs-lookup"><span data-stu-id="8072a-123">The Platform Update for Windows Vista is a set of run-time libraries that enables developers to target applications to both Windows 7 and down-level operating systems.</span></span> <span data-ttu-id="8072a-124">La actualización de la plataforma para Windows Server 2008 es un conjunto de bibliotecas en tiempo de ejecución que permite a los desarrolladores destinar aplicaciones a Windows Server 2008 R2 y versiones anteriores de Windows Server.</span><span class="sxs-lookup"><span data-stu-id="8072a-124">The Platform Update for Windows Server 2008 is a set of run-time libraries that enables developers to target applications to both Windows Server 2008 R2 and previous versions of Windows Server.</span></span> <span data-ttu-id="8072a-125">La actualización de la plataforma para Windows Vista y la actualización de la plataforma para Windows Server 2008 estarán disponibles para todos los clientes de Windows Vista y Windows Server 2008 a través de Windows Update.</span><span class="sxs-lookup"><span data-stu-id="8072a-125">The Platform Update for Windows Vista and the Platform Update for Windows Server 2008 will be available to all Windows Vista and Windows Server 2008 customers through Windows Update.</span></span> <span data-ttu-id="8072a-126">Las aplicaciones de terceros que requieren la actualización de la plataforma para Windows Vista o la actualización de la plataforma para Windows Server 2008 pueden detectar Windows Update detectar si está instalado; en caso contrario, Windows Update lo descargará e instalará en segundo plano.</span><span class="sxs-lookup"><span data-stu-id="8072a-126">Third-party applications that require Platform Update for Windows Vista or Platform Update for Windows Server 2008 can have Windows Update detect whether it is installed; if it is not, Windows Update will download and install it in the background.</span></span>

<span data-ttu-id="8072a-127">La actualización de la plataforma para Windows Vista y la actualización de la plataforma para Windows Server 2008 admiten todo el conjunto de características de Windows Automation API 3,0 en los sistemas operativos siguientes.</span><span class="sxs-lookup"><span data-stu-id="8072a-127">The Platform Update for Windows Vista and the Platform Update for Windows Server 2008 both support the entire Windows Automation API 3.0 feature set on the following operating systems.</span></span>

-   <span data-ttu-id="8072a-128">Windows XP (Inglés)</span><span class="sxs-lookup"><span data-stu-id="8072a-128">Windows XP (English)</span></span> <dl> <span data-ttu-id="8072a-129">Windows XP Home SP3 x86</span><span class="sxs-lookup"><span data-stu-id="8072a-129">Windows XP Home SP3 x86</span></span>  
    <span data-ttu-id="8072a-130">Windows XP Professional SP3 x86</span><span class="sxs-lookup"><span data-stu-id="8072a-130">Windows XP Professional SP3 x86</span></span>  
    </dl>
-   Windows Server 2003 (English) <dl> <span data-ttu-id="8072a-131">Windows Server 2003 SP2 (x86 y x64)</span><span class="sxs-lookup"><span data-stu-id="8072a-131">Windows Server 2003 SP2 (x86 and x64)</span></span>  
    </dl>
-   <span data-ttu-id="8072a-132">Windows Vista (Inglés)</span><span class="sxs-lookup"><span data-stu-id="8072a-132">Windows Vista (English)</span></span> <dl> <span data-ttu-id="8072a-133">Starter SP2 (x86 y x64)</span><span class="sxs-lookup"><span data-stu-id="8072a-133">Starter SP2 (x86 and x64)</span></span>  
    <span data-ttu-id="8072a-134">Home Premium SP2 (x86 y x64)</span><span class="sxs-lookup"><span data-stu-id="8072a-134">Home Premium SP2 (x86 and x64)</span></span>  
    <span data-ttu-id="8072a-135">Service Pack 2 (x86 y x64)</span><span class="sxs-lookup"><span data-stu-id="8072a-135">Business SP2 (x86 and x64)</span></span>  
    <span data-ttu-id="8072a-136">Enterprise SP2 (x86 y x64)</span><span class="sxs-lookup"><span data-stu-id="8072a-136">Enterprise SP2 (x86 and x64)</span></span>  
    <span data-ttu-id="8072a-137">Ultimate SP2 (x86 y x64)</span><span class="sxs-lookup"><span data-stu-id="8072a-137">Ultimate SP2 (x86 and x64)</span></span>  
    </dl>
-   <span data-ttu-id="8072a-138">Windows Server 2008 (Inglés)</span><span class="sxs-lookup"><span data-stu-id="8072a-138">Windows Server 2008 (English)</span></span> <dl> <span data-ttu-id="8072a-139">Windows Server 2008 SP2 (x86 y x64)</span><span class="sxs-lookup"><span data-stu-id="8072a-139">Windows Server 2008 SP2 (x86 and x64)</span></span>  
    </dl>

<span data-ttu-id="8072a-140">Para obtener más información acerca de ambas actualizaciones, consulte [actualización de la plataforma para Windows Vista](../win7ip/platform-update-for-windows-vista-portal.md).</span><span class="sxs-lookup"><span data-stu-id="8072a-140">For more information about both updates, see [Platform Update for Windows Vista](../win7ip/platform-update-for-windows-vista-portal.md).</span></span>

## <a name="in-this-section"></a><span data-ttu-id="8072a-141">En esta sección</span><span class="sxs-lookup"><span data-stu-id="8072a-141">In this section</span></span>

-   [<span data-ttu-id="8072a-142">Fundamentos de UI Automation</span><span class="sxs-lookup"><span data-stu-id="8072a-142">UI Automation Fundamentals</span></span>](entry-uiautocore-overview.md)
-   [<span data-ttu-id="8072a-143">Guía del programador del proveedor de UI Automation</span><span class="sxs-lookup"><span data-stu-id="8072a-143">UI Automation Provider Programmer's Guide</span></span>](uiauto-providerportal.md)
-   [<span data-ttu-id="8072a-144">Guía del programador del cliente de UI Automation</span><span class="sxs-lookup"><span data-stu-id="8072a-144">UI Automation Client Programmer's Guide</span></span>](uiauto-clientportal.md)
-   [<span data-ttu-id="8072a-145">Referencia</span><span class="sxs-lookup"><span data-stu-id="8072a-145">Reference</span></span>](entry-uiautocore-ref.md)
-   [<span data-ttu-id="8072a-146">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="8072a-146">Samples</span></span>](samples-entry.md)
-   [<span data-ttu-id="8072a-147">Apéndices</span><span class="sxs-lookup"><span data-stu-id="8072a-147">Appendixes</span></span>](appendix-entry.md)

 

 