---
title: MDM_VPNv2_RouteList02_01 (clase)
description: La \_ clase VPNv2 \_ RouteList02 \_ 01 de MDM contiene una lista opcional de rutas que se van a agregar a la tabla de enrutamiento para la interfaz VPN.
ms.assetid: 4271b0c4-9d29-4148-b956-ac9306316c9b
keywords:
- MDM_VPNv2_RouteList02_01 (clase)
- MDM_VPNv2_RouteList02_01 clase, descrita
topic_type:
- apiref
api_name:
- MDM_VPNv2_RouteList02_01
- MDM_VPNv2_RouteList02_01.InstanceID
- MDM_VPNv2_RouteList02_01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ebc274bb3efd2bc78850dd37c95b25db35c4cbe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079591"
---
# <a name="mdm_vpnv2_routelist02_01-class"></a><span data-ttu-id="33da5-105">\_Clase VPNv2 \_ RouteList02 \_ 01 de MDM</span><span class="sxs-lookup"><span data-stu-id="33da5-105">MDM\_VPNv2\_RouteList02\_01 class</span></span>

<span data-ttu-id="33da5-106">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="33da5-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="33da5-107">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="33da5-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="33da5-108">La **clase \_ VPNv2 \_ RouteList02 \_ 01 de MDM** contiene una lista opcional de rutas que se van a agregar a la tabla de enrutamiento para la interfaz VPN.</span><span class="sxs-lookup"><span data-stu-id="33da5-108">The **MDM\_VPNv2\_RouteList02\_01** class contains an optional list of routes to be added to the routing table for the VPN interface.</span></span>

<span data-ttu-id="33da5-109">Esto es necesario para el caso de túnel dividido en el que el sitio del servidor VPN tiene más subredes que la subred predeterminada en función de la dirección IP asignada a la interfaz.</span><span class="sxs-lookup"><span data-stu-id="33da5-109">This is required for split tunneling case where the VPN server site has more subnets that the default subnet based on the IP assigned to the interface.</span></span>

<span data-ttu-id="33da5-110">Cada equipo que ejecuta TCP/IP realiza decisiones de enrutamiento.</span><span class="sxs-lookup"><span data-stu-id="33da5-110">Every computer that runs TCP/IP makes routing decisions.</span></span> <span data-ttu-id="33da5-111">Estas decisiones están controladas por la tabla de enrutamiento IP.</span><span class="sxs-lookup"><span data-stu-id="33da5-111">These decisions are controlled by the IP routing table.</span></span> <span data-ttu-id="33da5-112">Al agregar valores en este nodo se actualiza la tabla de enrutamiento con rutas para la interfaz VPN post Connection.</span><span class="sxs-lookup"><span data-stu-id="33da5-112">Adding values under this node updates the routing table with routes for the VPN interface post connection.</span></span> <span data-ttu-id="33da5-113">Los valores de este nodo representan el prefijo de destino de las rutas IP.</span><span class="sxs-lookup"><span data-stu-id="33da5-113">The values under this node represent the destination prefix of IP routes.</span></span> <span data-ttu-id="33da5-114">Un prefijo de destino consta de un prefijo de dirección IP y una longitud de prefijo.</span><span class="sxs-lookup"><span data-stu-id="33da5-114">A destination prefix consists of an IP address prefix and a prefix length.</span></span>

<span data-ttu-id="33da5-115">Agregar una ruta aquí permite que la pila de red identifique el tráfico que necesita para pasar por la interfaz VPN para la VPN de túnel dividido.</span><span class="sxs-lookup"><span data-stu-id="33da5-115">Adding a route here allows the networking stack to identify the traffic that needs to go over the VPN interface for split tunnel VPN.</span></span> <span data-ttu-id="33da5-116">Algunos servidores VPN pueden configurar esto durante la negociación de la conexión y no necesitan esta información en el perfil de VPN.</span><span class="sxs-lookup"><span data-stu-id="33da5-116">Some VPN servers can configure this during connect negotiation and do not need this information in the VPN Profile.</span></span> <span data-ttu-id="33da5-117">Consulte con el administrador del servidor VPN para determinar si necesita esta información en el perfil de VPN.</span><span class="sxs-lookup"><span data-stu-id="33da5-117">Please check with your VPN server administrator to determine whether you need this information in the VPN profile.</span></span>

