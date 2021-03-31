---
title: Win32_TSGatewayConnection (clase)
description: Representa una conexión desde un equipo cliente a un servidor de puerta de enlace de Escritorio remoto (puerta de enlace de escritorio remoto).
ms.assetid: 6e76ae25-409d-436a-8eef-8f047194c29c
ms.tgt_platform: multiple
keywords:
- Win32_TSGatewayConnection clase Servicios de Escritorio remoto
- Servicios de Escritorio remoto de Win32_TSGatewayConnection de clase, se describe
topic_type:
- apiref
api_name:
- Win32_TSGatewayConnection
- Win32_TSGatewayConnection.ConnectionKey
- Win32_TSGatewayConnection.TunnelId
- Win32_TSGatewayConnection.ChannelId
- Win32_TSGatewayConnection.UserName
- Win32_TSGatewayConnection.FullUserName
- Win32_TSGatewayConnection.ClientAddress
- Win32_TSGatewayConnection.ConnectedTime
- Win32_TSGatewayConnection.IdleTime
- Win32_TSGatewayConnection.ConnectedResource
- Win32_TSGatewayConnection.ProtocolName
- Win32_TSGatewayConnection.ConnectedPort
- Win32_TSGatewayConnection.NumberOfKilobytesSent
- Win32_TSGatewayConnection.NumberOfKilobytesReceived
- Win32_TSGatewayConnection.ConnectionDuration
- Win32_TSGatewayConnection.TransportProtocol
api_location:
- AagWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6dbaa79213282a70b2f29e6bee9f94901700dddf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104151003"
---
# <a name="win32_tsgatewayconnection-class"></a><span data-ttu-id="65d04-105">\_Clase Win32 TSGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="65d04-105">Win32\_TSGatewayConnection class</span></span>

<span data-ttu-id="65d04-106">Representa una conexión desde un equipo cliente a un servidor de puerta de enlace de Escritorio remoto (puerta de enlace de escritorio remoto).</span><span class="sxs-lookup"><span data-stu-id="65d04-106">Represents a connection from a client computer to a Remote Desktop Gateway (RD Gateway) server.</span></span>

## <a name="syntax"></a><span data-ttu-id="65d04-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="65d04-107">Syntax</span></span>

``` syntax
[dynamic, provider("AAGProvider"), AMENDMENT]
class Win32_TSGatewayConnection
{
  string ConnectionKey;
  uint64 TunnelId;
  uint32 ChannelId;
  string UserName;
  string FullUserName;
  string ClientAddress;
  string ConnectedTime;
  string IdleTime;
  string ConnectedResource;
  string ProtocolName;
  uint32 ConnectedPort;
  uint64 NumberOfKilobytesSent;
  uint64 NumberOfKilobytesReceived;
  string ConnectionDuration;
  uint32 TransportProtocol;
};
```

## <a name="members"></a><span data-ttu-id="65d04-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="65d04-108">Members</span></span>

<span data-ttu-id="65d04-109">La **clase \_ TSGatewayConnection de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="65d04-109">The **Win32\_TSGatewayConnection** class has these types of members:</span></span>

-   [<span data-ttu-id="65d04-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="65d04-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="65d04-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="65d04-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="65d04-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="65d04-112">Methods</span></span>

<span data-ttu-id="65d04-113">La clase **Win32 \_ TSGatewayConnection** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="65d04-113">The **Win32\_TSGatewayConnection** class has these methods.</span></span>



| <span data-ttu-id="65d04-114">Método</span><span class="sxs-lookup"><span data-stu-id="65d04-114">Method</span></span>                                                                     | <span data-ttu-id="65d04-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="65d04-115">Description</span></span>                                                                                                                      |
|:---------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="65d04-116">**CheckStatus**</span><span class="sxs-lookup"><span data-stu-id="65d04-116">**CheckStatus**</span></span>](checkstatus-win32-tsgatewayconnection.md)               | <span data-ttu-id="65d04-117">Comprueba el estado de una conexión de servidor de puerta de enlace de escritorio remoto y si el servidor de destino está configurado para el equilibrio de carga.</span><span class="sxs-lookup"><span data-stu-id="65d04-117">Checks the status of an RD Gateway server connection, and whether the target server is configured for load balancing.</span></span><br/> |
| [<span data-ttu-id="65d04-118">**Desconectar**</span><span class="sxs-lookup"><span data-stu-id="65d04-118">**Disconnect**</span></span>](disconnect-win32-tsgatewayconnection.md)                 | <span data-ttu-id="65d04-119">Finaliza la conexión.</span><span class="sxs-lookup"><span data-stu-id="65d04-119">Ends the connection.</span></span><br/>                                                                                                  |
| [<span data-ttu-id="65d04-120">**DisconnectProtocol**</span><span class="sxs-lookup"><span data-stu-id="65d04-120">**DisconnectProtocol**</span></span>](disconnectprotocol-win32-tsgatewayconnection.md) | <span data-ttu-id="65d04-121">Finaliza todas las conexiones que usan el protocolo especificado.</span><span class="sxs-lookup"><span data-stu-id="65d04-121">Ends all connections that use the specified protocol.</span></span><br/>                                                                 |
| [<span data-ttu-id="65d04-122">**DisconnectUser**</span><span class="sxs-lookup"><span data-stu-id="65d04-122">**DisconnectUser**</span></span>](disconnectuser-win32-tsgatewayconnection.md)         | <span data-ttu-id="65d04-123">Finaliza todas las conexiones del usuario especificado.</span><span class="sxs-lookup"><span data-stu-id="65d04-123">Ends all connections of the specified user.</span></span><br/>                                                                           |



 

