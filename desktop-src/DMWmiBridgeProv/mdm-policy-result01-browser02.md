---
title: MDM_Policy_Result01_Browser02 (clase)
description: La \_ clase Result01 de Browser02 de directivas MDM \_ \_ representa las directivas de explorador disponibles. \_ \_ \_ La clase Browser02 de RESULT01 de directivas MDM representa las directivas de explorador disponibles.
ms.assetid: 06dc9f68-d9ea-4eec-93cb-1f26e8a6050d
keywords:
- MDM_Policy_Result01_Browser02 (clase)
- MDM_Policy_Result01_Browser02 clase, descrita
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_Browser02
- MDM_Policy_Result01_Browser02.InstanceID
- MDM_Policy_Result01_Browser02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 19d132c43b88b242864e248b705a0f6bca02e546
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905024"
---
# <a name="mdm_policy_result01_browser02-class"></a><span data-ttu-id="a62b1-105">\_ \_ Clase Browser02 de Result01 de directivas MDM \_</span><span class="sxs-lookup"><span data-stu-id="a62b1-105">MDM\_Policy\_Result01\_Browser02 class</span></span>

<span data-ttu-id="a62b1-106">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="a62b1-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="a62b1-107">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="a62b1-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="a62b1-108">La **clase \_ \_ Result01 de \_ Browser02 de directivas MDM** representa las directivas de explorador disponibles.</span><span class="sxs-lookup"><span data-stu-id="a62b1-108">The **MDM\_Policy\_Result01\_Browser02** class represents the browser policies available.</span></span>

<span data-ttu-id="a62b1-109">La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="a62b1-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="a62b1-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a62b1-110">Syntax</span></span>

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_Browser02
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

## <a name="members"></a><span data-ttu-id="a62b1-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="a62b1-111">Members</span></span>

<span data-ttu-id="a62b1-112">La clase Result01 de la **\_ Directiva MDM \_ \_ Browser02** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="a62b1-112">The **MDM\_Policy\_Result01\_Browser02** class has these types of members:</span></span>

