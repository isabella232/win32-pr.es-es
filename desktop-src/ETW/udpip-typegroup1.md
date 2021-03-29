---
description: Esta clase es la clase de tipo de evento para los eventos de envío y recepción de IPv4 de UDP/IP. La siguiente sintaxis se simplifica desde el código MOF.
ms.assetid: f04e0b4c-6a2b-4452-9bdf-38c08b487863
title: UdpIp_TypeGroup1 (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UdpIp_TypeGroup1
- UdpIp_TypeGroup1.PID
- UdpIp_TypeGroup1.size
- UdpIp_TypeGroup1.daddr
- UdpIp_TypeGroup1.saddr
- UdpIp_TypeGroup1.dport
- UdpIp_TypeGroup1.sport
- UdpIp_TypeGroup1.seqnum
- UdpIp_TypeGroup1.connid
api_type:
- NA
api_location: ''
ms.openlocfilehash: 8d977841cbfe9a88d14056d77a9b943f4d5d4a3e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104985095"
---
# <a name="udpip_typegroup1-class"></a><span data-ttu-id="d49a6-104">UdpIp \_ TypeGroup1 (clase)</span><span class="sxs-lookup"><span data-stu-id="d49a6-104">UdpIp\_TypeGroup1 class</span></span>

<span data-ttu-id="d49a6-105">Esta clase es la clase de tipo de evento para los eventos de envío y recepción de IPv4 de UDP/IP.</span><span class="sxs-lookup"><span data-stu-id="d49a6-105">This class is the event type class for UDP/IP IPv4 send and receive events.</span></span>

<span data-ttu-id="d49a6-106">La siguiente sintaxis se simplifica desde el código MOF.</span><span class="sxs-lookup"><span data-stu-id="d49a6-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="d49a6-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d49a6-107">Syntax</span></span>

``` syntax
[EventType{10, 11}, EventTypeName{"SendIPV4", "RecvIPV4"}]
class UdpIp_TypeGroup1 : UdpIp
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

## <a name="members"></a><span data-ttu-id="d49a6-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="d49a6-108">Members</span></span>

<span data-ttu-id="d49a6-109">La clase **UdpIp \_ TypeGroup1** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="d49a6-109">The **UdpIp\_TypeGroup1** class has these types of members:</span></span>

-   [<span data-ttu-id="d49a6-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d49a6-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d49a6-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d49a6-111">Properties</span></span>

<span data-ttu-id="d49a6-112">La clase **UdpIp \_ TypeGroup1** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="d49a6-112">The **UdpIp\_TypeGroup1** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d49a6-113">connid</span><span class="sxs-lookup"><span data-stu-id="d49a6-113">connid</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d49a6-114">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d49a6-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d49a6-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d49a6-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d49a6-116">Calificadores: WmiDataId (8), puntero</span><span class="sxs-lookup"><span data-stu-id="d49a6-116">Qualifiers: WmiDataId(8), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="d49a6-117">Un identificador de conexión único para correlacionar los eventos que pertenecen a la misma conexión.</span><span class="sxs-lookup"><span data-stu-id="d49a6-117">A unique connection identifier to correlate events belonging to the same connection.</span></span>

</dd> <dt>

<span data-ttu-id="d49a6-118">daddr</span><span class="sxs-lookup"><span data-stu-id="d49a6-118">daddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d49a6-119">Tipo de datos: **objeto**</span><span class="sxs-lookup"><span data-stu-id="d49a6-119">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="d49a6-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d49a6-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d49a6-121">Calificadores: WmiDataId (3), extensión ("IPAddrV4")</span><span class="sxs-lookup"><span data-stu-id="d49a6-121">Qualifiers: WmiDataId(3), Extension("IPAddrV4")</span></span>
</dt> </dl>

<span data-ttu-id="d49a6-122">Dirección IP de destino.</span><span class="sxs-lookup"><span data-stu-id="d49a6-122">Destination IP address.</span></span>

</dd> <dt>

<span data-ttu-id="d49a6-123">dport</span><span class="sxs-lookup"><span data-stu-id="d49a6-123">dport</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d49a6-124">Tipo de datos: **objeto**</span><span class="sxs-lookup"><span data-stu-id="d49a6-124">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="d49a6-125">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d49a6-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d49a6-126">Calificadores: WmiDataId (5), extensión ("puerto")</span><span class="sxs-lookup"><span data-stu-id="d49a6-126">Qualifiers: WmiDataId(5), Extension("Port")</span></span>
</dt> </dl>

<span data-ttu-id="d49a6-127">Número de puerto de destino.</span><span class="sxs-lookup"><span data-stu-id="d49a6-127">Destination port number.</span></span>

</dd> <dt>

<span data-ttu-id="d49a6-128">PID</span><span class="sxs-lookup"><span data-stu-id="d49a6-128">PID</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d49a6-129">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d49a6-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d49a6-130">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d49a6-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d49a6-131">Calificadores: WmiDataId (1)</span><span class="sxs-lookup"><span data-stu-id="d49a6-131">Qualifiers: WmiDataId(1)</span></span>
</dt> </dl>

<span data-ttu-id="d49a6-132">Identificador del proceso asociado a la solicitud.</span><span class="sxs-lookup"><span data-stu-id="d49a6-132">Identifier of the process associated with the request.</span></span>

</dd> <dt>

<span data-ttu-id="d49a6-133">saddr</span><span class="sxs-lookup"><span data-stu-id="d49a6-133">saddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d49a6-134">Tipo de datos: **objeto**</span><span class="sxs-lookup"><span data-stu-id="d49a6-134">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="d49a6-135">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d49a6-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d49a6-136">Calificadores: WmiDataId (4), extensión ("IPAddrV4")</span><span class="sxs-lookup"><span data-stu-id="d49a6-136">Qualifiers: WmiDataId(4), Extension("IPAddrV4")</span></span>
</dt> </dl>

<span data-ttu-id="d49a6-137">Dirección IP de origen.</span><span class="sxs-lookup"><span data-stu-id="d49a6-137">Source IP address.</span></span>

</dd> <dt>

<span data-ttu-id="d49a6-138">seqnum</span><span class="sxs-lookup"><span data-stu-id="d49a6-138">seqnum</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d49a6-139">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d49a6-139">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d49a6-140">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d49a6-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d49a6-141">Calificadores: WmiDataId (7)</span><span class="sxs-lookup"><span data-stu-id="d49a6-141">Qualifiers: WmiDataId(7)</span></span>
</dt> </dl>

<span data-ttu-id="d49a6-142">Número de secuencia.</span><span class="sxs-lookup"><span data-stu-id="d49a6-142">Sequence number.</span></span>

</dd> <dt>

<span data-ttu-id="d49a6-143">tamaño</span><span class="sxs-lookup"><span data-stu-id="d49a6-143">size</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d49a6-144">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d49a6-144">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d49a6-145">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d49a6-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d49a6-146">Calificadores: WmiDataId (2)</span><span class="sxs-lookup"><span data-stu-id="d49a6-146">Qualifiers: WmiDataId(2)</span></span>
</dt> </dl>

<span data-ttu-id="d49a6-147">Tamaño del paquete.</span><span class="sxs-lookup"><span data-stu-id="d49a6-147">Size of the packet.</span></span>

</dd> <dt>

<span data-ttu-id="d49a6-148">deportivo</span><span class="sxs-lookup"><span data-stu-id="d49a6-148">sport</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d49a6-149">Tipo de datos: **objeto**</span><span class="sxs-lookup"><span data-stu-id="d49a6-149">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="d49a6-150">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d49a6-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d49a6-151">Calificadores: WmiDataId (6), extensión ("puerto")</span><span class="sxs-lookup"><span data-stu-id="d49a6-151">Qualifiers: WmiDataId(6), Extension("Port")</span></span>
</dt> </dl>

<span data-ttu-id="d49a6-152">Número de puerto de origen.</span><span class="sxs-lookup"><span data-stu-id="d49a6-152">Source port number.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d49a6-153">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d49a6-153">Requirements</span></span>



| <span data-ttu-id="d49a6-154">Requisito</span><span class="sxs-lookup"><span data-stu-id="d49a6-154">Requirement</span></span> | <span data-ttu-id="d49a6-155">Value</span><span class="sxs-lookup"><span data-stu-id="d49a6-155">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="d49a6-156">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d49a6-156">Minimum supported client</span></span><br/> | <span data-ttu-id="d49a6-157">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="d49a6-157">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="d49a6-158">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d49a6-158">Minimum supported server</span></span><br/> | <span data-ttu-id="d49a6-159">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="d49a6-159">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d49a6-160">Vea también</span><span class="sxs-lookup"><span data-stu-id="d49a6-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d49a6-161">**UdpIp**</span><span class="sxs-lookup"><span data-stu-id="d49a6-161">**UdpIp**</span></span>](udpip.md)
</dt> </dl>

 

 




