---
title: MDM_Policy_Result01_WindowsDefenderSecurityCenter02 (clase)
description: La \_ clase Result01 de WindowsDefenderSecurityCenter02 de directivas MDM \_ \_ representa las directivas de Security Center de Windows Defender.
ms.assetid: 59047e16-a188-4ec9-9d1b-db2b15c1109b
keywords:
- MDM_Policy_Result01_WindowsDefenderSecurityCenter02 (clase)
- MDM_Policy_Result01_WindowsDefenderSecurityCenter02 clase, descrita
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_WindowsDefenderSecurityCenter02
- MDM_Policy_Result01_WindowsDefenderSecurityCenter02.InstanceID
- MDM_Policy_Result01_WindowsDefenderSecurityCenter02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff7739410347169637ca5f27fef5627e26f8347c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489203"
---
# <a name="mdm_policy_result01_windowsdefendersecuritycenter02-class"></a><span data-ttu-id="3e548-105">\_ \_ Clase WindowsDefenderSecurityCenter02 de Result01 de directivas MDM \_</span><span class="sxs-lookup"><span data-stu-id="3e548-105">MDM\_Policy\_Result01\_WindowsDefenderSecurityCenter02 class</span></span>

<span data-ttu-id="3e548-106">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="3e548-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="3e548-107">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="3e548-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="3e548-108">La \_ clase Result01 de WindowsDefenderSecurityCenter02 de directivas MDM \_ \_ representa las directivas de Security Center de Windows Defender.</span><span class="sxs-lookup"><span data-stu-id="3e548-108">The MDM\_Policy\_Result01\_WindowsDefenderSecurityCenter02 class represents the Windows Defender Security Center policies.</span></span>

