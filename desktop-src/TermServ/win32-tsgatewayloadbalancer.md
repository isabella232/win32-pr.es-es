---
title: Win32_TSGatewayLoadBalancer (clase)
description: Describe un conjunto de servidores de equilibrio de carga de puerta de enlace de Escritorio remoto (puerta de enlace de escritorio remoto). Se usan para equilibrar la carga de las conexiones de puerta de enlace de escritorio remoto entre varios servidores.
ms.assetid: aa7e7b77-7233-4c6a-8f41-cc332fa509d5
ms.tgt_platform: multiple
keywords:
- Win32_TSGatewayLoadBalancer clase Servicios de Escritorio remoto
- Servicios de Escritorio remoto de Win32_TSGatewayLoadBalancer de clase, se describe
topic_type:
- apiref
api_name:
- Win32_TSGatewayLoadBalancer
- Win32_TSGatewayLoadBalancer.Servers
api_location:
- AagWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4956ed4dc9536ff6f7e3263071a2a477cb0f515
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802089"
---
# <a name="win32_tsgatewayloadbalancer-class"></a><span data-ttu-id="2410e-106">\_Clase Win32 TSGatewayLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="2410e-106">Win32\_TSGatewayLoadBalancer class</span></span>

<span data-ttu-id="2410e-107">Describe un conjunto de servidores de equilibrio de carga de puerta de enlace de Escritorio remoto (puerta de enlace de escritorio remoto).</span><span class="sxs-lookup"><span data-stu-id="2410e-107">Describes a set of Remote Desktop Gateway (RD Gateway) load-balancing servers.</span></span> <span data-ttu-id="2410e-108">Se usan para equilibrar la carga de las conexiones de puerta de enlace de escritorio remoto entre varios servidores.</span><span class="sxs-lookup"><span data-stu-id="2410e-108">These are used to load balance RD Gateway connections across multiple servers.</span></span>

## <a name="syntax"></a><span data-ttu-id="2410e-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2410e-109">Syntax</span></span>

``` syntax
[dynamic, provider("AAGProvider"), AMENDMENT]
class Win32_TSGatewayLoadBalancer
{
  string Servers;
};
```

## <a name="members"></a><span data-ttu-id="2410e-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="2410e-110">Members</span></span>

<span data-ttu-id="2410e-111">La **clase \_ TSGatewayLoadBalancer de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="2410e-111">The **Win32\_TSGatewayLoadBalancer** class has these types of members:</span></span>

