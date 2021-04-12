---
title: Win32_TSGatewayRADIUSServer (clase)
description: Describe un servidor Servicio de autenticación remota telefónica de usuario (RADIUS), que tiene un conjunto de directivas de autorización de conexión Servicios de Escritorio remoto (RD \ 160; Cap).
ms.assetid: 40254354-f446-4e17-b7ec-649c98dd94f9
ms.tgt_platform: multiple
keywords:
- Win32_TSGatewayRADIUSServer clase Servicios de Escritorio remoto
- Servicios de Escritorio remoto de Win32_TSGatewayRADIUSServer de clase, se describe
topic_type:
- apiref
api_name:
- Win32_TSGatewayRADIUSServer
- Win32_TSGatewayRADIUSServer.Name
- Win32_TSGatewayRADIUSServer.Priority
- Win32_TSGatewayRADIUSServer.SharedSecret
api_location:
- AagWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4157d89dc942a1c2f8ff7d778f9f8048971902ba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490277"
---
# <a name="win32_tsgatewayradiusserver-class"></a><span data-ttu-id="1b696-105">\_Clase Win32 TSGatewayRADIUSServer</span><span class="sxs-lookup"><span data-stu-id="1b696-105">Win32\_TSGatewayRADIUSServer class</span></span>

<span data-ttu-id="1b696-106">Describe un servidor Servicio de autenticación remota telefónica de usuario (RADIUS), que tiene un conjunto de Servicios de Escritorio remoto directivas de autorización de conexión (Cap de RD).</span><span class="sxs-lookup"><span data-stu-id="1b696-106">Describes a Remote Authentication Dial-In User Service (RADIUS) server, which has a set of Remote Desktop Services connection authorization policies (RD CAPs).</span></span>

<span data-ttu-id="1b696-107">RADIUS es un protocolo estándar del sector que se usa para transmitir información de autenticación, autorización y configuración entre un equipo servidor y un servidor de autenticación, denominado servidor RADIUS, con una base de datos que almacena información de usuario.</span><span class="sxs-lookup"><span data-stu-id="1b696-107">RADIUS is an industry-standard protocol that is used to transmit authentication, authorization, and configuration information between a server computer and an authenticating server, called a RADIUS server, with a database that stores user information.</span></span> <span data-ttu-id="1b696-108">Para obtener más información, vea [protocolo RADIUS](/previous-versions/windows/it-pro/windows-server-2003/cc781821(v=ws.10)).</span><span class="sxs-lookup"><span data-stu-id="1b696-108">For more information, see [RADIUS Protocol](/previous-versions/windows/it-pro/windows-server-2003/cc781821(v=ws.10)).</span></span>

## <a name="syntax"></a><span data-ttu-id="1b696-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1b696-109">Syntax</span></span>

``` syntax
[dynamic, provider("AAGProvider"), AMENDMENT]
class Win32_TSGatewayRADIUSServer
{
  string Name;
  uint32 Priority;
  string SharedSecret;
};
```

## <a name="members"></a><span data-ttu-id="1b696-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="1b696-110">Members</span></span>

<span data-ttu-id="1b696-111">La **clase \_ TSGatewayRADIUSServer de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="1b696-111">The **Win32\_TSGatewayRADIUSServer** class has these types of members:</span></span>