<span data-ttu-id="3e548-109">La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="3e548-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="3e548-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3e548-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_WindowsDefenderSecurityCenter02
{
  string InstanceID;
  string ParentID;
  string CompanyName;
  sint32 DisableAppBrowserUI;
  sint32 DisableEnhancedNotifications;
  sint32 DisableFamilyUI;
  sint32 DisableHealthUI;
  sint32 DisableNetworkUI;
  sint32 DisableNotifications;
  sint32 DisableVirusUI;
  sint32 DisallowExploitProtectionOverride;
  string Email;
  sint32 EnableCustomizedToasts;
  sint32 EnableInAppCustomization;
  string Phone;
  string URL;
};
```

## <a name="members"></a><span data-ttu-id="3e548-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="3e548-111">Members</span></span>

<span data-ttu-id="3e548-112">La clase Result01 de la **\_ Directiva MDM \_ \_ WindowsDefenderSecurityCenter02** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="3e548-112">The **MDM\_Policy\_Result01\_WindowsDefenderSecurityCenter02** class has these types of members:</span></span>

-   [<span data-ttu-id="3e548-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="3e548-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3e548-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="3e548-114">Properties</span></span>

<span data-ttu-id="3e548-115">La **clase \_ \_ Result01 de \_ WindowsDefenderSecurityCenter02 de directivas MDM** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="3e548-115">The **MDM\_Policy\_Result01\_WindowsDefenderSecurityCenter02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="3e548-116">Compañía</span><span class="sxs-lookup"><span data-stu-id="3e548-116">CompanyName</span></span>](/windows/client-management/mdm/policy-csp-windowsdefendersecuritycenter#windowsdefendersecuritycenter-companyname)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e548-117">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="3e548-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3e548-118">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="3e548-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="3e548-119">DisableAppBrowserUI</span><span class="sxs-lookup"><span data-stu-id="3e548-119">DisableAppBrowserUI</span></span>](/windows/client-management/mdm/policy-csp-windowsdefendersecuritycenter#windowsdefendersecuritycenter-disableappbrowserui)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e548-120">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="3e548-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="3e548-121">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="3e548-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="3e548-122">DisableEnhancedNotifications</span><span class="sxs-lookup"><span data-stu-id="3e548-122">DisableEnhancedNotifications</span></span>](/windows/client-management/mdm/policy-csp-windowsdefendersecuritycenter#windowsdefendersecuritycenter-disableenhancednotifications)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e548-123">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="3e548-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="3e548-124">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="3e548-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="3e548-125">DisableFamilyUI</span><span class="sxs-lookup"><span data-stu-id="3e548-125">DisableFamilyUI</span></span>](/windows/client-management/mdm/policy-csp-windowsdefendersecuritycenter#windowsdefendersecuritycenter-disablefamilyui)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e548-126">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="3e548-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="3e548-127">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="3e548-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="3e548-128">DisableHealthUI</span><span class="sxs-lookup"><span data-stu-id="3e548-128">DisableHealthUI</span></span>](/windows/client-management/mdm/policy-csp-windowsdefendersecuritycenter#windowsdefendersecuritycenter-disablehealthui)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e548-129">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="3e548-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="3e548-130">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="3e548-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="3e548-131">DisableNetworkUI</span><span class="sxs-lookup"><span data-stu-id="3e548-131">DisableNetworkUI</span></span>](/windows/client-management/mdm/policy-csp-windowsdefendersecuritycenter#windowsdefendersecuritycenter-disablenetworkui)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e548-132">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="3e548-132">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="3e548-133">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="3e548-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="3e548-134">DisableNotifications</span><span class="sxs-lookup"><span data-stu-id="3e548-134">DisableNotifications</span></span>](/windows/client-management/mdm/policy-csp-windowsdefendersecuritycenter#windowsdefendersecuritycenter-disablenotifications)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e548-135">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="3e548-135">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="3e548-136">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="3e548-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="3e548-137">DisableVirusUI</span><span class="sxs-lookup"><span data-stu-id="3e548-137">DisableVirusUI</span></span>](/windows/client-management/mdm/policy-csp-windowsdefendersecuritycenter#windowsdefendersecuritycenter-disablevirusui)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e548-138">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="3e548-138">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="3e548-139">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="3e548-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="3e548-140">DisallowExploitProtectionOverride</span><span class="sxs-lookup"><span data-stu-id="3e548-140">DisallowExploitProtectionOverride</span></span>](/windows/client-management/mdm/policy-csp-windowsdefendersecuritycenter#windowsdefendersecuritycenter-disallowexploitprotectionoverride)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e548-141">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="3e548-141">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="3e548-142">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="3e548-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="3e548-143">Correo electrónico</span><span class="sxs-lookup"><span data-stu-id="3e548-143">Email</span></span>](/windows/client-management/mdm/policy-csp-windowsdefendersecuritycenter#windowsdefendersecuritycenter-email)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e548-144">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="3e548-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3e548-145">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="3e548-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="3e548-146">EnableCustomizedToasts</span><span class="sxs-lookup"><span data-stu-id="3e548-146">EnableCustomizedToasts</span></span>](/windows/client-management/mdm/policy-csp-windowsdefendersecuritycenter#windowsdefendersecuritycenter-enablecustomizedtoasts)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e548-147">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="3e548-147">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="3e548-148">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="3e548-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="3e548-149">EnableInAppCustomization</span><span class="sxs-lookup"><span data-stu-id="3e548-149">EnableInAppCustomization</span></span>](/windows/client-management/mdm/policy-csp-windowsdefendersecuritycenter#windowsdefendersecuritycenter-enableinappcustomization)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e548-150">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="3e548-150">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="3e548-151">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="3e548-151">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="3e548-152">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="3e548-152">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e548-153">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="3e548-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3e548-154">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3e548-154">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3e548-155">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="3e548-155">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="3e548-156">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="3e548-156">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e548-157">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="3e548-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3e548-158">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3e548-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3e548-159">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="3e548-159">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="3e548-160">Teléfono</span><span class="sxs-lookup"><span data-stu-id="3e548-160">Phone</span></span>](/windows/client-management/mdm/policy-csp-windowsdefendersecuritycenter#windowsdefendersecuritycenter-phone)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e548-161">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="3e548-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3e548-162">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="3e548-162">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="3e548-163">URL</span><span class="sxs-lookup"><span data-stu-id="3e548-163">URL</span></span>](/windows/client-management/mdm/policy-csp-windowsdefendersecuritycenter#windowsdefendersecuritycenter-url)
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e548-164">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="3e548-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3e548-165">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="3e548-165">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3e548-166">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3e548-166">Requirements</span></span>



| <span data-ttu-id="3e548-167">Requisito</span><span class="sxs-lookup"><span data-stu-id="3e548-167">Requirement</span></span> | <span data-ttu-id="3e548-168">Value</span><span class="sxs-lookup"><span data-stu-id="3e548-168">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3e548-169">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3e548-169">Minimum supported client</span></span><br/> | <span data-ttu-id="3e548-170">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="3e548-170">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="3e548-171">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3e548-171">Minimum supported server</span></span><br/> | <span data-ttu-id="3e548-172">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="3e548-172">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="3e548-173">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="3e548-173">Namespace</span></span><br/>                | <span data-ttu-id="3e548-174">Dmmap de MDM raíz de \\ cimv2 \\ \\</span><span class="sxs-lookup"><span data-stu-id="3e548-174">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="3e548-175">MOF</span><span class="sxs-lookup"><span data-stu-id="3e548-175">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3e548-176"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3e548-176"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="3e548-177">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="3e548-177">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3e548-178"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3e548-178"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

