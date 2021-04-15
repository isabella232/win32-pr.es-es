---
title: MDM_VPNv2_Proxy02 (clase)
description: La \_ clase Proxy02 de MDM VPNv2 \_ define un objeto de configuración para habilitar una compatibilidad con el proxy posterior a la conexión para VPN.
ms.assetid: 243f0824-4951-41c4-b8b4-b5c39aefd8ff
keywords:
- MDM_VPNv2_Proxy02 (clase)
- MDM_VPNv2_Proxy02 clase, descrita
topic_type:
- apiref
api_name:
- MDM_VPNv2_Proxy02
- MDM_VPNv2_Proxy02.InstanceID
- MDM_VPNv2_Proxy02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3dcf8197379f5b1ff69433baa845af2cd53bb9e5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490660"
---
# <a name="mdm_vpnv2_proxy02-class"></a><span data-ttu-id="62a8b-105">\_Clase Proxy02 VPNv2 de MDM \_</span><span class="sxs-lookup"><span data-stu-id="62a8b-105">MDM\_VPNv2\_Proxy02 class</span></span>

<span data-ttu-id="62a8b-106">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="62a8b-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="62a8b-107">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="62a8b-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="62a8b-108">La **clase \_ \_ Proxy02 de MDM VPNv2** define un objeto de configuración para habilitar una compatibilidad con el proxy posterior a la conexión para VPN.</span><span class="sxs-lookup"><span data-stu-id="62a8b-108">The **MDM\_VPNv2\_Proxy02** class defines a configuration object to enable a post-connect proxy support for VPN.</span></span> <span data-ttu-id="62a8b-109">El proxy definido para este perfil se aplica cuando este perfil está activo y conectado.</span><span class="sxs-lookup"><span data-stu-id="62a8b-109">The proxy defined for this profile is applied when this profile is active and connected.</span></span>

<span data-ttu-id="62a8b-110">La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="62a8b-110">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="62a8b-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="62a8b-111">Syntax</span></span>

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_VPNv2_Proxy02
{
  string InstanceID;
  string ParentID;
  string AutoConfigUrl;
};
```

## <a name="members"></a><span data-ttu-id="62a8b-112">Miembros</span><span class="sxs-lookup"><span data-stu-id="62a8b-112">Members</span></span>

<span data-ttu-id="62a8b-113">La **clase \_ \_ Proxy02 de MDM VPNv2** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="62a8b-113">The **MDM\_VPNv2\_Proxy02** class has these types of members:</span></span>

-   [<span data-ttu-id="62a8b-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="62a8b-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="62a8b-115">Propiedades</span><span class="sxs-lookup"><span data-stu-id="62a8b-115">Properties</span></span>

<span data-ttu-id="62a8b-116">La **clase \_ \_ Proxy02 de MDM VPNv2** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="62a8b-116">The **MDM\_VPNv2\_Proxy02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="62a8b-117">AutoConfigUrl</span><span class="sxs-lookup"><span data-stu-id="62a8b-117">AutoConfigUrl</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-proxy-autoconfigurl)
</dt> <dd> <dl> <dt>

<span data-ttu-id="62a8b-118">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="62a8b-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="62a8b-119">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="62a8b-119">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="62a8b-120">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="62a8b-120">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62a8b-121">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="62a8b-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="62a8b-122">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="62a8b-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="62a8b-123">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="62a8b-123">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="62a8b-124">Identifica el nombre del nodo primario.</span><span class="sxs-lookup"><span data-stu-id="62a8b-124">Identifies the name of the parent node.</span></span> <span data-ttu-id="62a8b-125">Una colección de objetos de configuración para habilitar una compatibilidad con el proxy posterior a la conexión para VPN.</span><span class="sxs-lookup"><span data-stu-id="62a8b-125">A collection of configuration objects to enable a post-connect proxy support for VPN.</span></span> <span data-ttu-id="62a8b-126">El proxy definido para este perfil se aplica cuando este perfil está activo y conectado.</span><span class="sxs-lookup"><span data-stu-id="62a8b-126">The proxy defined for this profile is applied when this profile is active and connected.</span></span>

</dd> <dt>

<span data-ttu-id="62a8b-127">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="62a8b-127">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62a8b-128">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="62a8b-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="62a8b-129">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="62a8b-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="62a8b-130">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="62a8b-130">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="62a8b-131">Describe la ruta de acceso completa al nodo primario.</span><span class="sxs-lookup"><span data-stu-id="62a8b-131">Describes the full path to the parent node.</span></span> <span data-ttu-id="62a8b-132">Para esta clase, la cadena es "./Vendor/MSFT/VPNv2/*ProfileName*"</span><span class="sxs-lookup"><span data-stu-id="62a8b-132">For this class, the string is "./Vendor/MSFT/VPNv2/*ProfileName*"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="62a8b-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="62a8b-133">Requirements</span></span>



| <span data-ttu-id="62a8b-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="62a8b-134">Requirement</span></span> | <span data-ttu-id="62a8b-135">Value</span><span class="sxs-lookup"><span data-stu-id="62a8b-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="62a8b-136">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="62a8b-136">Minimum supported client</span></span><br/> | <span data-ttu-id="62a8b-137">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="62a8b-137">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="62a8b-138">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="62a8b-138">Minimum supported server</span></span><br/> | <span data-ttu-id="62a8b-139">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="62a8b-139">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="62a8b-140">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="62a8b-140">Namespace</span></span><br/>                | <span data-ttu-id="62a8b-141">Dmmap de MDM raíz de \\ cimv2 \\ \\</span><span class="sxs-lookup"><span data-stu-id="62a8b-141">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="62a8b-142">MOF</span><span class="sxs-lookup"><span data-stu-id="62a8b-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="62a8b-143"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="62a8b-143"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="62a8b-144">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="62a8b-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="62a8b-145"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="62a8b-145"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="62a8b-146">Vea también</span><span class="sxs-lookup"><span data-stu-id="62a8b-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62a8b-147">Usar scripting de PowerShell con el proveedor de puente WMI</span><span class="sxs-lookup"><span data-stu-id="62a8b-147">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

