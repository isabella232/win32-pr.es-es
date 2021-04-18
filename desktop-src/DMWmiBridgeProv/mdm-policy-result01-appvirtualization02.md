---
title: MDM_Policy_Result01_AppVirtualization02 (clase)
description: La \_ clase Result01 de AppVirtualization02 de directivas MDM \_ \_ representa las directivas de virtualización de aplicaciones disponibles.
ms.assetid: fc28646f-f4b9-4648-a22d-b90d32ff888f
keywords:
- MDM_Policy_Result01_AppVirtualization02 (clase)
- MDM_Policy_Result01_AppVirtualization02 clase, descrita
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_AppVirtualization02
- MDM_Policy_Result01_AppVirtualization02.InstanceID
- MDM_Policy_Result01_AppVirtualization02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 968c4718d7978bdf6770bdf8f828e6ef268cd32d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491176"
---
# <a name="mdm_policy_result01_appvirtualization02-class"></a><span data-ttu-id="6ea18-105">\_ \_ Clase AppVirtualization02 de Result01 de directivas MDM \_</span><span class="sxs-lookup"><span data-stu-id="6ea18-105">MDM\_Policy\_Result01\_AppVirtualization02 class</span></span>

<span data-ttu-id="6ea18-106">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="6ea18-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="6ea18-107">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="6ea18-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="6ea18-108">La \_ clase Result01 de AppVirtualization02 de directivas MDM \_ \_ representa las directivas de virtualización de aplicaciones disponibles.</span><span class="sxs-lookup"><span data-stu-id="6ea18-108">The MDM\_Policy\_Result01\_AppVirtualization02 class represents the available app virtualization policies.</span></span>

