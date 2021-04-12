---
title: MDM_VPNv2_APNBinding02 (clase)
description: Reservado para uso futuro. | MDM_VPNv2_APNBinding02 (clase)
ms.assetid: ef530e79-b9cc-4bee-8d7b-45227ed55dbe
keywords:
- MDM_VPNv2_APNBinding02 (clase)
- MDM_VPNv2_APNBinding02 clase, descrita
topic_type:
- apiref
api_name:
- MDM_VPNv2_APNBinding02
- MDM_VPNv2_APNBinding02.InstanceID
- MDM_VPNv2_APNBinding02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d4447d1403903c9633523466504817338db969f
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104362079"
---
# <a name="mdm_vpnv2_apnbinding02-class"></a><span data-ttu-id="f0242-106">\_Clase APNBinding02 VPNv2 de MDM \_</span><span class="sxs-lookup"><span data-stu-id="f0242-106">MDM\_VPNv2\_APNBinding02 class</span></span>

<span data-ttu-id="f0242-107">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="f0242-107">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="f0242-108">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="f0242-108">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="f0242-109">Reservado para uso futuro</span><span class="sxs-lookup"><span data-stu-id="f0242-109">Reserved for Future Use</span></span>

<span data-ttu-id="f0242-110">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="f0242-110">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="f0242-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f0242-111">Syntax</span></span>

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_VPNv2_APNBinding02
{
  string  InstanceID;
  string  ParentID;
  string  ProviderId;
  string  AccessPointName;
  string  UserName;
  string  Password;
  boolean IsCompressionEnabled;
  string  AuthenticationType;
};
```

## <a name="members"></a><span data-ttu-id="f0242-112">Miembros</span><span class="sxs-lookup"><span data-stu-id="f0242-112">Members</span></span>

<span data-ttu-id="f0242-113">La **clase \_ \_ APNBinding02 de MDM VPNv2** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="f0242-113">The **MDM\_VPNv2\_APNBinding02** class has these types of members:</span></span>

-   [<span data-ttu-id="f0242-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f0242-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f0242-115">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f0242-115">Properties</span></span>

<span data-ttu-id="f0242-116">La **clase \_ \_ APNBinding02 de MDM VPNv2** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="f0242-116">The **MDM\_VPNv2\_APNBinding02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="f0242-117">AccessPointName</span><span class="sxs-lookup"><span data-stu-id="f0242-117">AccessPointName</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-apnbinding-accesspointname)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0242-118">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f0242-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f0242-119">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="f0242-119">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f0242-120">AuthenticationType</span><span class="sxs-lookup"><span data-stu-id="f0242-120">AuthenticationType</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-apnbinding-authenticationtype)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0242-121">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f0242-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f0242-122">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="f0242-122">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="f0242-123">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="f0242-123">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0242-124">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f0242-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f0242-125">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f0242-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f0242-126">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="f0242-126">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="f0242-127">Reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="f0242-127">Reserved for future use.</span></span>

</dd> <dt>

[<span data-ttu-id="f0242-128">IsCompressionEnabled</span><span class="sxs-lookup"><span data-stu-id="f0242-128">IsCompressionEnabled</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-apnbinding-iscompressionenabled)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0242-129">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="f0242-129">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f0242-130">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="f0242-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="f0242-131">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="f0242-131">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0242-132">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f0242-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f0242-133">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f0242-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f0242-134">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="f0242-134">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="f0242-135">Reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="f0242-135">Reserved for future use.</span></span>

</dd> <dt>

[<span data-ttu-id="f0242-136">Contraseña</span><span class="sxs-lookup"><span data-stu-id="f0242-136">Password</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-apnbinding-password)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0242-137">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f0242-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f0242-138">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="f0242-138">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f0242-139">ProviderId</span><span class="sxs-lookup"><span data-stu-id="f0242-139">ProviderId</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-apnbinding-providerid)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0242-140">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f0242-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f0242-141">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="f0242-141">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f0242-142">UserName</span><span class="sxs-lookup"><span data-stu-id="f0242-142">UserName</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-apnbinding-username)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f0242-143">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f0242-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f0242-144">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="f0242-144">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f0242-145">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f0242-145">Requirements</span></span>



| <span data-ttu-id="f0242-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="f0242-146">Requirement</span></span> | <span data-ttu-id="f0242-147">Value</span><span class="sxs-lookup"><span data-stu-id="f0242-147">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f0242-148">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f0242-148">Minimum supported client</span></span><br/> | <span data-ttu-id="f0242-149">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="f0242-149">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f0242-150">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f0242-150">Minimum supported server</span></span><br/> | <span data-ttu-id="f0242-151">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="f0242-151">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="f0242-152">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="f0242-152">Namespace</span></span><br/>                | <span data-ttu-id="f0242-153">Dmmap de MDM raíz de \\ cimv2 \\ \\</span><span class="sxs-lookup"><span data-stu-id="f0242-153">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="f0242-154">MOF</span><span class="sxs-lookup"><span data-stu-id="f0242-154">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f0242-155"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f0242-155"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="f0242-156">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f0242-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f0242-157"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f0242-157"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f0242-158">Vea también</span><span class="sxs-lookup"><span data-stu-id="f0242-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0242-159">Usar scripting de PowerShell con el proveedor de puente WMI</span><span class="sxs-lookup"><span data-stu-id="f0242-159">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

