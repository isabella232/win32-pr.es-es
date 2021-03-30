---
title: MDM_Policy_Config01_System02 (clase)
description: La \_ clase Config01 de System02 de directivas MDM \_ \_ representa las directivas del sistema disponibles.
ms.assetid: 0C3E21DF-309C-4AF3-8682-E921BF45BDEF
keywords:
- MDM_Policy_ConfigSource01_System02 (clase)
- MDM_Policy_ConfigSource01_System02 clase, descrita
topic_type:
- apiref
api_name:
- MDM_Policy_ConfigSource01_System02
- MDM_Policy_ConfigSource01_System02.InstanceID
- MDM_Policy_ConfigSource01_System02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d45ae8061b3e383abdd075d461d5b6dc2c46a053
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802407"
---
# <a name="mdm_policy_config01_system02-class"></a><span data-ttu-id="15060-105">\_ \_ Clase System02 de Config01 de directivas MDM \_</span><span class="sxs-lookup"><span data-stu-id="15060-105">MDM\_Policy\_Config01\_System02 class</span></span>

<span data-ttu-id="15060-106">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="15060-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="15060-107">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="15060-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="15060-108">La **clase \_ \_ Config01 de \_ System02 de directivas MDM** representa las directivas del sistema disponibles.</span><span class="sxs-lookup"><span data-stu-id="15060-108">The **MDM\_Policy\_Config01\_System02** class represents the System policies available.</span></span> <span data-ttu-id="15060-109">Estas directivas determinan las configuraciones del sistema que se permiten.</span><span class="sxs-lookup"><span data-stu-id="15060-109">These policies determine System configurations that are allowed.</span></span>

