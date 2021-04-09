---
title: MDM_Policy_Result01_Start02 (clase)
description: La \_ clase MDM Policy \_ Result01 \_ Start02 representa las directivas de pantalla de inicio disponibles.
ms.assetid: 997d64f9-b2be-47b8-8a84-97438e7fa842
keywords:
- MDM_Policy_Result01_Start02 (clase)
- MDM_Policy_Result01_Start02 clase, descrita
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_Start02
- MDM_Policy_Result01_Start02.InstanceID
- MDM_Policy_Result01_Start02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 412e9ccecdc9f691b03a94ba5528eb6b7e3d7315
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079252"
---
# <a name="mdm_policy_result01_start02-class"></a><span data-ttu-id="3a11d-105">\_ \_ Clase Start02 de Result01 de directivas MDM \_</span><span class="sxs-lookup"><span data-stu-id="3a11d-105">MDM\_Policy\_Result01\_Start02 class</span></span>

<span data-ttu-id="3a11d-106">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="3a11d-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="3a11d-107">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="3a11d-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="3a11d-108">La clase **MDM \_ Policy \_ Result01 \_ Start02** representa las directivas de pantalla de inicio disponibles.</span><span class="sxs-lookup"><span data-stu-id="3a11d-108">The **MDM\_Policy\_Result01\_Start02** class represents the start screen policies available.</span></span>

<span data-ttu-id="3a11d-109">La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="3a11d-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="3a11d-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3a11d-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_Start02
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

## <a name="members"></a><span data-ttu-id="3a11d-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="3a11d-111">Members</span></span>

<span data-ttu-id="3a11d-112">La clase Result01 de la **\_ Directiva MDM \_ \_ Start02** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="3a11d-112">The **MDM\_Policy\_Result01\_Start02** class has these types of members:</span></span>

