---
title: MDM_Policy_Config01_Search02 (clase)
description: La \_ clase Config01 de Search02 de directivas MDM \_ \_ representa las directivas de búsqueda disponibles.
ms.assetid: 0ae4876c-3584-4b22-be02-a499443f5df0
keywords:
- MDM_Policy_Config01_Search02 (clase)
- MDM_Policy_Config01_Search02 clase, descrita
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_Search02
- MDM_Policy_Config01_Search02.InstanceID
- MDM_Policy_Config01_Search02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18f3517cacf1fd9af6b37f64a0cbbc8294916cc7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490823"
---
# <a name="mdm_policy_config01_search02-class"></a><span data-ttu-id="fece7-105">\_ \_ Clase Search02 de Config01 de directivas MDM \_</span><span class="sxs-lookup"><span data-stu-id="fece7-105">MDM\_Policy\_Config01\_Search02 class</span></span>

<span data-ttu-id="fece7-106">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="fece7-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="fece7-107">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="fece7-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="fece7-108">La **clase \_ \_ Config01 de \_ Search02 de directivas MDM** representa las directivas de búsqueda disponibles.</span><span class="sxs-lookup"><span data-stu-id="fece7-108">The **MDM\_Policy\_Config01\_Search02** class represents the search policies available.</span></span>