-   [<span data-ttu-id="a62b1-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="a62b1-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a62b1-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="a62b1-114">Properties</span></span>

<span data-ttu-id="a62b1-115">La **clase \_ \_ Result01 de \_ Browser02 de directivas MDM** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="a62b1-115">The **MDM\_Policy\_Result01\_Browser02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="a62b1-116">AllowAddressBarDropdown</span><span class="sxs-lookup"><span data-stu-id="a62b1-116">AllowAddressBarDropdown</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-allowaddressbardropdown)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a62b1-117">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="a62b1-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="a62b1-118">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="a62b1-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a62b1-119">AllowAutofill</span><span class="sxs-lookup"><span data-stu-id="a62b1-119">AllowAutofill</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-allowautofill)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a62b1-120">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="a62b1-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="a62b1-121">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="a62b1-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a62b1-122">AllowCookies</span><span class="sxs-lookup"><span data-stu-id="a62b1-122">AllowCookies</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-allowcookies)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a62b1-123">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="a62b1-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="a62b1-124">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="a62b1-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a62b1-125">AllowDeveloperTools</span><span class="sxs-lookup"><span data-stu-id="a62b1-125">AllowDeveloperTools</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-allowdevelopertools)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a62b1-126">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="a62b1-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="a62b1-127">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="a62b1-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a62b1-128">AllowDoNotTrack</span><span class="sxs-lookup"><span data-stu-id="a62b1-128">AllowDoNotTrack</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-allowdonottrack)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a62b1-129">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="a62b1-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="a62b1-130">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="a62b1-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a62b1-131">AllowExtensions</span><span class="sxs-lookup"><span data-stu-id="a62b1-131">AllowExtensions</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-allowextensions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a62b1-132">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="a62b1-132">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="a62b1-133">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="a62b1-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a62b1-134">AllowFlash</span><span class="sxs-lookup"><span data-stu-id="a62b1-134">AllowFlash</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-allowflash)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a62b1-135">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="a62b1-135">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="a62b1-136">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="a62b1-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a62b1-137">AllowFlashClickToRun</span><span class="sxs-lookup"><span data-stu-id="a62b1-137">AllowFlashClickToRun</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-allowflashclicktorun)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a62b1-138">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="a62b1-138">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="a62b1-139">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="a62b1-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a62b1-140">AllowInPrivate</span><span class="sxs-lookup"><span data-stu-id="a62b1-140">AllowInPrivate</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-allowinprivate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a62b1-141">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="a62b1-141">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="a62b1-142">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="a62b1-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a62b1-143">AllowMicrosoftCompatibilityList</span><span class="sxs-lookup"><span data-stu-id="a62b1-143">AllowMicrosoftCompatibilityList</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-allowmicrosoftcompatibilitylist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a62b1-144">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="a62b1-144">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="a62b1-145">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="a62b1-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a62b1-146">AllowPasswordManager</span><span class="sxs-lookup"><span data-stu-id="a62b1-146">AllowPasswordManager</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-allowpasswordmanager)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a62b1-147">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="a62b1-147">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="a62b1-148">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="a62b1-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a62b1-149">AllowPopups</span><span class="sxs-lookup"><span data-stu-id="a62b1-149">AllowPopups</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-allowpopups)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a62b1-150">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="a62b1-150">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="a62b1-151">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="a62b1-151">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a62b1-152">AllowSearchEngineCustomization</span><span class="sxs-lookup"><span data-stu-id="a62b1-152">AllowSearchEngineCustomization</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-allowsearchenginecustomization)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a62b1-153">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="a62b1-153">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="a62b1-154">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="a62b1-154">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a62b1-155">AllowSearchSuggestionsinAddressBar</span><span class="sxs-lookup"><span data-stu-id="a62b1-155">AllowSearchSuggestionsinAddressBar</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-allowsearchsuggestionsinaddressbar)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a62b1-156">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="a62b1-156">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="a62b1-157">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="a62b1-157">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a62b1-158">AllowSmartScreen</span><span class="sxs-lookup"><span data-stu-id="a62b1-158">AllowSmartScreen</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-allowsmartscreen)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a62b1-159">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="a62b1-159">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="a62b1-160">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="a62b1-160">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a62b1-161">AlwaysEnableBooksLibrary</span><span class="sxs-lookup"><span data-stu-id="a62b1-161">AlwaysEnableBooksLibrary</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-alwaysenablebookslibrary)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a62b1-162">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="a62b1-162">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="a62b1-163">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="a62b1-163">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a62b1-164">ClearBrowsingDataOnExit</span><span class="sxs-lookup"><span data-stu-id="a62b1-164">ClearBrowsingDataOnExit</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-clearbrowsingdataonexit)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a62b1-165">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="a62b1-165">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="a62b1-166">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="a62b1-166">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a62b1-167">ConfigureAdditionalSearchEngines</span><span class="sxs-lookup"><span data-stu-id="a62b1-167">ConfigureAdditionalSearchEngines</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-configureadditionalsearchengines)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a62b1-168">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a62b1-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a62b1-169">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="a62b1-169">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a62b1-170">DisableLockdownOfStartPages</span><span class="sxs-lookup"><span data-stu-id="a62b1-170">DisableLockdownOfStartPages</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-disablelockdownofstartpages)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a62b1-171">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="a62b1-171">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="a62b1-172">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="a62b1-172">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a62b1-173">EnterpriseModeSiteList</span><span class="sxs-lookup"><span data-stu-id="a62b1-173">EnterpriseModeSiteList</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-enterprisemodesitelist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a62b1-174">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a62b1-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a62b1-175">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="a62b1-175">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a62b1-176">EnterpriseSiteListServiceUrl</span><span class="sxs-lookup"><span data-stu-id="a62b1-176">EnterpriseSiteListServiceUrl</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-enterprisesitelistserviceurl)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a62b1-177">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a62b1-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a62b1-178">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="a62b1-178">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a62b1-179">Páginas principales</span><span class="sxs-lookup"><span data-stu-id="a62b1-179">Homepages</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-homepages)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a62b1-180">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a62b1-180">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a62b1-181">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="a62b1-181">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="a62b1-182">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="a62b1-182">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a62b1-183">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a62b1-183">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a62b1-184">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a62b1-184">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a62b1-185">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="a62b1-185">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="a62b1-186">Identifica el nombre del nodo primario.</span><span class="sxs-lookup"><span data-stu-id="a62b1-186">Identifies the name of the parent node.</span></span> <span data-ttu-id="a62b1-187">Para esta clase, la cadena es "browser".</span><span class="sxs-lookup"><span data-stu-id="a62b1-187">For this class, the string is "Browser".</span></span>

</dd> <dt>