### <a name="properties"></a><span data-ttu-id="65d04-124">Propiedades</span><span class="sxs-lookup"><span data-stu-id="65d04-124">Properties</span></span>

<span data-ttu-id="65d04-125">La **clase \_ TSGatewayConnection de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="65d04-125">The **Win32\_TSGatewayConnection** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="65d04-126">**ChannelId**</span><span class="sxs-lookup"><span data-stu-id="65d04-126">**ChannelId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65d04-127">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="65d04-127">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="65d04-128">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="65d04-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="65d04-129">Identificador del canal.</span><span class="sxs-lookup"><span data-stu-id="65d04-129">Channel identifier.</span></span>

</dd> <dt>

<span data-ttu-id="65d04-130">**ClientAddress**</span><span class="sxs-lookup"><span data-stu-id="65d04-130">**ClientAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65d04-131">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="65d04-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="65d04-132">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="65d04-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="65d04-133">Dirección IP del cliente.</span><span class="sxs-lookup"><span data-stu-id="65d04-133">Client IP address.</span></span>

</dd> <dt>

<span data-ttu-id="65d04-134">**ConnectedPort**</span><span class="sxs-lookup"><span data-stu-id="65d04-134">**ConnectedPort**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65d04-135">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="65d04-135">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="65d04-136">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="65d04-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="65d04-137">Puerto del recurso conectado al que está conectado el usuario.</span><span class="sxs-lookup"><span data-stu-id="65d04-137">Port on the connected resource to which the user is connected.</span></span>

</dd> <dt>

<span data-ttu-id="65d04-138">**ConnectedResource**</span><span class="sxs-lookup"><span data-stu-id="65d04-138">**ConnectedResource**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65d04-139">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="65d04-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="65d04-140">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="65d04-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="65d04-141">Nombre del equipo (o clúster) al que está conectado el cliente.</span><span class="sxs-lookup"><span data-stu-id="65d04-141">Name of the computer (or cluster) to which the client is connected.</span></span>

</dd> <dt>

<span data-ttu-id="65d04-142">**ConnectedTime**</span><span class="sxs-lookup"><span data-stu-id="65d04-142">**ConnectedTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65d04-143">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="65d04-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="65d04-144">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="65d04-144">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="65d04-145">Marca de tiempo para el momento en que se estableció la conexión.</span><span class="sxs-lookup"><span data-stu-id="65d04-145">The time stamp for when the connection was established.</span></span> <span data-ttu-id="65d04-146">Esta vez se restablece cuando se restablece la conexión, incluso si se vuelve a conectar automáticamente.</span><span class="sxs-lookup"><span data-stu-id="65d04-146">This time is reset when the connection is reset, even if it is automatically reconnected.</span></span>

</dd> <dt>

<span data-ttu-id="65d04-147">**ConnectionDuration**</span><span class="sxs-lookup"><span data-stu-id="65d04-147">**ConnectionDuration**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65d04-148">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="65d04-148">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="65d04-149">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="65d04-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="65d04-150">Tiempo transcurrido desde la hora de conexión.</span><span class="sxs-lookup"><span data-stu-id="65d04-150">The time that has elapsed since the connected time.</span></span>

</dd> <dt>

