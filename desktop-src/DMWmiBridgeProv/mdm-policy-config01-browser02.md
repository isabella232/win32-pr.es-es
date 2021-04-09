---
title: MDM_Policy_Config01_Browser02 (clase)
description: La \_ clase Config01 de Browser02 de directivas MDM \_ \_ representa las directivas de explorador disponibles.
ms.assetid: 296e3be4-3bc1-4e06-9e31-532639a0b912
keywords:
- MDM_Policy_Config01_Browser02 (clase)
- MDM_Policy_Config01_Browser02 clase, descrita
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_Browser02
- MDM_Policy_Config01_Browser02.InstanceID
- MDM_Policy_Config01_Browser02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba68b4d3f6798a448447e7773dc299977c54434c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079180"
---
# <a name="mdm_policy_config01_browser02-class"></a><span data-ttu-id="0b40e-105">\_ \_ Clase Browser02 de Config01 de directivas MDM \_</span><span class="sxs-lookup"><span data-stu-id="0b40e-105">MDM\_Policy\_Config01\_Browser02 class</span></span>

<span data-ttu-id="0b40e-106">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="0b40e-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="0b40e-107">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="0b40e-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="0b40e-108">La **clase \_ \_ Config01 de \_ Browser02 de directivas MDM** representa las directivas de explorador disponibles.</span><span class="sxs-lookup"><span data-stu-id="0b40e-108">The **MDM\_Policy\_Config01\_Browser02** class represents the browser policies available.</span></span>