<span data-ttu-id="fece7-109">La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="fece7-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="fece7-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fece7-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_Search02
{
  string InstanceID;
  string ParentID;
  sint32 AllowCloudSearch;
  sint32 AllowSearchToUseLocation;
  sint32 AllowStoringImagesFromVisionSearch;
  sint32 AlwaysUseAutoLangDetection;
  sint32 PreventRemoteQueries;
  sint32 PreventIndexingLowDiskSpaceMB;
  sint32 DisableRemovableDriveIndexing;
  sint32 DisableBackoff;
  sint32 AllowUsingDiacritics;
  sint32 AllowWindowsIndexer;
  sint32 AllowIndexingEncryptedStoresOrItems;
};
```

## <a name="members"></a><span data-ttu-id="fece7-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="fece7-111">Members</span></span>

<span data-ttu-id="fece7-112">La clase Config01 de la **\_ Directiva MDM \_ \_ Search02** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="fece7-112">The **MDM\_Policy\_Config01\_Search02** class has these types of members:</span></span>

-   [<span data-ttu-id="fece7-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="fece7-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="fece7-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="fece7-114">Properties</span></span>

<span data-ttu-id="fece7-115">La **clase \_ \_ Config01 de \_ Search02 de directivas MDM** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="fece7-115">The **MDM\_Policy\_Config01\_Search02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="fece7-116">AllowCloudSearch</span><span class="sxs-lookup"><span data-stu-id="fece7-116">AllowCloudSearch</span></span>](/windows/client-management/mdm/policy-csp-search#search-allowcloudsearch)
</dt> <dd> <dl> <dt>

<span data-ttu-id="fece7-117">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="fece7-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="fece7-118">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="fece7-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="fece7-119">AllowIndexingEncryptedStoresOrItems</span><span class="sxs-lookup"><span data-stu-id="fece7-119">AllowIndexingEncryptedStoresOrItems</span></span>](/windows/client-management/mdm/policy-csp-search#search-allowindexingencryptedstoresoritems)
</dt> <dd> <dl> <dt>

<span data-ttu-id="fece7-120">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="fece7-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="fece7-121">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="fece7-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="fece7-122">AllowSearchToUseLocation</span><span class="sxs-lookup"><span data-stu-id="fece7-122">AllowSearchToUseLocation</span></span>](/windows/client-management/mdm/policy-csp-search#search-allowsearchtouselocation)
</dt> <dd> <dl> <dt>

<span data-ttu-id="fece7-123">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="fece7-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="fece7-124">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="fece7-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="fece7-125">AllowStoringImagesFromVisionSearch</span><span class="sxs-lookup"><span data-stu-id="fece7-125">AllowStoringImagesFromVisionSearch</span></span>](/windows/client-management/mdm/policy-csp-search#search-allowstoringimagesfromvisionsearch)
</dt> <dd> <dl> <dt>

<span data-ttu-id="fece7-126">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="fece7-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="fece7-127">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="fece7-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="fece7-128">AllowUsingDiacritics</span><span class="sxs-lookup"><span data-stu-id="fece7-128">AllowUsingDiacritics</span></span>](/windows/client-management/mdm/policy-csp-search#search-allowusingdiacritics)
</dt> <dd> <dl> <dt>

<span data-ttu-id="fece7-129">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="fece7-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="fece7-130">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="fece7-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="fece7-131">AllowWindowsIndexer</span><span class="sxs-lookup"><span data-stu-id="fece7-131">AllowWindowsIndexer</span></span>](/windows/client-management/mdm/policy-csp-search#search-allowwindowsindexer)
</dt> <dd> <dl> <dt>

<span data-ttu-id="fece7-132">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="fece7-132">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="fece7-133">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="fece7-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="fece7-134">AlwaysUseAutoLangDetection</span><span class="sxs-lookup"><span data-stu-id="fece7-134">AlwaysUseAutoLangDetection</span></span>](/windows/client-management/mdm/policy-csp-search#search-alwaysuseautolangdetection)
</dt> <dd> <dl> <dt>

<span data-ttu-id="fece7-135">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="fece7-135">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="fece7-136">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="fece7-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="fece7-137">DisableBackoff</span><span class="sxs-lookup"><span data-stu-id="fece7-137">DisableBackoff</span></span>](/windows/client-management/mdm/policy-csp-search#search-disablebackoff)
</dt> <dd> <dl> <dt>

<span data-ttu-id="fece7-138">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="fece7-138">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="fece7-139">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="fece7-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="fece7-140">DisableRemovableDriveIndexing</span><span class="sxs-lookup"><span data-stu-id="fece7-140">DisableRemovableDriveIndexing</span></span>](/windows/client-management/mdm/policy-csp-search#search-disableremovabledriveindexing)
</dt> <dd> <dl> <dt>

<span data-ttu-id="fece7-141">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="fece7-141">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="fece7-142">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="fece7-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="fece7-143">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="fece7-143">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fece7-144">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="fece7-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fece7-145">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="fece7-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fece7-146">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="fece7-146">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="fece7-147">Identifica el nombre del nodo primario.</span><span class="sxs-lookup"><span data-stu-id="fece7-147">Identifies the name of the parent node.</span></span> <span data-ttu-id="fece7-148">Para esta clase, la cadena es "Search".</span><span class="sxs-lookup"><span data-stu-id="fece7-148">For this class, the string is "Search".</span></span>

</dd> <dt>

<span data-ttu-id="fece7-149">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="fece7-149">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fece7-150">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="fece7-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fece7-151">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="fece7-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fece7-152">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="fece7-152">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="fece7-153">Describe la ruta de acceso completa al nodo primario.</span><span class="sxs-lookup"><span data-stu-id="fece7-153">Describes the full path to the parent node.</span></span> <span data-ttu-id="fece7-154">Para esta clase, la cadena es "./Vendor/MSFT/Policy/Config".</span><span class="sxs-lookup"><span data-stu-id="fece7-154">For this class, the string is "./Vendor/MSFT/Policy/Config"</span></span>

</dd> <dt>

[<span data-ttu-id="fece7-155">PreventIndexingLowDiskSpaceMB</span><span class="sxs-lookup"><span data-stu-id="fece7-155">PreventIndexingLowDiskSpaceMB</span></span>](/windows/client-management/mdm/policy-csp-search#search-preventindexinglowdiskspacemb)
</dt> <dd> <dl> <dt>

<span data-ttu-id="fece7-156">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="fece7-156">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="fece7-157">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="fece7-157">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="fece7-158">PreventRemoteQueries</span><span class="sxs-lookup"><span data-stu-id="fece7-158">PreventRemoteQueries</span></span>](/windows/client-management/mdm/policy-csp-search#search-preventremotequeries)
</dt> <dd> <dl> <dt>

<span data-ttu-id="fece7-159">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="fece7-159">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="fece7-160">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="fece7-160">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fece7-161">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fece7-161">Requirements</span></span>



| <span data-ttu-id="fece7-162">Requisito</span><span class="sxs-lookup"><span data-stu-id="fece7-162">Requirement</span></span> | <span data-ttu-id="fece7-163">Value</span><span class="sxs-lookup"><span data-stu-id="fece7-163">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fece7-164">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fece7-164">Minimum supported client</span></span><br/> | <span data-ttu-id="fece7-165">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="fece7-165">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="fece7-166">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fece7-166">Minimum supported server</span></span><br/> | <span data-ttu-id="fece7-167">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="fece7-167">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="fece7-168">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="fece7-168">Namespace</span></span><br/>                | <span data-ttu-id="fece7-169">DMMap de MDM raíz de \\ CIMv2 \\ \\</span><span class="sxs-lookup"><span data-stu-id="fece7-169">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="fece7-170">MOF</span><span class="sxs-lookup"><span data-stu-id="fece7-170">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fece7-171"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fece7-171"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="fece7-172">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="fece7-172">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fece7-173"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fece7-173"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fece7-174">Vea también</span><span class="sxs-lookup"><span data-stu-id="fece7-174">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fece7-175">Usar scripting de PowerShell con el proveedor de puente WMI</span><span class="sxs-lookup"><span data-stu-id="fece7-175">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

