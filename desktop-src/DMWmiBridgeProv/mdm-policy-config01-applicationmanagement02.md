---
title: MDM_Policy_Config01_ApplicationManagement02 (clase)
description: La \_ clase Config01 de ApplicationManagement02 de directivas MDM \_ \_ representa las directivas de administración de aplicaciones disponibles.
ms.assetid: f05c4852-e694-4e0d-94e1-07531c879613
keywords:
- MDM_Policy_Config01_ApplicationManagement02 (clase)
- MDM_Policy_Config01_ApplicationManagement02 clase, descrita
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_ApplicationManagement02
- MDM_Policy_Config01_ApplicationManagement02.InstanceID
- MDM_Policy_Config01_ApplicationManagement02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3588405fa60aeccb74ad4ca11eeb9cb658469d40
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105656504"
---
# <a name="mdm_policy_config01_applicationmanagement02-class"></a><span data-ttu-id="936ce-105">\_ \_ Clase ApplicationManagement02 de Config01 de directivas MDM \_</span><span class="sxs-lookup"><span data-stu-id="936ce-105">MDM\_Policy\_Config01\_ApplicationManagement02 class</span></span>

<span data-ttu-id="936ce-106">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="936ce-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="936ce-107">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="936ce-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="936ce-108">La **clase \_ \_ Config01 de \_ ApplicationManagement02 de directivas MDM** representa las directivas de administración de aplicaciones disponibles.</span><span class="sxs-lookup"><span data-stu-id="936ce-108">The **MDM\_Policy\_Config01\_ApplicationManagement02** class represents the application management policies available.</span></span>

