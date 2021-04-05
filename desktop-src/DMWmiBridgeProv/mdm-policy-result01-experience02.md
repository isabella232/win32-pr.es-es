---
title: MDM_Policy_Result01_Experience02 (clase)
description: La \_ clase Result01 de Experience02 de directivas MDM \_ \_ representa las directivas de experiencia disponibles.
ms.assetid: c6dc2ef1-1f12-40b0-9d5f-9e886fe1e128
keywords:
- MDM_Policy_Result01_Experience02 (clase)
- MDM_Policy_Result01_Experience02 clase, descrita
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_Experience02
- MDM_Policy_Result01_Experience02.InstanceID
- MDM_Policy_Result01_Experience02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a767c96d7ee23b4dad9719fa74850b39f0759b2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104078918"
---
# <a name="mdm_policy_result01_experience02-class"></a><span data-ttu-id="b011c-105">\_ \_ Clase Experience02 de Result01 de directivas MDM \_</span><span class="sxs-lookup"><span data-stu-id="b011c-105">MDM\_Policy\_Result01\_Experience02 class</span></span>

<span data-ttu-id="b011c-106">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="b011c-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="b011c-107">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="b011c-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="b011c-108">La **clase \_ \_ Result01 de \_ Experience02 de directivas MDM** representa las directivas de experiencia disponibles.</span><span class="sxs-lookup"><span data-stu-id="b011c-108">The **MDM\_Policy\_Result01\_Experience02** class represents the experience policies available.</span></span>

