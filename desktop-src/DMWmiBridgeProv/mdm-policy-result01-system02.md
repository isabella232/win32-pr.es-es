---
title: MDM_Policy_Result01_System02 (clase)
description: La \_ clase Result01 de System02 de directivas MDM \_ \_ representa las directivas del sistema disponibles.
ms.assetid: 9A0D9688-9062-429F-897F-75705DC8FD79
keywords:
- MDM_Policy_Result01_System02 (clase)
- MDM_Policy_Result01_System02 clase, descrita
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_System02
- MDM_Policy_Result01_System02.InstanceID
- MDM_Policy_Result01_System02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ffedc3c4e0eda857c071a3174690ad9677fd97da
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802047"
---
# <a name="mdm_policy_result01_system02-class"></a><span data-ttu-id="53dcd-105">\_ \_ Clase System02 de Result01 de directivas MDM \_</span><span class="sxs-lookup"><span data-stu-id="53dcd-105">MDM\_Policy\_Result01\_System02 class</span></span>

<span data-ttu-id="53dcd-106">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="53dcd-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="53dcd-107">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="53dcd-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="53dcd-108">La **clase \_ \_ Result01 de \_ System02 de directivas MDM** representa las directivas del sistema disponibles.</span><span class="sxs-lookup"><span data-stu-id="53dcd-108">The **MDM\_Policy\_Result01\_System02** class represents the System policies available.</span></span> <span data-ttu-id="53dcd-109">Estas directivas determinan las configuraciones del sistema que se permiten.</span><span class="sxs-lookup"><span data-stu-id="53dcd-109">These policies determine System configurations that are allowed.</span></span>

