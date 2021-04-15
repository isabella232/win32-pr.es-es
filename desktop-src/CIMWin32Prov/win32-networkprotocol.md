---
description: Win32 \_ NetworkProtocol&\# 8194; La clase WMI representa un protocolo y sus características de red en un sistema de Win32.
ms.assetid: c864a694-d507-4629-91c5-bd26ccf397f7
ms.tgt_platform: multiple
title: Win32_NetworkProtocol (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkProtocol
- Win32_NetworkProtocol.Caption
- Win32_NetworkProtocol.Description
- Win32_NetworkProtocol.InstallDate
- Win32_NetworkProtocol.Status
- Win32_NetworkProtocol.ConnectionlessService
- Win32_NetworkProtocol.GuaranteesDelivery
- Win32_NetworkProtocol.GuaranteesSequencing
- Win32_NetworkProtocol.MaximumAddressSize
- Win32_NetworkProtocol.MaximumMessageSize
- Win32_NetworkProtocol.MessageOriented
- Win32_NetworkProtocol.MinimumAddressSize
- Win32_NetworkProtocol.Name
- Win32_NetworkProtocol.PseudoStreamOriented
- Win32_NetworkProtocol.SupportsBroadcasting
- Win32_NetworkProtocol.SupportsConnectData
- Win32_NetworkProtocol.SupportsDisconnectData
- Win32_NetworkProtocol.SupportsEncryption
- Win32_NetworkProtocol.SupportsExpeditedData
- Win32_NetworkProtocol.SupportsFragmentation
- Win32_NetworkProtocol.SupportsGracefulClosing
- Win32_NetworkProtocol.SupportsGuaranteedBandwidth
- Win32_NetworkProtocol.SupportsMulticasting
- Win32_NetworkProtocol.SupportsQualityofService
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 33817fa4aa55747ecf9d4e89f5dcf406160c0c67
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496595"
---
# <a name="win32_networkprotocol-class"></a><span data-ttu-id="237c5-103">\_Clase Win32 NetworkProtocol</span><span class="sxs-lookup"><span data-stu-id="237c5-103">Win32\_NetworkProtocol class</span></span>

<span data-ttu-id="237c5-104">La  [clase WMI](../wmisdk/retrieving-a-class.md) **\_ NetworkProtocol de Win32** representa un protocolo y sus características de red en un sistema de Win32.</span><span class="sxs-lookup"><span data-stu-id="237c5-104">The **Win32\_NetworkProtocol** [WMI class](../wmisdk/retrieving-a-class.md) represents a protocol and its network characteristics on a Win32 computer system.</span></span>

<span data-ttu-id="237c5-105">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="237c5-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="237c5-106">Las propiedades y los métodos están en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="237c5-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="237c5-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="237c5-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4D8-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_NetworkProtocol : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Status;
  boolean  ConnectionlessService;
  boolean  GuaranteesDelivery;
  boolean  GuaranteesSequencing;
  uint32   MaximumAddressSize;
  uint32   MaximumMessageSize;
  boolean  MessageOriented;
  uint32   MinimumAddressSize;
  string   Name;
  boolean  PseudoStreamOriented;
  boolean  SupportsBroadcasting;
  boolean  SupportsConnectData;
  boolean  SupportsDisconnectData;
  boolean  SupportsEncryption;
  boolean  SupportsExpeditedData;
  boolean  SupportsFragmentation;
  boolean  SupportsGracefulClosing;
  boolean  SupportsGuaranteedBandwidth;
  boolean  SupportsMulticasting;
  boolean  SupportsQualityofService;
};
```

## <a name="members"></a><span data-ttu-id="237c5-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="237c5-108">Members</span></span>

<span data-ttu-id="237c5-109">La **clase \_ NetworkProtocol de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="237c5-109">The **Win32\_NetworkProtocol** class has these types of members:</span></span>

-   [<span data-ttu-id="237c5-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="237c5-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="237c5-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="237c5-111">Properties</span></span>

<span data-ttu-id="237c5-112">La **clase \_ NetworkProtocol de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="237c5-112">The **Win32\_NetworkProtocol** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="237c5-113">**Caption**</span><span class="sxs-lookup"><span data-stu-id="237c5-113">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="237c5-114">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="237c5-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="237c5-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="237c5-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="237c5-116">Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**displayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="237c5-116">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="237c5-117">Breve descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="237c5-117">A short textual description of the object.</span></span>

<span data-ttu-id="237c5-118">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="237c5-118">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="237c5-119">**ConnectionlessService**</span><span class="sxs-lookup"><span data-stu-id="237c5-119">**ConnectionlessService**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="237c5-120">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="237c5-120">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="237c5-121">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="237c5-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="237c5-122">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("API de Win32 \_ \| Windows Sockets Structs \| información de protocolo \_ \| dwServiceFlags \| XP1 \_ sin conexión")</span><span class="sxs-lookup"><span data-stu-id="237c5-122">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32\_API\|Windows Sockets Structures\|PROTOCOL\_INFO\|dwServiceFlags\|XP1\_CONNECTIONLESS")</span></span>
</dt> </dl>

<span data-ttu-id="237c5-123">El protocolo admite el servicio sin conexión.</span><span class="sxs-lookup"><span data-stu-id="237c5-123">Protocol supports connectionless service.</span></span> <span data-ttu-id="237c5-124">Un servicio sin conexión (datagrama) describe un protocolo de comunicaciones o transporte en el que los paquetes de datos se enrutan de forma independiente entre sí y pueden seguir rutas diferentes y llegar en un orden diferente al que se enviaron.</span><span class="sxs-lookup"><span data-stu-id="237c5-124">A connectionless (datagram) service describes a communications protocol or transport in which data packets are routed independently of each other and may follow different routes and arrive in a different order from that in which they were sent.</span></span> <span data-ttu-id="237c5-125">Por el contrario, un servicio orientado a la conexión proporciona un circuito virtual a través del cual los paquetes de datos se reciben en el mismo orden en que se transmitiron.</span><span class="sxs-lookup"><span data-stu-id="237c5-125">Conversely, a connection-oriented service provides a virtual circuit through which data packets are received in the same order they were transmitted.</span></span> <span data-ttu-id="237c5-126">Si se produce un error en la conexión entre equipos, se notifica a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="237c5-126">If the connection between computers fails, the application is notified.</span></span>

</dd> <dt>

<span data-ttu-id="237c5-127">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="237c5-127">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="237c5-128">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="237c5-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="237c5-129">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="237c5-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="237c5-130">Calificadores: [**displayName**](../wmisdk/standard-qualifiers.md) ("Descripción")</span><span class="sxs-lookup"><span data-stu-id="237c5-130">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="237c5-131">Una descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="237c5-131">A textual description of the object.</span></span>

<span data-ttu-id="237c5-132">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="237c5-132">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="237c5-133">**GuaranteesDelivery**</span><span class="sxs-lookup"><span data-stu-id="237c5-133">**GuaranteesDelivery**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="237c5-134">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="237c5-134">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="237c5-135">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="237c5-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="237c5-136">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("API de Win32 \_ \| Windows Sockets Structs \| información de protocolo \_ \| dwServiceFlags \| XP \_ entrega garantizada \_ ")</span><span class="sxs-lookup"><span data-stu-id="237c5-136">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32\_API\|Windows Sockets Structures\|PROTOCOL\_INFO\|dwServiceFlags\|XP\_GUARANTEED\_DELIVERY")</span></span>
</dt> </dl>

<span data-ttu-id="237c5-137">El protocolo admite la entrega de paquetes de datos.</span><span class="sxs-lookup"><span data-stu-id="237c5-137">Protocol supports delivery of data packets.</span></span> <span data-ttu-id="237c5-138">Si esta marca es **false**, no está seguro de que todos los datos enviados llegarán al destino previsto.</span><span class="sxs-lookup"><span data-stu-id="237c5-138">If this flag is **FALSE**, it is uncertain that all of the data sent will reach the intended destination.</span></span>

</dd> <dt>

<span data-ttu-id="237c5-139">**GuaranteesSequencing**</span><span class="sxs-lookup"><span data-stu-id="237c5-139">**GuaranteesSequencing**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="237c5-140">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="237c5-140">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="237c5-141">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="237c5-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="237c5-142">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \_ API Win32 \| Windows Sockets Structures \| Protocolo \_ info \| dwServiceFlags \| XP \_ \_ orden garantizado")</span><span class="sxs-lookup"><span data-stu-id="237c5-142">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32\_API\|Windows Sockets Structures\|PROTOCOL\_INFO\|dwServiceFlags\|XP\_GUARANTEED\_ORDER")</span></span>
</dt> </dl>

<span data-ttu-id="237c5-143">El protocolo garantiza que los datos llegarán en el orden en que se enviaron.</span><span class="sxs-lookup"><span data-stu-id="237c5-143">Protocol ensures that data will arrive in the order in which it was sent.</span></span> <span data-ttu-id="237c5-144">Tenga en cuenta que esta característica no garantiza la entrega de los datos, solo su orden.</span><span class="sxs-lookup"><span data-stu-id="237c5-144">Be aware that this characteristic does not ensure delivery of the data, only its order.</span></span>

</dd> <dt>

<span data-ttu-id="237c5-145">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="237c5-145">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="237c5-146">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="237c5-146">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="237c5-147">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="237c5-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="237c5-148">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| ComponentID \| 001,5 "), [**displayName**](../wmisdk/standard-qualifiers.md) (" instalación de fecha ")</span><span class="sxs-lookup"><span data-stu-id="237c5-148">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="237c5-149">Indica cuándo se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="237c5-149">Indicates when the object was installed.</span></span> <span data-ttu-id="237c5-150">La falta de un valor no indica que el objeto no está instalado.</span><span class="sxs-lookup"><span data-stu-id="237c5-150">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="237c5-151">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="237c5-151">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="237c5-152">**MaximumAddressSize**</span><span class="sxs-lookup"><span data-stu-id="237c5-152">**MaximumAddressSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="237c5-153">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="237c5-153">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="237c5-154">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="237c5-154">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="237c5-155">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32 \_ API \| Windows Sockets Structures \| Protocol \_ info \| iMaxSockAddr"), [**unidades**](../wmisdk/standard-qualifiers.md) ("caracteres")</span><span class="sxs-lookup"><span data-stu-id="237c5-155">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32\_API\|Windows Sockets Structures\|PROTOCOL\_INFO\|iMaxSockAddr"), [**units**](../wmisdk/standard-qualifiers.md) ("characters")</span></span>
</dt> </dl>

<span data-ttu-id="237c5-156">Longitud máxima de una dirección de socket compatible con el protocolo.</span><span class="sxs-lookup"><span data-stu-id="237c5-156">Maximum length of a socket address supported by the protocol.</span></span> <span data-ttu-id="237c5-157">Las direcciones de socket pueden ser elementos como una dirección URL ( `www.microsoft.com` ) o una dirección IP ( `130.215.24.1` ).</span><span class="sxs-lookup"><span data-stu-id="237c5-157">Socket addresses may be items such as a URL (`www.microsoft.com`) or an IP address (`130.215.24.1`).</span></span>

</dd> <dt>

<span data-ttu-id="237c5-158">**MaximumMessageSize**</span><span class="sxs-lookup"><span data-stu-id="237c5-158">**MaximumMessageSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="237c5-159">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="237c5-159">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="237c5-160">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="237c5-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="237c5-161">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32 \_ API \| Windows Sockets Structures \| Protocol \_ info \| dwMessageSize"), [**unidades**](../wmisdk/standard-qualifiers.md) ("caracteres")</span><span class="sxs-lookup"><span data-stu-id="237c5-161">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32\_API\|Windows Sockets Structures\|PROTOCOL\_INFO\|dwMessageSize"), [**units**](../wmisdk/standard-qualifiers.md) ("characters")</span></span>
</dt> </dl>

<span data-ttu-id="237c5-162">Tamaño máximo de mensaje admitido por el protocolo.</span><span class="sxs-lookup"><span data-stu-id="237c5-162">Maximum message size supported by the protocol.</span></span> <span data-ttu-id="237c5-163">Es el tamaño máximo de un mensaje que puede ser enviado o recibido por el host.</span><span class="sxs-lookup"><span data-stu-id="237c5-163">This is the maximum size of a message that can be sent from or received by the host.</span></span> <span data-ttu-id="237c5-164">En el caso de los protocolos que no admiten tramas de mensajes, el tamaño máximo real de un mensaje que se puede enviar a una dirección determinada puede ser inferior a este valor.</span><span class="sxs-lookup"><span data-stu-id="237c5-164">For protocols that do not support message framing, the actual maximum size of a message that can be sent to a given address may be less than this value.</span></span>

</dd> <dt>

<span data-ttu-id="237c5-165">**MessageOriented**</span><span class="sxs-lookup"><span data-stu-id="237c5-165">**MessageOriented**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="237c5-166">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="237c5-166">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="237c5-167">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="237c5-167">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="237c5-168">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("API de Win32 \_ \| Windows Sockets Structs \| información de protocolo \_ \| dwServiceFlags \| XP \_ Message \_ orientada")</span><span class="sxs-lookup"><span data-stu-id="237c5-168">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32\_API\|Windows Sockets Structures\|PROTOCOL\_INFO\|dwServiceFlags\|XP\_MESSAGE\_ORIENTED")</span></span>
</dt> </dl>

<span data-ttu-id="237c5-169">El protocolo está orientado a mensajes.</span><span class="sxs-lookup"><span data-stu-id="237c5-169">Protocol is message-oriented.</span></span> <span data-ttu-id="237c5-170">Un protocolo orientado a mensajes usa paquetes de datos para transferir información.</span><span class="sxs-lookup"><span data-stu-id="237c5-170">A message-oriented protocol uses packets of data to transfer information.</span></span> <span data-ttu-id="237c5-171">Por el contrario, los protocolos orientados a flujos transfieren los datos como una secuencia continua de bytes.</span><span class="sxs-lookup"><span data-stu-id="237c5-171">Conversely, stream-oriented protocols transfer data as a continuous stream of bytes.</span></span>

</dd> <dt>

<span data-ttu-id="237c5-172">**MinimumAddressSize**</span><span class="sxs-lookup"><span data-stu-id="237c5-172">**MinimumAddressSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="237c5-173">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="237c5-173">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="237c5-174">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="237c5-174">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="237c5-175">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32 \_ API \| Windows Sockets Structures \| Protocol \_ info \| iMinSockAddr"), [**unidades**](../wmisdk/standard-qualifiers.md) ("caracteres")</span><span class="sxs-lookup"><span data-stu-id="237c5-175">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32\_API\|Windows Sockets Structures\|PROTOCOL\_INFO\|iMinSockAddr "), [**units**](../wmisdk/standard-qualifiers.md) ("characters")</span></span>
</dt> </dl>

<span data-ttu-id="237c5-176">Longitud mínima de una dirección de socket compatible con el protocolo.</span><span class="sxs-lookup"><span data-stu-id="237c5-176">Minimum length of a socket address supported by the protocol.</span></span>

</dd> <dt>

<span data-ttu-id="237c5-177">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="237c5-177">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="237c5-178">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="237c5-178">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="237c5-179">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="237c5-179">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="237c5-180">Calificadores: [**clave**](../wmisdk/key-qualifier.md), [**invalidación**](../wmisdk/standard-qualifiers.md) ("Name"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \_ API de Win32 \| Windows Sockets de la información de \| Protocolo \_ \| lpProtocol")</span><span class="sxs-lookup"><span data-stu-id="237c5-180">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Name"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32\_API\|Windows Sockets Structures\|PROTOCOL\_INFO\|lpProtocol")</span></span>
</dt> </dl>

<span data-ttu-id="237c5-181">Nombre del protocolo.</span><span class="sxs-lookup"><span data-stu-id="237c5-181">Name for the protocol.</span></span>

<span data-ttu-id="237c5-182">Ejemplo: "TCP/IP"</span><span class="sxs-lookup"><span data-stu-id="237c5-182">Example: "TCP/IP"</span></span>

</dd> <dt>

<span data-ttu-id="237c5-183">**PseudoStreamOriented**</span><span class="sxs-lookup"><span data-stu-id="237c5-183">**PseudoStreamOriented**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="237c5-184">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="237c5-184">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="237c5-185">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="237c5-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="237c5-186">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32 \_ API \| Windows Sockets Structures \| Protocolo \_ info \| dwServiceFlags \| XP \_ pseudo \_ Stream")</span><span class="sxs-lookup"><span data-stu-id="237c5-186">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32\_API\|Windows Sockets Structures\|PROTOCOL\_INFO\|dwServiceFlags\|XP\_PSEUDO\_STREAM")</span></span>
</dt> </dl>

<span data-ttu-id="237c5-187">Es un protocolo orientado a mensajes que puede recibir paquetes de datos de longitud variable o datos transmitidos para todas las operaciones de recepción.</span><span class="sxs-lookup"><span data-stu-id="237c5-187">Protocol is a message-oriented protocol that can receive variable-length data packets or streamed data for all receive operations.</span></span> <span data-ttu-id="237c5-188">Esta capacidad opcional es útil cuando una aplicación no desea que el protocolo contenga el marco de mensajes y requiere características orientadas a flujos.</span><span class="sxs-lookup"><span data-stu-id="237c5-188">This optional ability is useful when an application does not want the protocol to frame messages, and requires stream-oriented characteristics.</span></span> <span data-ttu-id="237c5-189">Si es **true**, el protocolo está orientado a pseudo streaming.</span><span class="sxs-lookup"><span data-stu-id="237c5-189">If **TRUE**, the protocol is pseudo stream-oriented.</span></span>

</dd> <dt>

<span data-ttu-id="237c5-190">**Estado**</span><span class="sxs-lookup"><span data-stu-id="237c5-190">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="237c5-191">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="237c5-191">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="237c5-192">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="237c5-192">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="237c5-193">Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**displayName**](../wmisdk/standard-qualifiers.md) ("status")</span><span class="sxs-lookup"><span data-stu-id="237c5-193">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="237c5-194">Cadena que indica el estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="237c5-194">String that indicates the current status of the object.</span></span> <span data-ttu-id="237c5-195">Se puede definir un estado operativo y no operativo.</span><span class="sxs-lookup"><span data-stu-id="237c5-195">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="237c5-196">El estado operativo puede ser "correcto", "degradado" y "Pred FAIL".</span><span class="sxs-lookup"><span data-stu-id="237c5-196">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="237c5-197">"Pred FAIL" indica que un elemento funciona correctamente, pero está prediciendo un error (por ejemplo, una unidad de disco duro habilitada para SMART).</span><span class="sxs-lookup"><span data-stu-id="237c5-197">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="237c5-198">El estado no operativo puede incluir "error", "iniciando", "deteniendo" y "servicio".</span><span class="sxs-lookup"><span data-stu-id="237c5-198">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="237c5-199">"Servicio" puede aplicarse durante el reflejo del disco: Resilvering, recarga de una lista de permisos de usuario u otro trabajo administrativo.</span><span class="sxs-lookup"><span data-stu-id="237c5-199">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="237c5-200">No todo el trabajo está en línea, pero el elemento administrado no es "OK" ni en ninguno de los otros Estados.</span><span class="sxs-lookup"><span data-stu-id="237c5-200">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="237c5-201">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="237c5-201">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="237c5-202">Los valores son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="237c5-202">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="237c5-203">**Aceptar** ("Aceptar")</span><span class="sxs-lookup"><span data-stu-id="237c5-203">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="237c5-204">**Error** ("error")</span><span class="sxs-lookup"><span data-stu-id="237c5-204">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="237c5-205">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="237c5-205">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="237c5-206">**Desconocido** ("desconocido")</span><span class="sxs-lookup"><span data-stu-id="237c5-206">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="237c5-207">**Pred FAIL** ("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="237c5-207">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="237c5-208">**Iniciando** ("iniciando")</span><span class="sxs-lookup"><span data-stu-id="237c5-208">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="237c5-209">**Detener** ("detener")</span><span class="sxs-lookup"><span data-stu-id="237c5-209">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="237c5-210">**Servicio** ("servicio")</span><span class="sxs-lookup"><span data-stu-id="237c5-210">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="237c5-211">Con **estrés** ("acentuado")</span><span class="sxs-lookup"><span data-stu-id="237c5-211">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="237c5-212">**Recover** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="237c5-212">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="237c5-213">**Sin contacto** ("sin contacto")</span><span class="sxs-lookup"><span data-stu-id="237c5-213">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="237c5-214">**Comunicación perdida** ("pérdida de comunicación")</span><span class="sxs-lookup"><span data-stu-id="237c5-214">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="237c5-215">**SupportsBroadcasting**</span><span class="sxs-lookup"><span data-stu-id="237c5-215">**SupportsBroadcasting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="237c5-216">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="237c5-216">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="237c5-217">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="237c5-217">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="237c5-218">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32 \_ API \| Windows Sockets Structures \| Protocol \_ info \| dwServiceFlags \| XP \_ Supports \_ ")</span><span class="sxs-lookup"><span data-stu-id="237c5-218">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32\_API\|Windows Sockets Structures\|PROTOCOL\_INFO\|dwServiceFlags\|XP\_SUPPORTS\_BROADCAST")</span></span>
</dt> </dl>

<span data-ttu-id="237c5-219">El protocolo admite un mecanismo para difundir mensajes a través de la red.</span><span class="sxs-lookup"><span data-stu-id="237c5-219">Protocol supports a mechanism for broadcasting messages across the network.</span></span>

</dd> <dt>

<span data-ttu-id="237c5-220">**SupportsConnectData**</span><span class="sxs-lookup"><span data-stu-id="237c5-220">**SupportsConnectData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="237c5-221">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="237c5-221">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="237c5-222">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="237c5-222">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="237c5-223">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32 \_ API \| Windows Sockets Structures \| Protocolo \_ info \| dwServiceFlags \| XP \_ Connect \_ Data")</span><span class="sxs-lookup"><span data-stu-id="237c5-223">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32\_API\|Windows Sockets Structures\|PROTOCOL\_INFO\|dwServiceFlags\|XP\_CONNECT\_DATA")</span></span>
</dt> </dl>

<span data-ttu-id="237c5-224">El protocolo permite que los datos se conecten a través de la red.</span><span class="sxs-lookup"><span data-stu-id="237c5-224">Protocol allows data to be connected across the network.</span></span>

</dd> <dt>

<span data-ttu-id="237c5-225">**SupportsDisconnectData**</span><span class="sxs-lookup"><span data-stu-id="237c5-225">**SupportsDisconnectData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="237c5-226">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="237c5-226">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="237c5-227">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="237c5-227">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="237c5-228">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("API de Win32 \_ \| Windows Sockets Structs \| información de protocolo \_ \| dwServiceFlags \| XP \_ Disconnect \_ Data")</span><span class="sxs-lookup"><span data-stu-id="237c5-228">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32\_API\|Windows Sockets Structures\|PROTOCOL\_INFO\|dwServiceFlags\|XP\_DISCONNECT\_DATA")</span></span>
</dt> </dl>

<span data-ttu-id="237c5-229">El protocolo permite que los datos se desconecten a través de la red.</span><span class="sxs-lookup"><span data-stu-id="237c5-229">Protocol allows data to be disconnected across the network.</span></span>

</dd> <dt>

<span data-ttu-id="237c5-230">**SupportsEncryption**</span><span class="sxs-lookup"><span data-stu-id="237c5-230">**SupportsEncryption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="237c5-231">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="237c5-231">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="237c5-232">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="237c5-232">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="237c5-233">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("API de Win32 de \_ \| Windows Sockets Structs \| información de protocolo \_ \| dwServiceFlags \| XP \_ cifrado")</span><span class="sxs-lookup"><span data-stu-id="237c5-233">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32\_API\|Windows Sockets Structures\|PROTOCOL\_INFO\|dwServiceFlags\|XP\_ENCRYPTS")</span></span>
</dt> </dl>

<span data-ttu-id="237c5-234">El protocolo admite el cifrado de datos.</span><span class="sxs-lookup"><span data-stu-id="237c5-234">Protocol supports data encryption.</span></span>

</dd> <dt>

<span data-ttu-id="237c5-235">**SupportsExpeditedData**</span><span class="sxs-lookup"><span data-stu-id="237c5-235">**SupportsExpeditedData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="237c5-236">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="237c5-236">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="237c5-237">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="237c5-237">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="237c5-238">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \_ API Win32 \| Windows Sockets Structs \| información de protocolo \_ \| dwServiceFlags \| XP \_ datos acelerados \_ ")</span><span class="sxs-lookup"><span data-stu-id="237c5-238">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32\_API\|Windows Sockets Structures\|PROTOCOL\_INFO\|dwServiceFlags\|XP\_EXPEDITED\_DATA")</span></span>
</dt> </dl>

<span data-ttu-id="237c5-239">El protocolo admite datos inmediatos (también conocidos como datos urgentes) a través de la red.</span><span class="sxs-lookup"><span data-stu-id="237c5-239">Protocol supports expedited data (also known as urgent data) across the network.</span></span> <span data-ttu-id="237c5-240">Los datos expedidos pueden omitir el control de flujo y recibir prioridad sobre los paquetes de datos normales.</span><span class="sxs-lookup"><span data-stu-id="237c5-240">Expedited data can bypass flow control and receive priority over normal data packets.</span></span>

</dd> <dt>

<span data-ttu-id="237c5-241">**SupportsFragmentation**</span><span class="sxs-lookup"><span data-stu-id="237c5-241">**SupportsFragmentation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="237c5-242">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="237c5-242">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="237c5-243">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="237c5-243">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="237c5-244">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \_ API Win32 \| Windows Sockets Structs \| información de protocolo \_ \| dwServiceFlags \| fragmentación de XP \_ ")</span><span class="sxs-lookup"><span data-stu-id="237c5-244">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32\_API\|Windows Sockets Structures\|PROTOCOL\_INFO\|dwServiceFlags\|XP\_FRAGMENTATION")</span></span>
</dt> </dl>

<span data-ttu-id="237c5-245">El protocolo admite la transmisión de los datos en fragmentos.</span><span class="sxs-lookup"><span data-stu-id="237c5-245">Protocol supports transmitting the data in fragments.</span></span> <span data-ttu-id="237c5-246">La unidad de transferencia máxima (MTU) de red física está oculta en las aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="237c5-246">Physical network maximum transfer unit (MTU) is hidden from applications.</span></span> <span data-ttu-id="237c5-247">Cada tipo de medio tiene un tamaño de fotograma máximo que no se puede superar.</span><span class="sxs-lookup"><span data-stu-id="237c5-247">Each media type has a maximum frame size that cannot be exceeded.</span></span> <span data-ttu-id="237c5-248">La capa de vínculo detecta la MTU y la notifica a los protocolos usados.</span><span class="sxs-lookup"><span data-stu-id="237c5-248">The link layer discovers the MTU and reports it to the protocols used.</span></span>

</dd> <dt>

<span data-ttu-id="237c5-249">**SupportsGracefulClosing**</span><span class="sxs-lookup"><span data-stu-id="237c5-249">**SupportsGracefulClosing**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="237c5-250">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="237c5-250">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="237c5-251">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="237c5-251">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="237c5-252">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("API de Win32 de \_ \| Windows Sockets Structs \| información de protocolo \_ \| dwServiceFlags \| XP \_ \_ cierre correcto")</span><span class="sxs-lookup"><span data-stu-id="237c5-252">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32\_API\|Windows Sockets Structures\|PROTOCOL\_INFO\|dwServiceFlags\|XP\_GRACEFUL\_CLOSE")</span></span>
</dt> </dl>

<span data-ttu-id="237c5-253">El protocolo admite operaciones de cierre en dos fases, también conocidas como "operaciones de cierre correcto".</span><span class="sxs-lookup"><span data-stu-id="237c5-253">Protocol supports two-phase close operations, also known as "graceful close operations".</span></span> <span data-ttu-id="237c5-254">En caso contrario, el protocolo solo admite operaciones de cierre de anulación.</span><span class="sxs-lookup"><span data-stu-id="237c5-254">If not, the protocol supports only abortive close operations.</span></span>

</dd> <dt>

<span data-ttu-id="237c5-255">**SupportsGuaranteedBandwidth**</span><span class="sxs-lookup"><span data-stu-id="237c5-255">**SupportsGuaranteedBandwidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="237c5-256">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="237c5-256">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="237c5-257">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="237c5-257">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="237c5-258">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32 \_ API \| Windows Sockets Structures \| Protocolo \_ info \| dwServiceFlags \| XP \_ Bandwidth \_ Allocation")</span><span class="sxs-lookup"><span data-stu-id="237c5-258">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32\_API\|Windows Sockets Structures\|PROTOCOL\_INFO\|dwServiceFlags\|XP\_BANDWIDTH\_ALLOCATION")</span></span>
</dt> </dl>

<span data-ttu-id="237c5-259">El protocolo tiene un mecanismo para establecer y mantener un ancho de banda.</span><span class="sxs-lookup"><span data-stu-id="237c5-259">Protocol has a mechanism to establish and maintain a bandwidth.</span></span>

</dd> <dt>

<span data-ttu-id="237c5-260">**SupportsMulticasting**</span><span class="sxs-lookup"><span data-stu-id="237c5-260">**SupportsMulticasting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="237c5-261">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="237c5-261">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="237c5-262">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="237c5-262">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="237c5-263">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("API de Win32 de \_ \| Windows Sockets Structs \| información de protocolo \_ \| dwServiceFlags \| XP \_ admite \_ multidifusión")</span><span class="sxs-lookup"><span data-stu-id="237c5-263">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32\_API\|Windows Sockets Structures\|PROTOCOL\_INFO\|dwServiceFlags\|XP\_SUPPORTS\_MULTICAST")</span></span>
</dt> </dl>

<span data-ttu-id="237c5-264">El protocolo admite la multidifusión.</span><span class="sxs-lookup"><span data-stu-id="237c5-264">Protocol supports multicasting.</span></span>

</dd> <dt>

<span data-ttu-id="237c5-265">**SupportsQualityofService**</span><span class="sxs-lookup"><span data-stu-id="237c5-265">**SupportsQualityofService**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="237c5-266">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="237c5-266">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="237c5-267">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="237c5-267">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="237c5-268">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \_ API Win32 \| Windows Sockets Structures \| WSAPROTOCOL \_ info \| dwServiceFlags1 \| XP1 \_ QoS \_ Supported")</span><span class="sxs-lookup"><span data-stu-id="237c5-268">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32\_API\|Windows Sockets Structures\|WSAPROTOCOL\_INFO\|dwServiceFlags1\|XP1\_QOS\_SUPPORTED")</span></span>
</dt> </dl>

<span data-ttu-id="237c5-269">El protocolo es capaz de admitir la calidad de servicio (QoS) por parte del proveedor de servicios superpuestos o del operador de transporte subyacente.</span><span class="sxs-lookup"><span data-stu-id="237c5-269">Protocol is capable of Quality of Service (QoS) support by the underlying layered service provider or transport carrier.</span></span> <span data-ttu-id="237c5-270">QoS es una colección de componentes que permiten la diferenciación y el trato preferencial de los subconjuntos de datos transmitidos a través de la red.</span><span class="sxs-lookup"><span data-stu-id="237c5-270">QoS is a collection of components that enable differentiation and preferential treatment for subsets of data transmitted over the network.</span></span> <span data-ttu-id="237c5-271">QoS significa que los subconjuntos de datos obtienen mayor prioridad o servicio garantizado al atravesar una red.</span><span class="sxs-lookup"><span data-stu-id="237c5-271">QoS means subsets of data get higher priority or guaranteed service when traversing a network.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="237c5-272">Observaciones</span><span class="sxs-lookup"><span data-stu-id="237c5-272">Remarks</span></span>

<span data-ttu-id="237c5-273">La **clase \_ NetworkProtocol de Win32** se deriva de [**\_ LogicalElement de CIM**](cim-logicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="237c5-273">The **Win32\_NetworkProtocol** class is derived from [**CIM\_LogicalElement**](cim-logicalelement.md).</span></span>

## <a name="examples"></a><span data-ttu-id="237c5-274">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="237c5-274">Examples</span></span>

<span data-ttu-id="237c5-275">En el ejemplo de código de VBScript siguiente se muestra cómo recuperar una lista de servicios en ejecución de instancias de **Win32 \_ NetworkProtocol**.</span><span class="sxs-lookup"><span data-stu-id="237c5-275">The following VBScript code sample demonstrates how to retrieve a list of running services from instances of **Win32\_NetworkProtocol**.</span></span>


```VB
Set ProtocolSet = GetObject("winmgmts:").ExecQuery("select * from Win32_NetworkProtocol")

