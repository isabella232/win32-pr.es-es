---
description: El usuario puede usar la API del agente de Windows Update (WUA) en un equipo remoto o en una aplicación que se ejecuta en un equipo remoto. Sin embargo, el usuario o la aplicación remotos deben tener privilegios de administrador.
ms.assetid: 15f86590-bed8-4506-916d-43b0bac5db2a
title: Usar WUA desde un equipo remoto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bb14c019e48d6c36b210633ab9d57dcd157585a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696238"
---
# <a name="using-wua-from-a-remote-computer"></a><span data-ttu-id="4e971-104">Usar WUA desde un equipo remoto</span><span class="sxs-lookup"><span data-stu-id="4e971-104">Using WUA From a Remote Computer</span></span>

<span data-ttu-id="4e971-105">El usuario puede usar la API del agente de Windows Update (WUA) en un equipo remoto o en una aplicación que se ejecuta en un equipo remoto.</span><span class="sxs-lookup"><span data-stu-id="4e971-105">The Windows Update Agent (WUA) API can be used by a user on a remote computer or by an application that is running on a remote computer.</span></span> <span data-ttu-id="4e971-106">Sin embargo, el usuario o la aplicación remotos deben tener privilegios de administrador.</span><span class="sxs-lookup"><span data-stu-id="4e971-106">However, the remote user or application must have administrator privileges.</span></span>

<span data-ttu-id="4e971-107">La lista siguiente contiene las interfaces que están disponibles para usuarios y aplicaciones remotos:</span><span class="sxs-lookup"><span data-stu-id="4e971-107">The following list contains interfaces that are available to remote users and applications:</span></span>

-   [<span data-ttu-id="4e971-108">**IUpdateSession**</span><span class="sxs-lookup"><span data-stu-id="4e971-108">**IUpdateSession**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesession)
-   [<span data-ttu-id="4e971-109">**IUpdateSession2**</span><span class="sxs-lookup"><span data-stu-id="4e971-109">**IUpdateSession2**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesession2)
-   [<span data-ttu-id="4e971-110">**IUpdateSearcher**</span><span class="sxs-lookup"><span data-stu-id="4e971-110">**IUpdateSearcher**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesearcher)
-   [<span data-ttu-id="4e971-111">**IAutomaticUpdates**</span><span class="sxs-lookup"><span data-stu-id="4e971-111">**IAutomaticUpdates**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-iautomaticupdates)
-   [<span data-ttu-id="4e971-112">**ISearchResult**</span><span class="sxs-lookup"><span data-stu-id="4e971-112">**ISearchResult**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-isearchresult)
-   [<span data-ttu-id="4e971-113">**IUpdateCollection**</span><span class="sxs-lookup"><span data-stu-id="4e971-113">**IUpdateCollection**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-iupdatecollection)
-   [<span data-ttu-id="4e971-114">**IUpdate**</span><span class="sxs-lookup"><span data-stu-id="4e971-114">**IUpdate**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-iupdate)
-   [<span data-ttu-id="4e971-115">**IUpdate2**</span><span class="sxs-lookup"><span data-stu-id="4e971-115">**IUpdate2**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-iupdate2)
-   [<span data-ttu-id="4e971-116">**IWindowsDriverUpdate**</span><span class="sxs-lookup"><span data-stu-id="4e971-116">**IWindowsDriverUpdate**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-iwindowsdriverupdate)
-   [<span data-ttu-id="4e971-117">**IWindowsDriverUpdate2**</span><span class="sxs-lookup"><span data-stu-id="4e971-117">**IWindowsDriverUpdate2**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-iwindowsdriverupdate2)
-   [<span data-ttu-id="4e971-118">**IUpdateIdentity**</span><span class="sxs-lookup"><span data-stu-id="4e971-118">**IUpdateIdentity**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-iupdateidentity)
-   [<span data-ttu-id="4e971-119">**IImageInformation**</span><span class="sxs-lookup"><span data-stu-id="4e971-119">**IImageInformation**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-iimageinformation)
-   [<span data-ttu-id="4e971-120">**IInstallationBehavior**</span><span class="sxs-lookup"><span data-stu-id="4e971-120">**IInstallationBehavior**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-iinstallationbehavior)
-   [<span data-ttu-id="4e971-121">**IStringCollection**</span><span class="sxs-lookup"><span data-stu-id="4e971-121">**IStringCollection**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-istringcollection)
-   [<span data-ttu-id="4e971-122">**IUpdateHistoryEntryCollection**</span><span class="sxs-lookup"><span data-stu-id="4e971-122">**IUpdateHistoryEntryCollection**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-iupdatehistoryentrycollection)
-   [<span data-ttu-id="4e971-123">**IUpdateHistoryEntry**</span><span class="sxs-lookup"><span data-stu-id="4e971-123">**IUpdateHistoryEntry**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-iupdatehistoryentry)
-   [<span data-ttu-id="4e971-124">**ICategoryCollection**</span><span class="sxs-lookup"><span data-stu-id="4e971-124">**ICategoryCollection**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-icategorycollection)
-   [<span data-ttu-id="4e971-125">**ICategory**</span><span class="sxs-lookup"><span data-stu-id="4e971-125">**ICategory**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-icategory)
-   [<span data-ttu-id="4e971-126">**IUpdateExceptionCollection**</span><span class="sxs-lookup"><span data-stu-id="4e971-126">**IUpdateExceptionCollection**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-iupdateexceptioncollection)
-   [<span data-ttu-id="4e971-127">**IUpdateException**</span><span class="sxs-lookup"><span data-stu-id="4e971-127">**IUpdateException**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-iupdateexception)
-   [<span data-ttu-id="4e971-128">**IUpdateDownloadContentCollection**</span><span class="sxs-lookup"><span data-stu-id="4e971-128">**IUpdateDownloadContentCollection**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-iupdatedownloadcontentcollection)
-   [<span data-ttu-id="4e971-129">**IUpdateDownloadContent**</span><span class="sxs-lookup"><span data-stu-id="4e971-129">**IUpdateDownloadContent**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-iupdatedownloadcontent)
-   [<span data-ttu-id="4e971-130">**IUpdateServiceManager**</span><span class="sxs-lookup"><span data-stu-id="4e971-130">**IUpdateServiceManager**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-iupdateservicemanager)
-   [<span data-ttu-id="4e971-131">**IUpdateServiceCollection**</span><span class="sxs-lookup"><span data-stu-id="4e971-131">**IUpdateServiceCollection**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-iupdateservicecollection)
-   [<span data-ttu-id="4e971-132">**IUpdateService**</span><span class="sxs-lookup"><span data-stu-id="4e971-132">**IUpdateService**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-iupdateservice)
-   [<span data-ttu-id="4e971-133">**IWindowsUpdateAgentInfo**</span><span class="sxs-lookup"><span data-stu-id="4e971-133">**IWindowsUpdateAgentInfo**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-iwindowsupdateagentinfo)