-   [<span data-ttu-id="3a11d-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="3a11d-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3a11d-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="3a11d-114">Properties</span></span>

<span data-ttu-id="3a11d-115">La **clase \_ \_ Result01 de \_ Start02 de directivas MDM** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="3a11d-115">The **MDM\_Policy\_Result01\_Start02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="3a11d-116">AllowPinnedFolderDocuments</span><span class="sxs-lookup"><span data-stu-id="3a11d-116">AllowPinnedFolderDocuments</span></span>](/windows/client-management/mdm/policy-csp-start#start-allowpinnedfolderdocuments)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a11d-117">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="3a11d-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="3a11d-118">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="3a11d-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="3a11d-119">AllowPinnedFolderDownloads</span><span class="sxs-lookup"><span data-stu-id="3a11d-119">AllowPinnedFolderDownloads</span></span>](/windows/client-management/mdm/policy-csp-start#start-allowpinnedfolderdownloads)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a11d-120">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="3a11d-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="3a11d-121">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="3a11d-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="3a11d-122">AllowPinnedFolderFileExplorer</span><span class="sxs-lookup"><span data-stu-id="3a11d-122">AllowPinnedFolderFileExplorer</span></span>](/windows/client-management/mdm/policy-csp-start#start-allowpinnedfolderfileexplorer)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a11d-123">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="3a11d-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="3a11d-124">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="3a11d-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="3a11d-125">AllowPinnedFolderHomeGroup</span><span class="sxs-lookup"><span data-stu-id="3a11d-125">AllowPinnedFolderHomeGroup</span></span>](/windows/client-management/mdm/policy-csp-start#start-allowpinnedfolderhomegroup)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a11d-126">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="3a11d-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="3a11d-127">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="3a11d-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="3a11d-128">AllowPinnedFolderMusic</span><span class="sxs-lookup"><span data-stu-id="3a11d-128">AllowPinnedFolderMusic</span></span>](/windows/client-management/mdm/policy-csp-start#start-allowpinnedfoldermusic)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a11d-129">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="3a11d-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="3a11d-130">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="3a11d-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="3a11d-131">AllowPinnedFolderNetwork</span><span class="sxs-lookup"><span data-stu-id="3a11d-131">AllowPinnedFolderNetwork</span></span>](/windows/client-management/mdm/policy-csp-start#start-allowpinnedfoldernetwork)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a11d-132">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="3a11d-132">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="3a11d-133">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="3a11d-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="3a11d-134">AllowPinnedFolderPersonalFolder</span><span class="sxs-lookup"><span data-stu-id="3a11d-134">AllowPinnedFolderPersonalFolder</span></span>](/windows/client-management/mdm/policy-csp-start#start-allowpinnedfolderpersonalfolder)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a11d-135">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="3a11d-135">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="3a11d-136">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="3a11d-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="3a11d-137">AllowPinnedFolderPictures</span><span class="sxs-lookup"><span data-stu-id="3a11d-137">AllowPinnedFolderPictures</span></span>](/windows/client-management/mdm/policy-csp-start#start-allowpinnedfolderpictures)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a11d-138">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="3a11d-138">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="3a11d-139">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="3a11d-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="3a11d-140">AllowPinnedFolderSettings</span><span class="sxs-lookup"><span data-stu-id="3a11d-140">AllowPinnedFolderSettings</span></span>](/windows/client-management/mdm/policy-csp-start#start-allowpinnedfoldersettings)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a11d-141">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="3a11d-141">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="3a11d-142">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="3a11d-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="3a11d-143">AllowPinnedFolderVideos</span><span class="sxs-lookup"><span data-stu-id="3a11d-143">AllowPinnedFolderVideos</span></span>](/windows/client-management/mdm/policy-csp-start#start-allowpinnedfoldervideos)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a11d-144">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="3a11d-144">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="3a11d-145">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="3a11d-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="3a11d-146">ForceStartSize</span><span class="sxs-lookup"><span data-stu-id="3a11d-146">ForceStartSize</span></span>](/windows/client-management/mdm/policy-csp-start#start-forcestartsize)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a11d-147">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="3a11d-147">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="3a11d-148">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="3a11d-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="3a11d-149">HideAppList</span><span class="sxs-lookup"><span data-stu-id="3a11d-149">HideAppList</span></span>](/windows/client-management/mdm/policy-csp-start#start-hideapplist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a11d-150">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="3a11d-150">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="3a11d-151">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="3a11d-151">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="3a11d-152">HideChangeAccountSettings</span><span class="sxs-lookup"><span data-stu-id="3a11d-152">HideChangeAccountSettings</span></span>](/windows/client-management/mdm/policy-csp-start#start-hidechangeaccountsettings)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a11d-153">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="3a11d-153">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="3a11d-154">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="3a11d-154">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="3a11d-155">HideFrequentlyUsedApps</span><span class="sxs-lookup"><span data-stu-id="3a11d-155">HideFrequentlyUsedApps</span></span>](/windows/client-management/mdm/policy-csp-start#start-hidefrequentlyusedapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a11d-156">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="3a11d-156">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="3a11d-157">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="3a11d-157">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="3a11d-158">HideHibernate</span><span class="sxs-lookup"><span data-stu-id="3a11d-158">HideHibernate</span></span>](/windows/client-management/mdm/policy-csp-start#start-hidehibernate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a11d-159">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="3a11d-159">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="3a11d-160">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="3a11d-160">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="3a11d-161">HideLock</span><span class="sxs-lookup"><span data-stu-id="3a11d-161">HideLock</span></span>](/windows/client-management/mdm/policy-csp-start#start-hidelock)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a11d-162">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="3a11d-162">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="3a11d-163">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="3a11d-163">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="3a11d-164">HidePowerButton</span><span class="sxs-lookup"><span data-stu-id="3a11d-164">HidePowerButton</span></span>](/windows/client-management/mdm/policy-csp-start#start-hidepowerbutton)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a11d-165">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="3a11d-165">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="3a11d-166">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="3a11d-166">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="3a11d-167">HideRecentJumplists</span><span class="sxs-lookup"><span data-stu-id="3a11d-167">HideRecentJumplists</span></span>](/windows/client-management/mdm/policy-csp-start#start-hiderecentjumplists)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a11d-168">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="3a11d-168">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="3a11d-169">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="3a11d-169">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="3a11d-170">HideRecentlyAddedApps</span><span class="sxs-lookup"><span data-stu-id="3a11d-170">HideRecentlyAddedApps</span></span>](/windows/client-management/mdm/policy-csp-start#start-hiderecentlyaddedapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a11d-171">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="3a11d-171">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="3a11d-172">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="3a11d-172">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="3a11d-173">HideRestart</span><span class="sxs-lookup"><span data-stu-id="3a11d-173">HideRestart</span></span>](/windows/client-management/mdm/policy-csp-start#start-hiderestart)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a11d-174">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="3a11d-174">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="3a11d-175">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="3a11d-175">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="3a11d-176">HideShutDown</span><span class="sxs-lookup"><span data-stu-id="3a11d-176">HideShutDown</span></span>](/windows/client-management/mdm/policy-csp-start#start-hideshutdown)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a11d-177">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="3a11d-177">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="3a11d-178">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="3a11d-178">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="3a11d-179">HideSignOut</span><span class="sxs-lookup"><span data-stu-id="3a11d-179">HideSignOut</span></span>](/windows/client-management/mdm/policy-csp-start#start-hidesignout)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a11d-180">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="3a11d-180">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="3a11d-181">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="3a11d-181">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="3a11d-182">HideSleep</span><span class="sxs-lookup"><span data-stu-id="3a11d-182">HideSleep</span></span>](/windows/client-management/mdm/policy-csp-start#start-hidesleep)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a11d-183">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="3a11d-183">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="3a11d-184">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="3a11d-184">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="3a11d-185">HideSwitchAccount</span><span class="sxs-lookup"><span data-stu-id="3a11d-185">HideSwitchAccount</span></span>](/windows/client-management/mdm/policy-csp-start#start-hideswitchaccount)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a11d-186">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="3a11d-186">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="3a11d-187">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="3a11d-187">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="3a11d-188">HideUserTile</span><span class="sxs-lookup"><span data-stu-id="3a11d-188">HideUserTile</span></span>](/windows/client-management/mdm/policy-csp-start#start-hideusertile)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a11d-189">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="3a11d-189">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="3a11d-190">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="3a11d-190">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="3a11d-191">ImportEdgeAssets</span><span class="sxs-lookup"><span data-stu-id="3a11d-191">ImportEdgeAssets</span></span>](/windows/client-management/mdm/policy-csp-start#start-importedgeassets)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a11d-192">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="3a11d-192">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3a11d-193">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="3a11d-193">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="3a11d-194">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="3a11d-194">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a11d-195">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="3a11d-195">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3a11d-196">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3a11d-196">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3a11d-197">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="3a11d-197">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="3a11d-198">Identifica el nombre del nodo primario.</span><span class="sxs-lookup"><span data-stu-id="3a11d-198">Identifies the name of the parent node.</span></span> <span data-ttu-id="3a11d-199">Para esta clase, la cadena es "Start".</span><span class="sxs-lookup"><span data-stu-id="3a11d-199">For this class, the string is "Start"</span></span>

</dd> <dt>

[<span data-ttu-id="3a11d-200">NoPinningToTaskbar</span><span class="sxs-lookup"><span data-stu-id="3a11d-200">NoPinningToTaskbar</span></span>](/windows/client-management/mdm/policy-csp-start#start-nopinningtotaskbar)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a11d-201">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="3a11d-201">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="3a11d-202">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="3a11d-202">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="3a11d-203">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="3a11d-203">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a11d-204">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="3a11d-204">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3a11d-205">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3a11d-205">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3a11d-206">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="3a11d-206">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="3a11d-207">Describe la ruta de acceso completa al nodo primario.</span><span class="sxs-lookup"><span data-stu-id="3a11d-207">Describes the full path to the parent node.</span></span> <span data-ttu-id="3a11d-208">Para esta clase, la cadena es "./Vendor/MSFT/Policy/Result".</span><span class="sxs-lookup"><span data-stu-id="3a11d-208">For this class, the string is "./Vendor/MSFT/Policy/Result"</span></span>

</dd> <dt>

[<span data-ttu-id="3a11d-209">StartLayout</span><span class="sxs-lookup"><span data-stu-id="3a11d-209">StartLayout</span></span>](/windows/client-management/mdm/policy-csp-start#start-startlayout)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a11d-210">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="3a11d-210">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3a11d-211">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="3a11d-211">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3a11d-212">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3a11d-212">Requirements</span></span>



| <span data-ttu-id="3a11d-213">Requisito</span><span class="sxs-lookup"><span data-stu-id="3a11d-213">Requirement</span></span> | <span data-ttu-id="3a11d-214">Value</span><span class="sxs-lookup"><span data-stu-id="3a11d-214">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3a11d-215">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3a11d-215">Minimum supported client</span></span><br/> | <span data-ttu-id="3a11d-216">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="3a11d-216">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="3a11d-217">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3a11d-217">Minimum supported server</span></span><br/> | <span data-ttu-id="3a11d-218">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="3a11d-218">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="3a11d-219">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="3a11d-219">Namespace</span></span><br/>                | <span data-ttu-id="3a11d-220">DMMap de MDM raíz de \\ CIMv2 \\ \\</span><span class="sxs-lookup"><span data-stu-id="3a11d-220">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="3a11d-221">MOF</span><span class="sxs-lookup"><span data-stu-id="3a11d-221">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3a11d-222"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3a11d-222"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="3a11d-223">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="3a11d-223">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3a11d-224"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3a11d-224"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3a11d-225">Vea también</span><span class="sxs-lookup"><span data-stu-id="3a11d-225">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a11d-226">Usar scripting de PowerShell con el proveedor de puente WMI</span><span class="sxs-lookup"><span data-stu-id="3a11d-226">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