<span data-ttu-id="b011c-109">La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="b011c-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="b011c-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b011c-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_Experience02
{
  string InstanceID;
  string ParentID;
  sint32 AllowCortana;
  sint32 AllowDeviceDiscovery;
  sint32 AllowFindMyDevice;
  sint32 AllowManualMDMUnenrollment;
  sint32 AllowSharingOfOfficeFiles;
  sint32 AllowSIMErrorDialogPromptWhenNoSIM;
  sint32 AllowSaveAsOfOfficeFiles;
  sint32 AllowScreenCapture;
  sint32 AllowSyncMySettings;
  sint32 AllowWindowsTips;
  sint32 DoNotShowFeedbackNotifications;
};
```

## <a name="members"></a><span data-ttu-id="b011c-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="b011c-111">Members</span></span>

<span data-ttu-id="b011c-112">La clase Result01 de la **\_ Directiva MDM \_ \_ Experience02** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="b011c-112">The **MDM\_Policy\_Result01\_Experience02** class has these types of members:</span></span>

-   [<span data-ttu-id="b011c-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b011c-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b011c-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b011c-114">Properties</span></span>

<span data-ttu-id="b011c-115">La **clase \_ \_ Result01 de \_ Experience02 de directivas MDM** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="b011c-115">The **MDM\_Policy\_Result01\_Experience02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="b011c-116">AllowCortana</span><span class="sxs-lookup"><span data-stu-id="b011c-116">AllowCortana</span></span>](/windows/client-management/mdm/policy-csp-experience#experience-allowcortana)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b011c-117">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="b011c-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b011c-118">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="b011c-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b011c-119">AllowDeviceDiscovery</span><span class="sxs-lookup"><span data-stu-id="b011c-119">AllowDeviceDiscovery</span></span>](/windows/client-management/mdm/policy-csp-experience#experience-allowdevicediscovery)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b011c-120">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="b011c-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b011c-121">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="b011c-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b011c-122">AllowFindMyDevice</span><span class="sxs-lookup"><span data-stu-id="b011c-122">AllowFindMyDevice</span></span>](/windows/client-management/mdm/policy-csp-experience#experience-allowfindmydevice)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b011c-123">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="b011c-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b011c-124">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="b011c-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b011c-125">AllowManualMDMUnenrollment</span><span class="sxs-lookup"><span data-stu-id="b011c-125">AllowManualMDMUnenrollment</span></span>](/windows/client-management/mdm/policy-csp-experience#experience-allowmanualmdmunenrollment)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b011c-126">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="b011c-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b011c-127">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="b011c-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b011c-128">AllowSaveAsOfOfficeFiles</span><span class="sxs-lookup"><span data-stu-id="b011c-128">AllowSaveAsOfOfficeFiles</span></span>](/windows/client-management/mdm/policy-csp-experience#experience-allowsaveasofofficefiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b011c-129">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="b011c-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b011c-130">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="b011c-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="b011c-131">AllowScreenCapture</span><span class="sxs-lookup"><span data-stu-id="b011c-131">AllowScreenCapture</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b011c-132">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="b011c-132">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b011c-133">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="b011c-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b011c-134">AllowSharingOfOfficeFiles</span><span class="sxs-lookup"><span data-stu-id="b011c-134">AllowSharingOfOfficeFiles</span></span>](/windows/client-management/mdm/policy-csp-experience#experience-allowsharingofofficefiles)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b011c-135">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="b011c-135">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b011c-136">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="b011c-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="b011c-137">AllowSIMErrorDialogPromptWhenNoSIM</span><span class="sxs-lookup"><span data-stu-id="b011c-137">AllowSIMErrorDialogPromptWhenNoSIM</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b011c-138">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="b011c-138">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b011c-139">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="b011c-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b011c-140">AllowSyncMySettings</span><span class="sxs-lookup"><span data-stu-id="b011c-140">AllowSyncMySettings</span></span>](/windows/client-management/mdm/policy-csp-experience#experience-allowsyncmysettings)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b011c-141">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="b011c-141">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b011c-142">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="b011c-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b011c-143">AllowWindowsTips</span><span class="sxs-lookup"><span data-stu-id="b011c-143">AllowWindowsTips</span></span>](/windows/client-management/mdm/policy-csp-experience#experience-allowwindowstips)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b011c-144">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="b011c-144">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b011c-145">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="b011c-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="b011c-146">DoNotShowFeedbackNotifications</span><span class="sxs-lookup"><span data-stu-id="b011c-146">DoNotShowFeedbackNotifications</span></span>](/windows/client-management/mdm/policy-csp-experience#experience-donotshowfeedbacknotifications)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b011c-147">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="b011c-147">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="b011c-148">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="b011c-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="b011c-149">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="b011c-149">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b011c-150">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b011c-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b011c-151">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b011c-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b011c-152">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="b011c-152">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="b011c-153">Identifica el nombre del nodo primario.</span><span class="sxs-lookup"><span data-stu-id="b011c-153">Identifies the name of the parent node.</span></span> <span data-ttu-id="b011c-154">Para esta clase, la cadena es "Experience".</span><span class="sxs-lookup"><span data-stu-id="b011c-154">For this class, the string is "Experience".</span></span>

</dd> <dt>

<span data-ttu-id="b011c-155">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="b011c-155">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b011c-156">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b011c-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b011c-157">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b011c-157">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b011c-158">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="b011c-158">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="b011c-159">Describe la ruta de acceso completa al nodo primario.</span><span class="sxs-lookup"><span data-stu-id="b011c-159">Describes the full path to the parent node.</span></span> <span data-ttu-id="b011c-160">Para esta clase, la cadena es "./Vendor/MSFT/Policy/Result".</span><span class="sxs-lookup"><span data-stu-id="b011c-160">For this class, the string is "./Vendor/MSFT/Policy/Result"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b011c-161">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b011c-161">Requirements</span></span>



| <span data-ttu-id="b011c-162">Requisito</span><span class="sxs-lookup"><span data-stu-id="b011c-162">Requirement</span></span> | <span data-ttu-id="b011c-163">Value</span><span class="sxs-lookup"><span data-stu-id="b011c-163">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b011c-164">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b011c-164">Minimum supported client</span></span><br/> | <span data-ttu-id="b011c-165">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="b011c-165">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b011c-166">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b011c-166">Minimum supported server</span></span><br/> | <span data-ttu-id="b011c-167">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="b011c-167">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="b011c-168">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="b011c-168">Namespace</span></span><br/>                | <span data-ttu-id="b011c-169">DMMap de MDM raíz de \\ CIMv2 \\ \\</span><span class="sxs-lookup"><span data-stu-id="b011c-169">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="b011c-170">MOF</span><span class="sxs-lookup"><span data-stu-id="b011c-170">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b011c-171"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b011c-171"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="b011c-172">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b011c-172">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b011c-173"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b011c-173"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b011c-174">Vea también</span><span class="sxs-lookup"><span data-stu-id="b011c-174">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b011c-175">Usar scripting de PowerShell con el proveedor de puente WMI</span><span class="sxs-lookup"><span data-stu-id="b011c-175">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

