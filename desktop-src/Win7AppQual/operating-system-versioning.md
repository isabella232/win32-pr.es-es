---
description: .
ms.assetid: 974650d9-504a-4f19-bc71-90fbc92672d9
title: Control de versiones del sistema operativo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44e71cb671e19463ca6137c9b0ce7af04c2793e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678419"
---
# <a name="operating-system-versioning"></a><span data-ttu-id="e003c-103">Control de versiones del sistema operativo</span><span class="sxs-lookup"><span data-stu-id="e003c-103">Operating System Versioning</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="e003c-104">Plataformas afectadas</span><span class="sxs-lookup"><span data-stu-id="e003c-104">Affected Platforms</span></span>

<span data-ttu-id="e003c-105">**Clientes** : Windows 7</span><span class="sxs-lookup"><span data-stu-id="e003c-105">**Clients** - Windows 7</span></span>  
<span data-ttu-id="e003c-106">**Servidores** : Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="e003c-106">**Servers** - Windows Server 2008 R2</span></span>  









## <a name="feature-impact"></a><span data-ttu-id="e003c-107">Impacto en las características</span><span class="sxs-lookup"><span data-stu-id="e003c-107">Feature Impact</span></span>

<span data-ttu-id="e003c-108">**Gravedad** alta</span><span class="sxs-lookup"><span data-stu-id="e003c-108">**Severity** - High</span></span>  
<span data-ttu-id="e003c-109">**Frecuencia** : alta</span><span class="sxs-lookup"><span data-stu-id="e003c-109">**Frequency** - High</span></span>  









## <a name="description"></a><span data-ttu-id="e003c-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="e003c-110">Description</span></span>

<span data-ttu-id="e003c-111">El número de versión interno para Windows 7 y Windows Server 2008 R2 es 6,1.</span><span class="sxs-lookup"><span data-stu-id="e003c-111">The internal version number for Windows 7 and Windows Server 2008 R2 is 6.1.</span></span> <span data-ttu-id="e003c-112">La función GetVersion devolverá ahora este número de versión a las aplicaciones cuando se realicen consultas.</span><span class="sxs-lookup"><span data-stu-id="e003c-112">The GetVersion function will now return this version number to applications when queried.</span></span> <span data-ttu-id="e003c-113">Esto es especialmente importante para AntiVirus, copias de seguridad, aplicaciones de utilidad y protección contra copia.</span><span class="sxs-lookup"><span data-stu-id="e003c-113">This is especially important for AntiVirus, backup, utility applications, and copy protection.</span></span>

## <a name="manifestation-of-impact"></a><span data-ttu-id="e003c-114">Manifiesto de impacto</span><span class="sxs-lookup"><span data-stu-id="e003c-114">Manifestation of Impact</span></span>

<span data-ttu-id="e003c-115">La manifestación de este cambio es específica de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="e003c-115">The manifestation of this change is application-specific.</span></span> <span data-ttu-id="e003c-116">Esto significa que cualquier aplicación que compruebe específicamente la versión del sistema operativo obtendrá un número de versión superior, lo que puede dar lugar a una o varias de las siguientes situaciones:</span><span class="sxs-lookup"><span data-stu-id="e003c-116">This means that any application that specifically checks for the operating system version will get a higher version number, which can lead to one or more of the following situations:</span></span>

-   <span data-ttu-id="e003c-117">Es posible que los instaladores de aplicaciones no puedan instalar la aplicación y que las aplicaciones no puedan iniciarse</span><span class="sxs-lookup"><span data-stu-id="e003c-117">Application installers might be unable to install the application, and applications might be unable to start</span></span>
-   <span data-ttu-id="e003c-118">Las aplicaciones pueden volverse inestables o bloquearse</span><span class="sxs-lookup"><span data-stu-id="e003c-118">Applications might become unstable or crash</span></span>
-   <span data-ttu-id="e003c-119">Las aplicaciones pueden generar mensajes de error, pero siguen funcionando correctamente</span><span class="sxs-lookup"><span data-stu-id="e003c-119">Applications might generate error messages, but continue to function properly</span></span>