<span data-ttu-id="6ea18-109">La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="6ea18-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="6ea18-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6ea18-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_AppVirtualization02
{
  string InstanceID;
  string ParentID;
  string AllowAppVClient;
  string AllowDynamicVirtualization;
  string AllowPackageCleanup;
  string AllowPackageScripts;
  string AllowPublishingRefreshUX;
  string AllowReportingServer;
  string AllowRoamingFileExclusions;
  string AllowRoamingRegistryExclusions;
  string AllowStreamingAutoload;
  string ClientCoexistenceAllowMigrationmode;
  string IntegrationAllowRootGlobal;
  string IntegrationAllowRootUser;
  string PublishingAllowServer1;
  string PublishingAllowServer2;
  string PublishingAllowServer3;
  string PublishingAllowServer4;
  string PublishingAllowServer5;
  string StreamingAllowCertificateFilterForClient_SSL;
  string StreamingAllowHighCostLaunch;
  string StreamingAllowLocationProvider;
  string StreamingAllowPackageInstallationRoot;
  string StreamingAllowPackageSourceRoot;
  string StreamingAllowReestablishmentInterval;
  string StreamingAllowReestablishmentRetries;
  string StreamingSharedContentStoreMode;
  string StreamingSupportBranchCache;
  string StreamingVerifyCertificateRevocationList;
  string VirtualComponentsAllowList;
};
```

## <a name="members"></a><span data-ttu-id="6ea18-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="6ea18-111">Members</span></span>

<span data-ttu-id="6ea18-112">La clase Result01 de la **\_ Directiva MDM \_ \_ AppVirtualization02** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="6ea18-112">The **MDM\_Policy\_Result01\_AppVirtualization02** class has these types of members:</span></span>

-   [<span data-ttu-id="6ea18-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="6ea18-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6ea18-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="6ea18-114">Properties</span></span>

<span data-ttu-id="6ea18-115">La **clase \_ \_ Result01 de \_ AppVirtualization02 de directivas MDM** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="6ea18-115">The **MDM\_Policy\_Result01\_AppVirtualization02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="6ea18-116">AllowAppVClient</span><span class="sxs-lookup"><span data-stu-id="6ea18-116">AllowAppVClient</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-allowappvclient)
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ea18-117">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="6ea18-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6ea18-118">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="6ea18-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="6ea18-119">AllowDynamicVirtualization</span><span class="sxs-lookup"><span data-stu-id="6ea18-119">AllowDynamicVirtualization</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-allowdynamicvirtualization)
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ea18-120">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="6ea18-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6ea18-121">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="6ea18-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="6ea18-122">AllowPackageCleanup</span><span class="sxs-lookup"><span data-stu-id="6ea18-122">AllowPackageCleanup</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-allowpackagecleanup)
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ea18-123">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="6ea18-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6ea18-124">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="6ea18-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="6ea18-125">AllowPackageScripts</span><span class="sxs-lookup"><span data-stu-id="6ea18-125">AllowPackageScripts</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-allowpackagescripts)
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ea18-126">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="6ea18-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6ea18-127">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="6ea18-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="6ea18-128">AllowPublishingRefreshUX</span><span class="sxs-lookup"><span data-stu-id="6ea18-128">AllowPublishingRefreshUX</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-allowpublishingrefreshux)
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ea18-129">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="6ea18-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6ea18-130">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="6ea18-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="6ea18-131">AllowReportingServer</span><span class="sxs-lookup"><span data-stu-id="6ea18-131">AllowReportingServer</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-allowreportingserver)
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ea18-132">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="6ea18-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6ea18-133">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="6ea18-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="6ea18-134">AllowRoamingFileExclusions</span><span class="sxs-lookup"><span data-stu-id="6ea18-134">AllowRoamingFileExclusions</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-allowroamingfileexclusions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ea18-135">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="6ea18-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6ea18-136">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="6ea18-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="6ea18-137">AllowRoamingRegistryExclusions</span><span class="sxs-lookup"><span data-stu-id="6ea18-137">AllowRoamingRegistryExclusions</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-allowroamingregistryexclusions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ea18-138">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="6ea18-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6ea18-139">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="6ea18-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="6ea18-140">AllowStreamingAutoload</span><span class="sxs-lookup"><span data-stu-id="6ea18-140">AllowStreamingAutoload</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-allowstreamingautoload)
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ea18-141">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="6ea18-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6ea18-142">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="6ea18-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="6ea18-143">ClientCoexistenceAllowMigrationmode</span><span class="sxs-lookup"><span data-stu-id="6ea18-143">ClientCoexistenceAllowMigrationmode</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-clientcoexistenceallowmigrationmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ea18-144">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="6ea18-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6ea18-145">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="6ea18-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="6ea18-146">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="6ea18-146">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ea18-147">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="6ea18-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6ea18-148">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6ea18-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6ea18-149">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="6ea18-149">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="6ea18-150">IntegrationAllowRootGlobal</span><span class="sxs-lookup"><span data-stu-id="6ea18-150">IntegrationAllowRootGlobal</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-integrationallowrootglobal)
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ea18-151">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="6ea18-151">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6ea18-152">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="6ea18-152">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="6ea18-153">IntegrationAllowRootUser</span><span class="sxs-lookup"><span data-stu-id="6ea18-153">IntegrationAllowRootUser</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-integrationallowrootuser)
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ea18-154">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="6ea18-154">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6ea18-155">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="6ea18-155">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="6ea18-156">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="6ea18-156">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ea18-157">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="6ea18-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6ea18-158">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6ea18-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6ea18-159">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="6ea18-159">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="6ea18-160">PublishingAllowServer1</span><span class="sxs-lookup"><span data-stu-id="6ea18-160">PublishingAllowServer1</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-publishingallowserver1)
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ea18-161">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="6ea18-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6ea18-162">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="6ea18-162">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="6ea18-163">PublishingAllowServer2</span><span class="sxs-lookup"><span data-stu-id="6ea18-163">PublishingAllowServer2</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-publishingallowserver2)
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ea18-164">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="6ea18-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6ea18-165">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="6ea18-165">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="6ea18-166">PublishingAllowServer3</span><span class="sxs-lookup"><span data-stu-id="6ea18-166">PublishingAllowServer3</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-publishingallowserver3)
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ea18-167">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="6ea18-167">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6ea18-168">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="6ea18-168">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="6ea18-169">PublishingAllowServer4</span><span class="sxs-lookup"><span data-stu-id="6ea18-169">PublishingAllowServer4</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-publishingallowserver4)
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ea18-170">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="6ea18-170">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6ea18-171">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="6ea18-171">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="6ea18-172">PublishingAllowServer5</span><span class="sxs-lookup"><span data-stu-id="6ea18-172">PublishingAllowServer5</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-publishingallowserver5)
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ea18-173">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="6ea18-173">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6ea18-174">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="6ea18-174">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="6ea18-175">StreamingAllowCertificateFilterForClient \_ SSL</span><span class="sxs-lookup"><span data-stu-id="6ea18-175">StreamingAllowCertificateFilterForClient\_SSL</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-streamingallowcertificatefilterforclient-ssl)
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ea18-176">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="6ea18-176">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6ea18-177">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="6ea18-177">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="6ea18-178">StreamingAllowHighCostLaunch</span><span class="sxs-lookup"><span data-stu-id="6ea18-178">StreamingAllowHighCostLaunch</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-streamingallowhighcostlaunch)
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ea18-179">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="6ea18-179">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6ea18-180">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="6ea18-180">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="6ea18-181">StreamingAllowLocationProvider</span><span class="sxs-lookup"><span data-stu-id="6ea18-181">StreamingAllowLocationProvider</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-streamingallowlocationprovider)
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ea18-182">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="6ea18-182">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6ea18-183">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="6ea18-183">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="6ea18-184">StreamingAllowPackageInstallationRoot</span><span class="sxs-lookup"><span data-stu-id="6ea18-184">StreamingAllowPackageInstallationRoot</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-streamingallowpackageinstallationroot)
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ea18-185">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="6ea18-185">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6ea18-186">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="6ea18-186">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="6ea18-187">StreamingAllowPackageSourceRoot</span><span class="sxs-lookup"><span data-stu-id="6ea18-187">StreamingAllowPackageSourceRoot</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-streamingallowpackagesourceroot)
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ea18-188">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="6ea18-188">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6ea18-189">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="6ea18-189">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="6ea18-190">StreamingAllowReestablishmentInterval</span><span class="sxs-lookup"><span data-stu-id="6ea18-190">StreamingAllowReestablishmentInterval</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-streamingallowreestablishmentinterval)
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ea18-191">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="6ea18-191">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6ea18-192">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="6ea18-192">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="6ea18-193">StreamingAllowReestablishmentRetries</span><span class="sxs-lookup"><span data-stu-id="6ea18-193">StreamingAllowReestablishmentRetries</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-streamingallowreestablishmentretries)
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ea18-194">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="6ea18-194">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6ea18-195">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="6ea18-195">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="6ea18-196">StreamingSharedContentStoreMode</span><span class="sxs-lookup"><span data-stu-id="6ea18-196">StreamingSharedContentStoreMode</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-streamingsharedcontentstoremode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ea18-197">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="6ea18-197">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6ea18-198">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="6ea18-198">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="6ea18-199">StreamingSupportBranchCache</span><span class="sxs-lookup"><span data-stu-id="6ea18-199">StreamingSupportBranchCache</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-streamingsupportbranchcache)
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ea18-200">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="6ea18-200">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6ea18-201">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="6ea18-201">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="6ea18-202">StreamingVerifyCertificateRevocationList</span><span class="sxs-lookup"><span data-stu-id="6ea18-202">StreamingVerifyCertificateRevocationList</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-streamingverifycertificaterevocationlist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ea18-203">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="6ea18-203">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6ea18-204">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="6ea18-204">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="6ea18-205">VirtualComponentsAllowList</span><span class="sxs-lookup"><span data-stu-id="6ea18-205">VirtualComponentsAllowList</span></span>](/windows/client-management/mdm/policy-csp-appvirtualization#appvirtualization-virtualcomponentsallowlist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ea18-206">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="6ea18-206">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6ea18-207">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="6ea18-207">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6ea18-208">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6ea18-208">Requirements</span></span>



| <span data-ttu-id="6ea18-209">Requisito</span><span class="sxs-lookup"><span data-stu-id="6ea18-209">Requirement</span></span> | <span data-ttu-id="6ea18-210">Value</span><span class="sxs-lookup"><span data-stu-id="6ea18-210">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6ea18-211">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6ea18-211">Minimum supported client</span></span><br/> | <span data-ttu-id="6ea18-212">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="6ea18-212">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="6ea18-213">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6ea18-213">Minimum supported server</span></span><br/> | <span data-ttu-id="6ea18-214">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="6ea18-214">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="6ea18-215">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="6ea18-215">Namespace</span></span><br/>                | <span data-ttu-id="6ea18-216">Dmmap de MDM raíz de \\ cimv2 \\ \\</span><span class="sxs-lookup"><span data-stu-id="6ea18-216">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="6ea18-217">MOF</span><span class="sxs-lookup"><span data-stu-id="6ea18-217">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6ea18-218"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6ea18-218"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="6ea18-219">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="6ea18-219">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6ea18-220"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6ea18-220"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

