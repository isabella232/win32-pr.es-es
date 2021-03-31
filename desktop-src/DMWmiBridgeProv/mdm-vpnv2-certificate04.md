---
title: MDM_VPNv2_Certificate04 (clase)
description: Reservado para uso futuro.
ms.assetid: 0fa831e0-918a-472f-88bf-7e40c4081417
keywords:
- MDM_VPNv2_Certificate04 (clase)
- MDM_VPNv2_Certificate04 clase, descrita
topic_type:
- apiref
api_name:
- MDM_VPNv2_Certificate04
- MDM_VPNv2_Certificate04.InstanceID
- MDM_VPNv2_Certificate04.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea88bd26e8dc9916e7e2db97b980065d7a8733ec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996406"
---
# <a name="mdm_vpnv2_certificate04-class"></a><span data-ttu-id="e57de-105">\_Clase Certificate04 VPNv2 de MDM \_</span><span class="sxs-lookup"><span data-stu-id="e57de-105">MDM\_VPNv2\_Certificate04 class</span></span>

<span data-ttu-id="e57de-106">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="e57de-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="e57de-107">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="e57de-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="e57de-108">Reservado para uso futuro</span><span class="sxs-lookup"><span data-stu-id="e57de-108">Reserved for future Use</span></span>

<span data-ttu-id="e57de-109">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="e57de-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="e57de-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e57de-110">Syntax</span></span>

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_VPNv2_Certificate04
{
  string InstanceID;
  string ParentID;
  string Issuer;
  string Eku;
};
```

## <a name="members"></a><span data-ttu-id="e57de-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="e57de-111">Members</span></span>

<span data-ttu-id="e57de-112">La **clase \_ \_ Certificate04 de MDM VPNv2** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="e57de-112">The **MDM\_VPNv2\_Certificate04** class has these types of members:</span></span>

-   [<span data-ttu-id="e57de-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="e57de-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e57de-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="e57de-114">Properties</span></span>

<span data-ttu-id="e57de-115">La **clase \_ \_ Certificate04 de MDM VPNv2** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="e57de-115">The **MDM\_VPNv2\_Certificate04** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="e57de-116">EKU</span><span class="sxs-lookup"><span data-stu-id="e57de-116">Eku</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-nativeprofile-authentication-certificate-eku)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e57de-117">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="e57de-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e57de-118">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="e57de-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="e57de-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="e57de-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e57de-120">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="e57de-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e57de-121">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e57de-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e57de-122">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="e57de-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="e57de-123">Identifica el nombre del nodo primario.</span><span class="sxs-lookup"><span data-stu-id="e57de-123">Identifies the name of the parent node.</span></span> <span data-ttu-id="e57de-124">Para esta clase, la cadena es "EAP"</span><span class="sxs-lookup"><span data-stu-id="e57de-124">For this class, the string is "Eap"</span></span>

</dd> <dt>

[<span data-ttu-id="e57de-125">Emisor</span><span class="sxs-lookup"><span data-stu-id="e57de-125">Issuer</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-nativeprofile-authentication-certificate-issuer)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e57de-126">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="e57de-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e57de-127">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="e57de-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="e57de-128">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="e57de-128">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e57de-129">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="e57de-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e57de-130">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e57de-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e57de-131">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="e57de-131">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="e57de-132">Describe la ruta de acceso completa al nodo primario.</span><span class="sxs-lookup"><span data-stu-id="e57de-132">Describes the full path to the parent node.</span></span> <span data-ttu-id="e57de-133">Para esta clase, la cadena es "./Vendor/MSFT/VPNv2/*ProfileName*/NativeProfile/Authentication"</span><span class="sxs-lookup"><span data-stu-id="e57de-133">For this class, the string is "./Vendor/MSFT/VPNv2/*ProfileName*/NativeProfile/Authentication"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e57de-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e57de-134">Requirements</span></span>



| <span data-ttu-id="e57de-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="e57de-135">Requirement</span></span> | <span data-ttu-id="e57de-136">Value</span><span class="sxs-lookup"><span data-stu-id="e57de-136">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e57de-137">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e57de-137">Minimum supported client</span></span><br/> | <span data-ttu-id="e57de-138">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="e57de-138">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e57de-139">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e57de-139">Minimum supported server</span></span><br/> | <span data-ttu-id="e57de-140">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="e57de-140">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="e57de-141">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="e57de-141">Namespace</span></span><br/>                | <span data-ttu-id="e57de-142">Dmmap de MDM raíz de \\ cimv2 \\ \\</span><span class="sxs-lookup"><span data-stu-id="e57de-142">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="e57de-143">MOF</span><span class="sxs-lookup"><span data-stu-id="e57de-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e57de-144"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e57de-144"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="e57de-145">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="e57de-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e57de-146"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e57de-146"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e57de-147">Vea también</span><span class="sxs-lookup"><span data-stu-id="e57de-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e57de-148">Usar scripting de PowerShell con el proveedor de puente WMI</span><span class="sxs-lookup"><span data-stu-id="e57de-148">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

