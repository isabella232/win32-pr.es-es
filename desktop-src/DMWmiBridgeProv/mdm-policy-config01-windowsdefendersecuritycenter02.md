---
title: MDM_Policy_Config01_WindowsDefenderSecurityCenter02 (clase)
description: La \_ clase Config01 de WindowsDefenderSecurityCenter02 de directivas MDM \_ \_ representa las directivas de Security Center de Windows Defender.
ms.assetid: 406c3992-e9ed-49c5-a4c4-97d91013d416
keywords:
- MDM_Policy_Config01_WindowsDefenderSecurityCenter02 (clase)
- MDM_Policy_Config01_WindowsDefenderSecurityCenter02 clase, descrita
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_WindowsDefenderSecurityCenter02
- MDM_Policy_Config01_WindowsDefenderSecurityCenter02.InstanceID
- MDM_Policy_Config01_WindowsDefenderSecurityCenter02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b341eb66cc5d1186a962278babce536c0050523d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905279"
---
# <a name="mdm_policy_config01_windowsdefendersecuritycenter02-class"></a><span data-ttu-id="32f13-105">\_ \_ Clase WindowsDefenderSecurityCenter02 de Config01 de directivas MDM \_</span><span class="sxs-lookup"><span data-stu-id="32f13-105">MDM\_Policy\_Config01\_WindowsDefenderSecurityCenter02 class</span></span>

<span data-ttu-id="32f13-106">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="32f13-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="32f13-107">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="32f13-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="32f13-108">La \_ clase Config01 de WindowsDefenderSecurityCenter02 de directivas MDM \_ \_ representa las directivas de Security Center de Windows Defender.</span><span class="sxs-lookup"><span data-stu-id="32f13-108">The MDM\_Policy\_Config01\_WindowsDefenderSecurityCenter02 class represents the Windows Defender Security Center policies.</span></span>

<span data-ttu-id="32f13-109">La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="32f13-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="32f13-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="32f13-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_WindowsDefenderSecurityCenter02
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

## <a name="members"></a><span data-ttu-id="32f13-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="32f13-111">Members</span></span>

<span data-ttu-id="32f13-112">La clase Config01 de la **\_ Directiva MDM \_ \_ WindowsDefenderSecurityCenter02** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="32f13-112">The **MDM\_Policy\_Config01\_WindowsDefenderSecurityCenter02** class has these types of members:</span></span>