-   [<span data-ttu-id="1b696-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="1b696-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="1b696-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="1b696-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="1b696-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="1b696-114">Methods</span></span>

<span data-ttu-id="1b696-115">La clase **Win32 \_ TSGatewayRADIUSServer** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="1b696-115">The **Win32\_TSGatewayRADIUSServer** class has these methods.</span></span>



| <span data-ttu-id="1b696-116">Método</span><span class="sxs-lookup"><span data-stu-id="1b696-116">Method</span></span>                                                                 | <span data-ttu-id="1b696-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="1b696-117">Description</span></span>                                                                  |
|:-----------------------------------------------------------------------|:-----------------------------------------------------------------------------|
| [<span data-ttu-id="1b696-118">**Agréguela**</span><span class="sxs-lookup"><span data-stu-id="1b696-118">**Add**</span></span>](win32-tsgatewayradiusserver-add.md)                         | <span data-ttu-id="1b696-119">Agrega un nuevo servidor RADIUS.</span><span class="sxs-lookup"><span data-stu-id="1b696-119">Adds a new RADIUS server.</span></span><br/>                                         |
| [<span data-ttu-id="1b696-120">**Bajar**</span><span class="sxs-lookup"><span data-stu-id="1b696-120">**MoveDown**</span></span>](movedown-win32-tsgatewayradiusserver.md)               | <span data-ttu-id="1b696-121">Mueve el servidor RADIUS una posición hacia abajo en el orden de prioridad.</span><span class="sxs-lookup"><span data-stu-id="1b696-121">Moves this RADIUS server one position down in the priority order.</span></span><br/> |
| [<span data-ttu-id="1b696-122">**MoveUp**</span><span class="sxs-lookup"><span data-stu-id="1b696-122">**MoveUp**</span></span>](moveup-win32-tsgatewayradiusserver.md)                   | <span data-ttu-id="1b696-123">Mueve el servidor RADIUS una posición hacia arriba en el orden de prioridad.</span><span class="sxs-lookup"><span data-stu-id="1b696-123">Moves this RADIUS server one position up in the priority order.</span></span><br/>   |
| [<span data-ttu-id="1b696-124">**Retirar**</span><span class="sxs-lookup"><span data-stu-id="1b696-124">**Remove**</span></span>](win32-tsgatewayradiusserver-remove.md)                   | <span data-ttu-id="1b696-125">Quita el servidor RADIUS actual.</span><span class="sxs-lookup"><span data-stu-id="1b696-125">Removes the current RADIUS server.</span></span><br/>                                |
| [<span data-ttu-id="1b696-126">**SetName**</span><span class="sxs-lookup"><span data-stu-id="1b696-126">**SetName**</span></span>](setname-win32-tsgatewayradiusserver.md)                 | <span data-ttu-id="1b696-127">Establece la propiedad de **nombre** para este servidor RADIUS.</span><span class="sxs-lookup"><span data-stu-id="1b696-127">Sets the **Name** property for this RADIUS server.</span></span><br/>                |
| [<span data-ttu-id="1b696-128">**SetSharedSecret**</span><span class="sxs-lookup"><span data-stu-id="1b696-128">**SetSharedSecret**</span></span>](setsharedsecret-win32-tsgatewayradiusserver.md) | <span data-ttu-id="1b696-129">Establece la propiedad **SharedSecret** para este servidor RADIUS.</span><span class="sxs-lookup"><span data-stu-id="1b696-129">Sets the **SharedSecret** property for this RADIUS server.</span></span><br/>        |
| [<span data-ttu-id="1b696-130">**Update**</span><span class="sxs-lookup"><span data-stu-id="1b696-130">**Update**</span></span>](update-win32-tsgatewayradiusserver.md)                   | <span data-ttu-id="1b696-131">Actualiza el servidor RADIUS actual.</span><span class="sxs-lookup"><span data-stu-id="1b696-131">Updates the current RADIUS server.</span></span><br/>                                |



 

### <a name="properties"></a><span data-ttu-id="1b696-132">Propiedades</span><span class="sxs-lookup"><span data-stu-id="1b696-132">Properties</span></span>

<span data-ttu-id="1b696-133">La **clase \_ TSGatewayRADIUSServer de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="1b696-133">The **Win32\_TSGatewayRADIUSServer** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1b696-134">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="1b696-134">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b696-135">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="1b696-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1b696-136">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1b696-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1b696-137">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="1b696-137">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="1b696-138">Nombre del servidor RADIUS.</span><span class="sxs-lookup"><span data-stu-id="1b696-138">Name of the RADIUS server.</span></span> <span data-ttu-id="1b696-139">Esta propiedad se puede cambiar con el método [**setName**](setname-win32-tsgatewayradiusserver.md) .</span><span class="sxs-lookup"><span data-stu-id="1b696-139">This property can be changed with the [**SetName**](setname-win32-tsgatewayradiusserver.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="1b696-140">**Prioridad**</span><span class="sxs-lookup"><span data-stu-id="1b696-140">**Priority**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b696-141">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1b696-141">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1b696-142">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1b696-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1b696-143">Prioridad del servidor RADIUS.</span><span class="sxs-lookup"><span data-stu-id="1b696-143">Priority of the RADIUS server.</span></span> <span data-ttu-id="1b696-144">El servidor de puerta de enlace de escritorio remoto busca Cap de RD en servidores RADIUS según la prioridad.</span><span class="sxs-lookup"><span data-stu-id="1b696-144">The RD Gateway server looks for RD CAPs on RADIUS servers based on the priority.</span></span> <span data-ttu-id="1b696-145">Esta propiedad se puede cambiar con los métodos [**moveUp**](moveup-win32-tsgatewayradiusserver.md), [**moveDown**](movedown-win32-tsgatewayradiusserver.md), [**Add**](win32-tsgatewayradiusserver-add.md)y [**Remove**](win32-tsgatewayradiusserver-remove.md) .</span><span class="sxs-lookup"><span data-stu-id="1b696-145">This property can be changed with the [**MoveUp**](moveup-win32-tsgatewayradiusserver.md), [**MoveDown**](movedown-win32-tsgatewayradiusserver.md), [**Add**](win32-tsgatewayradiusserver-add.md), and [**Remove**](win32-tsgatewayradiusserver-remove.md) methods.</span></span>

</dd> <dt>

<span data-ttu-id="1b696-146">**SharedSecret**</span><span class="sxs-lookup"><span data-stu-id="1b696-146">**SharedSecret**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1b696-147">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="1b696-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1b696-148">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1b696-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1b696-149">Secreto compartido para el servidor RADIUS.</span><span class="sxs-lookup"><span data-stu-id="1b696-149">Shared secret for the RADIUS server.</span></span> <span data-ttu-id="1b696-150">Esta propiedad se puede cambiar con el método [**SetSharedSecret**](setsharedsecret-win32-tsgatewayradiusserver.md) .</span><span class="sxs-lookup"><span data-stu-id="1b696-150">This property can be changed with the [**SetSharedSecret**](setsharedsecret-win32-tsgatewayradiusserver.md) method.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1b696-151">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1b696-151">Remarks</span></span>

<span data-ttu-id="1b696-152">Para usar esta clase, debe ser miembro del grupo administradores.</span><span class="sxs-lookup"><span data-stu-id="1b696-152">You must be a member of the Administrators group to use this class.</span></span>

<span data-ttu-id="1b696-153">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="1b696-153">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="1b696-154">Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="1b696-154">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="1b696-155">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="1b696-155">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="1b696-156">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="1b696-156">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="1b696-157">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1b696-157">Requirements</span></span>



| <span data-ttu-id="1b696-158">Requisito</span><span class="sxs-lookup"><span data-stu-id="1b696-158">Requirement</span></span> | <span data-ttu-id="1b696-159">Value</span><span class="sxs-lookup"><span data-stu-id="1b696-159">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="1b696-160">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1b696-160">Minimum supported client</span></span><br/> | <span data-ttu-id="1b696-161">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="1b696-161">None supported</span></span><br/>                                                                |
| <span data-ttu-id="1b696-162">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1b696-162">Minimum supported server</span></span><br/> | <span data-ttu-id="1b696-163">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1b696-163">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="1b696-164">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="1b696-164">Namespace</span></span><br/>                | <span data-ttu-id="1b696-165">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="1b696-165">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="1b696-166">MOF</span><span class="sxs-lookup"><span data-stu-id="1b696-166">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1b696-167"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1b696-167"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="1b696-168">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="1b696-168">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1b696-169"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1b696-169"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="1b696-170">Vea también</span><span class="sxs-lookup"><span data-stu-id="1b696-170">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1b696-171">**Win32 \_ TSGatewayConnection**</span><span class="sxs-lookup"><span data-stu-id="1b696-171">**Win32\_TSGatewayConnection**</span></span>](win32-tsgatewayconnection.md)
</dt> <dt>

[<span data-ttu-id="1b696-172">**Win32 \_ TSGatewayConnectionAuthorizationPolicy**</span><span class="sxs-lookup"><span data-stu-id="1b696-172">**Win32\_TSGatewayConnectionAuthorizationPolicy**</span></span>](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> <dt>

[<span data-ttu-id="1b696-173">**Win32 \_ TSGatewayLoadBalancer**</span><span class="sxs-lookup"><span data-stu-id="1b696-173">**Win32\_TSGatewayLoadBalancer**</span></span>](win32-tsgatewayloadbalancer.md)
</dt> <dt>

[<span data-ttu-id="1b696-174">**Win32 \_ TSGatewayResourceAuthorizationPolicy**</span><span class="sxs-lookup"><span data-stu-id="1b696-174">**Win32\_TSGatewayResourceAuthorizationPolicy**</span></span>](win32-tsgatewayresourceauthorizationpolicy.md)
</dt> <dt>

[<span data-ttu-id="1b696-175">**Win32 \_ TSGatewayResourceGroup**</span><span class="sxs-lookup"><span data-stu-id="1b696-175">**Win32\_TSGatewayResourceGroup**</span></span>](win32-tsgatewayresourcegroup.md)
</dt> <dt>

[<span data-ttu-id="1b696-176">**Win32 \_ TSGatewayServerSettings**</span><span class="sxs-lookup"><span data-stu-id="1b696-176">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> </dl>

 