## <a name="mitigation"></a><span data-ttu-id="e003c-120">Mitigación</span><span class="sxs-lookup"><span data-stu-id="e003c-120">Mitigation</span></span>

<span data-ttu-id="e003c-121">La mayoría de las aplicaciones funcionarán correctamente en Windows 7 y Windows Server 2008 R2 porque la compatibilidad de aplicaciones en Windows 7 y Windows Server 2008 R2 es muy alta.</span><span class="sxs-lookup"><span data-stu-id="e003c-121">Most applications will function properly on Windows 7 and Windows Server 2008 R2 because the application compatibility in Windows 7 and Windows Server 2008 R2 is very high.</span></span> <span data-ttu-id="e003c-122">Sin embargo, Windows 7 y Windows Server 2008 R2 incluyen una vista de compatibilidad para los instaladores y las aplicaciones que comprueban la versión del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="e003c-122">However, Windows 7 and Windows Server 2008 R2 include a Compatibility View for installers and applications that check for operating system version.</span></span>

<span data-ttu-id="e003c-123">Para habilitar la vista de compatibilidad, los usuarios pueden hacer clic con el botón secundario en el acceso directo o el archivo ejecutable y, a continuación, aplicar la vista de compatibilidad de Windows XP SP2 o Windows Vista desde la pestaña Compatibilidad. En la mayoría de los casos, esto debe permitir que la aplicación funcione correctamente sin necesidad de realizar cambios en la aplicación.</span><span class="sxs-lookup"><span data-stu-id="e003c-123">To enable the compatibility view, users can right-click the shortcut or the executable file, and then apply the Windows XP SP2 or Windows Vista Compatibility View from the Compatibility tab. In most cases, this should enable the application to operate properly without the need for any changes to the application.</span></span>

<span data-ttu-id="e003c-124">Los profesionales de ti también pueden aplicar cualquiera de las correcciones de compatibilidad de VersionLie aplicables mediante la herramienta de administrador de compatibilidad, que se instala con el kit de herramientas de compatibilidad de aplicaciones (ACT).</span><span class="sxs-lookup"><span data-stu-id="e003c-124">IT Professionals can also apply any of the applicable VersionLie compatibility fixes, by using the Compatibility Administrator tool, which installs with the Application Compatibility Toolkit (ACT).</span></span> <span data-ttu-id="e003c-125">Por ejemplo, si una aplicación no funciona porque está comprobando, pero no buscando, la información de la versión de Windows XP® con Service Pack 2 (SP2), se puede aplicar WinXPSP2VersionLie para devolver la información de número de versión adecuada a la aplicación, independientemente de la versión del sistema operativo real que se esté ejecutando en el equipo.</span><span class="sxs-lookup"><span data-stu-id="e003c-125">For example, if an application fails to function because it is checking for, but not finding, the Windows XP® with Service Pack 2 (SP2) version information, the WinXPSP2VersionLie can be applied to return the proper version number information to the application, regardless of the actual operating system version that is running on the computer.</span></span> <span data-ttu-id="e003c-126">Las correcciones de compatibilidad de VersionLie disponibles son:</span><span class="sxs-lookup"><span data-stu-id="e003c-126">The available VersionLie compatibility fixes are:</span></span>