<span data-ttu-id="15060-110">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="15060-110">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="15060-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="15060-111">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_System02
{
  string InstanceID = "System";
  string ParentID;
  sint32 AllowBuildPreview;
  sint32 AllowEmbeddedMode;
  sint32 AllowExperimentation;
  sint32 AllowFontProviders;
  sint32 AllowLocation;
  sint32 AllowStorageCard;
  sint32 AllowTelemetry;
  string TelemetryProxy;
  sint32 AllowUserToResetPhone;
  string BootStartDriverInitialization;
  sint32 DisableEnterpriseAuthProxy;
  sint32 DisableOneDriveFileSync;
  string DisableSystemRestore;
  sint32 LimitEnhancedDiagnosticDataWindowsAnalytics;
  sint32 FeedbackHubAlwaysSaveDiagnosticsLocally;
};
```

## <a name="members"></a><span data-ttu-id="15060-112">Miembros</span><span class="sxs-lookup"><span data-stu-id="15060-112">Members</span></span>

<span data-ttu-id="15060-113">La clase ConfigSource01 de la **\_ Directiva MDM \_ \_ System02** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="15060-113">The **MDM\_Policy\_ConfigSource01\_System02** class has these types of members:</span></span>

-   [<span data-ttu-id="15060-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="15060-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="15060-115">Propiedades</span><span class="sxs-lookup"><span data-stu-id="15060-115">Properties</span></span>

<span data-ttu-id="15060-116">La **clase \_ \_ ConfigSource01 de \_ System02 de directivas MDM** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="15060-116">The **MDM\_Policy\_ConfigSource01\_System02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="15060-117">AllowBuildPreview</span><span class="sxs-lookup"><span data-stu-id="15060-117">AllowBuildPreview</span></span>](/windows/client-management/mdm/policy-csp-system#system-allowbuildpreview)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15060-118">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="15060-118">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="15060-119">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15060-119">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15060-120">AllowEmbeddedMode</span><span class="sxs-lookup"><span data-stu-id="15060-120">AllowEmbeddedMode</span></span>](/windows/client-management/mdm/policy-csp-system#system-allowembeddedmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15060-121">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="15060-121">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="15060-122">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15060-122">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15060-123">AllowExperimentation</span><span class="sxs-lookup"><span data-stu-id="15060-123">AllowExperimentation</span></span>](/windows/client-management/mdm/policy-csp-system#system-allowexperimentation)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15060-124">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="15060-124">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="15060-125">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15060-125">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15060-126">AllowFontProviders</span><span class="sxs-lookup"><span data-stu-id="15060-126">AllowFontProviders</span></span>](/windows/client-management/mdm/policy-csp-system#system-allowfontproviders)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15060-127">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="15060-127">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="15060-128">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15060-128">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15060-129">AllowLocation</span><span class="sxs-lookup"><span data-stu-id="15060-129">AllowLocation</span></span>](/windows/client-management/mdm/policy-csp-system#system-allowlocation)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15060-130">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="15060-130">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="15060-131">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15060-131">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15060-132">AllowStorageCard</span><span class="sxs-lookup"><span data-stu-id="15060-132">AllowStorageCard</span></span>](/windows/client-management/mdm/policy-csp-system#system-allowstoragecard)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15060-133">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="15060-133">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="15060-134">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15060-134">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15060-135">AllowTelemetry</span><span class="sxs-lookup"><span data-stu-id="15060-135">AllowTelemetry</span></span>](/windows/client-management/mdm/policy-csp-system#system-allowtelemetry)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15060-136">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="15060-136">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="15060-137">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15060-137">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15060-138">AllowUserToResetPhone</span><span class="sxs-lookup"><span data-stu-id="15060-138">AllowUserToResetPhone</span></span>](/windows/client-management/mdm/policy-csp-system#system-allowusertoresetphone)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15060-139">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="15060-139">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="15060-140">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15060-140">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15060-141">BootStartDriverInitialization</span><span class="sxs-lookup"><span data-stu-id="15060-141">BootStartDriverInitialization</span></span>](/windows/client-management/mdm/policy-csp-system#system-bootstartdriverinitialization)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15060-142">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15060-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15060-143">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15060-143">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15060-144">DisableEnterpriseAuthProxy</span><span class="sxs-lookup"><span data-stu-id="15060-144">DisableEnterpriseAuthProxy</span></span>](/windows/client-management/mdm/policy-csp-system#system-disableenterpriseauthproxy)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15060-145">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="15060-145">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="15060-146">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15060-146">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15060-147">DisableOneDriveFileSync</span><span class="sxs-lookup"><span data-stu-id="15060-147">DisableOneDriveFileSync</span></span>](/windows/client-management/mdm/policy-csp-system#system-disableonedrivefilesync)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15060-148">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="15060-148">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="15060-149">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15060-149">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15060-150">DisableSystemRestore</span><span class="sxs-lookup"><span data-stu-id="15060-150">DisableSystemRestore</span></span>](/windows/client-management/mdm/policy-csp-system#system-disablesystemrestore)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15060-151">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15060-151">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15060-152">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15060-152">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="15060-153">FeedbackHubAlwaysSaveDiagnosticsLocally</span><span class="sxs-lookup"><span data-stu-id="15060-153">FeedbackHubAlwaysSaveDiagnosticsLocally</span></span>](/windows/client-management/mdm/policy-csp-system#system-feedbackhubalwayssavediagnosticslocally)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15060-154">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="15060-154">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="15060-155">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15060-155">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="15060-156">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="15060-156">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15060-157">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15060-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15060-158">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="15060-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="15060-159">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="15060-159">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="15060-160">Identifica el nombre del nodo primario.</span><span class="sxs-lookup"><span data-stu-id="15060-160">Identifies the name of the parent node.</span></span> <span data-ttu-id="15060-161">Para esta clase, la cadena es "System".</span><span class="sxs-lookup"><span data-stu-id="15060-161">For this class, the string is "System".</span></span>

</dd> <dt>

[<span data-ttu-id="15060-162">LimitEnhancedDiagnosticDataWindowsAnalytics</span><span class="sxs-lookup"><span data-stu-id="15060-162">LimitEnhancedDiagnosticDataWindowsAnalytics</span></span>](/windows/client-management/mdm/policy-csp-system#system-limitenhanceddiagnosticdatawindowsanalytics)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15060-163">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="15060-163">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="15060-164">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15060-164">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="15060-165">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="15060-165">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15060-166">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15060-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15060-167">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="15060-167">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="15060-168">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="15060-168">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="15060-169">Describe la ruta de acceso completa al nodo primario.</span><span class="sxs-lookup"><span data-stu-id="15060-169">Describes the full path to the parent node.</span></span> <span data-ttu-id="15060-170">Para esta clase, la cadena es "./Vendor/MSFT/Policy/Config".</span><span class="sxs-lookup"><span data-stu-id="15060-170">For this class, the string is "./Vendor/MSFT/Policy/Config"</span></span>

<span data-ttu-id="15060-171">"./Vendor/MSFT/Policy/Config"</span><span class="sxs-lookup"><span data-stu-id="15060-171">"./Vendor/MSFT/Policy/Config"</span></span>

</dd> <dt>

[<span data-ttu-id="15060-172">TelemetryProxy</span><span class="sxs-lookup"><span data-stu-id="15060-172">TelemetryProxy</span></span>](/windows/client-management/mdm/policy-csp-system#system-telemetryproxy)
</dt> <dd> <dl> <dt>

<span data-ttu-id="15060-173">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="15060-173">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15060-174">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="15060-174">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="15060-175">Requisitos</span><span class="sxs-lookup"><span data-stu-id="15060-175">Requirements</span></span>



| <span data-ttu-id="15060-176">Requisito</span><span class="sxs-lookup"><span data-stu-id="15060-176">Requirement</span></span> | <span data-ttu-id="15060-177">Value</span><span class="sxs-lookup"><span data-stu-id="15060-177">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="15060-178">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="15060-178">Minimum supported client</span></span><br/> | <span data-ttu-id="15060-179">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="15060-179">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="15060-180">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="15060-180">Minimum supported server</span></span><br/> | <span data-ttu-id="15060-181">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="15060-181">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="15060-182">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="15060-182">Namespace</span></span><br/>                | <span data-ttu-id="15060-183">DMMap de MDM raíz de \\ CIMv2 \\ \\</span><span class="sxs-lookup"><span data-stu-id="15060-183">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="15060-184">MOF</span><span class="sxs-lookup"><span data-stu-id="15060-184">MOF</span></span><br/>                      | <dl> <span data-ttu-id="15060-185"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="15060-185"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="15060-186">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="15060-186">DLL</span></span><br/>                      | <dl> <span data-ttu-id="15060-187"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="15060-187"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="15060-188">Vea también</span><span class="sxs-lookup"><span data-stu-id="15060-188">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15060-189">Usar scripting de PowerShell con el proveedor de puente WMI</span><span class="sxs-lookup"><span data-stu-id="15060-189">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