<span data-ttu-id="0b40e-109">La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="0b40e-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="0b40e-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0b40e-110">Syntax</span></span>

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_Browser02
{
  string InstanceID;
  string ParentID;
  sint32 AllowAddressBarDropdown;
  sint32 AllowAutofill;
  sint32 AllowCookies;
  sint32 AllowDeveloperTools;
  sint32 AllowInPrivate;
  sint32 AllowMicrosoftCompatibilityList;
  sint32 AllowDoNotTrack;
  sint32 AllowFlashClickToRun;
  sint32 AllowFlash;
  sint32 AllowExtensions;
  sint32 AllowPasswordManager;
  sint32 AllowPopups;
  sint32 AllowSearchEngineCustomization;
  sint32 AllowSearchSuggestionsinAddressBar;
  sint32 AllowSmartScreen;
  sint32 AlwaysEnableBooksLibrary;
  sint32 DisableLockdownOfStartPages;
  string ConfigureAdditionalSearchEngines;
  sint32 ClearBrowsingDataOnExit;
  string EnterpriseModeSiteList;
  string EnterpriseSiteListServiceUrl;
  string Homepages;
  sint32 LockdownFavorites;
  sint32 PreventAccessToAboutFlagsInMicrosoftEdge;
  sint32 PreventLiveTileDataCollection;
  sint32 PreventFirstRunPage;
  sint32 PreventSmartScreenPromptOverride;
  sint32 PreventSmartScreenPromptOverrideForFiles;
  sint32 PreventUsingLocalHostIPAddressForWebRTC;
  string ProvisionFavorites;
  sint32 SendIntranetTraffictoInternetExplorer;
  string SetDefaultSearchEngine;
  sint32 ShowMessageWhenOpeningSitesInInternetExplorer;
  sint32 SyncFavoritesBetweenIEAndMicrosoftEdge;
};
```

## <a name="members"></a><span data-ttu-id="0b40e-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="0b40e-111">Members</span></span>

<span data-ttu-id="0b40e-112">La clase Config01 de la **\_ Directiva MDM \_ \_ Browser02** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="0b40e-112">The **MDM\_Policy\_Config01\_Browser02** class has these types of members:</span></span>

-   [<span data-ttu-id="0b40e-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="0b40e-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0b40e-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="0b40e-114">Properties</span></span>

<span data-ttu-id="0b40e-115">La **clase \_ \_ Config01 de \_ Browser02 de directivas MDM** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="0b40e-115">The **MDM\_Policy\_Config01\_Browser02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="0b40e-116">AllowAddressBarDropdown</span><span class="sxs-lookup"><span data-stu-id="0b40e-116">AllowAddressBarDropdown</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-allowaddressbardropdown)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b40e-117">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="0b40e-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="0b40e-118">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="0b40e-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b40e-119">AllowAutofill</span><span class="sxs-lookup"><span data-stu-id="0b40e-119">AllowAutofill</span></span>](/windows/client-management/mdm/policy-configuration-service-provider)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b40e-120">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="0b40e-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="0b40e-121">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="0b40e-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b40e-122">AllowCookies</span><span class="sxs-lookup"><span data-stu-id="0b40e-122">AllowCookies</span></span>](/windows/client-management/mdm/policy-configuration-service-provider)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b40e-123">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="0b40e-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="0b40e-124">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="0b40e-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b40e-125">AllowDeveloperTools</span><span class="sxs-lookup"><span data-stu-id="0b40e-125">AllowDeveloperTools</span></span>](/windows/client-management/mdm/policy-configuration-service-provider)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b40e-126">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="0b40e-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="0b40e-127">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="0b40e-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b40e-128">AllowDoNotTrack</span><span class="sxs-lookup"><span data-stu-id="0b40e-128">AllowDoNotTrack</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-allowdonottrack)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b40e-129">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="0b40e-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="0b40e-130">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="0b40e-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b40e-131">AllowExtensions</span><span class="sxs-lookup"><span data-stu-id="0b40e-131">AllowExtensions</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-allowextensions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b40e-132">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="0b40e-132">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="0b40e-133">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="0b40e-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b40e-134">AllowFlash</span><span class="sxs-lookup"><span data-stu-id="0b40e-134">AllowFlash</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-allowflash)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b40e-135">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="0b40e-135">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="0b40e-136">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="0b40e-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b40e-137">AllowFlashClickToRun</span><span class="sxs-lookup"><span data-stu-id="0b40e-137">AllowFlashClickToRun</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-allowflashclicktorun)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b40e-138">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="0b40e-138">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="0b40e-139">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="0b40e-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b40e-140">AllowInPrivate</span><span class="sxs-lookup"><span data-stu-id="0b40e-140">AllowInPrivate</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-allowinprivate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b40e-141">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="0b40e-141">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="0b40e-142">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="0b40e-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b40e-143">AllowMicrosoftCompatibilityList</span><span class="sxs-lookup"><span data-stu-id="0b40e-143">AllowMicrosoftCompatibilityList</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-allowmicrosoftcompatibilitylist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b40e-144">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="0b40e-144">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="0b40e-145">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="0b40e-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b40e-146">AllowPasswordManager</span><span class="sxs-lookup"><span data-stu-id="0b40e-146">AllowPasswordManager</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-allowpasswordmanager)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b40e-147">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="0b40e-147">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="0b40e-148">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="0b40e-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b40e-149">AllowPopups</span><span class="sxs-lookup"><span data-stu-id="0b40e-149">AllowPopups</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-allowpopups)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b40e-150">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="0b40e-150">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="0b40e-151">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="0b40e-151">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b40e-152">AllowSearchEngineCustomization</span><span class="sxs-lookup"><span data-stu-id="0b40e-152">AllowSearchEngineCustomization</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-allowsearchenginecustomization)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b40e-153">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="0b40e-153">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="0b40e-154">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="0b40e-154">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b40e-155">AllowSearchSuggestionsinAddressBar</span><span class="sxs-lookup"><span data-stu-id="0b40e-155">AllowSearchSuggestionsinAddressBar</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-allowsearchsuggestionsinaddressbar)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b40e-156">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="0b40e-156">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="0b40e-157">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="0b40e-157">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b40e-158">AllowSmartScreen</span><span class="sxs-lookup"><span data-stu-id="0b40e-158">AllowSmartScreen</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-allowsmartscreen)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b40e-159">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="0b40e-159">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="0b40e-160">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="0b40e-160">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b40e-161">AlwaysEnableBooksLibrary</span><span class="sxs-lookup"><span data-stu-id="0b40e-161">AlwaysEnableBooksLibrary</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-alwaysenablebookslibrary)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b40e-162">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="0b40e-162">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="0b40e-163">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="0b40e-163">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b40e-164">ClearBrowsingDataOnExit</span><span class="sxs-lookup"><span data-stu-id="0b40e-164">ClearBrowsingDataOnExit</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-clearbrowsingdataonexit)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b40e-165">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="0b40e-165">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="0b40e-166">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="0b40e-166">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b40e-167">ConfigureAdditionalSearchEngines</span><span class="sxs-lookup"><span data-stu-id="0b40e-167">ConfigureAdditionalSearchEngines</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-configureadditionalsearchengines)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b40e-168">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="0b40e-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b40e-169">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="0b40e-169">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b40e-170">DisableLockdownOfStartPages</span><span class="sxs-lookup"><span data-stu-id="0b40e-170">DisableLockdownOfStartPages</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-disablelockdownofstartpages)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b40e-171">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="0b40e-171">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="0b40e-172">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="0b40e-172">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b40e-173">EnterpriseModeSiteList</span><span class="sxs-lookup"><span data-stu-id="0b40e-173">EnterpriseModeSiteList</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-enterprisemodesitelist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b40e-174">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="0b40e-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b40e-175">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="0b40e-175">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b40e-176">EnterpriseSiteListServiceUrl</span><span class="sxs-lookup"><span data-stu-id="0b40e-176">EnterpriseSiteListServiceUrl</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-enterprisesitelistserviceurl)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b40e-177">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="0b40e-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b40e-178">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="0b40e-178">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b40e-179">Páginas principales</span><span class="sxs-lookup"><span data-stu-id="0b40e-179">Homepages</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-homepages)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b40e-180">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="0b40e-180">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b40e-181">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="0b40e-181">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="0b40e-182">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="0b40e-182">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b40e-183">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="0b40e-183">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b40e-184">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0b40e-184">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0b40e-185">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="0b40e-185">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="0b40e-186">Identifica el nombre del nodo primario.</span><span class="sxs-lookup"><span data-stu-id="0b40e-186">Identifies the name of the parent node.</span></span> <span data-ttu-id="0b40e-187">Para esta clase, la cadena es "browser".</span><span class="sxs-lookup"><span data-stu-id="0b40e-187">For this class, the string is "Browser".</span></span>

</dd> <dt>

[<span data-ttu-id="0b40e-188">LockdownFavorites</span><span class="sxs-lookup"><span data-stu-id="0b40e-188">LockdownFavorites</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-lockdownfavorites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b40e-189">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="0b40e-189">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="0b40e-190">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="0b40e-190">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="0b40e-191">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="0b40e-191">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b40e-192">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="0b40e-192">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b40e-193">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0b40e-193">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0b40e-194">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="0b40e-194">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="0b40e-195">Describe la ruta de acceso completa al nodo primario.</span><span class="sxs-lookup"><span data-stu-id="0b40e-195">Describes the full path to the parent node.</span></span> <span data-ttu-id="0b40e-196">Para esta clase, la cadena es "./Vendor/MSFT/Policy/Config".</span><span class="sxs-lookup"><span data-stu-id="0b40e-196">For this class, the string is "./Vendor/MSFT/Policy/Config"</span></span>

</dd> <dt>

[<span data-ttu-id="0b40e-197">PreventAccessToAboutFlagsInMicrosoftEdge</span><span class="sxs-lookup"><span data-stu-id="0b40e-197">PreventAccessToAboutFlagsInMicrosoftEdge</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-preventaccesstoaboutflagsinmicrosoftedge)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b40e-198">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="0b40e-198">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="0b40e-199">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="0b40e-199">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b40e-200">PreventFirstRunPage</span><span class="sxs-lookup"><span data-stu-id="0b40e-200">PreventFirstRunPage</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-preventfirstrunpage)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b40e-201">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="0b40e-201">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="0b40e-202">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="0b40e-202">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b40e-203">PreventLiveTileDataCollection</span><span class="sxs-lookup"><span data-stu-id="0b40e-203">PreventLiveTileDataCollection</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-preventlivetiledatacollection)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b40e-204">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="0b40e-204">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="0b40e-205">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="0b40e-205">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b40e-206">PreventSmartScreenPromptOverride</span><span class="sxs-lookup"><span data-stu-id="0b40e-206">PreventSmartScreenPromptOverride</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-preventsmartscreenpromptoverride)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b40e-207">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="0b40e-207">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="0b40e-208">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="0b40e-208">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b40e-209">PreventSmartScreenPromptOverrideForFiles</span><span class="sxs-lookup"><span data-stu-id="0b40e-209">PreventSmartScreenPromptOverrideForFiles</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-preventsmartscreenpromptoverrideforfiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b40e-210">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="0b40e-210">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="0b40e-211">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="0b40e-211">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b40e-212">PreventUsingLocalHostIPAddressForWebRTC</span><span class="sxs-lookup"><span data-stu-id="0b40e-212">PreventUsingLocalHostIPAddressForWebRTC</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-preventusinglocalhostipaddressforwebrtc)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b40e-213">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="0b40e-213">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="0b40e-214">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="0b40e-214">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b40e-215">ProvisionFavorites</span><span class="sxs-lookup"><span data-stu-id="0b40e-215">ProvisionFavorites</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-provisionfavorites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b40e-216">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="0b40e-216">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b40e-217">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="0b40e-217">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b40e-218">SendIntranetTraffictoInternetExplorer</span><span class="sxs-lookup"><span data-stu-id="0b40e-218">SendIntranetTraffictoInternetExplorer</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-sendintranettraffictointernetexplorer)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b40e-219">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="0b40e-219">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="0b40e-220">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="0b40e-220">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b40e-221">SetDefaultSearchEngine</span><span class="sxs-lookup"><span data-stu-id="0b40e-221">SetDefaultSearchEngine</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-setdefaultsearchengine)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b40e-222">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="0b40e-222">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b40e-223">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="0b40e-223">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b40e-224">ShowMessageWhenOpeningSitesInInternetExplorer</span><span class="sxs-lookup"><span data-stu-id="0b40e-224">ShowMessageWhenOpeningSitesInInternetExplorer</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-showmessagewhenopeningsitesininternetexplorer)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b40e-225">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="0b40e-225">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="0b40e-226">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="0b40e-226">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="0b40e-227">SyncFavoritesBetweenIEAndMicrosoftEdge</span><span class="sxs-lookup"><span data-stu-id="0b40e-227">SyncFavoritesBetweenIEAndMicrosoftEdge</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-syncfavoritesbetweenieandmicrosoftedge)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b40e-228">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="0b40e-228">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="0b40e-229">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="0b40e-229">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0b40e-230">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0b40e-230">Requirements</span></span>



| <span data-ttu-id="0b40e-231">Requisito</span><span class="sxs-lookup"><span data-stu-id="0b40e-231">Requirement</span></span> | <span data-ttu-id="0b40e-232">Value</span><span class="sxs-lookup"><span data-stu-id="0b40e-232">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0b40e-233">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0b40e-233">Minimum supported client</span></span><br/> | <span data-ttu-id="0b40e-234">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="0b40e-234">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="0b40e-235">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0b40e-235">Minimum supported server</span></span><br/> | <span data-ttu-id="0b40e-236">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="0b40e-236">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="0b40e-237">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="0b40e-237">Namespace</span></span><br/>                | <span data-ttu-id="0b40e-238">DMMap de MDM raíz de \\ CIMv2 \\ \\</span><span class="sxs-lookup"><span data-stu-id="0b40e-238">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="0b40e-239">MOF</span><span class="sxs-lookup"><span data-stu-id="0b40e-239">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0b40e-240"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0b40e-240"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="0b40e-241">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="0b40e-241">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0b40e-242"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0b40e-242"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0b40e-243">Vea también</span><span class="sxs-lookup"><span data-stu-id="0b40e-243">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b40e-244">Usar scripting de PowerShell con el proveedor de puente WMI</span><span class="sxs-lookup"><span data-stu-id="0b40e-244">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