<span data-ttu-id="4e971-134">La lista siguiente contiene las interfaces y las propiedades que no están disponibles para los usuarios y las aplicaciones remotos:</span><span class="sxs-lookup"><span data-stu-id="4e971-134">The following list contains interfaces and properties that are not available to remote users and applications:</span></span>

-   [<span data-ttu-id="4e971-135">**IUpdateSession::CreateUpdateDownloader**</span><span class="sxs-lookup"><span data-stu-id="4e971-135">**IUpdateSession::CreateUpdateDownloader**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesession-createupdatedownloader)
-   [<span data-ttu-id="4e971-136">**IUpdateSession::CreateUpdateInstaller**</span><span class="sxs-lookup"><span data-stu-id="4e971-136">**IUpdateSession::CreateUpdateInstaller**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesession-createupdateinstaller)
-   [<span data-ttu-id="4e971-137">**Propiedad WebProxy de IUpdateSession**</span><span class="sxs-lookup"><span data-stu-id="4e971-137">**WebProxy Property of IUpdateSession**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesession-get_webproxy)
-   [<span data-ttu-id="4e971-138">**IUpdateSearcher::BeginSearch**</span><span class="sxs-lookup"><span data-stu-id="4e971-138">**IUpdateSearcher::BeginSearch**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-beginsearch)
-   [<span data-ttu-id="4e971-139">**IUpdateSearcher::EndSearch**</span><span class="sxs-lookup"><span data-stu-id="4e971-139">**IUpdateSearcher::EndSearch**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-endsearch)
-   <span data-ttu-id="4e971-140">La [**propiedad IsHidden de IUpdate**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_ishidden) (**IsHidden** es de solo lectura cuando se llama de forma remota).</span><span class="sxs-lookup"><span data-stu-id="4e971-140">[**IsHidden Property of IUpdate**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_ishidden) (**IsHidden** is read-only when it is called remotely.)</span></span>
-   [<span data-ttu-id="4e971-141">**IUpdate:: AcceptEula**</span><span class="sxs-lookup"><span data-stu-id="4e971-141">**IUpdate::AcceptEula**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-accepteula)
-   [<span data-ttu-id="4e971-142">**IUpdate::CopyFromCache**</span><span class="sxs-lookup"><span data-stu-id="4e971-142">**IUpdate::CopyFromCache**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-copyfromcache)
-   [<span data-ttu-id="4e971-143">**IUpdate2::CopyToCache**</span><span class="sxs-lookup"><span data-stu-id="4e971-143">**IUpdate2::CopyToCache**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdate2-copytocache)
-   [<span data-ttu-id="4e971-144">**IWindowsDriverUpdate2::CopyToCache**</span><span class="sxs-lookup"><span data-stu-id="4e971-144">**IWindowsDriverUpdate2::CopyToCache**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iwindowsdriverupdate2-copytocache)
-   [<span data-ttu-id="4e971-145">**IUpdateServiceManager:: AddService**</span><span class="sxs-lookup"><span data-stu-id="4e971-145">**IUpdateServiceManager::AddService**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservicemanager-addservice)
-   [<span data-ttu-id="4e971-146">**IUpdateServiceManager::RegisterServiceWithAU**</span><span class="sxs-lookup"><span data-stu-id="4e971-146">**IUpdateServiceManager::RegisterServiceWithAU**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservicemanager-registerservicewithau)
-   [<span data-ttu-id="4e971-147">**IUpdateServiceManager::UnregisterServiceWithAU**</span><span class="sxs-lookup"><span data-stu-id="4e971-147">**IUpdateServiceManager::UnregisterServiceWithAU**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservicemanager-unregisterservicewithau)
-   [<span data-ttu-id="4e971-148">**IAutomaticUpdate::P ause**</span><span class="sxs-lookup"><span data-stu-id="4e971-148">**IAutomaticUpdate::Pause**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdates-pause)
-   [<span data-ttu-id="4e971-149">**IAutomaticUpdates:: resume**</span><span class="sxs-lookup"><span data-stu-id="4e971-149">**IAutomaticUpdates::Resume**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdates-resume)
-   [<span data-ttu-id="4e971-150">**IAutomaticUpdates::ShowSettingsDialog**</span><span class="sxs-lookup"><span data-stu-id="4e971-150">**IAutomaticUpdates::ShowSettingsDialog**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdates-showsettingsdialog)
-   [<span data-ttu-id="4e971-151">**Propiedad de configuración de IAutomaticUpdates**</span><span class="sxs-lookup"><span data-stu-id="4e971-151">**Settings Property of IAutomaticUpdates**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdates-get_settings)
-   [<span data-ttu-id="4e971-152">**Propiedad ServiceEnabled de IAutomaticUpdates**</span><span class="sxs-lookup"><span data-stu-id="4e971-152">**ServiceEnabled Property of IAutomaticUpdates**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdates-get_serviceenabled)
-   [<span data-ttu-id="4e971-153">**IAutomaticUpdates::EnableService**</span><span class="sxs-lookup"><span data-stu-id="4e971-153">**IAutomaticUpdates::EnableService**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdates-enableservice)
-   [<span data-ttu-id="4e971-154">**ISystemInformation**</span><span class="sxs-lookup"><span data-stu-id="4e971-154">**ISystemInformation**</span></span>](/windows/desktop/api/Wuapi/nn-wuapi-isysteminformation)

