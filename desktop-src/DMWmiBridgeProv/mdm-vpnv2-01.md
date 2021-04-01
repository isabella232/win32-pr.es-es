---
title: MDM_VPNv2_01 (clase)
description: La \_ clase VPNv2 \_ 01 de MDM permite configurar el perfil de VPN del dispositivo.
ms.assetid: cfef674b-880c-4c9f-a2c1-6c2cb03189da
keywords:
- MDM_VPNv2_01 (clase)
- MDM_VPNv2_01 clase, descrita
topic_type:
- apiref
api_name:
- MDM_VPNv2_01
- MDM_VPNv2_01.InstanceID
- MDM_VPNv2_01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3457220c438d0143db90c1955d48352353fee29d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996552"
---
# <a name="mdm_vpnv2_01-class"></a><span data-ttu-id="a3e16-105">\_Clase VPNv2 \_ 01 de MDM</span><span class="sxs-lookup"><span data-stu-id="a3e16-105">MDM\_VPNv2\_01 class</span></span>

<span data-ttu-id="a3e16-106">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="a3e16-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="a3e16-107">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="a3e16-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="a3e16-108">La **clase \_ VPNv2 \_ 01 de MDM** permite configurar el perfil de VPN del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a3e16-108">The **MDM\_VPNv2\_01** class allows configuration of the VPN profile of the device.</span></span>

<span data-ttu-id="a3e16-109">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="a3e16-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="a3e16-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a3e16-110">Syntax</span></span>

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_VPNv2_01
{
  string  InstanceID;
  string  ParentID;
  string  EdpModeId;
  boolean RememberCredentials;
  boolean AlwaysOn;
  string  DnsSuffix;
  boolean ByPassForLocal;
  string  TrustedNetworkDetection;
  string  ProfileXML;
  boolean LockDown;
};
```

## <a name="members"></a><span data-ttu-id="a3e16-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="a3e16-111">Members</span></span>

<span data-ttu-id="a3e16-112">La clase **MDM \_ VPNv2 \_ 01** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="a3e16-112">The **MDM\_VPNv2\_01** class has these types of members:</span></span>

-   [<span data-ttu-id="a3e16-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="a3e16-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a3e16-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="a3e16-114">Properties</span></span>

<span data-ttu-id="a3e16-115">La clase **MDM \_ VPNv2 \_ 01** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="a3e16-115">The **MDM\_VPNv2\_01** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="a3e16-116">AlwaysOn</span><span class="sxs-lookup"><span data-stu-id="a3e16-116">AlwaysOn</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-alwayson)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a3e16-117">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="a3e16-117">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a3e16-118">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="a3e16-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a3e16-119">ByPassForLocal</span><span class="sxs-lookup"><span data-stu-id="a3e16-119">ByPassForLocal</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-bypassforlocal)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a3e16-120">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="a3e16-120">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a3e16-121">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="a3e16-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a3e16-122">DnsSuffix</span><span class="sxs-lookup"><span data-stu-id="a3e16-122">DnsSuffix</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-dnssuffix)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a3e16-123">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a3e16-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a3e16-124">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="a3e16-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a3e16-125">EdpModeId</span><span class="sxs-lookup"><span data-stu-id="a3e16-125">EdpModeId</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-edpmodeid)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a3e16-126">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a3e16-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a3e16-127">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="a3e16-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="a3e16-128">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="a3e16-128">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a3e16-129">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a3e16-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a3e16-130">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a3e16-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a3e16-131">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="a3e16-131">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="a3e16-132">Identifica el nombre del nodo primario.</span><span class="sxs-lookup"><span data-stu-id="a3e16-132">Identifies the name of the parent node.</span></span> <span data-ttu-id="a3e16-133">Para esta clase, la cadena es el nombre del perfil de VPN.</span><span class="sxs-lookup"><span data-stu-id="a3e16-133">For this class, the string is the VPN profile name.</span></span>

</dd> <dt>

[<span data-ttu-id="a3e16-134">LockDown</span><span class="sxs-lookup"><span data-stu-id="a3e16-134">LockDown</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-lockdown)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a3e16-135">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="a3e16-135">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a3e16-136">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="a3e16-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="a3e16-137">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="a3e16-137">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a3e16-138">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a3e16-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a3e16-139">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a3e16-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a3e16-140">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="a3e16-140">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="a3e16-141">Describe la ruta de acceso completa al nodo primario.</span><span class="sxs-lookup"><span data-stu-id="a3e16-141">Describes the full path to the parent node.</span></span> <span data-ttu-id="a3e16-142">Para esta clase, la cadena es "./Vendor/MSFT/VPNv2".</span><span class="sxs-lookup"><span data-stu-id="a3e16-142">For this class, the string is "./Vendor/MSFT/VPNv2"</span></span>

</dd> <dt>

[<span data-ttu-id="a3e16-143">ProfileXML</span><span class="sxs-lookup"><span data-stu-id="a3e16-143">ProfileXML</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-profilexml)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a3e16-144">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a3e16-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a3e16-145">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="a3e16-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a3e16-146">RememberCredentials</span><span class="sxs-lookup"><span data-stu-id="a3e16-146">RememberCredentials</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-remembercredentials)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a3e16-147">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="a3e16-147">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a3e16-148">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="a3e16-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a3e16-149">TrustedNetworkDetection</span><span class="sxs-lookup"><span data-stu-id="a3e16-149">TrustedNetworkDetection</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-trustednetworkdetection)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a3e16-150">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a3e16-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a3e16-151">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="a3e16-151">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a3e16-152">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a3e16-152">Requirements</span></span>



| <span data-ttu-id="a3e16-153">Requisito</span><span class="sxs-lookup"><span data-stu-id="a3e16-153">Requirement</span></span> | <span data-ttu-id="a3e16-154">Value</span><span class="sxs-lookup"><span data-stu-id="a3e16-154">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a3e16-155">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a3e16-155">Minimum supported client</span></span><br/> | <span data-ttu-id="a3e16-156">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="a3e16-156">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a3e16-157">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a3e16-157">Minimum supported server</span></span><br/> | <span data-ttu-id="a3e16-158">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="a3e16-158">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="a3e16-159">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="a3e16-159">Namespace</span></span><br/>                | <span data-ttu-id="a3e16-160">DMMap de MDM raíz de \\ CIMv2 \\ \\</span><span class="sxs-lookup"><span data-stu-id="a3e16-160">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="a3e16-161">MOF</span><span class="sxs-lookup"><span data-stu-id="a3e16-161">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a3e16-162"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a3e16-162"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="a3e16-163">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="a3e16-163">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a3e16-164"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a3e16-164"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a3e16-165">Vea también</span><span class="sxs-lookup"><span data-stu-id="a3e16-165">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a3e16-166">Usar scripting de PowerShell con el proveedor de puente WMI</span><span class="sxs-lookup"><span data-stu-id="a3e16-166">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

