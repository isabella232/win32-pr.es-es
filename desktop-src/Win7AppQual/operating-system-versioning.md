---
description: Control de versiones del sistema operativo
ms.assetid: 974650d9-504a-4f19-bc71-90fbc92672d9
title: Control de versiones del sistema operativo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43b2b8c60994eaee7a3becfa9acc03fe2c61fb12
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088043"
---
# <a name="operating-system-versioning"></a><span data-ttu-id="04a14-103">Control de versiones del sistema operativo</span><span class="sxs-lookup"><span data-stu-id="04a14-103">Operating System Versioning</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="04a14-104">Plataformas afectadas</span><span class="sxs-lookup"><span data-stu-id="04a14-104">Affected Platforms</span></span>

<span data-ttu-id="04a14-105">**Clientes:** Windows 7</span><span class="sxs-lookup"><span data-stu-id="04a14-105">**Clients** - Windows 7</span></span>  
<span data-ttu-id="04a14-106">**Servidores:** Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="04a14-106">**Servers** - Windows Server 2008 R2</span></span>  









## <a name="feature-impact"></a><span data-ttu-id="04a14-107">Impacto en las características</span><span class="sxs-lookup"><span data-stu-id="04a14-107">Feature Impact</span></span>

<span data-ttu-id="04a14-108">**Gravedad:** alta</span><span class="sxs-lookup"><span data-stu-id="04a14-108">**Severity** - High</span></span>  
<span data-ttu-id="04a14-109">**Frecuencia:** alta</span><span class="sxs-lookup"><span data-stu-id="04a14-109">**Frequency** - High</span></span>  









## <a name="description"></a><span data-ttu-id="04a14-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="04a14-110">Description</span></span>

<span data-ttu-id="04a14-111">El número de versión interno para Windows 7 y Windows Server 2008 R2 es 6.1.</span><span class="sxs-lookup"><span data-stu-id="04a14-111">The internal version number for Windows 7 and Windows Server 2008 R2 is 6.1.</span></span> <span data-ttu-id="04a14-112">La función GetVersion devolverá ahora este número de versión a las aplicaciones cuando se consulta.</span><span class="sxs-lookup"><span data-stu-id="04a14-112">The GetVersion function will now return this version number to applications when queried.</span></span> <span data-ttu-id="04a14-113">Esto es especialmente importante para antivirus, copia de seguridad, aplicaciones de utilidad y protección de copia.</span><span class="sxs-lookup"><span data-stu-id="04a14-113">This is especially important for AntiVirus, backup, utility applications, and copy protection.</span></span>

## <a name="manifestation-of-impact"></a><span data-ttu-id="04a14-114">Demostración de impacto</span><span class="sxs-lookup"><span data-stu-id="04a14-114">Manifestation of Impact</span></span>

<span data-ttu-id="04a14-115">La expresión de este cambio es específica de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="04a14-115">The manifestation of this change is application-specific.</span></span> <span data-ttu-id="04a14-116">Esto significa que cualquier aplicación que comprueba específicamente la versión del sistema operativo recibirá un número de versión mayor, lo que puede dar lugar a una o varias de las situaciones siguientes:</span><span class="sxs-lookup"><span data-stu-id="04a14-116">This means that any application that specifically checks for the operating system version will get a higher version number, which can lead to one or more of the following situations:</span></span>

-   <span data-ttu-id="04a14-117">Es posible que los instaladores de aplicaciones no puedan instalar la aplicación y que las aplicaciones no puedan iniciarse.</span><span class="sxs-lookup"><span data-stu-id="04a14-117">Application installers might be unable to install the application, and applications might be unable to start</span></span>
-   <span data-ttu-id="04a14-118">Las aplicaciones pueden volverse inestables o bloquearse</span><span class="sxs-lookup"><span data-stu-id="04a14-118">Applications might become unstable or crash</span></span>
-   <span data-ttu-id="04a14-119">Las aplicaciones pueden generar mensajes de error, pero siguen funcionando correctamente</span><span class="sxs-lookup"><span data-stu-id="04a14-119">Applications might generate error messages, but continue to function properly</span></span>