for each Protocol in ProtocolSet
 WScript.Echo Protocol.Name
next
```



<span data-ttu-id="237c5-276">El siguiente ejemplo de código Perl muestra cómo recuperar una lista de servicios en ejecución de instancias de **Win32 \_ NetworkProtocol**.</span><span class="sxs-lookup"><span data-stu-id="237c5-276">The following Perl code sample demonstrates how to retrieve a list of running services from instances of **Win32\_NetworkProtocol**.</span></span>


```
use strict;
use Win32::OLE;

my ( $ProtocolSet, $Protocol );

eval { $ProtocolSet = Win32::OLE->GetObject("winmgmts:{impersonationLevel=impersonate}!\\\\.\\root\\cimv2")->
 ExecQuery("SELECT * FROM Win32_NetworkProtocol"); };
unless($@)
{
 print "\n";
 foreach $Protocol (in $ProtocolSet) 
 {
  print $Protocol->{Name}, "\n";
 }
}
else
{
 print STDERR Win32::OLE->LastError, "\n";
}
```



## <a name="requirements"></a><span data-ttu-id="237c5-277">Requisitos</span><span class="sxs-lookup"><span data-stu-id="237c5-277">Requirements</span></span>



| <span data-ttu-id="237c5-278">Requisito</span><span class="sxs-lookup"><span data-stu-id="237c5-278">Requirement</span></span> | <span data-ttu-id="237c5-279">Value</span><span class="sxs-lookup"><span data-stu-id="237c5-279">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="237c5-280">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="237c5-280">Minimum supported client</span></span><br/> | <span data-ttu-id="237c5-281">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="237c5-281">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="237c5-282">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="237c5-282">Minimum supported server</span></span><br/> | <span data-ttu-id="237c5-283">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="237c5-283">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="237c5-284">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="237c5-284">Namespace</span></span><br/>                | <span data-ttu-id="237c5-285">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="237c5-285">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="237c5-286">MOF</span><span class="sxs-lookup"><span data-stu-id="237c5-286">MOF</span></span><br/>                      | <dl> <span data-ttu-id="237c5-287"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="237c5-287"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="237c5-288">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="237c5-288">DLL</span></span><br/>                      | <dl> <span data-ttu-id="237c5-289"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="237c5-289"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="237c5-290">Vea también</span><span class="sxs-lookup"><span data-stu-id="237c5-290">See also</span></span>

<dl> <dt>

[<span data-ttu-id="237c5-291">**\_LOGICALELEMENT CIM**</span><span class="sxs-lookup"><span data-stu-id="237c5-291">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> <dt>

[<span data-ttu-id="237c5-292">Clases de sistema operativo</span><span class="sxs-lookup"><span data-stu-id="237c5-292">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
