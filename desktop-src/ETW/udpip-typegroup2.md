---
description: Esta clase es la clase de tipo de evento para los eventos de envío y recepción IPv6 de UDP/IP. La siguiente sintaxis se simplifica desde el código MOF.
ms.assetid: 059041f6-bf34-4bf8-8e1a-2dfbc6c30edc
title: UdpIp_TypeGroup2 (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UdpIp_TypeGroup2
- UdpIp_TypeGroup2.PID
- UdpIp_TypeGroup2.size
- UdpIp_TypeGroup2.daddr
- UdpIp_TypeGroup2.saddr
- UdpIp_TypeGroup2.dport
- UdpIp_TypeGroup2.sport
- UdpIp_TypeGroup2.seqnum
- UdpIp_TypeGroup2.connid
api_type:
- NA
api_location: ''
ms.openlocfilehash: 88d9cb4935d005f3c25f1fb6c3c421328fb285bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104985094"
---
# <a name="udpip_typegroup2-class"></a><span data-ttu-id="a3376-104">UdpIp \_ TypeGroup2 (clase)</span><span class="sxs-lookup"><span data-stu-id="a3376-104">UdpIp\_TypeGroup2 class</span></span>

<span data-ttu-id="a3376-105">Esta clase es la clase de tipo de evento para los eventos de envío y recepción IPv6 de UDP/IP.</span><span class="sxs-lookup"><span data-stu-id="a3376-105">This class is the event type class for UDP/IP IPv6 send and receive events.</span></span>

<span data-ttu-id="a3376-106">La siguiente sintaxis se simplifica desde el código MOF.</span><span class="sxs-lookup"><span data-stu-id="a3376-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="a3376-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a3376-107">Syntax</span></span>

``` syntax
[EventType{26, 27}, EventTypeName{"SendIPV6", "RecvIPV6"}]
class UdpIp_TypeGroup2 : UdpIp
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

## <a name="members"></a><span data-ttu-id="a3376-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="a3376-108">Members</span></span>

<span data-ttu-id="a3376-109">La clase **UdpIp \_ TypeGroup2** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="a3376-109">The **UdpIp\_TypeGroup2** class has these types of members:</span></span>

-   [<span data-ttu-id="a3376-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="a3376-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a3376-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="a3376-111">Properties</span></span>

<span data-ttu-id="a3376-112">La clase **UdpIp \_ TypeGroup2** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="a3376-112">The **UdpIp\_TypeGroup2** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a3376-113">connid</span><span class="sxs-lookup"><span data-stu-id="a3376-113">connid</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a3376-114">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a3376-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a3376-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a3376-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a3376-116">Calificadores: WmiDataId (8), puntero</span><span class="sxs-lookup"><span data-stu-id="a3376-116">Qualifiers: WmiDataId(8), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="a3376-117">Un identificador de conexión único para correlacionar los eventos que pertenecen a la misma conexión.</span><span class="sxs-lookup"><span data-stu-id="a3376-117">A unique connection identifier to correlate events belonging to the same connection.</span></span>

</dd> <dt>

<span data-ttu-id="a3376-118">daddr</span><span class="sxs-lookup"><span data-stu-id="a3376-118">daddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a3376-119">Tipo de datos: **objeto**</span><span class="sxs-lookup"><span data-stu-id="a3376-119">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="a3376-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a3376-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a3376-121">Calificadores: WmiDataId (3), extensión ("IPAddrV6")</span><span class="sxs-lookup"><span data-stu-id="a3376-121">Qualifiers: WmiDataId(3), Extension("IPAddrV6")</span></span>
</dt> </dl>

<span data-ttu-id="a3376-122">Dirección IP de destino.</span><span class="sxs-lookup"><span data-stu-id="a3376-122">Destination IP address.</span></span>

</dd> <dt>

<span data-ttu-id="a3376-123">dport</span><span class="sxs-lookup"><span data-stu-id="a3376-123">dport</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a3376-124">Tipo de datos: **objeto**</span><span class="sxs-lookup"><span data-stu-id="a3376-124">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="a3376-125">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a3376-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a3376-126">Calificadores: WmiDataId (5), extensión ("puerto")</span><span class="sxs-lookup"><span data-stu-id="a3376-126">Qualifiers: WmiDataId(5), Extension("Port")</span></span>
</dt> </dl>

<span data-ttu-id="a3376-127">Número de puerto de destino.</span><span class="sxs-lookup"><span data-stu-id="a3376-127">Destination port number.</span></span>

</dd> <dt>

<span data-ttu-id="a3376-128">PID</span><span class="sxs-lookup"><span data-stu-id="a3376-128">PID</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a3376-129">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a3376-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a3376-130">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a3376-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a3376-131">Calificadores: WmiDataId (1)</span><span class="sxs-lookup"><span data-stu-id="a3376-131">Qualifiers: WmiDataId(1)</span></span>
</dt> </dl>

<span data-ttu-id="a3376-132">Identificador del proceso asociado a la solicitud.</span><span class="sxs-lookup"><span data-stu-id="a3376-132">Identifier of the process associated with the request.</span></span>

</dd> <dt>

<span data-ttu-id="a3376-133">saddr</span><span class="sxs-lookup"><span data-stu-id="a3376-133">saddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a3376-134">Tipo de datos: **objeto**</span><span class="sxs-lookup"><span data-stu-id="a3376-134">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="a3376-135">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a3376-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a3376-136">Calificadores: WmiDataId (4), extensión ("IPAddrV6")</span><span class="sxs-lookup"><span data-stu-id="a3376-136">Qualifiers: WmiDataId(4), Extension("IPAddrV6")</span></span>
</dt> </dl>

<span data-ttu-id="a3376-137">Dirección IP de origen.</span><span class="sxs-lookup"><span data-stu-id="a3376-137">Source IP address.</span></span>

</dd> <dt>

<span data-ttu-id="a3376-138">seqnum</span><span class="sxs-lookup"><span data-stu-id="a3376-138">seqnum</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a3376-139">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a3376-139">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a3376-140">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a3376-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a3376-141">Calificadores: WmiDataId (7)</span><span class="sxs-lookup"><span data-stu-id="a3376-141">Qualifiers: WmiDataId(7)</span></span>
</dt> </dl>

<span data-ttu-id="a3376-142">Número de secuencia.</span><span class="sxs-lookup"><span data-stu-id="a3376-142">Sequence number.</span></span>

</dd> <dt>

<span data-ttu-id="a3376-143">tamaño</span><span class="sxs-lookup"><span data-stu-id="a3376-143">size</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a3376-144">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a3376-144">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a3376-145">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a3376-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a3376-146">Calificadores: WmiDataId (2)</span><span class="sxs-lookup"><span data-stu-id="a3376-146">Qualifiers: WmiDataId(2)</span></span>
</dt> </dl>

<span data-ttu-id="a3376-147">Tamaño del paquete.</span><span class="sxs-lookup"><span data-stu-id="a3376-147">Size of the packet.</span></span>

</dd> <dt>

<span data-ttu-id="a3376-148">deportivo</span><span class="sxs-lookup"><span data-stu-id="a3376-148">sport</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a3376-149">Tipo de datos: **objeto**</span><span class="sxs-lookup"><span data-stu-id="a3376-149">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="a3376-150">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a3376-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a3376-151">Calificadores: WmiDataId (6), extensión ("puerto")</span><span class="sxs-lookup"><span data-stu-id="a3376-151">Qualifiers: WmiDataId(6), Extension("Port")</span></span>
</dt> </dl>

<span data-ttu-id="a3376-152">Número de puerto de origen.</span><span class="sxs-lookup"><span data-stu-id="a3376-152">Source port number.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a3376-153">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a3376-153">Requirements</span></span>



| <span data-ttu-id="a3376-154">Requisito</span><span class="sxs-lookup"><span data-stu-id="a3376-154">Requirement</span></span> | <span data-ttu-id="a3376-155">Value</span><span class="sxs-lookup"><span data-stu-id="a3376-155">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="a3376-156">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a3376-156">Minimum supported client</span></span><br/> | <span data-ttu-id="a3376-157">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="a3376-157">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="a3376-158">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a3376-158">Minimum supported server</span></span><br/> | <span data-ttu-id="a3376-159">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="a3376-159">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a3376-160">Vea también</span><span class="sxs-lookup"><span data-stu-id="a3376-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a3376-161">**UdpIp**</span><span class="sxs-lookup"><span data-stu-id="a3376-161">**UdpIp**</span></span>](udpip.md)
</dt> </dl>

 

 




