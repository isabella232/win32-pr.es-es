---
title: MDM_VPNv2_Authentication03 (clase)
description: La \_ \_ clase Authentication03 de VPNV2 de MDM contiene información de autenticación para el perfil de VPN nativo.
ms.assetid: 931752a9-6de5-46d4-b9d9-2c59c49e8ed9
keywords:
- MDM_VPNv2_Authentication03 (clase)
- MDM_VPNv2_Authentication03 clase, descrita
topic_type:
- apiref
api_name:
- MDM_VPNv2_Authentication03
- MDM_VPNv2_Authentication03.InstanceID
- MDM_VPNv2_Authentication03.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ca50bcc83df01b4aa5e7ec900985cf15f7e67d1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079390"
---
# <a name="mdm_vpnv2_authentication03-class"></a><span data-ttu-id="cc94d-105">\_Clase Authentication03 VPNv2 de MDM \_</span><span class="sxs-lookup"><span data-stu-id="cc94d-105">MDM\_VPNv2\_Authentication03 class</span></span>

<span data-ttu-id="cc94d-106">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="cc94d-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="cc94d-107">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="cc94d-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="cc94d-108">La [**clase \_ \_ Authentication03 de VPNv2 de MDM**](mdm-vpnv2-01.md) contiene información de autenticación para el perfil de VPN nativo.</span><span class="sxs-lookup"><span data-stu-id="cc94d-108">The [**MDM\_VPNv2\_Authentication03**](mdm-vpnv2-01.md) class contains authentication information for the native VPN profile.</span></span>

<span data-ttu-id="cc94d-109">La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="cc94d-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="cc94d-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="cc94d-110">Syntax</span></span>

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_VPNv2_Authentication03
{
  string InstanceID;
  string ParentID;
  string UserMethod;
  string MachineMethod;
};
```

## <a name="members"></a><span data-ttu-id="cc94d-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="cc94d-111">Members</span></span>

<span data-ttu-id="cc94d-112">La **clase \_ \_ Authentication03 de MDM VPNv2** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="cc94d-112">The **MDM\_VPNv2\_Authentication03** class has these types of members:</span></span>

-   [<span data-ttu-id="cc94d-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="cc94d-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="cc94d-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="cc94d-114">Properties</span></span>

<span data-ttu-id="cc94d-115">La **clase \_ \_ Authentication03 de MDM VPNv2** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="cc94d-115">The **MDM\_VPNv2\_Authentication03** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="cc94d-116">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="cc94d-116">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cc94d-117">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="cc94d-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cc94d-118">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="cc94d-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cc94d-119">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="cc94d-119">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="cc94d-120">Identifica el nombre del nodo primario.</span><span class="sxs-lookup"><span data-stu-id="cc94d-120">Identifies the name of the parent node.</span></span>

</dd> <dt>

[<span data-ttu-id="cc94d-121">MachineMethod</span><span class="sxs-lookup"><span data-stu-id="cc94d-121">MachineMethod</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-nativeprofile-authentication-machinemethod)
</dt> <dd> <dl> <dt>

<span data-ttu-id="cc94d-122">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="cc94d-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cc94d-123">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="cc94d-123">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="cc94d-124">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="cc94d-124">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cc94d-125">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="cc94d-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cc94d-126">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="cc94d-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cc94d-127">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="cc94d-127">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="cc94d-128">Describe la ruta de acceso completa al nodo primario.</span><span class="sxs-lookup"><span data-stu-id="cc94d-128">Describes the full path to the parent node.</span></span> <span data-ttu-id="cc94d-129">Para esta clase, la cadena es "./Vendor/MSFT/VPNv2/*ProfileName*/NativeProfile"</span><span class="sxs-lookup"><span data-stu-id="cc94d-129">For this class, the string is "./Vendor/MSFT/VPNv2/*ProfileName*/NativeProfile"</span></span>

</dd> <dt>

[<span data-ttu-id="cc94d-130">UserMethod</span><span class="sxs-lookup"><span data-stu-id="cc94d-130">UserMethod</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-nativeprofile-authentication-usermethod)
</dt> <dd> <dl> <dt>

<span data-ttu-id="cc94d-131">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="cc94d-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cc94d-132">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="cc94d-132">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="cc94d-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cc94d-133">Requirements</span></span>



| <span data-ttu-id="cc94d-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="cc94d-134">Requirement</span></span> | <span data-ttu-id="cc94d-135">Value</span><span class="sxs-lookup"><span data-stu-id="cc94d-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cc94d-136">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cc94d-136">Minimum supported client</span></span><br/> | <span data-ttu-id="cc94d-137">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="cc94d-137">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="cc94d-138">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cc94d-138">Minimum supported server</span></span><br/> | <span data-ttu-id="cc94d-139">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="cc94d-139">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="cc94d-140">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="cc94d-140">Namespace</span></span><br/>                | <span data-ttu-id="cc94d-141">Dmmap de MDM raíz de \\ cimv2 \\ \\</span><span class="sxs-lookup"><span data-stu-id="cc94d-141">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="cc94d-142">MOF</span><span class="sxs-lookup"><span data-stu-id="cc94d-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cc94d-143"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="cc94d-143"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="cc94d-144">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="cc94d-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cc94d-145"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cc94d-145"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cc94d-146">Vea también</span><span class="sxs-lookup"><span data-stu-id="cc94d-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cc94d-147">Usar scripting de PowerShell con el proveedor de puente WMI</span><span class="sxs-lookup"><span data-stu-id="cc94d-147">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

