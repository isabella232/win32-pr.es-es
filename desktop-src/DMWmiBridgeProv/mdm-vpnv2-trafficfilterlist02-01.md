---
title: MDM_VPNv2_TrafficFilterList02_01 (clase)
description: La \_ clase VPNv2 \_ TrafficFilterList02 \_ 01 de MDM contiene una lista opcional de reglas. Solo el tráfico que coincida con estas reglas se podrá enviar a través de la interfaz VPN.
ms.assetid: 3cffe96d-7454-43a1-aa5b-33e820369e7e
keywords:
- MDM_VPNv2_TrafficFilterList02_01 (clase)
- MDM_VPNv2_TrafficFilterList02_01 clase, descrita
topic_type:
- apiref
api_name:
- MDM_VPNv2_TrafficFilterList02_01
- MDM_VPNv2_TrafficFilterList02_01.InstanceID
- MDM_VPNv2_TrafficFilterList02_01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f3005026a85aa118a4122e073579fcb06389a9fd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150711"
---
# <a name="mdm_vpnv2_trafficfilterlist02_01-class"></a><span data-ttu-id="7e312-106">\_Clase VPNv2 \_ TrafficFilterList02 \_ 01 de MDM</span><span class="sxs-lookup"><span data-stu-id="7e312-106">MDM\_VPNv2\_TrafficFilterList02\_01 class</span></span>

<span data-ttu-id="7e312-107">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="7e312-107">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="7e312-108">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="7e312-108">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="7e312-109">La **clase \_ VPNv2 \_ TrafficFilterList02 \_ 01 de MDM** contiene una lista opcional de reglas.</span><span class="sxs-lookup"><span data-stu-id="7e312-109">The **MDM\_VPNv2\_TrafficFilterList02\_01** class contains an optional list of rules.</span></span> <span data-ttu-id="7e312-110">Solo el tráfico que coincida con estas reglas se podrá enviar a través de la interfaz VPN.</span><span class="sxs-lookup"><span data-stu-id="7e312-110">Only traffic that matches these rules can be sent via the VPN Interface.</span></span>