-   <span data-ttu-id="e003c-127">Win95VersionLie</span><span class="sxs-lookup"><span data-stu-id="e003c-127">Win95VersionLie</span></span>
-   <span data-ttu-id="e003c-128">Win98VersionLie</span><span class="sxs-lookup"><span data-stu-id="e003c-128">Win98VersionLie</span></span>
-   <span data-ttu-id="e003c-129">WinNT4SP5VersionLie</span><span class="sxs-lookup"><span data-stu-id="e003c-129">WinNT4SP5VersionLie</span></span>
-   <span data-ttu-id="e003c-130">Win2000VersionLie</span><span class="sxs-lookup"><span data-stu-id="e003c-130">Win2000VersionLie</span></span>
-   <span data-ttu-id="e003c-131">Win2000SP1VersionLie</span><span class="sxs-lookup"><span data-stu-id="e003c-131">Win2000SP1VersionLie</span></span>
-   <span data-ttu-id="e003c-132">Win2000SP2VersionLie</span><span class="sxs-lookup"><span data-stu-id="e003c-132">Win2000SP2VersionLie</span></span>
-   <span data-ttu-id="e003c-133">Win2000SP3VersionLie</span><span class="sxs-lookup"><span data-stu-id="e003c-133">Win2000SP3VersionLie</span></span>
-   <span data-ttu-id="e003c-134">WinXPVersionLie</span><span class="sxs-lookup"><span data-stu-id="e003c-134">WinXPVersionLie</span></span>
-   <span data-ttu-id="e003c-135">WinXPSP1VersionLie</span><span class="sxs-lookup"><span data-stu-id="e003c-135">WinXPSP1VersionLie</span></span>
-   <span data-ttu-id="e003c-136">WinXPSP2VersionLie</span><span class="sxs-lookup"><span data-stu-id="e003c-136">WinXPSP2VersionLie</span></span>
-   <span data-ttu-id="e003c-137">VistaRTMVersionLie</span><span class="sxs-lookup"><span data-stu-id="e003c-137">VistaRTMVersionLie</span></span>
-   <span data-ttu-id="e003c-138">VistaSP1VersionLie</span><span class="sxs-lookup"><span data-stu-id="e003c-138">VistaSP1VersionLie</span></span>
-   <span data-ttu-id="e003c-139">VistaSP2VersionLie</span><span class="sxs-lookup"><span data-stu-id="e003c-139">VistaSP2VersionLie</span></span>
-   <span data-ttu-id="e003c-140">Win2K3RTMVersionLie</span><span class="sxs-lookup"><span data-stu-id="e003c-140">Win2K3RTMVersionLie</span></span>
-   <span data-ttu-id="e003c-141">Win2K3SP1VersionLie</span><span class="sxs-lookup"><span data-stu-id="e003c-141">Win2K3SP1VersionLie</span></span>

## <a name="solution"></a><span data-ttu-id="e003c-142">Solución</span><span class="sxs-lookup"><span data-stu-id="e003c-142">Solution</span></span>

<span data-ttu-id="e003c-143">Por lo general, las aplicaciones no deben realizar comprobaciones de la versión del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="e003c-143">Generally, applications should not perform operating system version checks.</span></span> <span data-ttu-id="e003c-144">Si una aplicación necesita una característica específica, es preferible intentar encontrar la característica y producir un error solo si falta la característica necesaria.</span><span class="sxs-lookup"><span data-stu-id="e003c-144">If an application needs a specific feature, it is preferable to try to find the feature, and fail only if the needed feature is missing.</span></span> <span data-ttu-id="e003c-145">Como mínimo, las aplicaciones deben aceptar siempre los números de versión superiores o iguales a la versión más antigua admitida del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="e003c-145">At a minimum, applications should always accept version numbers greater than or equal to the lowest supported version of the operating system.</span></span> <span data-ttu-id="e003c-146">Las excepciones solo deben producirse si hay un requisito específico de la empresa o del sistema.</span><span class="sxs-lookup"><span data-stu-id="e003c-146">Exceptions should occur only if there is a specific legal, business, or system-component requirement.</span></span>

## <a name="links-to-other-resources"></a><span data-ttu-id="e003c-147">Vínculos a otros recursos</span><span class="sxs-lookup"><span data-stu-id="e003c-147">Links to Other Resources</span></span>

-   [<span data-ttu-id="e003c-148">Descarga del kit de herramientas de compatibilidad de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="e003c-148">Application Compatibility Toolkit Download</span></span>](/windows-hardware/get-started/adk-install)
-   <span data-ttu-id="e003c-149">[Correcciones de compatibilidad conocidas, modos de compatibilidad y mensajes de AppHelp](/previous-versions/windows/it-pro/windows-7/cc765984(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="e003c-149">[Known Compatibility Fixes, Compatibility Modes, and AppHelp Messages](/previous-versions/windows/it-pro/windows-7/cc765984(v=ws.10))</span></span>

 

 