<span data-ttu-id="4e971-155">Se deben agregar los siguientes puertos y excepciones a la configuración de Firewall de Windows para Windows Vista y Windows Server 2008 para que se llame a la API de WUA de forma remota.</span><span class="sxs-lookup"><span data-stu-id="4e971-155">The following ports and exceptions must be added to the Windows firewall settings for Windows Vista and Windows Server 2008 for the WUA API to be called remotely.</span></span>

<dl> <dt>

<span data-ttu-id="4e971-156"><span id="Exception_1"></span><span id="exception_1"></span><span id="EXCEPTION_1"></span>Excepción 1</span><span class="sxs-lookup"><span data-stu-id="4e971-156"><span id="Exception_1"></span><span id="exception_1"></span><span id="EXCEPTION_1"></span>Exception 1</span></span>
</dt> <dd> <dl> <dd><span data-ttu-id="4e971-157">Puerto local: 135</span><span class="sxs-lookup"><span data-stu-id="4e971-157">Local port: 135</span></span></dd> <dd><span data-ttu-id="4e971-158">Puerto remoto: todos</span><span class="sxs-lookup"><span data-stu-id="4e971-158">Remote port: ALL</span></span></dd> <dd><span data-ttu-id="4e971-159">Número de protocolo: 6</span><span class="sxs-lookup"><span data-stu-id="4e971-159">Protocol number: 6</span></span></dd> <dd><span data-ttu-id="4e971-160">Ejecutable:% WINDIR% \\ system32 \\svchost.exe</span><span class="sxs-lookup"><span data-stu-id="4e971-160">Executable: %windir%\\system32\\svchost.exe</span></span></dd> <dd><span data-ttu-id="4e971-161">Servicio: RPCSS</span><span class="sxs-lookup"><span data-stu-id="4e971-161">Service: rpcss</span></span></dd> <dd><span data-ttu-id="4e971-162">Privilegio remoto: administrador</span><span class="sxs-lookup"><span data-stu-id="4e971-162">Remote privilege: Administrator</span></span></dd> </dl> </dd> <dt>