<span data-ttu-id="65d04-151">**ConnectionKey**</span><span class="sxs-lookup"><span data-stu-id="65d04-151">**ConnectionKey**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65d04-152">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="65d04-152">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="65d04-153">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="65d04-153">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="65d04-154">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="65d04-154">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="65d04-155">Identificador de conexión en el formato "tunnelId: channelID".</span><span class="sxs-lookup"><span data-stu-id="65d04-155">Connection identifier in the format "tunnelId:channelID".</span></span>

</dd> <dt>

<span data-ttu-id="65d04-156">**FullUserName**</span><span class="sxs-lookup"><span data-stu-id="65d04-156">**FullUserName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65d04-157">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="65d04-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="65d04-158">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="65d04-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="65d04-159">Nombre de usuario completo del usuario conectado.</span><span class="sxs-lookup"><span data-stu-id="65d04-159">Full user name of the connected user.</span></span>

</dd> <dt>

<span data-ttu-id="65d04-160">**Tiempo de inactividad**</span><span class="sxs-lookup"><span data-stu-id="65d04-160">**IdleTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65d04-161">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="65d04-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="65d04-162">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="65d04-162">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="65d04-163">Tiempo de inactividad de la conexión.</span><span class="sxs-lookup"><span data-stu-id="65d04-163">Idle time of the connection.</span></span>

</dd> <dt>

<span data-ttu-id="65d04-164">**NumberOfKilobytesReceived**</span><span class="sxs-lookup"><span data-stu-id="65d04-164">**NumberOfKilobytesReceived**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65d04-165">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="65d04-165">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="65d04-166">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="65d04-166">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="65d04-167">Número de kilobytes recibidos desde el equipo cliente por el servidor de puerta de enlace de escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="65d04-167">Number of kilobytes received from the client computer by the RD Gateway server.</span></span>

</dd> <dt>

<span data-ttu-id="65d04-168">**NumberOfKilobytesSent**</span><span class="sxs-lookup"><span data-stu-id="65d04-168">**NumberOfKilobytesSent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65d04-169">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="65d04-169">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="65d04-170">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="65d04-170">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="65d04-171">Número de kilobytes enviados al equipo cliente por el servidor de puerta de enlace de escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="65d04-171">Number of kilobytes sent to the client computer by the RD Gateway server.</span></span>

</dd> <dt>

<span data-ttu-id="65d04-172">**ProtocolName**</span><span class="sxs-lookup"><span data-stu-id="65d04-172">**ProtocolName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65d04-173">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="65d04-173">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="65d04-174">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="65d04-174">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="65d04-175">Protocolo que se usa para conectarse al servidor de puerta de enlace de escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="65d04-175">Protocol that is used to connect to the RD Gateway server.</span></span>

<dt>

<span data-ttu-id="65d04-176">RDP</span><span class="sxs-lookup"><span data-stu-id="65d04-176">"RDP"</span></span>
</dt> <dd>

<span data-ttu-id="65d04-177">El protocolo para el servidor de puerta de enlace de escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="65d04-177">The protocol for the RD Gateway server.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="65d04-178">**TransportProtocol**</span><span class="sxs-lookup"><span data-stu-id="65d04-178">**TransportProtocol**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65d04-179">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="65d04-179">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="65d04-180">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="65d04-180">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="65d04-181">Especifica el tipo de transporte para la conexión.</span><span class="sxs-lookup"><span data-stu-id="65d04-181">Specifies the transport type for the connection.</span></span> <span data-ttu-id="65d04-182">Debe ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="65d04-182">This must be one of the following values.</span></span>

<dt>

<span data-ttu-id="65d04-183">0</span><span class="sxs-lookup"><span data-stu-id="65d04-183">0</span></span>
</dt> <dd>

<span data-ttu-id="65d04-184">Transporte RPC a través de HTTP.</span><span class="sxs-lookup"><span data-stu-id="65d04-184">RPC over HTTP transport.</span></span>

</dd> <dt>

<span data-ttu-id="65d04-185">1</span><span class="sxs-lookup"><span data-stu-id="65d04-185">1</span></span>
</dt> <dd>

<span data-ttu-id="65d04-186">Transporte HTTP.</span><span class="sxs-lookup"><span data-stu-id="65d04-186">HTTP transport.</span></span>

</dd> <dt>

<span data-ttu-id="65d04-187">2</span><span class="sxs-lookup"><span data-stu-id="65d04-187">2</span></span>
</dt> <dd>

