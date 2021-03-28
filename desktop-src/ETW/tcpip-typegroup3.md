---
description: Esta clase es la clase de tipo de evento para eventos TCP/IP de IPv6. La siguiente sintaxis se simplifica desde el código MOF.
ms.assetid: d24e667e-ec7f-492a-989e-a02ff4c8ac10
title: TcpIp_TypeGroup3 (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TcpIp_TypeGroup3
- TcpIp_TypeGroup3.PID
- TcpIp_TypeGroup3.size
- TcpIp_TypeGroup3.daddr
- TcpIp_TypeGroup3.saddr
- TcpIp_TypeGroup3.dport
- TcpIp_TypeGroup3.sport
- TcpIp_TypeGroup3.seqnum
- TcpIp_TypeGroup3.connid
api_type:
- NA
api_location: ''
ms.openlocfilehash: 82aa119c0d770a26060b1e8d6ab74433146bb3c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984783"
---
# <a name="tcpip_typegroup3-class"></a><span data-ttu-id="63ef6-104">\_Clase TypeGroup3 de TCPIP</span><span class="sxs-lookup"><span data-stu-id="63ef6-104">TcpIp\_TypeGroup3 class</span></span>

<span data-ttu-id="63ef6-105">Esta clase es la clase de tipo de evento para eventos TCP/IP de IPv6.</span><span class="sxs-lookup"><span data-stu-id="63ef6-105">This class is the event type class for IPv6 TCP/IP events.</span></span>

<span data-ttu-id="63ef6-106">La siguiente sintaxis se simplifica desde el código MOF.</span><span class="sxs-lookup"><span data-stu-id="63ef6-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="63ef6-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="63ef6-107">Syntax</span></span>

``` syntax
[EventType{27, 29, 30, 32, 34}, EventTypeName{"RecvIPV6", "DisconnectIPV6", "RetransmitIPV6", "ReconnectIPV6", "TCPCopyIPV6"}]
class TcpIp_TypeGroup3 : TcpIp
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

## <a name="members"></a><span data-ttu-id="63ef6-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="63ef6-108">Members</span></span>

<span data-ttu-id="63ef6-109">La **clase \_ TypeGroup3 de TCPIP** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="63ef6-109">The **TcpIp\_TypeGroup3** class has these types of members:</span></span>

-   [<span data-ttu-id="63ef6-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="63ef6-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="63ef6-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="63ef6-111">Properties</span></span>

<span data-ttu-id="63ef6-112">La **clase \_ TypeGroup3 de TCPIP** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="63ef6-112">The **TcpIp\_TypeGroup3** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="63ef6-113">connid</span><span class="sxs-lookup"><span data-stu-id="63ef6-113">connid</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63ef6-114">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="63ef6-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="63ef6-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="63ef6-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="63ef6-116">Calificadores: WmiDataId (6), puntero</span><span class="sxs-lookup"><span data-stu-id="63ef6-116">Qualifiers: WmiDataId(6), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="63ef6-117">Un identificador de conexión único para correlacionar los eventos que pertenecen a la misma conexión.</span><span class="sxs-lookup"><span data-stu-id="63ef6-117">A unique connection identifier to correlate events belonging to the same connection.</span></span>

</dd> <dt>

<span data-ttu-id="63ef6-118">daddr</span><span class="sxs-lookup"><span data-stu-id="63ef6-118">daddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63ef6-119">Tipo de datos: **objeto**</span><span class="sxs-lookup"><span data-stu-id="63ef6-119">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="63ef6-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="63ef6-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="63ef6-121">Calificadores: WmiDataId (3), extensión ("IPAddrV6")</span><span class="sxs-lookup"><span data-stu-id="63ef6-121">Qualifiers: WmiDataId(3), Extension("IPAddrV6")</span></span>
</dt> </dl>

<span data-ttu-id="63ef6-122">Dirección IP de destino.</span><span class="sxs-lookup"><span data-stu-id="63ef6-122">Destination IP address.</span></span>

</dd> <dt>

<span data-ttu-id="63ef6-123">dport</span><span class="sxs-lookup"><span data-stu-id="63ef6-123">dport</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63ef6-124">Tipo de datos: **objeto**</span><span class="sxs-lookup"><span data-stu-id="63ef6-124">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="63ef6-125">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="63ef6-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="63ef6-126">Calificadores: WmiDataId (5), extensión ("puerto")</span><span class="sxs-lookup"><span data-stu-id="63ef6-126">Qualifiers: WmiDataId(5), Extension("Port")</span></span>
</dt> </dl>

<span data-ttu-id="63ef6-127">Número de puerto de destino.</span><span class="sxs-lookup"><span data-stu-id="63ef6-127">Destination port number.</span></span>

</dd> <dt>

<span data-ttu-id="63ef6-128">PID</span><span class="sxs-lookup"><span data-stu-id="63ef6-128">PID</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63ef6-129">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="63ef6-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="63ef6-130">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="63ef6-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="63ef6-131">Calificadores: WmiDataId (1)</span><span class="sxs-lookup"><span data-stu-id="63ef6-131">Qualifiers: WmiDataId(1)</span></span>
</dt> </dl>

<span data-ttu-id="63ef6-132">Identificador del proceso asociado a la solicitud.</span><span class="sxs-lookup"><span data-stu-id="63ef6-132">Identifier of the process associated with the request.</span></span>

</dd> <dt>

<span data-ttu-id="63ef6-133">saddr</span><span class="sxs-lookup"><span data-stu-id="63ef6-133">saddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63ef6-134">Tipo de datos: **objeto**</span><span class="sxs-lookup"><span data-stu-id="63ef6-134">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="63ef6-135">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="63ef6-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="63ef6-136">Calificadores: WmiDataId (4), extensión ("IPAddrV6")</span><span class="sxs-lookup"><span data-stu-id="63ef6-136">Qualifiers: WmiDataId(4), Extension("IPAddrV6")</span></span>
</dt> </dl>

<span data-ttu-id="63ef6-137">Dirección IP de origen.</span><span class="sxs-lookup"><span data-stu-id="63ef6-137">Source IP address.</span></span>

</dd> <dt>

<span data-ttu-id="63ef6-138">seqnum</span><span class="sxs-lookup"><span data-stu-id="63ef6-138">seqnum</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63ef6-139">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="63ef6-139">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="63ef6-140">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="63ef6-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="63ef6-141">Calificadores: WmiDataId (7)</span><span class="sxs-lookup"><span data-stu-id="63ef6-141">Qualifiers: WmiDataId(7)</span></span>
</dt> </dl>

<span data-ttu-id="63ef6-142">Número de secuencia.</span><span class="sxs-lookup"><span data-stu-id="63ef6-142">Sequence number.</span></span>

</dd> <dt>

<span data-ttu-id="63ef6-143">tamaño</span><span class="sxs-lookup"><span data-stu-id="63ef6-143">size</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63ef6-144">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="63ef6-144">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="63ef6-145">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="63ef6-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="63ef6-146">Calificadores: WmiDataId (2)</span><span class="sxs-lookup"><span data-stu-id="63ef6-146">Qualifiers: WmiDataId(2)</span></span>
</dt> </dl>

<span data-ttu-id="63ef6-147">Tamaño del paquete.</span><span class="sxs-lookup"><span data-stu-id="63ef6-147">Size of the packet.</span></span>

</dd> <dt>

<span data-ttu-id="63ef6-148">deportivo</span><span class="sxs-lookup"><span data-stu-id="63ef6-148">sport</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63ef6-149">Tipo de datos: **objeto**</span><span class="sxs-lookup"><span data-stu-id="63ef6-149">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="63ef6-150">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="63ef6-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="63ef6-151">Calificadores: WmiDataId (6), extensión ("puerto")</span><span class="sxs-lookup"><span data-stu-id="63ef6-151">Qualifiers: WmiDataId(6), Extension("Port")</span></span>
</dt> </dl>

<span data-ttu-id="63ef6-152">Número de puerto de origen.</span><span class="sxs-lookup"><span data-stu-id="63ef6-152">Source port number.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="63ef6-153">Requisitos</span><span class="sxs-lookup"><span data-stu-id="63ef6-153">Requirements</span></span>



| <span data-ttu-id="63ef6-154">Requisito</span><span class="sxs-lookup"><span data-stu-id="63ef6-154">Requirement</span></span> | <span data-ttu-id="63ef6-155">Value</span><span class="sxs-lookup"><span data-stu-id="63ef6-155">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="63ef6-156">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="63ef6-156">Minimum supported client</span></span><br/> | <span data-ttu-id="63ef6-157">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="63ef6-157">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="63ef6-158">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="63ef6-158">Minimum supported server</span></span><br/> | <span data-ttu-id="63ef6-159">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="63ef6-159">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="63ef6-160">Vea también</span><span class="sxs-lookup"><span data-stu-id="63ef6-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63ef6-161">**Luego**</span><span class="sxs-lookup"><span data-stu-id="63ef6-161">**TcpIp**</span></span>](tcpip.md)
</dt> </dl>

 

 




