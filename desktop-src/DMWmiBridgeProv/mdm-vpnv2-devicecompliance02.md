---
title: MDM_VPNv2_DeviceCompliance02 (clase)
description: Reservado para uso futuro. | MDM_VPNv2_DeviceCompliance02 (clase)
ms.assetid: f84f4812-3083-46c4-a60c-919ec92c844f
keywords:
- MDM_VPNv2_DeviceCompliance02 (clase)
- MDM_VPNv2_DeviceCompliance02 clase, descrita
topic_type:
- apiref
api_name:
- MDM_VPNv2_DeviceCompliance02
- MDM_VPNv2_DeviceCompliance02.InstanceID
- MDM_VPNv2_DeviceCompliance02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a454a5cce3a40066c7cf14a60bdeeb81dcabab9
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105649359"
---
# <a name="mdm_vpnv2_devicecompliance02-class"></a><span data-ttu-id="b4313-106">\_Clase DeviceCompliance02 VPNv2 de MDM \_</span><span class="sxs-lookup"><span data-stu-id="b4313-106">MDM\_VPNv2\_DeviceCompliance02 class</span></span>

<span data-ttu-id="b4313-107">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="b4313-107">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="b4313-108">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="b4313-108">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="b4313-109">Reservado para uso futuro</span><span class="sxs-lookup"><span data-stu-id="b4313-109">Reserved for Future Use</span></span>

<span data-ttu-id="b4313-110">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="b4313-110">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="b4313-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b4313-111">Syntax</span></span>

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_VPNv2_DeviceCompliance02
{
  string  InstanceID;
  string  ParentID;
  boolean Enabled;
};
```

## <a name="members"></a><span data-ttu-id="b4313-112">Miembros</span><span class="sxs-lookup"><span data-stu-id="b4313-112">Members</span></span>

<span data-ttu-id="b4313-113">La **clase \_ \_ DeviceCompliance02 de MDM VPNv2** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="b4313-113">The **MDM\_VPNv2\_DeviceCompliance02** class has these types of members:</span></span>

-   [<span data-ttu-id="b4313-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b4313-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b4313-115">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b4313-115">Properties</span></span>

<span data-ttu-id="b4313-116">La **clase \_ \_ DeviceCompliance02 de MDM VPNv2** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="b4313-116">The **MDM\_VPNv2\_DeviceCompliance02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="b4313-117">Enabled</span><span class="sxs-lookup"><span data-stu-id="b4313-117">Enabled</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-devicecompliance-sso-enabled)
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4313-118">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="b4313-118">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b4313-119">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="b4313-119">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="b4313-120">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="b4313-120">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4313-121">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b4313-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b4313-122">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b4313-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b4313-123">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="b4313-123">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="b4313-124">Agregado en Windows 10, versión 1607.</span><span class="sxs-lookup"><span data-stu-id="b4313-124">Added in Windows 10, version 1607.</span></span> <span data-ttu-id="b4313-125">Los nodos de DeviceCompliance se pueden usar para habilitar el acceso condicional basado en AAD para VPN.</span><span class="sxs-lookup"><span data-stu-id="b4313-125">Nodes under DeviceCompliance can be used to enable AAD-based Conditional Access for VPN.</span></span>

</dd> <dt>

<span data-ttu-id="b4313-126">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="b4313-126">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b4313-127">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b4313-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b4313-128">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b4313-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b4313-129">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="b4313-129">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="b4313-130">Agregado en Windows 10, versión 1607.</span><span class="sxs-lookup"><span data-stu-id="b4313-130">Added in Windows 10, version 1607.</span></span> <span data-ttu-id="b4313-131">Describe la ruta de acceso completa al nodo primario.</span><span class="sxs-lookup"><span data-stu-id="b4313-131">Describes the full path to the parent node.</span></span> <span data-ttu-id="b4313-132">Para esta clase, la cadena es "./Vendor/MSFT/VPNv2/*ProfileName*"</span><span class="sxs-lookup"><span data-stu-id="b4313-132">For this class, the string is "./Vendor/MSFT/VPNv2/*ProfileName*"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b4313-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b4313-133">Requirements</span></span>



| <span data-ttu-id="b4313-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="b4313-134">Requirement</span></span> | <span data-ttu-id="b4313-135">Value</span><span class="sxs-lookup"><span data-stu-id="b4313-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b4313-136">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b4313-136">Minimum supported client</span></span><br/> | <span data-ttu-id="b4313-137">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="b4313-137">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b4313-138">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b4313-138">Minimum supported server</span></span><br/> | <span data-ttu-id="b4313-139">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="b4313-139">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="b4313-140">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="b4313-140">Namespace</span></span><br/>                | <span data-ttu-id="b4313-141">Dmmap de MDM raíz de \\ cimv2 \\ \\</span><span class="sxs-lookup"><span data-stu-id="b4313-141">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="b4313-142">MOF</span><span class="sxs-lookup"><span data-stu-id="b4313-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b4313-143"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b4313-143"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="b4313-144">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b4313-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b4313-145"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b4313-145"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b4313-146">Vea también</span><span class="sxs-lookup"><span data-stu-id="b4313-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b4313-147">Usar scripting de PowerShell con el proveedor de puente WMI</span><span class="sxs-lookup"><span data-stu-id="b4313-147">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

