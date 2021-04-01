---
title: MDM_VPNv2_TrafficFilterList02_App04 (clase)
description: La \_ \_ clase App04 de TRAFFICFILTERLIST02 de MDM proporciona la configuración de las aplicaciones que se permiten a través de la interfaz VPN.
ms.assetid: a56d004b-8fe3-4187-8aad-962f1cab8f7f
keywords:
- MDM_VPNv2_TrafficFilterList02_App04 (clase)
- MDM_VPNv2_TrafficFilterList02_App04 clase, descrita
topic_type:
- apiref
api_name:
- MDM_VPNv2_TrafficFilterList02_App04
- MDM_VPNv2_TrafficFilterList02_App04.InstanceID
- MDM_VPNv2_TrafficFilterList02_App04.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8b1cd3edbfec5fa270f8404983af57dba4fad31
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150710"
---
# <a name="mdm_vpnv2_trafficfilterlist02_app04-class"></a><span data-ttu-id="2e4c7-105">\_ \_ Clase App04 de TrafficFilterList02 de VPNv2 MDM \_</span><span class="sxs-lookup"><span data-stu-id="2e4c7-105">MDM\_VPNv2\_TrafficFilterList02\_App04 class</span></span>

<span data-ttu-id="2e4c7-106">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="2e4c7-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="2e4c7-107">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="2e4c7-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="2e4c7-108">La **clase \_ \_ App04 de TrafficFilterList02 de MDM** proporciona la configuración de las aplicaciones que se permiten a través de la interfaz VPN.</span><span class="sxs-lookup"><span data-stu-id="2e4c7-108">The **MDM\_TrafficFilterList02\_App04** class provides configuration of the apps that are allowed over the VPN interface.</span></span>

<span data-ttu-id="2e4c7-109">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="2e4c7-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="2e4c7-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2e4c7-110">Syntax</span></span>

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_VPNv2_TrafficFilterList02_App04
{
  string InstanceID;
  string ParentID;
  string Id;
  string Type;
};
```

## <a name="members"></a><span data-ttu-id="2e4c7-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="2e4c7-111">Members</span></span>

<span data-ttu-id="2e4c7-112">La clase **App04 de MDM \_ VPNv2 \_ TrafficFilterList02 \_** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="2e4c7-112">The **MDM\_VPNv2\_TrafficFilterList02\_App04** class has these types of members:</span></span>

-   [<span data-ttu-id="2e4c7-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="2e4c7-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2e4c7-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="2e4c7-114">Properties</span></span>

<span data-ttu-id="2e4c7-115">La clase **App04 de MDM \_ VPNv2 \_ TrafficFilterList02 \_** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="2e4c7-115">The **MDM\_VPNv2\_TrafficFilterList02\_App04** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="2e4c7-116">Id</span><span class="sxs-lookup"><span data-stu-id="2e4c7-116">Id</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-trafficfilterlist-trafficfilterid-app-id)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e4c7-117">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2e4c7-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2e4c7-118">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="2e4c7-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="2e4c7-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="2e4c7-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e4c7-120">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2e4c7-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2e4c7-121">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2e4c7-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2e4c7-122">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="2e4c7-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="2e4c7-123">Por regla de VPN por aplicación.</span><span class="sxs-lookup"><span data-stu-id="2e4c7-123">Per app VPN rule.</span></span> <span data-ttu-id="2e4c7-124">Esto permitirá que solo se permitan las aplicaciones especificadas a través de la interfaz VPN.</span><span class="sxs-lookup"><span data-stu-id="2e4c7-124">This will allow only the apps specified to be allowed over the VPN interface.</span></span> <span data-ttu-id="2e4c7-125">Para esta clase, la cadena es "app".</span><span class="sxs-lookup"><span data-stu-id="2e4c7-125">For this class, the string is "App"</span></span>

</dd> <dt>

<span data-ttu-id="2e4c7-126">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="2e4c7-126">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e4c7-127">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2e4c7-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2e4c7-128">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2e4c7-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2e4c7-129">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="2e4c7-129">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="2e4c7-130">Describe la ruta de acceso completa al nodo primario.</span><span class="sxs-lookup"><span data-stu-id="2e4c7-130">Describes the full path to the parent node.</span></span> <span data-ttu-id="2e4c7-131">Para esta clase, la cadena es "./Vendor/MSFT/VPNv2/*ProfileName*/TrafficFilterList/*trafficFilterListId*"</span><span class="sxs-lookup"><span data-stu-id="2e4c7-131">For this class, the string is "./Vendor/MSFT/VPNv2/*ProfileName*/TrafficFilterList/*trafficFilterListId*"</span></span>

</dd> <dt>

[<span data-ttu-id="2e4c7-132">Tipo</span><span class="sxs-lookup"><span data-stu-id="2e4c7-132">Type</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-apptriggerlist-apptriggerrowid-app-type)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e4c7-133">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2e4c7-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2e4c7-134">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="2e4c7-134">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2e4c7-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2e4c7-135">Requirements</span></span>



| <span data-ttu-id="2e4c7-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="2e4c7-136">Requirement</span></span> | <span data-ttu-id="2e4c7-137">Value</span><span class="sxs-lookup"><span data-stu-id="2e4c7-137">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2e4c7-138">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2e4c7-138">Minimum supported client</span></span><br/> | <span data-ttu-id="2e4c7-139">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="2e4c7-139">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="2e4c7-140">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2e4c7-140">Minimum supported server</span></span><br/> | <span data-ttu-id="2e4c7-141">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="2e4c7-141">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="2e4c7-142">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="2e4c7-142">Namespace</span></span><br/>                | <span data-ttu-id="2e4c7-143">DMMap de MDM raíz de \\ CIMv2 \\ \\</span><span class="sxs-lookup"><span data-stu-id="2e4c7-143">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="2e4c7-144">MOF</span><span class="sxs-lookup"><span data-stu-id="2e4c7-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2e4c7-145"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2e4c7-145"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="2e4c7-146">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="2e4c7-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2e4c7-147"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2e4c7-147"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2e4c7-148">Vea también</span><span class="sxs-lookup"><span data-stu-id="2e4c7-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e4c7-149">Usar scripting de PowerShell con el proveedor de puente WMI</span><span class="sxs-lookup"><span data-stu-id="2e4c7-149">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

