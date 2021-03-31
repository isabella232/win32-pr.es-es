---
title: MDM_Policy_Config01_Start02 (clase)
description: La \_ clase MDM Policy \_ Config01 \_ Start02 representa las directivas de pantalla de inicio disponibles.
ms.assetid: 2aef29c8-164a-4111-9c1a-e63eeec2531e
keywords:
- MDM_Policy_Config01_Start02 (clase)
- MDM_Policy_Config01_Start02 clase, descrita
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_Start02
- MDM_Policy_Config01_Start02.InstanceID
- MDM_Policy_Config01_Start02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9095fcf1611ef106fed5ad93f059e165ebcac15
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490822"
---
# <a name="mdm_policy_config01_start02-class"></a><span data-ttu-id="dd532-105">\_ \_ Clase Start02 de Config01 de directivas MDM \_</span><span class="sxs-lookup"><span data-stu-id="dd532-105">MDM\_Policy\_Config01\_Start02 class</span></span>

<span data-ttu-id="dd532-106">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="dd532-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="dd532-107">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="dd532-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="dd532-108">La clase **MDM \_ Policy \_ Config01 \_ Start02** representa las directivas de pantalla de inicio disponibles.</span><span class="sxs-lookup"><span data-stu-id="dd532-108">The **MDM\_Policy\_Config01\_Start02** class represents the start screen policies available.</span></span>

