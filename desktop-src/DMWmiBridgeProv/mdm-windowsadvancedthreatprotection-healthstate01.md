---
title: MDM_WindowsAdvancedThreatProtection_HealthState01 (clase)
description: La \_ \_ clase HealthState01 de WINDOWSADVANCEDTHREATPROTECTION de MDM se usa para determinar el estado de mantenimiento de los puntos de conexión de protección contra amenazas avanzada (WDATP) de Windows Defender.
ms.assetid: 8d630b95-9895-4cb8-99f2-8f869c4dfd18
keywords:
- MDM_WindowsAdvancedThreatProtection_HealthState01 (clase)
- MDM_WindowsAdvancedThreatProtection_HealthState01 clase, descrita
topic_type:
- apiref
api_name:
- MDM_WindowsAdvancedThreatProtection_HealthState01
- MDM_WindowsAdvancedThreatProtection_HealthState01.InstanceID
- MDM_WindowsAdvancedThreatProtection_HealthState01.ParentID
api_location:
- Mofs\DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5519b731cf54a633a659ec865e7a1f0e12deda75
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996781"
---
# <a name="mdm_windowsadvancedthreatprotection_healthstate01-class"></a><span data-ttu-id="26bb1-105">\_Clase HealthState01 WindowsAdvancedThreatProtection de MDM \_</span><span class="sxs-lookup"><span data-stu-id="26bb1-105">MDM\_WindowsAdvancedThreatProtection\_HealthState01 class</span></span>

<span data-ttu-id="26bb1-106">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="26bb1-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="26bb1-107">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="26bb1-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="26bb1-108">La **clase \_ \_ HealthState01 de WindowsAdvancedThreatProtection de MDM** se usa para determinar el estado de mantenimiento de los puntos de conexión de protección contra amenazas avanzada (WDATP) de Windows Defender.</span><span class="sxs-lookup"><span data-stu-id="26bb1-108">The **MDM\_WindowsAdvancedThreatProtection\_HealthState01** class is used to determine the health status of Windows Defender Advanced Threat Protection (WDATP) endpoints.</span></span>

