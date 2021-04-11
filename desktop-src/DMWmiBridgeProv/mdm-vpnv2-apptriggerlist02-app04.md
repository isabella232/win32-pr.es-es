---
title: MDM_VPNv2_AppTriggerList02_App04 (clase)
description: La \_ \_ clase App04 de VPNV2APPTRIGGERLIST02 de MDM describe una lista de las aplicaciones configuradas para desencadenar la VPN.
ms.assetid: d17ec7b9-8a66-47da-8373-81b56168b495
keywords:
- MDM_VPNv2_AppTriggerList02_App04 (clase)
- MDM_VPNv2_AppTriggerList02_App04 clase, descrita
topic_type:
- apiref
api_name:
- MDM_VPNv2_AppTriggerList02_App04
- MDM_VPNv2_AppTriggerList02_App04.InstanceID
- MDM_VPNv2_AppTriggerList02_App04.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 62685ea94b99e843625e87e7c653a2ff19ab737d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150448"
---
# <a name="mdm_vpnv2_apptriggerlist02_app04-class"></a><span data-ttu-id="fd7ab-105">\_ \_ Clase App04 de AppTriggerList02 de VPNv2 MDM \_</span><span class="sxs-lookup"><span data-stu-id="fd7ab-105">MDM\_VPNv2\_AppTriggerList02\_App04 class</span></span>

<span data-ttu-id="fd7ab-106">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="fd7ab-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="fd7ab-107">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="fd7ab-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="fd7ab-108">La **clase \_ \_ App04 de VPNv2AppTriggerList02 de MDM** describe una lista de las aplicaciones configuradas para desencadenar la VPN.</span><span class="sxs-lookup"><span data-stu-id="fd7ab-108">The **MDM\_VPNv2AppTriggerList02\_App04** class describes a list of applications set to trigger the VPN.</span></span>

<span data-ttu-id="fd7ab-109">Si se inicia alguna de estas aplicaciones y el perfil de VPN es actualmente el perfil activo, este perfil de VPN se desencadenará para conectarse.</span><span class="sxs-lookup"><span data-stu-id="fd7ab-109">If any of these apps are launched and the VPN profile is currently the active profile, this VPN profile will be triggered to connect.</span></span>

<span data-ttu-id="fd7ab-110">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="fd7ab-110">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="fd7ab-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fd7ab-111">Syntax</span></span>

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_VPNv2_AppTriggerList02_App04
{
  string InstanceID;
  string ParentID;
  string Id;
  string Type;
};
```

## <a name="members"></a><span data-ttu-id="fd7ab-112">Miembros</span><span class="sxs-lookup"><span data-stu-id="fd7ab-112">Members</span></span>

<span data-ttu-id="fd7ab-113">La clase **App04 de MDM \_ VPNv2 \_ AppTriggerList02 \_** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="fd7ab-113">The **MDM\_VPNv2\_AppTriggerList02\_App04** class has these types of members:</span></span>

-   [<span data-ttu-id="fd7ab-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="fd7ab-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="fd7ab-115">Propiedades</span><span class="sxs-lookup"><span data-stu-id="fd7ab-115">Properties</span></span>

<span data-ttu-id="fd7ab-116">La clase **App04 de MDM \_ VPNv2 \_ AppTriggerList02 \_** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="fd7ab-116">The **MDM\_VPNv2\_AppTriggerList02\_App04** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="fd7ab-117">Id</span><span class="sxs-lookup"><span data-stu-id="fd7ab-117">Id</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-trafficfilterlist-trafficfilterid-app-id)
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd7ab-118">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="fd7ab-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fd7ab-119">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="fd7ab-119">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="fd7ab-120">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="fd7ab-120">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd7ab-121">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="fd7ab-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fd7ab-122">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="fd7ab-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fd7ab-123">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="fd7ab-123">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="fd7ab-124">Nodo de la aplicación bajo el ID. de fila.</span><span class="sxs-lookup"><span data-stu-id="fd7ab-124">App Node under the Row Id.</span></span>

</dd> <dt>

<span data-ttu-id="fd7ab-125">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="fd7ab-125">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd7ab-126">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="fd7ab-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fd7ab-127">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="fd7ab-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fd7ab-128">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="fd7ab-128">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="fd7ab-129">Describe la ruta de acceso completa al nodo primario.</span><span class="sxs-lookup"><span data-stu-id="fd7ab-129">Describes the full path to the parent node.</span></span> <span data-ttu-id="fd7ab-130">Para esta clase, la cadena es "./Vendor/MSFT/VPNv2/*ProfileName*/AppTriggerList/*appTriggerRowId*"</span><span class="sxs-lookup"><span data-stu-id="fd7ab-130">For this class, the string is "./Vendor/MSFT/VPNv2/*ProfileName*/AppTriggerList/*appTriggerRowId*"</span></span>

</dd> <dt>

[<span data-ttu-id="fd7ab-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="fd7ab-131">Type</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-apptriggerlist-apptriggerrowid-app-type)
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd7ab-132">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="fd7ab-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fd7ab-133">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="fd7ab-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fd7ab-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fd7ab-134">Requirements</span></span>



| <span data-ttu-id="fd7ab-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="fd7ab-135">Requirement</span></span> | <span data-ttu-id="fd7ab-136">Value</span><span class="sxs-lookup"><span data-stu-id="fd7ab-136">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fd7ab-137">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fd7ab-137">Minimum supported client</span></span><br/> | <span data-ttu-id="fd7ab-138">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="fd7ab-138">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="fd7ab-139">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fd7ab-139">Minimum supported server</span></span><br/> | <span data-ttu-id="fd7ab-140">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="fd7ab-140">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="fd7ab-141">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="fd7ab-141">Namespace</span></span><br/>                | <span data-ttu-id="fd7ab-142">DMMap de MDM raíz de \\ CIMv2 \\ \\</span><span class="sxs-lookup"><span data-stu-id="fd7ab-142">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="fd7ab-143">MOF</span><span class="sxs-lookup"><span data-stu-id="fd7ab-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fd7ab-144"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fd7ab-144"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="fd7ab-145">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="fd7ab-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fd7ab-146"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fd7ab-146"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fd7ab-147">Vea también</span><span class="sxs-lookup"><span data-stu-id="fd7ab-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd7ab-148">Usar scripting de PowerShell con el proveedor de puente WMI</span><span class="sxs-lookup"><span data-stu-id="fd7ab-148">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