<span data-ttu-id="4e971-163"><span id="Exception_2"></span><span id="exception_2"></span><span id="EXCEPTION_2"></span>Excepción 2</span><span class="sxs-lookup"><span data-stu-id="4e971-163"><span id="Exception_2"></span><span id="exception_2"></span><span id="EXCEPTION_2"></span>Exception 2</span></span>
</dt> <dd> <dl> <dd><span data-ttu-id="4e971-164">Puerto local: RPC dinámico</span><span class="sxs-lookup"><span data-stu-id="4e971-164">Local port: Dynamic RPC</span></span></dd> <dd><span data-ttu-id="4e971-165">Puerto remoto: todos</span><span class="sxs-lookup"><span data-stu-id="4e971-165">Remote port: ALL</span></span></dd> <dd><span data-ttu-id="4e971-166">Número de protocolo: 6</span><span class="sxs-lookup"><span data-stu-id="4e971-166">Protocol number: 6</span></span></dd> <dd><span data-ttu-id="4e971-167">Ejecutable:% WINDIR% \\ system32 \\dllhost.exe</span><span class="sxs-lookup"><span data-stu-id="4e971-167">Executable: %windir%\\system32\\dllhost.exe</span></span></dd> <dd><span data-ttu-id="4e971-168">Privilegio remoto: administrador</span><span class="sxs-lookup"><span data-stu-id="4e971-168">Remote privilege: Administrator</span></span></dd> </dl> </dd> </dl>

<span data-ttu-id="4e971-169">La lista siguiente contiene herramientas que se pueden usar para configurar el Firewall de Windows:</span><span class="sxs-lookup"><span data-stu-id="4e971-169">The following list contains tools that can be used to configure Windows Firewall settings:</span></span>

-   <span data-ttu-id="4e971-170">Firewall de Windows con complemento de seguridad avanzada</span><span class="sxs-lookup"><span data-stu-id="4e971-170">Windows Firewall with Advanced Security snap-in</span></span>
-   <span data-ttu-id="4e971-171">Directiva de grupo</span><span class="sxs-lookup"><span data-stu-id="4e971-171">Group Policy</span></span>
-   <span data-ttu-id="4e971-172">Herramienta de línea de comandos Netsh advfirewall</span><span class="sxs-lookup"><span data-stu-id="4e971-172">Netsh advfirewall command-line tool</span></span>

<span data-ttu-id="4e971-173">Para obtener más información sobre cómo usar las herramientas para configurar las opciones del firewall de Windows, consulte [Introducción con firewall de Windows con seguridad avanzada](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc748991(v=ws.10)).</span><span class="sxs-lookup"><span data-stu-id="4e971-173">For more information about how to use tools to configure Windows Firewall settings, see [Getting Started with Windows Firewall with Advanced Security](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc748991(v=ws.10)).</span></span>

 

 