<span data-ttu-id="26bb1-109">La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="26bb1-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="26bb1-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="26bb1-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_WindowsAdvancedThreatProtection_HealthState01
{
  string   InstanceID;
  string   ParentID;
  datetime LastConnected;
  boolean  SenseIsRunning;
  sint32   OnboardingState;
  string   OrgId;
};
```

## <a name="members"></a><span data-ttu-id="26bb1-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="26bb1-111">Members</span></span>

<span data-ttu-id="26bb1-112">La **clase \_ \_ HealthState01 de MDM WindowsAdvancedThreatProtection** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="26bb1-112">The **MDM\_WindowsAdvancedThreatProtection\_HealthState01** class has these types of members:</span></span>

-   [<span data-ttu-id="26bb1-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="26bb1-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="26bb1-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="26bb1-114">Properties</span></span>

<span data-ttu-id="26bb1-115">La **clase \_ \_ HealthState01 de MDM WindowsAdvancedThreatProtection** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="26bb1-115">The **MDM\_WindowsAdvancedThreatProtection\_HealthState01** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="26bb1-116">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="26bb1-116">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26bb1-117">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="26bb1-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="26bb1-118">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="26bb1-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="26bb1-119">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="26bb1-119">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="26bb1-120">Identifica el nombre del nodo primario.</span><span class="sxs-lookup"><span data-stu-id="26bb1-120">Identifies the name of the parent node.</span></span> <span data-ttu-id="26bb1-121">Para esta clase, la cadena es "HealthState".</span><span class="sxs-lookup"><span data-stu-id="26bb1-121">For this class, the string is "HealthState".</span></span>

</dd> <dt>

[<span data-ttu-id="26bb1-122">LastConnected</span><span class="sxs-lookup"><span data-stu-id="26bb1-122">LastConnected</span></span>](/windows/client-management/mdm/windowsadvancedthreatprotection-csp#healthstate-lastconnected)
</dt> <dd> <dl> <dt>

<span data-ttu-id="26bb1-123">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="26bb1-123">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="26bb1-124">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="26bb1-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="26bb1-125">OnboardingState</span><span class="sxs-lookup"><span data-stu-id="26bb1-125">OnboardingState</span></span>](/windows/client-management/mdm/windowsadvancedthreatprotection-csp#healthstate-onboardingstate)
</dt> <dd> <dl> <dt>

<span data-ttu-id="26bb1-126">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="26bb1-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="26bb1-127">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="26bb1-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="26bb1-128">OrgId</span><span class="sxs-lookup"><span data-stu-id="26bb1-128">OrgId</span></span>](/windows/client-management/mdm/windowsadvancedthreatprotection-csp#healthstate-orgid)
</dt> <dd> <dl> <dt>

<span data-ttu-id="26bb1-129">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="26bb1-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="26bb1-130">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="26bb1-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="26bb1-131">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="26bb1-131">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="26bb1-132">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="26bb1-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="26bb1-133">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="26bb1-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="26bb1-134">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="26bb1-134">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="26bb1-135">Describe la ruta de acceso completa al nodo primario.</span><span class="sxs-lookup"><span data-stu-id="26bb1-135">Describes the full path to the parent node.</span></span> <span data-ttu-id="26bb1-136">Para esta clase, la cadena es "./Vendor/MSFT/WindowsAdvancedThreatProtection".</span><span class="sxs-lookup"><span data-stu-id="26bb1-136">For this class, the string is "./Vendor/MSFT/WindowsAdvancedThreatProtection"</span></span>

</dd> <dt>

[<span data-ttu-id="26bb1-137">SenseIsRunning</span><span class="sxs-lookup"><span data-stu-id="26bb1-137">SenseIsRunning</span></span>](/windows/client-management/mdm/windowsadvancedthreatprotection-csp#healthstate-senseisrunning)
</dt> <dd> <dl> <dt>

<span data-ttu-id="26bb1-138">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="26bb1-138">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="26bb1-139">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="26bb1-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="26bb1-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="26bb1-140">Requirements</span></span>



| <span data-ttu-id="26bb1-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="26bb1-141">Requirement</span></span> | <span data-ttu-id="26bb1-142">Value</span><span class="sxs-lookup"><span data-stu-id="26bb1-142">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="26bb1-143">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="26bb1-143">Minimum supported client</span></span><br/> | <span data-ttu-id="26bb1-144">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="26bb1-144">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="26bb1-145">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="26bb1-145">Minimum supported server</span></span><br/> | <span data-ttu-id="26bb1-146">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="26bb1-146">None supported</span></span><br/>                                                                            |
| <span data-ttu-id="26bb1-147">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="26bb1-147">Namespace</span></span><br/>                | <span data-ttu-id="26bb1-148">Dmmap de MDM raíz de \\ cimv2 \\ \\</span><span class="sxs-lookup"><span data-stu-id="26bb1-148">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                                   |
| <span data-ttu-id="26bb1-149">MOF</span><span class="sxs-lookup"><span data-stu-id="26bb1-149">MOF</span></span><br/>                      | <dl> <span data-ttu-id="26bb1-150"><dt>DMWmiBridgeProv1. mof</dt></span><span class="sxs-lookup"><span data-stu-id="26bb1-150"><dt>DMWmiBridgeProv1.mof</dt></span></span> </dl>      |
| <span data-ttu-id="26bb1-151">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="26bb1-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="26bb1-152"><dt>\\DMWmiBridgeProv.dllMOF</dt></span><span class="sxs-lookup"><span data-stu-id="26bb1-152"><dt>Mofs\\DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="26bb1-153">Vea también</span><span class="sxs-lookup"><span data-stu-id="26bb1-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26bb1-154">Usar scripting de PowerShell con el proveedor de puente WMI</span><span class="sxs-lookup"><span data-stu-id="26bb1-154">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

