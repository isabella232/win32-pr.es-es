---
title: MDM_WindowsAdvancedThreatProtection (clase)
description: La \_ clase WindowsAdvancedThreatProtection de MDM se usa para incorporar puntos de conexión y externalización para la protección contra amenazas avanzada de Windows Defender (WDATP).
ms.assetid: 7a95253e-6d13-4c1b-b78d-c56c6378f7c3
keywords:
- MDM_WindowsAdvancedThreatProtection (clase)
- MDM_WindowsAdvancedThreatProtection clase, descrita
topic_type:
- apiref
api_name:
- MDM_WindowsAdvancedThreatProtection
- MDM_WindowsAdvancedThreatProtection.InstanceID
- MDM_WindowsAdvancedThreatProtection.ParentID
api_location:
- Mofs\DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c369406a3c8bcf982aeb18b4bbb53c1af4983e84
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105658271"
---
# <a name="mdm_windowsadvancedthreatprotection-class"></a><span data-ttu-id="35ed9-105">\_Clase WindowsAdvancedThreatProtection de MDM</span><span class="sxs-lookup"><span data-stu-id="35ed9-105">MDM\_WindowsAdvancedThreatProtection class</span></span>

<span data-ttu-id="35ed9-106">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="35ed9-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="35ed9-107">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="35ed9-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="35ed9-108">La **clase \_ WindowsAdvancedThreatProtection de MDM** se usa para incorporar puntos de conexión y externalización para la protección contra amenazas avanzada de Windows Defender (WDATP).</span><span class="sxs-lookup"><span data-stu-id="35ed9-108">The **MDM\_WindowsAdvancedThreatProtection** class is used to onboard and offboard endpoints for Windows Defender Advanced Threat Protection (WDATP).</span></span>

<span data-ttu-id="35ed9-109">La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="35ed9-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="35ed9-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="35ed9-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_WindowsAdvancedThreatProtection
{
  string InstanceID;
  string ParentID;
  string Onboarding;
  string Offboarding;
};
```

## <a name="members"></a><span data-ttu-id="35ed9-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="35ed9-111">Members</span></span>

<span data-ttu-id="35ed9-112">La **clase \_ WindowsAdvancedThreatProtection de MDM** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="35ed9-112">The **MDM\_WindowsAdvancedThreatProtection** class has these types of members:</span></span>

-   [<span data-ttu-id="35ed9-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="35ed9-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="35ed9-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="35ed9-114">Properties</span></span>

<span data-ttu-id="35ed9-115">La **clase \_ WindowsAdvancedThreatProtection de MDM** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="35ed9-115">The **MDM\_WindowsAdvancedThreatProtection** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="35ed9-116">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="35ed9-116">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35ed9-117">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="35ed9-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="35ed9-118">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="35ed9-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="35ed9-119">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="35ed9-119">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="35ed9-120">Identifica el nombre del nodo primario.</span><span class="sxs-lookup"><span data-stu-id="35ed9-120">Identifies the name of the parent node.</span></span> <span data-ttu-id="35ed9-121">Para esta clase, la cadena es "WindowsAdvancedThreatProtection".</span><span class="sxs-lookup"><span data-stu-id="35ed9-121">For this class, the string is "WindowsAdvancedThreatProtection".</span></span>

</dd> <dt>

[<span data-ttu-id="35ed9-122">Retirada</span><span class="sxs-lookup"><span data-stu-id="35ed9-122">Offboarding</span></span>](/windows/client-management/mdm/windowsadvancedthreatprotection-csp#offboarding)
</dt> <dd> <dl> <dt>

<span data-ttu-id="35ed9-123">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="35ed9-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="35ed9-124">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="35ed9-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="35ed9-125">Incorporación</span><span class="sxs-lookup"><span data-stu-id="35ed9-125">Onboarding</span></span>](/windows/client-management/mdm/windowsadvancedthreatprotection-csp#onboarding)
</dt> <dd> <dl> <dt>

<span data-ttu-id="35ed9-126">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="35ed9-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="35ed9-127">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="35ed9-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="35ed9-128">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="35ed9-128">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35ed9-129">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="35ed9-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="35ed9-130">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="35ed9-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="35ed9-131">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="35ed9-131">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="35ed9-132">Describe la ruta de acceso completa al nodo primario.</span><span class="sxs-lookup"><span data-stu-id="35ed9-132">Describes the full path to the parent node.</span></span> <span data-ttu-id="35ed9-133">Para esta clase, la cadena es "./Vendor/MSFT/".</span><span class="sxs-lookup"><span data-stu-id="35ed9-133">For this class, the string is "./Vendor/MSFT/"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="35ed9-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="35ed9-134">Requirements</span></span>



| <span data-ttu-id="35ed9-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="35ed9-135">Requirement</span></span> | <span data-ttu-id="35ed9-136">Value</span><span class="sxs-lookup"><span data-stu-id="35ed9-136">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="35ed9-137">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="35ed9-137">Minimum supported client</span></span><br/> | <span data-ttu-id="35ed9-138">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="35ed9-138">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="35ed9-139">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="35ed9-139">Minimum supported server</span></span><br/> | <span data-ttu-id="35ed9-140">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="35ed9-140">None supported</span></span><br/>                                                                            |
| <span data-ttu-id="35ed9-141">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="35ed9-141">Namespace</span></span><br/>                | <span data-ttu-id="35ed9-142">Dmmap de MDM raíz de \\ cimv2 \\ \\</span><span class="sxs-lookup"><span data-stu-id="35ed9-142">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                                   |
| <span data-ttu-id="35ed9-143">MOF</span><span class="sxs-lookup"><span data-stu-id="35ed9-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="35ed9-144"><dt>DMWmiBridgeProv1. mof</dt></span><span class="sxs-lookup"><span data-stu-id="35ed9-144"><dt>DMWmiBridgeProv1.mof</dt></span></span> </dl>      |
| <span data-ttu-id="35ed9-145">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="35ed9-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="35ed9-146"><dt>\\DMWmiBridgeProv.dllMOF</dt></span><span class="sxs-lookup"><span data-stu-id="35ed9-146"><dt>Mofs\\DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="35ed9-147">Vea también</span><span class="sxs-lookup"><span data-stu-id="35ed9-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35ed9-148">Usar scripting de PowerShell con el proveedor de puente WMI</span><span class="sxs-lookup"><span data-stu-id="35ed9-148">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