<span data-ttu-id="33da5-118">La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="33da5-118">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="33da5-119">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="33da5-119">Syntax</span></span>

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_VPNv2_RouteList02_01
{
  string InstanceID;
  string ParentID;
  string Address;
  sint32 PrefixSize;
};
```

## <a name="members"></a><span data-ttu-id="33da5-120">Miembros</span><span class="sxs-lookup"><span data-stu-id="33da5-120">Members</span></span>

<span data-ttu-id="33da5-121">La **clase \_ VPNv2 \_ RouteList02 \_ 01 de MDM** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="33da5-121">The **MDM\_VPNv2\_RouteList02\_01** class has these types of members:</span></span>

-   [<span data-ttu-id="33da5-122">Propiedades</span><span class="sxs-lookup"><span data-stu-id="33da5-122">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="33da5-123">Propiedades</span><span class="sxs-lookup"><span data-stu-id="33da5-123">Properties</span></span>

<span data-ttu-id="33da5-124">La **clase \_ VPNv2 \_ RouteList02 \_ 01 de MDM** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="33da5-124">The **MDM\_VPNv2\_RouteList02\_01** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="33da5-125">Dirección</span><span class="sxs-lookup"><span data-stu-id="33da5-125">Address</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-routelist-routerowid-address)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33da5-126">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="33da5-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33da5-127">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="33da5-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="33da5-128">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="33da5-128">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="33da5-129">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="33da5-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33da5-130">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="33da5-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="33da5-131">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="33da5-131">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="33da5-132">Identifica el nombre del nodo primario.</span><span class="sxs-lookup"><span data-stu-id="33da5-132">Identifies the name of the parent node.</span></span>

</dd> <dt>

<span data-ttu-id="33da5-133">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="33da5-133">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="33da5-134">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="33da5-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="33da5-135">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="33da5-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="33da5-136">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="33da5-136">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="33da5-137">Describe la ruta de acceso completa al nodo primario.</span><span class="sxs-lookup"><span data-stu-id="33da5-137">Describes the full path to the parent node.</span></span> <span data-ttu-id="33da5-138">Para esta clase, la cadena es "./Vendor/MSFT/VPNv2/*ProfileName*/RouteList"</span><span class="sxs-lookup"><span data-stu-id="33da5-138">For this class, the string is "./Vendor/MSFT/VPNv2/*ProfileName*/RouteList"</span></span>

</dd> <dt>

[<span data-ttu-id="33da5-139">PrefixSize</span><span class="sxs-lookup"><span data-stu-id="33da5-139">PrefixSize</span></span>](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-routelist-routerowid-prefixsize)
</dt> <dd> <dl> <dt>

<span data-ttu-id="33da5-140">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="33da5-140">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="33da5-141">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="33da5-141">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="33da5-142">Requisitos</span><span class="sxs-lookup"><span data-stu-id="33da5-142">Requirements</span></span>



| <span data-ttu-id="33da5-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="33da5-143">Requirement</span></span> | <span data-ttu-id="33da5-144">Value</span><span class="sxs-lookup"><span data-stu-id="33da5-144">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="33da5-145">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="33da5-145">Minimum supported client</span></span><br/> | <span data-ttu-id="33da5-146">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="33da5-146">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="33da5-147">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="33da5-147">Minimum supported server</span></span><br/> | <span data-ttu-id="33da5-148">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="33da5-148">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="33da5-149">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="33da5-149">Namespace</span></span><br/>                | <span data-ttu-id="33da5-150">Dmmap de MDM raíz de \\ cimv2 \\ \\</span><span class="sxs-lookup"><span data-stu-id="33da5-150">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="33da5-151">MOF</span><span class="sxs-lookup"><span data-stu-id="33da5-151">MOF</span></span><br/>                      | <dl> <span data-ttu-id="33da5-152"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="33da5-152"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="33da5-153">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="33da5-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="33da5-154"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="33da5-154"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="33da5-155">Vea también</span><span class="sxs-lookup"><span data-stu-id="33da5-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33da5-156">Usar scripting de PowerShell con el proveedor de puente WMI</span><span class="sxs-lookup"><span data-stu-id="33da5-156">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