<span data-ttu-id="53dcd-110">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="53dcd-110">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="53dcd-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="53dcd-111">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_System02
{
  string InstanceID;
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

## <a name="members"></a><span data-ttu-id="53dcd-112">Miembros</span><span class="sxs-lookup"><span data-stu-id="53dcd-112">Members</span></span>

<span data-ttu-id="53dcd-113">La clase Result01 de la **\_ Directiva MDM \_ \_ System02** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="53dcd-113">The **MDM\_Policy\_Result01\_System02** class has these types of members:</span></span>

-   [<span data-ttu-id="53dcd-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="53dcd-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="53dcd-115">Propiedades</span><span class="sxs-lookup"><span data-stu-id="53dcd-115">Properties</span></span>

<span data-ttu-id="53dcd-116">La **clase \_ \_ Result01 de \_ System02 de directivas MDM** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="53dcd-116">The **MDM\_Policy\_Result01\_System02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="53dcd-117">AllowBuildPreview</span><span class="sxs-lookup"><span data-stu-id="53dcd-117">AllowBuildPreview</span></span>](/windows/client-management/mdm/policy-csp-system#system-allowbuildpreview)
</dt> <dd> <dl> <dt>

<span data-ttu-id="53dcd-118">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="53dcd-118">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="53dcd-119">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="53dcd-119">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="53dcd-120">AllowEmbeddedMode</span><span class="sxs-lookup"><span data-stu-id="53dcd-120">AllowEmbeddedMode</span></span>](/windows/client-management/mdm/policy-csp-system#system-allowembeddedmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="53dcd-121">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="53dcd-121">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="53dcd-122">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="53dcd-122">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="53dcd-123">AllowExperimentation</span><span class="sxs-lookup"><span data-stu-id="53dcd-123">AllowExperimentation</span></span>](/windows/client-management/mdm/policy-csp-system#system-allowexperimentation)
</dt> <dd> <dl> <dt>

<span data-ttu-id="53dcd-124">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="53dcd-124">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="53dcd-125">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="53dcd-125">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="53dcd-126">AllowFontProviders</span><span class="sxs-lookup"><span data-stu-id="53dcd-126">AllowFontProviders</span></span>](/windows/client-management/mdm/policy-csp-system#system-allowfontproviders)
</dt> <dd> <dl> <dt>

<span data-ttu-id="53dcd-127">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="53dcd-127">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="53dcd-128">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="53dcd-128">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="53dcd-129">AllowLocation</span><span class="sxs-lookup"><span data-stu-id="53dcd-129">AllowLocation</span></span>](/windows/client-management/mdm/policy-csp-system#system-allowlocation)
</dt> <dd> <dl> <dt>

<span data-ttu-id="53dcd-130">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="53dcd-130">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="53dcd-131">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="53dcd-131">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="53dcd-132">AllowStorageCard</span><span class="sxs-lookup"><span data-stu-id="53dcd-132">AllowStorageCard</span></span>](/windows/client-management/mdm/policy-csp-system#system-allowstoragecard)
</dt> <dd> <dl> <dt>

<span data-ttu-id="53dcd-133">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="53dcd-133">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="53dcd-134">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="53dcd-134">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="53dcd-135">AllowTelemetry</span><span class="sxs-lookup"><span data-stu-id="53dcd-135">AllowTelemetry</span></span>](/windows/client-management/mdm/policy-csp-system#system-allowtelemetry)
</dt> <dd> <dl> <dt>

<span data-ttu-id="53dcd-136">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="53dcd-136">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="53dcd-137">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="53dcd-137">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="53dcd-138">AllowUserToResetPhone</span><span class="sxs-lookup"><span data-stu-id="53dcd-138">AllowUserToResetPhone</span></span>](/windows/client-management/mdm/policy-csp-system#system-allowusertoresetphone)
</dt> <dd> <dl> <dt>

<span data-ttu-id="53dcd-139">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="53dcd-139">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="53dcd-140">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="53dcd-140">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="53dcd-141">BootStartDriverInitialization</span><span class="sxs-lookup"><span data-stu-id="53dcd-141">BootStartDriverInitialization</span></span>](/windows/client-management/mdm/policy-csp-system#system-bootstartdriverinitialization)
</dt> <dd> <dl> <dt>

<span data-ttu-id="53dcd-142">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="53dcd-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="53dcd-143">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="53dcd-143">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="53dcd-144">DisableEnterpriseAuthProxy</span><span class="sxs-lookup"><span data-stu-id="53dcd-144">DisableEnterpriseAuthProxy</span></span>](/windows/client-management/mdm/policy-csp-system#system-disableenterpriseauthproxy)
</dt> <dd> <dl> <dt>

<span data-ttu-id="53dcd-145">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="53dcd-145">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="53dcd-146">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="53dcd-146">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="53dcd-147">DisableOneDriveFileSync</span><span class="sxs-lookup"><span data-stu-id="53dcd-147">DisableOneDriveFileSync</span></span>](/windows/client-management/mdm/policy-csp-system#system-disableonedrivefilesync)
</dt> <dd> <dl> <dt>

<span data-ttu-id="53dcd-148">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="53dcd-148">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="53dcd-149">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="53dcd-149">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="53dcd-150">DisableSystemRestore</span><span class="sxs-lookup"><span data-stu-id="53dcd-150">DisableSystemRestore</span></span>](/windows/client-management/mdm/policy-csp-system#system-disablesystemrestore)
</dt> <dd> <dl> <dt>

<span data-ttu-id="53dcd-151">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="53dcd-151">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="53dcd-152">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="53dcd-152">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="53dcd-153">FeedbackHubAlwaysSaveDiagnosticsLocally</span><span class="sxs-lookup"><span data-stu-id="53dcd-153">FeedbackHubAlwaysSaveDiagnosticsLocally</span></span>](/windows/client-management/mdm/policy-csp-system#system-feedbackhubalwayssavediagnosticslocally)
</dt> <dd> <dl> <dt>

<span data-ttu-id="53dcd-154">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="53dcd-154">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="53dcd-155">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="53dcd-155">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="53dcd-156">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="53dcd-156">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="53dcd-157">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="53dcd-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="53dcd-158">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="53dcd-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="53dcd-159">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="53dcd-159">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="53dcd-160">Identifica el nombre del nodo primario.</span><span class="sxs-lookup"><span data-stu-id="53dcd-160">Identifies the name of the parent node.</span></span> <span data-ttu-id="53dcd-161">Para esta clase, la cadena es "System".</span><span class="sxs-lookup"><span data-stu-id="53dcd-161">For this class, the string is "System".</span></span>

</dd> <dt>

[<span data-ttu-id="53dcd-162">LimitEnhancedDiagnosticDataWindowsAnalytics</span><span class="sxs-lookup"><span data-stu-id="53dcd-162">LimitEnhancedDiagnosticDataWindowsAnalytics</span></span>](/windows/client-management/mdm/policy-csp-system#system-limitenhanceddiagnosticdatawindowsanalytics)
</dt> <dd> <dl> <dt>

<span data-ttu-id="53dcd-163">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="53dcd-163">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="53dcd-164">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="53dcd-164">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="53dcd-165">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="53dcd-165">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="53dcd-166">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="53dcd-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="53dcd-167">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="53dcd-167">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="53dcd-168">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="53dcd-168">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="53dcd-169">Describe la ruta de acceso completa al nodo primario.</span><span class="sxs-lookup"><span data-stu-id="53dcd-169">Describes the full path to the parent node.</span></span> <span data-ttu-id="53dcd-170">Para esta clase, la cadena es "./Vendor/MSFT/Policy/Result".</span><span class="sxs-lookup"><span data-stu-id="53dcd-170">For this class, the string is "./Vendor/MSFT/Policy/Result"</span></span>

</dd> <dt>

[<span data-ttu-id="53dcd-171">TelemetryProxy</span><span class="sxs-lookup"><span data-stu-id="53dcd-171">TelemetryProxy</span></span>](/windows/client-management/mdm/policy-csp-system#system-telemetryproxy)
</dt> <dd> <dl> <dt>

<span data-ttu-id="53dcd-172">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="53dcd-172">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="53dcd-173">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="53dcd-173">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="53dcd-174">Requisitos</span><span class="sxs-lookup"><span data-stu-id="53dcd-174">Requirements</span></span>



| <span data-ttu-id="53dcd-175">Requisito</span><span class="sxs-lookup"><span data-stu-id="53dcd-175">Requirement</span></span> | <span data-ttu-id="53dcd-176">Value</span><span class="sxs-lookup"><span data-stu-id="53dcd-176">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="53dcd-177">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="53dcd-177">Minimum supported client</span></span><br/> | <span data-ttu-id="53dcd-178">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="53dcd-178">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="53dcd-179">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="53dcd-179">Minimum supported server</span></span><br/> | <span data-ttu-id="53dcd-180">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="53dcd-180">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="53dcd-181">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="53dcd-181">Namespace</span></span><br/>                | <span data-ttu-id="53dcd-182">DMMap de MDM raíz de \\ CIMv2 \\ \\</span><span class="sxs-lookup"><span data-stu-id="53dcd-182">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="53dcd-183">MOF</span><span class="sxs-lookup"><span data-stu-id="53dcd-183">MOF</span></span><br/>                      | <dl> <span data-ttu-id="53dcd-184"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="53dcd-184"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="53dcd-185">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="53dcd-185">DLL</span></span><br/>                      | <dl> <span data-ttu-id="53dcd-186"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="53dcd-186"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="53dcd-187">Vea también</span><span class="sxs-lookup"><span data-stu-id="53dcd-187">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53dcd-188">Usar scripting de PowerShell con el proveedor de puente WMI</span><span class="sxs-lookup"><span data-stu-id="53dcd-188">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