## <a name="mitigation"></a><span data-ttu-id="04a14-120">Mitigación</span><span class="sxs-lookup"><span data-stu-id="04a14-120">Mitigation</span></span>

<span data-ttu-id="04a14-121">La mayoría de las aplicaciones funcionarán correctamente en Windows 7 y Windows Server 2008 R2 porque la compatibilidad de aplicaciones en Windows 7 y Windows Server 2008 R2 es muy alta.</span><span class="sxs-lookup"><span data-stu-id="04a14-121">Most applications will function properly on Windows 7 and Windows Server 2008 R2 because the application compatibility in Windows 7 and Windows Server 2008 R2 is very high.</span></span> <span data-ttu-id="04a14-122">Sin embargo, Windows 7 y Windows Server 2008 R2 incluyen un Vista de compatibilidad para instaladores y aplicaciones que comprueban la versión del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="04a14-122">However, Windows 7 and Windows Server 2008 R2 include a Compatibility View for installers and applications that check for operating system version.</span></span>

<span data-ttu-id="04a14-123">Para habilitar la vista de compatibilidad, los usuarios pueden hacer clic con el botón derecho en el acceso directo o en el archivo ejecutable y, a continuación, aplicar el Vista de compatibilidad Windows XP SP2 o Windows Vista desde la pestaña Compatibilidad. En la mayoría de los casos, esto debería permitir que la aplicación funcione correctamente sin necesidad de realizar ningún cambio en la aplicación.</span><span class="sxs-lookup"><span data-stu-id="04a14-123">To enable the compatibility view, users can right-click the shortcut or the executable file, and then apply the Windows XP SP2 or Windows Vista Compatibility View from the Compatibility tab. In most cases, this should enable the application to operate properly without the need for any changes to the application.</span></span>

<span data-ttu-id="04a14-124">Los profesionales de TI también pueden aplicar cualquiera de las correcciones de compatibilidad de VersionLie aplicables, mediante la herramienta Administrador de compatibilidad, que se instala con Application Compatibility Toolkit (ACT).</span><span class="sxs-lookup"><span data-stu-id="04a14-124">IT Professionals can also apply any of the applicable VersionLie compatibility fixes, by using the Compatibility Administrator tool, which installs with the Application Compatibility Toolkit (ACT).</span></span> <span data-ttu-id="04a14-125">Por ejemplo, si una aplicación no funciona porque está comprobando, pero no buscando, la información de la versión de Windows XP® con Service Pack 2 (SP2), se puede aplicar WinXPSP2VersionLie para devolver la información de número de versión adecuada a la aplicación, independientemente de la versión real del sistema operativo que se ejecute en el equipo.</span><span class="sxs-lookup"><span data-stu-id="04a14-125">For example, if an application fails to function because it is checking for, but not finding, the Windows XP® with Service Pack 2 (SP2) version information, the WinXPSP2VersionLie can be applied to return the proper version number information to the application, regardless of the actual operating system version that is running on the computer.</span></span> <span data-ttu-id="04a14-126">Las correcciones de compatibilidad de VersionLie disponibles son:</span><span class="sxs-lookup"><span data-stu-id="04a14-126">The available VersionLie compatibility fixes are:</span></span>