<span data-ttu-id="936ce-109">La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="936ce-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="936ce-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="936ce-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_ApplicationManagement02
{
  string InstanceID;
  string ParentID;
  sint32 AllowAllTrustedApps;
  sint32 AllowAppStoreAutoUpdate;
  sint32 AllowDeveloperUnlock;
  sint32 AllowGameDVR;
  sint32 AllowSharedUserAppData;
  sint32 DisableStoreOriginatedApps;
  sint32 RestrictAppDataToSystemVolume;
  sint32 RestrictAppToSystemVolume;
};
```

## <a name="members"></a><span data-ttu-id="936ce-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="936ce-111">Members</span></span>

<span data-ttu-id="936ce-112">La clase Config01 de la **\_ Directiva MDM \_ \_ ApplicationManagement02** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="936ce-112">The **MDM\_Policy\_Config01\_ApplicationManagement02** class has these types of members:</span></span>

-   [<span data-ttu-id="936ce-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="936ce-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="936ce-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="936ce-114">Properties</span></span>

<span data-ttu-id="936ce-115">La **clase \_ \_ Config01 de \_ ApplicationManagement02 de directivas MDM** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="936ce-115">The **MDM\_Policy\_Config01\_ApplicationManagement02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="936ce-116">AllowAllTrustedApps</span><span class="sxs-lookup"><span data-stu-id="936ce-116">AllowAllTrustedApps</span></span>](/windows/client-management/mdm/policy-csp-applicationmanagement#applicationmanagement-allowalltrustedapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="936ce-117">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="936ce-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="936ce-118">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="936ce-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="936ce-119">AllowAppStoreAutoUpdate</span><span class="sxs-lookup"><span data-stu-id="936ce-119">AllowAppStoreAutoUpdate</span></span>](/windows/client-management/mdm/policy-csp-applicationmanagement#applicationmanagement-allowappstoreautoupdate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="936ce-120">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="936ce-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="936ce-121">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="936ce-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="936ce-122">AllowDeveloperUnlock</span><span class="sxs-lookup"><span data-stu-id="936ce-122">AllowDeveloperUnlock</span></span>](/windows/client-management/mdm/policy-csp-applicationmanagement#applicationmanagement-allowdeveloperunlock)
</dt> <dd> <dl> <dt>

<span data-ttu-id="936ce-123">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="936ce-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="936ce-124">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="936ce-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="936ce-125">AllowGameDVR</span><span class="sxs-lookup"><span data-stu-id="936ce-125">AllowGameDVR</span></span>](/windows/client-management/mdm/policy-csp-applicationmanagement#applicationmanagement-allowgamedvr)
</dt> <dd> <dl> <dt>

<span data-ttu-id="936ce-126">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="936ce-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="936ce-127">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="936ce-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="936ce-128">AllowSharedUserAppData</span><span class="sxs-lookup"><span data-stu-id="936ce-128">AllowSharedUserAppData</span></span>](/windows/client-management/mdm/policy-csp-applicationmanagement#applicationmanagement-allowshareduserappdata)
</dt> <dd> <dl> <dt>

<span data-ttu-id="936ce-129">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="936ce-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="936ce-130">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="936ce-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="936ce-131">DisableStoreOriginatedApps</span><span class="sxs-lookup"><span data-stu-id="936ce-131">DisableStoreOriginatedApps</span></span>](/windows/client-management/mdm/policy-csp-applicationmanagement#applicationmanagement-disablestoreoriginatedapps)
</dt> <dd> <dl> <dt>

<span data-ttu-id="936ce-132">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="936ce-132">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="936ce-133">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="936ce-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="936ce-134">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="936ce-134">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="936ce-135">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="936ce-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="936ce-136">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="936ce-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="936ce-137">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="936ce-137">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="936ce-138">Identifica el nombre del nodo primario.</span><span class="sxs-lookup"><span data-stu-id="936ce-138">Identifies the name of the parent node.</span></span> <span data-ttu-id="936ce-139">Para esta clase, la cadena es "ApplicationManagement".</span><span class="sxs-lookup"><span data-stu-id="936ce-139">For this class, the string is "ApplicationManagement".</span></span>

</dd> <dt>

<span data-ttu-id="936ce-140">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="936ce-140">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="936ce-141">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="936ce-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="936ce-142">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="936ce-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="936ce-143">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="936ce-143">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="936ce-144">Describe la ruta de acceso completa al nodo primario.</span><span class="sxs-lookup"><span data-stu-id="936ce-144">Describes the full path to the parent node.</span></span> <span data-ttu-id="936ce-145">Para esta clase, la cadena es "./Vendor/MSFT/Policy/Config".</span><span class="sxs-lookup"><span data-stu-id="936ce-145">For this class, the string is "./Vendor/MSFT/Policy/Config"</span></span>

</dd> <dt>

[<span data-ttu-id="936ce-146">RestrictAppDataToSystemVolume</span><span class="sxs-lookup"><span data-stu-id="936ce-146">RestrictAppDataToSystemVolume</span></span>](/windows/client-management/mdm/policy-csp-applicationmanagement#applicationmanagement-restrictappdatatosystemvolume)
</dt> <dd> <dl> <dt>

<span data-ttu-id="936ce-147">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="936ce-147">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="936ce-148">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="936ce-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="936ce-149">RestrictAppToSystemVolume</span><span class="sxs-lookup"><span data-stu-id="936ce-149">RestrictAppToSystemVolume</span></span>](/windows/client-management/mdm/policy-csp-applicationmanagement#applicationmanagement-restrictapptosystemvolume)
</dt> <dd> <dl> <dt>

<span data-ttu-id="936ce-150">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="936ce-150">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="936ce-151">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="936ce-151">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="936ce-152">Requisitos</span><span class="sxs-lookup"><span data-stu-id="936ce-152">Requirements</span></span>



| <span data-ttu-id="936ce-153">Requisito</span><span class="sxs-lookup"><span data-stu-id="936ce-153">Requirement</span></span> | <span data-ttu-id="936ce-154">Value</span><span class="sxs-lookup"><span data-stu-id="936ce-154">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="936ce-155">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="936ce-155">Minimum supported client</span></span><br/> | <span data-ttu-id="936ce-156">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="936ce-156">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="936ce-157">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="936ce-157">Minimum supported server</span></span><br/> | <span data-ttu-id="936ce-158">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="936ce-158">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="936ce-159">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="936ce-159">Namespace</span></span><br/>                | <span data-ttu-id="936ce-160">DMMap de MDM raíz de \\ CIMv2 \\ \\</span><span class="sxs-lookup"><span data-stu-id="936ce-160">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="936ce-161">MOF</span><span class="sxs-lookup"><span data-stu-id="936ce-161">MOF</span></span><br/>                      | <dl> <span data-ttu-id="936ce-162"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="936ce-162"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="936ce-163">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="936ce-163">DLL</span></span><br/>                      | <dl> <span data-ttu-id="936ce-164"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="936ce-164"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="936ce-165">Vea también</span><span class="sxs-lookup"><span data-stu-id="936ce-165">See also</span></span>

<dl> <dt>

[<span data-ttu-id="936ce-166">Usar scripting de PowerShell con el proveedor de puente WMI</span><span class="sxs-lookup"><span data-stu-id="936ce-166">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

