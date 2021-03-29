---
title: MDM_VPNv2_NativeProfile02 (clase)
description: La \_ clase NativeProfile2 de MDM VPNv2 \_ define la información de perfil cuando se usa un protocolo VPN de bandeja de entrada de Windows (IKEV2, PPTP, L2TP).
ms.assetid: 50c4adc6-baef-437c-8223-9aeaaec813af
keywords:
- MDM_VPNv2_NativeProfile02 (clase)
- MDM_VPNv2_NativeProfile02 clase, descrita
topic_type:
- apiref
api_name:
- MDM_VPNv2_NativeProfile02
- MDM_VPNv2_NativeProfile02.InstanceID
- MDM_VPNv2_NativeProfile02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8573975c488df6e5c759e719d5c687f6a71c505
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905540"
---
# <a name="mdm_vpnv2_nativeprofile02-class"></a><span data-ttu-id="55a67-105">\_Clase NativeProfile02 VPNv2 de MDM \_</span><span class="sxs-lookup"><span data-stu-id="55a67-105">MDM\_VPNv2\_NativeProfile02 class</span></span>

<span data-ttu-id="55a67-106">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="55a67-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="55a67-107">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="55a67-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="55a67-108">La **clase \_ \_ NativeProfile2 de MDM VPNv2** define la información de perfil cuando se usa un protocolo VPN de bandeja de entrada de Windows (IKEV2, PPTP, L2TP).</span><span class="sxs-lookup"><span data-stu-id="55a67-108">The **MDM\_VPNv2\_NativeProfile2** class defines profile information when using a Windows Inbox VPN Protocol (IKEv2, PPTP, L2TP).</span></span>

<span data-ttu-id="55a67-109">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="55a67-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="55a67-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="55a67-110">Syntax</span></span>

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_VPNv2_NativeProfile02
{
  string InstanceID;
  string ParentID;
  string Servers;
  string RoutingPolicyType;
  string NativeProtocolType;
  string L2tpPsk;
};
```

## <a name="members"></a><span data-ttu-id="55a67-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="55a67-111">Members</span></span>

<span data-ttu-id="55a67-112">La **clase \_ \_ NativeProfile02 de MDM VPNv2** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="55a67-112">The **MDM\_VPNv2\_NativeProfile02** class has these types of members:</span></span>

-   [<span data-ttu-id="55a67-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="55a67-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="55a67-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="55a67-114">Properties</span></span>

<span data-ttu-id="55a67-115">La **clase \_ \_ NativeProfile02 de MDM VPNv2** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="55a67-115">The **MDM\_VPNv2\_NativeProfile02** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="55a67-116">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="55a67-116">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55a67-117">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="55a67-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="55a67-118">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="55a67-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="55a67-119">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="55a67-119">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="55a67-120">Identifica el nombre del nodo primario.</span><span class="sxs-lookup"><span data-stu-id="55a67-120">Identifies the name of the parent node.</span></span>

</dd> <dt>

[<span data-ttu-id="55a67-121">L2tpPsk</span><span class="sxs-lookup"><span data-stu-id="55a67-121">L2tpPsk</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-nativeprofile-l2tppsk)
</dt> <dd> <dl> <dt>

<span data-ttu-id="55a67-122">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="55a67-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="55a67-123">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="55a67-123">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="55a67-124">NativeProtocolType</span><span class="sxs-lookup"><span data-stu-id="55a67-124">NativeProtocolType</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-nativeprofile-nativeprotocoltype)
</dt> <dd> <dl> <dt>

<span data-ttu-id="55a67-125">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="55a67-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="55a67-126">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="55a67-126">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="55a67-127">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="55a67-127">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55a67-128">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="55a67-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="55a67-129">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="55a67-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="55a67-130">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="55a67-130">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="55a67-131">Describe la ruta de acceso completa al nodo primario.</span><span class="sxs-lookup"><span data-stu-id="55a67-131">Describes the full path to the parent node.</span></span> <span data-ttu-id="55a67-132">Para esta clase, la cadena es "./Vendor/MSFT/VPNv2/*ProfileName*"</span><span class="sxs-lookup"><span data-stu-id="55a67-132">For this class, the string is "./Vendor/MSFT/VPNv2/*ProfileName*"</span></span>

</dd> <dt>

[<span data-ttu-id="55a67-133">RoutingPolicyType</span><span class="sxs-lookup"><span data-stu-id="55a67-133">RoutingPolicyType</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-trafficfilterlist-trafficfilterid-routingpolicytype)
</dt> <dd> <dl> <dt>

<span data-ttu-id="55a67-134">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="55a67-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="55a67-135">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="55a67-135">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="55a67-136">Servidores</span><span class="sxs-lookup"><span data-stu-id="55a67-136">Servers</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-nativeprofile-servers)
</dt> <dd> <dl> <dt>

<span data-ttu-id="55a67-137">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="55a67-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="55a67-138">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="55a67-138">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="55a67-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="55a67-139">Requirements</span></span>



| <span data-ttu-id="55a67-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="55a67-140">Requirement</span></span> | <span data-ttu-id="55a67-141">Value</span><span class="sxs-lookup"><span data-stu-id="55a67-141">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="55a67-142">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="55a67-142">Minimum supported client</span></span><br/> | <span data-ttu-id="55a67-143">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="55a67-143">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="55a67-144">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="55a67-144">Minimum supported server</span></span><br/> | <span data-ttu-id="55a67-145">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="55a67-145">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="55a67-146">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="55a67-146">Namespace</span></span><br/>                | <span data-ttu-id="55a67-147">Dmmap de MDM raíz de \\ cimv2 \\ \\</span><span class="sxs-lookup"><span data-stu-id="55a67-147">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="55a67-148">MOF</span><span class="sxs-lookup"><span data-stu-id="55a67-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="55a67-149"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="55a67-149"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="55a67-150">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="55a67-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="55a67-151"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="55a67-151"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="55a67-152">Vea también</span><span class="sxs-lookup"><span data-stu-id="55a67-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="55a67-153">Usar scripting de PowerShell con el proveedor de puente WMI</span><span class="sxs-lookup"><span data-stu-id="55a67-153">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

