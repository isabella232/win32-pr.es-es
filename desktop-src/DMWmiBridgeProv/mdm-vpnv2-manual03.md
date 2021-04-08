---
title: MDM_VPNv2_Manual03 (clase)
description: MDM \_ VPNv2 \_ Manual03class es un nodo opcional que contiene la configuración del servidor manual.
ms.assetid: c294c5a2-35e2-46ca-b7d8-9c63f9d3cdd6
keywords:
- MDM_VPNv2_Manual03 (clase)
- MDM_VPNv2_Manual03 clase, descrita
topic_type:
- apiref
api_name:
- MDM_VPNv2_Manual03
- MDM_VPNv2_Manual03.InstanceID
- MDM_VPNv2_Manual03.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 561e36d9a048e3a5a523770b9a3987a346fe2283
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996955"
---
# <a name="mdm_vpnv2_manual03-class"></a><span data-ttu-id="814dd-105">\_Clase Manual03 VPNv2 de MDM \_</span><span class="sxs-lookup"><span data-stu-id="814dd-105">MDM\_VPNv2\_Manual03 class</span></span>

<span data-ttu-id="814dd-106">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="814dd-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="814dd-107">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="814dd-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="814dd-108">La **clase \_ \_ Manual03 de MDM VPNv2** es un nodo opcional que contiene la configuración del servidor manual.</span><span class="sxs-lookup"><span data-stu-id="814dd-108">The **MDM\_VPNv2\_Manual03** class is an optional node containing the manual server settings.</span></span>

<span data-ttu-id="814dd-109">La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="814dd-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="814dd-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="814dd-110">Syntax</span></span>

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_VPNv2_Manual03
{
  string InstanceID;
  string ParentID;
  string Server;
};
```

## <a name="members"></a><span data-ttu-id="814dd-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="814dd-111">Members</span></span>

<span data-ttu-id="814dd-112">La **clase \_ \_ Manual03 de MDM VPNv2** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="814dd-112">The **MDM\_VPNv2\_Manual03** class has these types of members:</span></span>

-   [<span data-ttu-id="814dd-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="814dd-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="814dd-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="814dd-114">Properties</span></span>

<span data-ttu-id="814dd-115">La **clase \_ \_ Manual03 de MDM VPNv2** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="814dd-115">The **MDM\_VPNv2\_Manual03** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="814dd-116">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="814dd-116">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="814dd-117">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="814dd-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="814dd-118">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="814dd-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="814dd-119">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="814dd-119">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="814dd-120">Identifica el nombre del nodo primario.</span><span class="sxs-lookup"><span data-stu-id="814dd-120">Identifies the name of the parent node.</span></span>

</dd> <dt>

<span data-ttu-id="814dd-121">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="814dd-121">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="814dd-122">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="814dd-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="814dd-123">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="814dd-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="814dd-124">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="814dd-124">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="814dd-125">Describe la ruta de acceso completa al nodo primario.</span><span class="sxs-lookup"><span data-stu-id="814dd-125">Describes the full path to the parent node.</span></span> <span data-ttu-id="814dd-126">Para esta clase, la cadena es "./Vendor/MSFT/VPNv2/*ProfileName*/proxy/"</span><span class="sxs-lookup"><span data-stu-id="814dd-126">For this class, the string is "./Vendor/MSFT/VPNv2/*ProfileName*/Proxy/"</span></span>

</dd> <dt>

[<span data-ttu-id="814dd-127">Server</span><span class="sxs-lookup"><span data-stu-id="814dd-127">Server</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-proxy-manual-server)
</dt> <dd> <dl> <dt>

<span data-ttu-id="814dd-128">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="814dd-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="814dd-129">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="814dd-129">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="814dd-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="814dd-130">Requirements</span></span>



| <span data-ttu-id="814dd-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="814dd-131">Requirement</span></span> | <span data-ttu-id="814dd-132">Value</span><span class="sxs-lookup"><span data-stu-id="814dd-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="814dd-133">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="814dd-133">Minimum supported client</span></span><br/> | <span data-ttu-id="814dd-134">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="814dd-134">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="814dd-135">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="814dd-135">Minimum supported server</span></span><br/> | <span data-ttu-id="814dd-136">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="814dd-136">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="814dd-137">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="814dd-137">Namespace</span></span><br/>                | <span data-ttu-id="814dd-138">Dmmap de MDM raíz de \\ cimv2 \\ \\</span><span class="sxs-lookup"><span data-stu-id="814dd-138">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="814dd-139">MOF</span><span class="sxs-lookup"><span data-stu-id="814dd-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="814dd-140"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="814dd-140"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="814dd-141">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="814dd-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="814dd-142"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="814dd-142"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="814dd-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="814dd-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="814dd-144">Usar scripting de PowerShell con el proveedor de puente WMI</span><span class="sxs-lookup"><span data-stu-id="814dd-144">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