-   [<span data-ttu-id="2410e-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="2410e-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="2410e-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="2410e-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="2410e-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="2410e-114">Methods</span></span>

<span data-ttu-id="2410e-115">La clase **Win32 \_ TSGatewayLoadBalancer** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="2410e-115">The **Win32\_TSGatewayLoadBalancer** class has these methods.</span></span>



| <span data-ttu-id="2410e-116">Método</span><span class="sxs-lookup"><span data-stu-id="2410e-116">Method</span></span>                                                                             | <span data-ttu-id="2410e-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="2410e-117">Description</span></span>                                                                                                      |
|:-----------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2410e-118">**AddServers**</span><span class="sxs-lookup"><span data-stu-id="2410e-118">**AddServers**</span></span>](addservers-win32-tsgatewayloadbalancer.md)                       | <span data-ttu-id="2410e-119">Agrega servidores a la propiedad **servidores** .</span><span class="sxs-lookup"><span data-stu-id="2410e-119">Adds servers to the **Servers** property.</span></span><br/>                                                             |
| [<span data-ttu-id="2410e-120">**DeleteAllServers**</span><span class="sxs-lookup"><span data-stu-id="2410e-120">**DeleteAllServers**</span></span>](deleteallservers-win32-tsgatewayloadbalancer.md)           | <span data-ttu-id="2410e-121">Elimina todos los servidores de equilibrio de carga de puerta de enlace de escritorio remoto que participan en la granja de equilibrio de carga.</span><span class="sxs-lookup"><span data-stu-id="2410e-121">Deletes all RD Gateway load-balancing servers participating in the load-balancing farm.</span></span><br/>               |
| [<span data-ttu-id="2410e-122">**DeleteServers**</span><span class="sxs-lookup"><span data-stu-id="2410e-122">**DeleteServers**</span></span>](deleteservers-win32-tsgatewayloadbalancer.md)                 | <span data-ttu-id="2410e-123">Elimina los servidores de la propiedad **servidores** .</span><span class="sxs-lookup"><span data-stu-id="2410e-123">Deletes servers from the **Servers** property.</span></span><br/>                                                        |
| [<span data-ttu-id="2410e-124">**IsLoadBalancingServer**</span><span class="sxs-lookup"><span data-stu-id="2410e-124">**IsLoadBalancingServer**</span></span>](win32-tsgatewayloadbalancer-isloadbalancingserver.md) | <span data-ttu-id="2410e-125">Determina si el servidor puede realizar el equilibrio de carga.</span><span class="sxs-lookup"><span data-stu-id="2410e-125">Determines whether the server can perform load balancing.</span></span><br/>                                             |
| [<span data-ttu-id="2410e-126">**SetServers**</span><span class="sxs-lookup"><span data-stu-id="2410e-126">**SetServers**</span></span>](setservers-win32-tsgatewayloadbalancer.md)                       | <span data-ttu-id="2410e-127">Establece la propiedad **servidores** con la lista separada por punto y coma de servidores de equilibrio de carga de puerta de enlace de escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="2410e-127">Sets the **Servers** property with the semicolon-separated list of RD Gateway load-balancing servers.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="2410e-128">Propiedades</span><span class="sxs-lookup"><span data-stu-id="2410e-128">Properties</span></span>

<span data-ttu-id="2410e-129">La **clase \_ TSGatewayLoadBalancer de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="2410e-129">The **Win32\_TSGatewayLoadBalancer** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2410e-130">**Servidores**</span><span class="sxs-lookup"><span data-stu-id="2410e-130">**Servers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2410e-131">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2410e-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2410e-132">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2410e-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2410e-133">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="2410e-133">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="2410e-134">Lista separada por punto y coma de servidores de equilibrio de carga de puerta de enlace de escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="2410e-134">Semicolon-separated list of RD Gateway load-balancing servers.</span></span> <span data-ttu-id="2410e-135">Esta propiedad se puede cambiar con los métodos [**SetServers**](setservers-win32-tsgatewayloadbalancer.md), [**AddServers**](addservers-win32-tsgatewayloadbalancer.md), [**DeleteServers**](deleteservers-win32-tsgatewayloadbalancer.md)y [**DeleteAllServers**](deleteallservers-win32-tsgatewayloadbalancer.md) .</span><span class="sxs-lookup"><span data-stu-id="2410e-135">This property can be changed with the [**SetServers**](setservers-win32-tsgatewayloadbalancer.md), [**AddServers**](addservers-win32-tsgatewayloadbalancer.md), [**DeleteServers**](deleteservers-win32-tsgatewayloadbalancer.md), and [**DeleteAllServers**](deleteallservers-win32-tsgatewayloadbalancer.md) methods.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2410e-136">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2410e-136">Remarks</span></span>

<span data-ttu-id="2410e-137">Para usar esta clase, debe ser miembro del grupo administradores.</span><span class="sxs-lookup"><span data-stu-id="2410e-137">You must be a member of the Administrators group to use this class.</span></span>

<span data-ttu-id="2410e-138">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="2410e-138">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="2410e-139">Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="2410e-139">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="2410e-140">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="2410e-140">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="2410e-141">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="2410e-141">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="2410e-142">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2410e-142">Requirements</span></span>



| <span data-ttu-id="2410e-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="2410e-143">Requirement</span></span> | <span data-ttu-id="2410e-144">Value</span><span class="sxs-lookup"><span data-stu-id="2410e-144">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="2410e-145">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2410e-145">Minimum supported client</span></span><br/> | <span data-ttu-id="2410e-146">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="2410e-146">None supported</span></span><br/>                                                                |
| <span data-ttu-id="2410e-147">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2410e-147">Minimum supported server</span></span><br/> | <span data-ttu-id="2410e-148">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2410e-148">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="2410e-149">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="2410e-149">Namespace</span></span><br/>                | <span data-ttu-id="2410e-150">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="2410e-150">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="2410e-151">MOF</span><span class="sxs-lookup"><span data-stu-id="2410e-151">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2410e-152"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2410e-152"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="2410e-153">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="2410e-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2410e-154"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2410e-154"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="2410e-155">Vea también</span><span class="sxs-lookup"><span data-stu-id="2410e-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2410e-156">**Win32 \_ TSGatewayConnection**</span><span class="sxs-lookup"><span data-stu-id="2410e-156">**Win32\_TSGatewayConnection**</span></span>](win32-tsgatewayconnection.md)
</dt> <dt>

[<span data-ttu-id="2410e-157">**Win32 \_ TSGatewayConnectionAuthorizationPolicy**</span><span class="sxs-lookup"><span data-stu-id="2410e-157">**Win32\_TSGatewayConnectionAuthorizationPolicy**</span></span>](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> <dt>

[<span data-ttu-id="2410e-158">**Win32 \_ TSGatewayRADIUSServer**</span><span class="sxs-lookup"><span data-stu-id="2410e-158">**Win32\_TSGatewayRADIUSServer**</span></span>](win32-tsgatewayradiusserver.md)
</dt> <dt>

[<span data-ttu-id="2410e-159">**Win32 \_ TSGatewayResourceAuthorizationPolicy**</span><span class="sxs-lookup"><span data-stu-id="2410e-159">**Win32\_TSGatewayResourceAuthorizationPolicy**</span></span>](win32-tsgatewayresourceauthorizationpolicy.md)
</dt> <dt>

[<span data-ttu-id="2410e-160">**Win32 \_ TSGatewayResourceGroup**</span><span class="sxs-lookup"><span data-stu-id="2410e-160">**Win32\_TSGatewayResourceGroup**</span></span>](win32-tsgatewayresourcegroup.md)
</dt> <dt>

[<span data-ttu-id="2410e-161">**Win32 \_ TSGatewayServerSettings**</span><span class="sxs-lookup"><span data-stu-id="2410e-161">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> </dl>

 

