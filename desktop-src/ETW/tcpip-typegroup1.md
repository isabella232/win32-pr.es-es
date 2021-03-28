---
description: Esta clase es la clase de tipo de evento para eventos TCP/IP de IPv4. La siguiente sintaxis se simplifica desde el código MOF.
ms.assetid: ed835df8-6f53-46a3-abf2-c66a1f13f987
title: TcpIp_TypeGroup1 (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TcpIp_TypeGroup1
- TcpIp_TypeGroup1.PID
- TcpIp_TypeGroup1.size
- TcpIp_TypeGroup1.daddr
- TcpIp_TypeGroup1.saddr
- TcpIp_TypeGroup1.dport
- TcpIp_TypeGroup1.sport
- TcpIp_TypeGroup1.seqnum
- TcpIp_TypeGroup1.connid
api_type:
- NA
api_location: ''
ms.openlocfilehash: 70ac95d3d3de5a9bcef610607f3b5a9046b63ea3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984791"
---
# <a name="tcpip_typegroup1-class"></a><span data-ttu-id="10f2b-104">\_Clase TypeGroup1 de TCPIP</span><span class="sxs-lookup"><span data-stu-id="10f2b-104">TcpIp\_TypeGroup1 class</span></span>

<span data-ttu-id="10f2b-105">Esta clase es la clase de tipo de evento para eventos TCP/IP de IPv4.</span><span class="sxs-lookup"><span data-stu-id="10f2b-105">This class is the event type class for IPv4 TCP/IP events.</span></span>

<span data-ttu-id="10f2b-106">La siguiente sintaxis se simplifica desde el código MOF.</span><span class="sxs-lookup"><span data-stu-id="10f2b-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="10f2b-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="10f2b-107">Syntax</span></span>

``` syntax
[EventType{11, 13, 14, 16, 18}, EventTypeName{"RecvIPV4", "DisconnectIPV4", "RetransmitIPV4", "ReconnectIPV4", "TCPCopyIPV4"}]
class TcpIp_TypeGroup1 : TcpIp
{
  uint32 PID;
  uint32 size;
  object daddr;
  object saddr;
  object dport;
  object sport;
  uint32 seqnum;
  uint32 connid;
};
```

## <a name="members"></a><span data-ttu-id="10f2b-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="10f2b-108">Members</span></span>

<span data-ttu-id="10f2b-109">La **clase \_ TypeGroup1 de TCPIP** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="10f2b-109">The **TcpIp\_TypeGroup1** class has these types of members:</span></span>

-   [<span data-ttu-id="10f2b-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="10f2b-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="10f2b-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="10f2b-111">Properties</span></span>

<span data-ttu-id="10f2b-112">La **clase \_ TypeGroup1 de TCPIP** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="10f2b-112">The **TcpIp\_TypeGroup1** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="10f2b-113">connid</span><span class="sxs-lookup"><span data-stu-id="10f2b-113">connid</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10f2b-114">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="10f2b-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="10f2b-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="10f2b-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10f2b-116">Calificadores: WmiDataId (8), puntero</span><span class="sxs-lookup"><span data-stu-id="10f2b-116">Qualifiers: WmiDataId(8), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="10f2b-117">Un identificador de conexión único para correlacionar los eventos que pertenecen a la misma conexión.</span><span class="sxs-lookup"><span data-stu-id="10f2b-117">A unique connection identifier to correlate events belonging to the same connection.</span></span>

</dd> <dt>

<span data-ttu-id="10f2b-118">daddr</span><span class="sxs-lookup"><span data-stu-id="10f2b-118">daddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10f2b-119">Tipo de datos: **objeto**</span><span class="sxs-lookup"><span data-stu-id="10f2b-119">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="10f2b-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="10f2b-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10f2b-121">Calificadores: WmiDataId (3), extensión ("IPAddrV4")</span><span class="sxs-lookup"><span data-stu-id="10f2b-121">Qualifiers: WmiDataId(3), Extension("IPAddrV4")</span></span>
</dt> </dl>

<span data-ttu-id="10f2b-122">Dirección IP de destino.</span><span class="sxs-lookup"><span data-stu-id="10f2b-122">Destination IP address.</span></span>

</dd> <dt>

<span data-ttu-id="10f2b-123">dport</span><span class="sxs-lookup"><span data-stu-id="10f2b-123">dport</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10f2b-124">Tipo de datos: **objeto**</span><span class="sxs-lookup"><span data-stu-id="10f2b-124">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="10f2b-125">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="10f2b-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10f2b-126">Calificadores: WmiDataId (5), extensión ("puerto")</span><span class="sxs-lookup"><span data-stu-id="10f2b-126">Qualifiers: WmiDataId(5), Extension("Port")</span></span>
</dt> </dl>

<span data-ttu-id="10f2b-127">Número de puerto de destino.</span><span class="sxs-lookup"><span data-stu-id="10f2b-127">Destination port number.</span></span>

</dd> <dt>

<span data-ttu-id="10f2b-128">PID</span><span class="sxs-lookup"><span data-stu-id="10f2b-128">PID</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10f2b-129">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="10f2b-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="10f2b-130">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="10f2b-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10f2b-131">Calificadores: WmiDataId (1)</span><span class="sxs-lookup"><span data-stu-id="10f2b-131">Qualifiers: WmiDataId(1)</span></span>
</dt> </dl>

<span data-ttu-id="10f2b-132">Identificador del proceso asociado a la solicitud.</span><span class="sxs-lookup"><span data-stu-id="10f2b-132">Identifier of the process associated with the request.</span></span>

</dd> <dt>

<span data-ttu-id="10f2b-133">saddr</span><span class="sxs-lookup"><span data-stu-id="10f2b-133">saddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10f2b-134">Tipo de datos: **objeto**</span><span class="sxs-lookup"><span data-stu-id="10f2b-134">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="10f2b-135">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="10f2b-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10f2b-136">Calificadores: WmiDataId (4), extensión ("IPAddrV4")</span><span class="sxs-lookup"><span data-stu-id="10f2b-136">Qualifiers: WmiDataId(4), Extension("IPAddrV4")</span></span>
</dt> </dl>

<span data-ttu-id="10f2b-137">Dirección IP de origen.</span><span class="sxs-lookup"><span data-stu-id="10f2b-137">Source IP address.</span></span>

</dd> <dt>

<span data-ttu-id="10f2b-138">seqnum</span><span class="sxs-lookup"><span data-stu-id="10f2b-138">seqnum</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10f2b-139">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="10f2b-139">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="10f2b-140">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="10f2b-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10f2b-141">Calificadores: WmiDataId (7)</span><span class="sxs-lookup"><span data-stu-id="10f2b-141">Qualifiers: WmiDataId(7)</span></span>
</dt> </dl>

<span data-ttu-id="10f2b-142">Número de secuencia.</span><span class="sxs-lookup"><span data-stu-id="10f2b-142">Sequence number.</span></span>

</dd> <dt>

<span data-ttu-id="10f2b-143">tamaño</span><span class="sxs-lookup"><span data-stu-id="10f2b-143">size</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10f2b-144">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="10f2b-144">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="10f2b-145">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="10f2b-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10f2b-146">Calificadores: WmiDataId (2)</span><span class="sxs-lookup"><span data-stu-id="10f2b-146">Qualifiers: WmiDataId(2)</span></span>
</dt> </dl>

<span data-ttu-id="10f2b-147">Tamaño del paquete.</span><span class="sxs-lookup"><span data-stu-id="10f2b-147">Size of the packet.</span></span>

</dd> <dt>

<span data-ttu-id="10f2b-148">deportivo</span><span class="sxs-lookup"><span data-stu-id="10f2b-148">sport</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="10f2b-149">Tipo de datos: **objeto**</span><span class="sxs-lookup"><span data-stu-id="10f2b-149">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="10f2b-150">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="10f2b-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="10f2b-151">Calificadores: WmiDataId (6), extensión ("puerto")</span><span class="sxs-lookup"><span data-stu-id="10f2b-151">Qualifiers: WmiDataId(6), Extension("Port")</span></span>
</dt> </dl>

<span data-ttu-id="10f2b-152">Número de puerto de origen.</span><span class="sxs-lookup"><span data-stu-id="10f2b-152">Source port number.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="10f2b-153">Requisitos</span><span class="sxs-lookup"><span data-stu-id="10f2b-153">Requirements</span></span>



| <span data-ttu-id="10f2b-154">Requisito</span><span class="sxs-lookup"><span data-stu-id="10f2b-154">Requirement</span></span> | <span data-ttu-id="10f2b-155">Value</span><span class="sxs-lookup"><span data-stu-id="10f2b-155">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="10f2b-156">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="10f2b-156">Minimum supported client</span></span><br/> | <span data-ttu-id="10f2b-157">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="10f2b-157">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="10f2b-158">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="10f2b-158">Minimum supported server</span></span><br/> | <span data-ttu-id="10f2b-159">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="10f2b-159">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="10f2b-160">Vea también</span><span class="sxs-lookup"><span data-stu-id="10f2b-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="10f2b-161">**Luego**</span><span class="sxs-lookup"><span data-stu-id="10f2b-161">**TcpIp**</span></span>](tcpip.md)
</dt> </dl>

 

 