<span data-ttu-id="65d04-188">Transporte UDP.</span><span class="sxs-lookup"><span data-stu-id="65d04-188">UDP transport.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="65d04-189">**TunnelId**</span><span class="sxs-lookup"><span data-stu-id="65d04-189">**TunnelId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65d04-190">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="65d04-190">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="65d04-191">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="65d04-191">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="65d04-192">Identificador de túnel.</span><span class="sxs-lookup"><span data-stu-id="65d04-192">Tunnel identifier.</span></span>

</dd> <dt>

<span data-ttu-id="65d04-193">**UserName**</span><span class="sxs-lookup"><span data-stu-id="65d04-193">**UserName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="65d04-194">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="65d04-194">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="65d04-195">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="65d04-195">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="65d04-196">Nombre de usuario conectado al servidor de puerta de enlace de escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="65d04-196">User name connected to the RD Gateway server.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="65d04-197">Observaciones</span><span class="sxs-lookup"><span data-stu-id="65d04-197">Remarks</span></span>

<span data-ttu-id="65d04-198">Para usar esta clase, debe ser miembro del grupo administradores.</span><span class="sxs-lookup"><span data-stu-id="65d04-198">You must be a member of the Administrators group to use this class.</span></span>

<span data-ttu-id="65d04-199">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="65d04-199">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="65d04-200">Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="65d04-200">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="65d04-201">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="65d04-201">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="65d04-202">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="65d04-202">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="65d04-203">Requisitos</span><span class="sxs-lookup"><span data-stu-id="65d04-203">Requirements</span></span>



| <span data-ttu-id="65d04-204">Requisito</span><span class="sxs-lookup"><span data-stu-id="65d04-204">Requirement</span></span> | <span data-ttu-id="65d04-205">Value</span><span class="sxs-lookup"><span data-stu-id="65d04-205">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="65d04-206">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="65d04-206">Minimum supported client</span></span><br/> | <span data-ttu-id="65d04-207">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="65d04-207">None supported</span></span><br/>                                                                |
| <span data-ttu-id="65d04-208">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="65d04-208">Minimum supported server</span></span><br/> | <span data-ttu-id="65d04-209">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="65d04-209">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="65d04-210">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="65d04-210">Namespace</span></span><br/>                | <span data-ttu-id="65d04-211">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="65d04-211">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="65d04-212">MOF</span><span class="sxs-lookup"><span data-stu-id="65d04-212">MOF</span></span><br/>                      | <dl> <span data-ttu-id="65d04-213"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="65d04-213"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="65d04-214">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="65d04-214">DLL</span></span><br/>                      | <dl> <span data-ttu-id="65d04-215"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="65d04-215"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="65d04-216">Vea también</span><span class="sxs-lookup"><span data-stu-id="65d04-216">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65d04-217">**Win32 \_ TSGatewayConnectionAuthorizationPolicy**</span><span class="sxs-lookup"><span data-stu-id="65d04-217">**Win32\_TSGatewayConnectionAuthorizationPolicy**</span></span>](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> <dt>

[<span data-ttu-id="65d04-218">**Win32 \_ TSGatewayLoadBalancer**</span><span class="sxs-lookup"><span data-stu-id="65d04-218">**Win32\_TSGatewayLoadBalancer**</span></span>](win32-tsgatewayloadbalancer.md)
</dt> <dt>

[<span data-ttu-id="65d04-219">**Win32 \_ TSGatewayRADIUSServer**</span><span class="sxs-lookup"><span data-stu-id="65d04-219">**Win32\_TSGatewayRADIUSServer**</span></span>](win32-tsgatewayradiusserver.md)
</dt> <dt>

[<span data-ttu-id="65d04-220">**Win32 \_ TSGatewayResourceAuthorizationPolicy**</span><span class="sxs-lookup"><span data-stu-id="65d04-220">**Win32\_TSGatewayResourceAuthorizationPolicy**</span></span>](win32-tsgatewayresourceauthorizationpolicy.md)
</dt> <dt>

[<span data-ttu-id="65d04-221">**Win32 \_ TSGatewayResourceGroup**</span><span class="sxs-lookup"><span data-stu-id="65d04-221">**Win32\_TSGatewayResourceGroup**</span></span>](win32-tsgatewayresourcegroup.md)
</dt> <dt>

[<span data-ttu-id="65d04-222">**Win32 \_ TSGatewayServerSettings**</span><span class="sxs-lookup"><span data-stu-id="65d04-222">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> </dl>

 