<span data-ttu-id="dd532-109">La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="dd532-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="dd532-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="dd532-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_Start02
{
  string InstanceID;
  string ParentID;
  sint32 AllowPinnedFolderVideos;
  sint32 AllowPinnedFolderSettings;
  sint32 AllowPinnedFolderPictures;
  sint32 AllowPinnedFolderPersonalFolder;
  sint32 AllowPinnedFolderNetwork;
  sint32 AllowPinnedFolderMusic;
  sint32 AllowPinnedFolderHomeGroup;
  sint32 AllowPinnedFolderFileExplorer;
  sint32 AllowPinnedFolderDownloads;
  sint32 AllowPinnedFolderDocuments;
  sint32 ForceStartSize;
  string StartLayout;
  sint32 NoPinningToTaskbar;
  string ImportEdgeAssets;
  sint32 HideUserTile;
  sint32 HideSwitchAccount;
  sint32 HideSleep;
  sint32 HideSignOut;
  sint32 HideShutDown;
  sint32 HideRestart;
  sint32 HideRecentlyAddedApps;
  sint32 HideRecentJumplists;
  sint32 HidePowerButton;
  sint32 HideLock;
  sint32 HideHibernate;
  sint32 HideFrequentlyUsedApps;
  sint32 HideChangeAccountSettings;
  sint32 HideAppList;
};
```

## <a name="members"></a><span data-ttu-id="dd532-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="dd532-111">Members</span></span>

<span data-ttu-id="dd532-112">La clase Config01 de la **\_ Directiva MDM \_ \_ Start02** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="dd532-112">The **MDM\_Policy\_Config01\_Start02** class has these types of members:</span></span>

-   [<span data-ttu-id="dd532-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="dd532-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="dd532-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="dd532-114">Properties</span></span>

<span data-ttu-id="dd532-115">La **clase \_ \_ Config01 de \_ Start02 de directivas MDM** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="dd532-115">The **MDM\_Policy\_Config01\_Start02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="dd532-116">AllowPinnedFolderDocuments</span><span class="sxs-lookup"><span data-stu-id="dd532-116">AllowPinnedFolderDocuments</span></span>](/windows/client-management/mdm/policy-csp-start#start-allowpinnedfolderdocuments)
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd532-117">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="dd532-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="dd532-118">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="dd532-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="dd532-119">AllowPinnedFolderDownloads</span><span class="sxs-lookup"><span data-stu-id="dd532-119">AllowPinnedFolderDownloads</span></span>](/windows/client-management/mdm/policy-csp-start#start-allowpinnedfolderdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd532-120">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="dd532-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="dd532-121">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="dd532-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="dd532-122">AllowPinnedFolderFileExplorer</span><span class="sxs-lookup"><span data-stu-id="dd532-122">AllowPinnedFolderFileExplorer</span></span>](/windows/client-management/mdm/policy-csp-start#start-allowpinnedfolderfileexplorer)
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd532-123">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="dd532-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="dd532-124">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="dd532-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="dd532-125">AllowPinnedFolderHomeGroup</span><span class="sxs-lookup"><span data-stu-id="dd532-125">AllowPinnedFolderHomeGroup</span></span>](/windows/client-management/mdm/policy-csp-start#start-allowpinnedfolderhomegroup)
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd532-126">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="dd532-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="dd532-127">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="dd532-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="dd532-128">AllowPinnedFolderMusic</span><span class="sxs-lookup"><span data-stu-id="dd532-128">AllowPinnedFolderMusic</span></span>](/windows/client-management/mdm/policy-csp-start#start-allowpinnedfoldermusic)
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd532-129">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="dd532-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="dd532-130">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="dd532-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="dd532-131">AllowPinnedFolderNetwork</span><span class="sxs-lookup"><span data-stu-id="dd532-131">AllowPinnedFolderNetwork</span></span>](/windows/client-management/mdm/policy-csp-start#start-allowpinnedfoldernetwork)
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd532-132">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="dd532-132">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="dd532-133">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="dd532-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="dd532-134">AllowPinnedFolderPersonalFolder</span><span class="sxs-lookup"><span data-stu-id="dd532-134">AllowPinnedFolderPersonalFolder</span></span>](/windows/client-management/mdm/policy-csp-start#start-allowpinnedfolderpersonalfolder)
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd532-135">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="dd532-135">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="dd532-136">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="dd532-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="dd532-137">AllowPinnedFolderPictures</span><span class="sxs-lookup"><span data-stu-id="dd532-137">AllowPinnedFolderPictures</span></span>](/windows/client-management/mdm/policy-csp-start#start-allowpinnedfolderpictures)
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd532-138">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="dd532-138">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="dd532-139">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="dd532-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="dd532-140">AllowPinnedFolderSettings</span><span class="sxs-lookup"><span data-stu-id="dd532-140">AllowPinnedFolderSettings</span></span>](/windows/client-management/mdm/policy-csp-start#start-allowpinnedfoldersettings)
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd532-141">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="dd532-141">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="dd532-142">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="dd532-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="dd532-143">AllowPinnedFolderVideos</span><span class="sxs-lookup"><span data-stu-id="dd532-143">AllowPinnedFolderVideos</span></span>](/windows/client-management/mdm/policy-csp-start#start-allowpinnedfoldervideos)
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd532-144">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="dd532-144">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="dd532-145">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="dd532-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="dd532-146">ForceStartSize</span><span class="sxs-lookup"><span data-stu-id="dd532-146">ForceStartSize</span></span>](/windows/client-management/mdm/policy-csp-start#start-forcestartsize)
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd532-147">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="dd532-147">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="dd532-148">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="dd532-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="dd532-149">HideAppList</span><span class="sxs-lookup"><span data-stu-id="dd532-149">HideAppList</span></span>](/windows/client-management/mdm/policy-csp-start#start-hideapplist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd532-150">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="dd532-150">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="dd532-151">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="dd532-151">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="dd532-152">HideChangeAccountSettings</span><span class="sxs-lookup"><span data-stu-id="dd532-152">HideChangeAccountSettings</span></span>](/windows/client-management/mdm/policy-csp-start#start-hidechangeaccountsettings)
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd532-153">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="dd532-153">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="dd532-154">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="dd532-154">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="dd532-155">HideFrequentlyUsedApps</span><span class="sxs-lookup"><span data-stu-id="dd532-155">HideFrequentlyUsedApps</span></span>](/windows/client-management/mdm/policy-csp-start#start-hidefrequentlyusedapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd532-156">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="dd532-156">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="dd532-157">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="dd532-157">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="dd532-158">HideHibernate</span><span class="sxs-lookup"><span data-stu-id="dd532-158">HideHibernate</span></span>](/windows/client-management/mdm/policy-csp-start#start-hidehibernate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd532-159">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="dd532-159">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="dd532-160">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="dd532-160">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="dd532-161">HideLock</span><span class="sxs-lookup"><span data-stu-id="dd532-161">HideLock</span></span>](/windows/client-management/mdm/policy-csp-start#start-hidelock)
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd532-162">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="dd532-162">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="dd532-163">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="dd532-163">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="dd532-164">HidePowerButton</span><span class="sxs-lookup"><span data-stu-id="dd532-164">HidePowerButton</span></span>](/windows/client-management/mdm/policy-csp-start#start-hidepowerbutton)
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd532-165">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="dd532-165">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="dd532-166">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="dd532-166">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="dd532-167">HideRecentJumplists</span><span class="sxs-lookup"><span data-stu-id="dd532-167">HideRecentJumplists</span></span>](/windows/client-management/mdm/policy-csp-start#start-hiderecentjumplists)
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd532-168">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="dd532-168">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="dd532-169">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="dd532-169">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="dd532-170">HideRecentlyAddedApps</span><span class="sxs-lookup"><span data-stu-id="dd532-170">HideRecentlyAddedApps</span></span>](/windows/client-management/mdm/policy-csp-start#start-hiderecentlyaddedapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd532-171">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="dd532-171">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="dd532-172">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="dd532-172">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="dd532-173">HideRestart</span><span class="sxs-lookup"><span data-stu-id="dd532-173">HideRestart</span></span>](/windows/client-management/mdm/policy-csp-start#start-hiderestart)
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd532-174">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="dd532-174">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="dd532-175">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="dd532-175">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="dd532-176">HideShutDown</span><span class="sxs-lookup"><span data-stu-id="dd532-176">HideShutDown</span></span>](/windows/client-management/mdm/policy-csp-start#start-hideshutdown)
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd532-177">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="dd532-177">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="dd532-178">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="dd532-178">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="dd532-179">HideSignOut</span><span class="sxs-lookup"><span data-stu-id="dd532-179">HideSignOut</span></span>](/windows/client-management/mdm/policy-csp-start#start-hidesignout)
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd532-180">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="dd532-180">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="dd532-181">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="dd532-181">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="dd532-182">HideSleep</span><span class="sxs-lookup"><span data-stu-id="dd532-182">HideSleep</span></span>](/windows/client-management/mdm/policy-csp-start#start-hidesleep)
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd532-183">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="dd532-183">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="dd532-184">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="dd532-184">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="dd532-185">HideSwitchAccount</span><span class="sxs-lookup"><span data-stu-id="dd532-185">HideSwitchAccount</span></span>](/windows/client-management/mdm/policy-csp-start#start-hideswitchaccount)
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd532-186">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="dd532-186">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="dd532-187">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="dd532-187">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="dd532-188">HideUserTile</span><span class="sxs-lookup"><span data-stu-id="dd532-188">HideUserTile</span></span>](/windows/client-management/mdm/policy-csp-start#start-hideusertile)
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd532-189">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="dd532-189">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="dd532-190">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="dd532-190">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="dd532-191">ImportEdgeAssets</span><span class="sxs-lookup"><span data-stu-id="dd532-191">ImportEdgeAssets</span></span>](/windows/client-management/mdm/policy-csp-start#start-importedgeassets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd532-192">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="dd532-192">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dd532-193">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="dd532-193">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="dd532-194">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="dd532-194">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd532-195">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="dd532-195">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dd532-196">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="dd532-196">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dd532-197">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="dd532-197">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="dd532-198">Identifica el nombre del nodo primario.</span><span class="sxs-lookup"><span data-stu-id="dd532-198">Identifies the name of the parent node.</span></span> <span data-ttu-id="dd532-199">Para esta clase, la cadena es "Start".</span><span class="sxs-lookup"><span data-stu-id="dd532-199">For this class, the string is "Start"</span></span>

</dd> <dt>

[<span data-ttu-id="dd532-200">NoPinningToTaskbar</span><span class="sxs-lookup"><span data-stu-id="dd532-200">NoPinningToTaskbar</span></span>](/windows/client-management/mdm/policy-csp-start#start-nopinningtotaskbar)
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd532-201">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="dd532-201">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="dd532-202">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="dd532-202">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="dd532-203">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="dd532-203">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd532-204">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="dd532-204">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dd532-205">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="dd532-205">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dd532-206">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="dd532-206">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="dd532-207">Describe la ruta de acceso completa al nodo primario.</span><span class="sxs-lookup"><span data-stu-id="dd532-207">Describes the full path to the parent node.</span></span> <span data-ttu-id="dd532-208">Para esta clase, la cadena es "./Vendor/MSFT/Policy/Config".</span><span class="sxs-lookup"><span data-stu-id="dd532-208">For this class, the string is "./Vendor/MSFT/Policy/Config"</span></span>

</dd> <dt>

[<span data-ttu-id="dd532-209">StartLayout</span><span class="sxs-lookup"><span data-stu-id="dd532-209">StartLayout</span></span>](/windows/client-management/mdm/policy-csp-start#start-startlayout)
</dt> <dd> <dl> <dt>

<span data-ttu-id="dd532-210">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="dd532-210">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dd532-211">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="dd532-211">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="dd532-212">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dd532-212">Requirements</span></span>



| <span data-ttu-id="dd532-213">Requisito</span><span class="sxs-lookup"><span data-stu-id="dd532-213">Requirement</span></span> | <span data-ttu-id="dd532-214">Value</span><span class="sxs-lookup"><span data-stu-id="dd532-214">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dd532-215">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dd532-215">Minimum supported client</span></span><br/> | <span data-ttu-id="dd532-216">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="dd532-216">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="dd532-217">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dd532-217">Minimum supported server</span></span><br/> | <span data-ttu-id="dd532-218">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="dd532-218">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="dd532-219">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="dd532-219">Namespace</span></span><br/>                | <span data-ttu-id="dd532-220">DMMap de MDM raíz de \\ CIMv2 \\ \\</span><span class="sxs-lookup"><span data-stu-id="dd532-220">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="dd532-221">MOF</span><span class="sxs-lookup"><span data-stu-id="dd532-221">MOF</span></span><br/>                      | <dl> <span data-ttu-id="dd532-222"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="dd532-222"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="dd532-223">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="dd532-223">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dd532-224"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dd532-224"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dd532-225">Vea también</span><span class="sxs-lookup"><span data-stu-id="dd532-225">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dd532-226">Usar scripting de PowerShell con el proveedor de puente WMI</span><span class="sxs-lookup"><span data-stu-id="dd532-226">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