-   [<span data-ttu-id="32f13-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="32f13-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="32f13-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="32f13-114">Properties</span></span>

<span data-ttu-id="32f13-115">La **clase \_ \_ Config01 de \_ WindowsDefenderSecurityCenter02 de directivas MDM** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="32f13-115">The **MDM\_Policy\_Config01\_WindowsDefenderSecurityCenter02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="32f13-116">Compañía</span><span class="sxs-lookup"><span data-stu-id="32f13-116">CompanyName</span></span>](/windows/client-management/mdm/policy-csp-windowsdefendersecuritycenter#windowsdefendersecuritycenter-companyname)
</dt> <dd> <dl> <dt>

<span data-ttu-id="32f13-117">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="32f13-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="32f13-118">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="32f13-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="32f13-119">DisableAppBrowserUI</span><span class="sxs-lookup"><span data-stu-id="32f13-119">DisableAppBrowserUI</span></span>](/windows/client-management/mdm/policy-csp-windowsdefendersecuritycenter#windowsdefendersecuritycenter-disableappbrowserui)
</dt> <dd> <dl> <dt>

<span data-ttu-id="32f13-120">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="32f13-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="32f13-121">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="32f13-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="32f13-122">DisableEnhancedNotifications</span><span class="sxs-lookup"><span data-stu-id="32f13-122">DisableEnhancedNotifications</span></span>](/windows/client-management/mdm/policy-csp-windowsdefendersecuritycenter#windowsdefendersecuritycenter-disableenhancednotifications)
</dt> <dd> <dl> <dt>

<span data-ttu-id="32f13-123">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="32f13-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="32f13-124">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="32f13-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="32f13-125">DisableFamilyUI</span><span class="sxs-lookup"><span data-stu-id="32f13-125">DisableFamilyUI</span></span>](/windows/client-management/mdm/policy-csp-windowsdefendersecuritycenter#windowsdefendersecuritycenter-disablefamilyui)
</dt> <dd> <dl> <dt>

<span data-ttu-id="32f13-126">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="32f13-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="32f13-127">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="32f13-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="32f13-128">DisableHealthUI</span><span class="sxs-lookup"><span data-stu-id="32f13-128">DisableHealthUI</span></span>](/windows/client-management/mdm/policy-csp-windowsdefendersecuritycenter#windowsdefendersecuritycenter-disablehealthui)
</dt> <dd> <dl> <dt>

<span data-ttu-id="32f13-129">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="32f13-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="32f13-130">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="32f13-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="32f13-131">DisableNetworkUI</span><span class="sxs-lookup"><span data-stu-id="32f13-131">DisableNetworkUI</span></span>](/windows/client-management/mdm/policy-csp-windowsdefendersecuritycenter#windowsdefendersecuritycenter-disablenetworkui)
</dt> <dd> <dl> <dt>

<span data-ttu-id="32f13-132">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="32f13-132">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="32f13-133">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="32f13-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="32f13-134">DisableNotifications</span><span class="sxs-lookup"><span data-stu-id="32f13-134">DisableNotifications</span></span>](/windows/client-management/mdm/policy-csp-windowsdefendersecuritycenter#windowsdefendersecuritycenter-disablenotifications)
</dt> <dd> <dl> <dt>

<span data-ttu-id="32f13-135">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="32f13-135">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="32f13-136">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="32f13-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="32f13-137">DisableVirusUI</span><span class="sxs-lookup"><span data-stu-id="32f13-137">DisableVirusUI</span></span>](/windows/client-management/mdm/policy-csp-windowsdefendersecuritycenter#windowsdefendersecuritycenter-disablevirusui)
</dt> <dd> <dl> <dt>

<span data-ttu-id="32f13-138">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="32f13-138">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="32f13-139">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="32f13-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="32f13-140">DisallowExploitProtectionOverride</span><span class="sxs-lookup"><span data-stu-id="32f13-140">DisallowExploitProtectionOverride</span></span>](/windows/client-management/mdm/policy-csp-windowsdefendersecuritycenter#windowsdefendersecuritycenter-disallowexploitprotectionoverride)
</dt> <dd> <dl> <dt>

<span data-ttu-id="32f13-141">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="32f13-141">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="32f13-142">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="32f13-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="32f13-143">Correo electrónico</span><span class="sxs-lookup"><span data-stu-id="32f13-143">Email</span></span>](/windows/client-management/mdm/policy-csp-windowsdefendersecuritycenter#windowsdefendersecuritycenter-email)
</dt> <dd> <dl> <dt>

<span data-ttu-id="32f13-144">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="32f13-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="32f13-145">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="32f13-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="32f13-146">EnableCustomizedToasts</span><span class="sxs-lookup"><span data-stu-id="32f13-146">EnableCustomizedToasts</span></span>](/windows/client-management/mdm/policy-csp-windowsdefendersecuritycenter#windowsdefendersecuritycenter-enablecustomizedtoasts)
</dt> <dd> <dl> <dt>

<span data-ttu-id="32f13-147">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="32f13-147">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="32f13-148">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="32f13-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="32f13-149">EnableInAppCustomization</span><span class="sxs-lookup"><span data-stu-id="32f13-149">EnableInAppCustomization</span></span>](/windows/client-management/mdm/policy-csp-windowsdefendersecuritycenter#windowsdefendersecuritycenter-enableinappcustomization)
</dt> <dd> <dl> <dt>

<span data-ttu-id="32f13-150">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="32f13-150">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="32f13-151">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="32f13-151">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="32f13-152">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="32f13-152">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="32f13-153">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="32f13-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="32f13-154">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="32f13-154">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="32f13-155">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="32f13-155">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="32f13-156">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="32f13-156">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="32f13-157">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="32f13-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="32f13-158">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="32f13-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="32f13-159">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="32f13-159">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="32f13-160">Teléfono</span><span class="sxs-lookup"><span data-stu-id="32f13-160">Phone</span></span>](/windows/client-management/mdm/policy-csp-windowsdefendersecuritycenter#windowsdefendersecuritycenter-phone)
</dt> <dd> <dl> <dt>

<span data-ttu-id="32f13-161">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="32f13-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="32f13-162">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="32f13-162">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="32f13-163">URL</span><span class="sxs-lookup"><span data-stu-id="32f13-163">URL</span></span>](/windows/client-management/mdm/policy-csp-windowsdefendersecuritycenter#windowsdefendersecuritycenter-url)
</dt> <dd> <dl> <dt>

<span data-ttu-id="32f13-164">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="32f13-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="32f13-165">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="32f13-165">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="32f13-166">Requisitos</span><span class="sxs-lookup"><span data-stu-id="32f13-166">Requirements</span></span>



| <span data-ttu-id="32f13-167">Requisito</span><span class="sxs-lookup"><span data-stu-id="32f13-167">Requirement</span></span> | <span data-ttu-id="32f13-168">Value</span><span class="sxs-lookup"><span data-stu-id="32f13-168">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="32f13-169">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="32f13-169">Minimum supported client</span></span><br/> | <span data-ttu-id="32f13-170">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="32f13-170">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="32f13-171">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="32f13-171">Minimum supported server</span></span><br/> | <span data-ttu-id="32f13-172">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="32f13-172">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="32f13-173">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="32f13-173">Namespace</span></span><br/>                | <span data-ttu-id="32f13-174">Dmmap de MDM raíz de \\ cimv2 \\ \\</span><span class="sxs-lookup"><span data-stu-id="32f13-174">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="32f13-175">MOF</span><span class="sxs-lookup"><span data-stu-id="32f13-175">MOF</span></span><br/>                      | <dl> <span data-ttu-id="32f13-176"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="32f13-176"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="32f13-177">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="32f13-177">DLL</span></span><br/>                      | <dl> <span data-ttu-id="32f13-178"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="32f13-178"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