[<span data-ttu-id="a62b1-188">LockdownFavorites</span><span class="sxs-lookup"><span data-stu-id="a62b1-188">LockdownFavorites</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-lockdownfavorites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a62b1-189">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="a62b1-189">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="a62b1-190">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="a62b1-190">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="a62b1-191">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="a62b1-191">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a62b1-192">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a62b1-192">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a62b1-193">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a62b1-193">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a62b1-194">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="a62b1-194">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="a62b1-195">Describe la ruta de acceso completa al nodo primario.</span><span class="sxs-lookup"><span data-stu-id="a62b1-195">Describes the full path to the parent node.</span></span> <span data-ttu-id="a62b1-196">Para esta clase, la cadena es "./Vendor/MSFT/Policy/Result".</span><span class="sxs-lookup"><span data-stu-id="a62b1-196">For this class, the string is "./Vendor/MSFT/Policy/Result"</span></span>

</dd> <dt>

[<span data-ttu-id="a62b1-197">PreventAccessToAboutFlagsInMicrosoftEdge</span><span class="sxs-lookup"><span data-stu-id="a62b1-197">PreventAccessToAboutFlagsInMicrosoftEdge</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-preventaccesstoaboutflagsinmicrosoftedge)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a62b1-198">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="a62b1-198">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="a62b1-199">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="a62b1-199">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a62b1-200">PreventFirstRunPage</span><span class="sxs-lookup"><span data-stu-id="a62b1-200">PreventFirstRunPage</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-preventfirstrunpage)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a62b1-201">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="a62b1-201">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="a62b1-202">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="a62b1-202">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a62b1-203">PreventLiveTileDataCollection</span><span class="sxs-lookup"><span data-stu-id="a62b1-203">PreventLiveTileDataCollection</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-preventlivetiledatacollection)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a62b1-204">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="a62b1-204">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="a62b1-205">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="a62b1-205">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a62b1-206">PreventSmartScreenPromptOverride</span><span class="sxs-lookup"><span data-stu-id="a62b1-206">PreventSmartScreenPromptOverride</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-preventsmartscreenpromptoverride)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a62b1-207">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="a62b1-207">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="a62b1-208">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="a62b1-208">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a62b1-209">PreventSmartScreenPromptOverrideForFiles</span><span class="sxs-lookup"><span data-stu-id="a62b1-209">PreventSmartScreenPromptOverrideForFiles</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-preventsmartscreenpromptoverrideforfiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a62b1-210">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="a62b1-210">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="a62b1-211">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="a62b1-211">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a62b1-212">PreventUsingLocalHostIPAddressForWebRTC</span><span class="sxs-lookup"><span data-stu-id="a62b1-212">PreventUsingLocalHostIPAddressForWebRTC</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-preventusinglocalhostipaddressforwebrtc)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a62b1-213">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="a62b1-213">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="a62b1-214">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="a62b1-214">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a62b1-215">ProvisionFavorites</span><span class="sxs-lookup"><span data-stu-id="a62b1-215">ProvisionFavorites</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-provisionfavorites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a62b1-216">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a62b1-216">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a62b1-217">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="a62b1-217">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a62b1-218">SendIntranetTraffictoInternetExplorer</span><span class="sxs-lookup"><span data-stu-id="a62b1-218">SendIntranetTraffictoInternetExplorer</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-sendintranettraffictointernetexplorer)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a62b1-219">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="a62b1-219">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="a62b1-220">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="a62b1-220">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a62b1-221">SetDefaultSearchEngine</span><span class="sxs-lookup"><span data-stu-id="a62b1-221">SetDefaultSearchEngine</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-setdefaultsearchengine)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a62b1-222">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a62b1-222">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a62b1-223">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="a62b1-223">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a62b1-224">ShowMessageWhenOpeningSitesInInternetExplorer</span><span class="sxs-lookup"><span data-stu-id="a62b1-224">ShowMessageWhenOpeningSitesInInternetExplorer</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-showmessagewhenopeningsitesininternetexplorer)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a62b1-225">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="a62b1-225">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="a62b1-226">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="a62b1-226">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a62b1-227">SyncFavoritesBetweenIEAndMicrosoftEdge</span><span class="sxs-lookup"><span data-stu-id="a62b1-227">SyncFavoritesBetweenIEAndMicrosoftEdge</span></span>](/windows/client-management/mdm/policy-csp-browser#browser-syncfavoritesbetweenieandmicrosoftedge)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a62b1-228">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="a62b1-228">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="a62b1-229">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="a62b1-229">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a62b1-230">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a62b1-230">Requirements</span></span>



| <span data-ttu-id="a62b1-231">Requisito</span><span class="sxs-lookup"><span data-stu-id="a62b1-231">Requirement</span></span> | <span data-ttu-id="a62b1-232">Value</span><span class="sxs-lookup"><span data-stu-id="a62b1-232">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a62b1-233">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a62b1-233">Minimum supported client</span></span><br/> | <span data-ttu-id="a62b1-234">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="a62b1-234">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a62b1-235">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a62b1-235">Minimum supported server</span></span><br/> | <span data-ttu-id="a62b1-236">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="a62b1-236">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="a62b1-237">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="a62b1-237">Namespace</span></span><br/>                | <span data-ttu-id="a62b1-238">DMMap de MDM raíz de \\ CIMv2 \\ \\</span><span class="sxs-lookup"><span data-stu-id="a62b1-238">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="a62b1-239">MOF</span><span class="sxs-lookup"><span data-stu-id="a62b1-239">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a62b1-240"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a62b1-240"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="a62b1-241">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="a62b1-241">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a62b1-242"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a62b1-242"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a62b1-243">Vea también</span><span class="sxs-lookup"><span data-stu-id="a62b1-243">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a62b1-244">Usar scripting de PowerShell con el proveedor de puente WMI</span><span class="sxs-lookup"><span data-stu-id="a62b1-244">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