-   <span data-ttu-id="04a14-127">Win95VersionLie</span><span class="sxs-lookup"><span data-stu-id="04a14-127">Win95VersionLie</span></span>
-   <span data-ttu-id="04a14-128">Win98VersionLie</span><span class="sxs-lookup"><span data-stu-id="04a14-128">Win98VersionLie</span></span>
-   <span data-ttu-id="04a14-129">WinNT4SP5VersionLie</span><span class="sxs-lookup"><span data-stu-id="04a14-129">WinNT4SP5VersionLie</span></span>
-   <span data-ttu-id="04a14-130">Win2000VersionLie</span><span class="sxs-lookup"><span data-stu-id="04a14-130">Win2000VersionLie</span></span>
-   <span data-ttu-id="04a14-131">Win2000SP1VersionLie</span><span class="sxs-lookup"><span data-stu-id="04a14-131">Win2000SP1VersionLie</span></span>
-   <span data-ttu-id="04a14-132">Win2000SP2VersionLie</span><span class="sxs-lookup"><span data-stu-id="04a14-132">Win2000SP2VersionLie</span></span>
-   <span data-ttu-id="04a14-133">Win2000SP3VersionLie</span><span class="sxs-lookup"><span data-stu-id="04a14-133">Win2000SP3VersionLie</span></span>
-   <span data-ttu-id="04a14-134">WinXPVersionLie</span><span class="sxs-lookup"><span data-stu-id="04a14-134">WinXPVersionLie</span></span>
-   <span data-ttu-id="04a14-135">WinXPSP1VersionLie</span><span class="sxs-lookup"><span data-stu-id="04a14-135">WinXPSP1VersionLie</span></span>
-   <span data-ttu-id="04a14-136">WinXPSP2VersionLie</span><span class="sxs-lookup"><span data-stu-id="04a14-136">WinXPSP2VersionLie</span></span>
-   <span data-ttu-id="04a14-137">VistaRTMVersionLie</span><span class="sxs-lookup"><span data-stu-id="04a14-137">VistaRTMVersionLie</span></span>
-   <span data-ttu-id="04a14-138">VistaSP1VersionLie</span><span class="sxs-lookup"><span data-stu-id="04a14-138">VistaSP1VersionLie</span></span>
-   <span data-ttu-id="04a14-139">VistaSP2VersionLie</span><span class="sxs-lookup"><span data-stu-id="04a14-139">VistaSP2VersionLie</span></span>
-   <span data-ttu-id="04a14-140">Win2K3RTMVersionLie</span><span class="sxs-lookup"><span data-stu-id="04a14-140">Win2K3RTMVersionLie</span></span>
-   <span data-ttu-id="04a14-141">Win2K3SP1VersionLie</span><span class="sxs-lookup"><span data-stu-id="04a14-141">Win2K3SP1VersionLie</span></span>

## <a name="solution"></a><span data-ttu-id="04a14-142">Solución</span><span class="sxs-lookup"><span data-stu-id="04a14-142">Solution</span></span>

<span data-ttu-id="04a14-143">Por lo general, las aplicaciones no deben realizar comprobaciones de versión del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="04a14-143">Generally, applications should not perform operating system version checks.</span></span> <span data-ttu-id="04a14-144">Si una aplicación necesita una característica específica, es preferible intentar encontrarla y producir un error solo si falta la característica necesaria.</span><span class="sxs-lookup"><span data-stu-id="04a14-144">If an application needs a specific feature, it is preferable to try to find the feature, and fail only if the needed feature is missing.</span></span> <span data-ttu-id="04a14-145">Como mínimo, las aplicaciones siempre deben aceptar números de versión mayores o iguales que la versión más baja admitida del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="04a14-145">At a minimum, applications should always accept version numbers greater than or equal to the lowest supported version of the operating system.</span></span> <span data-ttu-id="04a14-146">Las excepciones solo deben producirse si hay un requisito legal, empresarial o de componente del sistema específico.</span><span class="sxs-lookup"><span data-stu-id="04a14-146">Exceptions should occur only if there is a specific legal, business, or system-component requirement.</span></span>

## <a name="links-to-other-resources"></a><span data-ttu-id="04a14-147">Vínculos a otros recursos</span><span class="sxs-lookup"><span data-stu-id="04a14-147">Links to Other Resources</span></span>

-   [<span data-ttu-id="04a14-148">Descarga del kit de herramientas de compatibilidad de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="04a14-148">Application Compatibility Toolkit Download</span></span>](/windows-hardware/get-started/adk-install)
-   <span data-ttu-id="04a14-149">[Correcciones de compatibilidad conocidas, modos de compatibilidad y mensajes de AppHelp](/previous-versions/windows/it-pro/windows-7/cc765984(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="04a14-149">[Known Compatibility Fixes, Compatibility Modes, and AppHelp Messages](/previous-versions/windows/it-pro/windows-7/cc765984(v=ws.10))</span></span>

 

 