<span data-ttu-id="7e312-111">La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="7e312-111">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="7e312-112">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7e312-112">Syntax</span></span>

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_VPNv2_TrafficFilterList02_01
{
  string InstanceID;
  string ParentID;
  string Claims;
  sint32 Protocol;
  string LocalPortRanges;
  string RemotePortRanges;
  string LocalAddressRanges;
  string RemoteAddressRanges;
  string RoutingPolicyType;
};
```

## <a name="members"></a><span data-ttu-id="7e312-113">Miembros</span><span class="sxs-lookup"><span data-stu-id="7e312-113">Members</span></span>

<span data-ttu-id="7e312-114">La **clase \_ VPNv2 \_ TrafficFilterList02 \_ 01 de MDM** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="7e312-114">The **MDM\_VPNv2\_TrafficFilterList02\_01** class has these types of members:</span></span>

-   [<span data-ttu-id="7e312-115">Propiedades</span><span class="sxs-lookup"><span data-stu-id="7e312-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7e312-116">Propiedades</span><span class="sxs-lookup"><span data-stu-id="7e312-116">Properties</span></span>

<span data-ttu-id="7e312-117">La **clase \_ VPNv2 \_ TrafficFilterList02 \_ 01 de MDM** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="7e312-117">The **MDM\_VPNv2\_TrafficFilterList02\_01** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="7e312-118">Notificaciones</span><span class="sxs-lookup"><span data-stu-id="7e312-118">Claims</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-trafficfilterlist-trafficfilterid-claims)
</dt> <dd> <dl> <dt>

<span data-ttu-id="7e312-119">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="7e312-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7e312-120">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="7e312-120">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="7e312-121">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="7e312-121">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7e312-122">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="7e312-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7e312-123">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7e312-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7e312-124">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="7e312-124">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="7e312-125">Identifica el nombre del nodo primario.</span><span class="sxs-lookup"><span data-stu-id="7e312-125">Identifies the name of the parent node.</span></span>

</dd> <dt>

[<span data-ttu-id="7e312-126">LocalAddressRanges</span><span class="sxs-lookup"><span data-stu-id="7e312-126">LocalAddressRanges</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-trafficfilterlist-trafficfilterid-localaddressranges)
</dt> <dd> <dl> <dt>

<span data-ttu-id="7e312-127">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="7e312-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7e312-128">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="7e312-128">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="7e312-129">LocalPortRanges</span><span class="sxs-lookup"><span data-stu-id="7e312-129">LocalPortRanges</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-trafficfilterlist-trafficfilterid-localportranges)
</dt> <dd> <dl> <dt>

<span data-ttu-id="7e312-130">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="7e312-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7e312-131">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="7e312-131">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="7e312-132">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="7e312-132">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7e312-133">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="7e312-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7e312-134">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7e312-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7e312-135">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="7e312-135">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="7e312-136">Describe la ruta de acceso completa al nodo primario.</span><span class="sxs-lookup"><span data-stu-id="7e312-136">Describes the full path to the parent node.</span></span> <span data-ttu-id="7e312-137">Para esta clase, la cadena es "./Vendor/MSFT/VPNv2/*ProfileName*/TrafficFilterList"</span><span class="sxs-lookup"><span data-stu-id="7e312-137">For this class, the string is "./Vendor/MSFT/VPNv2/*ProfileName*/TrafficFilterList"</span></span>

</dd> <dt>

[<span data-ttu-id="7e312-138">Protocolo</span><span class="sxs-lookup"><span data-stu-id="7e312-138">Protocol</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-trafficfilterlist-trafficfilterid-protocol)
</dt> <dd> <dl> <dt>

<span data-ttu-id="7e312-139">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="7e312-139">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="7e312-140">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="7e312-140">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="7e312-141">RemoteAddressRanges</span><span class="sxs-lookup"><span data-stu-id="7e312-141">RemoteAddressRanges</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-trafficfilterlist-trafficfilterid-remoteaddressranges)
</dt> <dd> <dl> <dt>

<span data-ttu-id="7e312-142">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="7e312-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7e312-143">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="7e312-143">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="7e312-144">RemotePortRanges</span><span class="sxs-lookup"><span data-stu-id="7e312-144">RemotePortRanges</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-trafficfilterlist-trafficfilterid-remoteportranges)
</dt> <dd> <dl> <dt>

<span data-ttu-id="7e312-145">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="7e312-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7e312-146">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="7e312-146">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="7e312-147">RoutingPolicyType</span><span class="sxs-lookup"><span data-stu-id="7e312-147">RoutingPolicyType</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-trafficfilterlist-trafficfilterid-routingpolicytype)
</dt> <dd> <dl> <dt>

<span data-ttu-id="7e312-148">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="7e312-148">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7e312-149">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="7e312-149">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7e312-150">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7e312-150">Requirements</span></span>



| <span data-ttu-id="7e312-151">Requisito</span><span class="sxs-lookup"><span data-stu-id="7e312-151">Requirement</span></span> | <span data-ttu-id="7e312-152">Value</span><span class="sxs-lookup"><span data-stu-id="7e312-152">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7e312-153">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7e312-153">Minimum supported client</span></span><br/> | <span data-ttu-id="7e312-154">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="7e312-154">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="7e312-155">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7e312-155">Minimum supported server</span></span><br/> | <span data-ttu-id="7e312-156">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="7e312-156">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="7e312-157">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="7e312-157">Namespace</span></span><br/>                | <span data-ttu-id="7e312-158">Dmmap de MDM raíz de \\ cimv2 \\ \\</span><span class="sxs-lookup"><span data-stu-id="7e312-158">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="7e312-159">MOF</span><span class="sxs-lookup"><span data-stu-id="7e312-159">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7e312-160"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7e312-160"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="7e312-161">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="7e312-161">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7e312-162"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7e312-162"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7e312-163">Vea también</span><span class="sxs-lookup"><span data-stu-id="7e312-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7e312-164">Usar scripting de PowerShell con el proveedor de puente WMI</span><span class="sxs-lookup"><span data-stu-id="7e312-164">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

