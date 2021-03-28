---
description: Esta clase es la clase de tipo de evento para los eventos de envío de TCP/IP de IPv6. La siguiente sintaxis se simplifica desde el código MOF.
ms.assetid: 231ef62f-e3a5-497d-b10a-79449dc73c71
title: TcpIp_SendIPV6 (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TcpIp_SendIPV6
- TcpIp_SendIPV6.PID
- TcpIp_SendIPV6.size
- TcpIp_SendIPV6.daddr
- TcpIp_SendIPV6.saddr
- TcpIp_SendIPV6.dport
- TcpIp_SendIPV6.sport
- TcpIp_SendIPV6.startime
- TcpIp_SendIPV6.endtime
- TcpIp_SendIPV6.seqnum
- TcpIp_SendIPV6.connid
api_type:
- NA
api_location: ''
ms.openlocfilehash: 190b7d4fc64660b1e12240b6461e73066102b6a3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984790"
---
# <a name="tcpip_sendipv6-class"></a><span data-ttu-id="44e9e-104">\_Clase SendIPV6 de TCPIP</span><span class="sxs-lookup"><span data-stu-id="44e9e-104">TcpIp\_SendIPV6 class</span></span>

<span data-ttu-id="44e9e-105">Esta clase es la clase de tipo de evento para los eventos de envío de TCP/IP de IPv6.</span><span class="sxs-lookup"><span data-stu-id="44e9e-105">This class is the event type class for IPv6 TCP/IP send events.</span></span>

<span data-ttu-id="44e9e-106">La siguiente sintaxis se simplifica desde el código MOF.</span><span class="sxs-lookup"><span data-stu-id="44e9e-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="44e9e-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="44e9e-107">Syntax</span></span>

``` syntax
[EventType{26}, EventTypeName{"SendIPV6"}]
class TcpIp_SendIPV6 : TcpIp
{
  uint32 PID;
  uint32 size;
  object daddr;
  object saddr;
  object dport;
  object sport;
  uint32 startime;
  uint32 endtime;
  uint32 seqnum;
  uint32 connid;
};
```

## <a name="members"></a><span data-ttu-id="44e9e-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="44e9e-108">Members</span></span>

<span data-ttu-id="44e9e-109">La **clase \_ SendIPV6 de TCPIP** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="44e9e-109">The **TcpIp\_SendIPV6** class has these types of members:</span></span>

-   [<span data-ttu-id="44e9e-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="44e9e-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="44e9e-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="44e9e-111">Properties</span></span>

<span data-ttu-id="44e9e-112">La **clase \_ SendIPV6 de TCPIP** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="44e9e-112">The **TcpIp\_SendIPV6** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="44e9e-113">connid</span><span class="sxs-lookup"><span data-stu-id="44e9e-113">connid</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44e9e-114">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="44e9e-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="44e9e-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="44e9e-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="44e9e-116">Calificadores: WmiDataId (10), puntero</span><span class="sxs-lookup"><span data-stu-id="44e9e-116">Qualifiers: WmiDataId(10), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="44e9e-117">Un identificador de conexión único para correlacionar los eventos que pertenecen a la misma conexión.</span><span class="sxs-lookup"><span data-stu-id="44e9e-117">A unique connection identifier to correlate events belonging to the same connection.</span></span>

</dd> <dt>

<span data-ttu-id="44e9e-118">daddr</span><span class="sxs-lookup"><span data-stu-id="44e9e-118">daddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44e9e-119">Tipo de datos: **objeto**</span><span class="sxs-lookup"><span data-stu-id="44e9e-119">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="44e9e-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="44e9e-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="44e9e-121">Calificadores: WmiDataId (3), extensión ("IPAddrV6")</span><span class="sxs-lookup"><span data-stu-id="44e9e-121">Qualifiers: WmiDataId(3), Extension("IPAddrV6")</span></span>
</dt> </dl>

<span data-ttu-id="44e9e-122">Dirección IP de destino.</span><span class="sxs-lookup"><span data-stu-id="44e9e-122">Destination IP address.</span></span>

</dd> <dt>

<span data-ttu-id="44e9e-123">dport</span><span class="sxs-lookup"><span data-stu-id="44e9e-123">dport</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44e9e-124">Tipo de datos: **objeto**</span><span class="sxs-lookup"><span data-stu-id="44e9e-124">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="44e9e-125">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="44e9e-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="44e9e-126">Calificadores: WmiDataId (5), extensión ("puerto")</span><span class="sxs-lookup"><span data-stu-id="44e9e-126">Qualifiers: WmiDataId(5), Extension("Port")</span></span>
</dt> </dl>

<span data-ttu-id="44e9e-127">Número de puerto de destino.</span><span class="sxs-lookup"><span data-stu-id="44e9e-127">Destination port number.</span></span>

</dd> <dt>

<span data-ttu-id="44e9e-128">**EndTime**</span><span class="sxs-lookup"><span data-stu-id="44e9e-128">**endtime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44e9e-129">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="44e9e-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="44e9e-130">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="44e9e-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="44e9e-131">Calificadores: WmiDataId (8)</span><span class="sxs-lookup"><span data-stu-id="44e9e-131">Qualifiers: WmiDataId(8)</span></span>
</dt> </dl>

<span data-ttu-id="44e9e-132">Fin del tiempo de solicitud de envío.</span><span class="sxs-lookup"><span data-stu-id="44e9e-132">End send request time.</span></span>

</dd> <dt>

<span data-ttu-id="44e9e-133">PID</span><span class="sxs-lookup"><span data-stu-id="44e9e-133">PID</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44e9e-134">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="44e9e-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="44e9e-135">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="44e9e-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="44e9e-136">Calificadores: WmiDataId (1)</span><span class="sxs-lookup"><span data-stu-id="44e9e-136">Qualifiers: WmiDataId(1)</span></span>
</dt> </dl>

<span data-ttu-id="44e9e-137">Identificador del proceso asociado a la solicitud.</span><span class="sxs-lookup"><span data-stu-id="44e9e-137">Identifier of the process associated with the request.</span></span>

</dd> <dt>

<span data-ttu-id="44e9e-138">saddr</span><span class="sxs-lookup"><span data-stu-id="44e9e-138">saddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44e9e-139">Tipo de datos: **objeto**</span><span class="sxs-lookup"><span data-stu-id="44e9e-139">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="44e9e-140">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="44e9e-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="44e9e-141">Calificadores: WmiDataId (4), extensión ("IPAddrV6")</span><span class="sxs-lookup"><span data-stu-id="44e9e-141">Qualifiers: WmiDataId(4), Extension("IPAddrV6")</span></span>
</dt> </dl>

<span data-ttu-id="44e9e-142">Dirección IP de origen.</span><span class="sxs-lookup"><span data-stu-id="44e9e-142">Source IP address.</span></span>

</dd> <dt>

<span data-ttu-id="44e9e-143">seqnum</span><span class="sxs-lookup"><span data-stu-id="44e9e-143">seqnum</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44e9e-144">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="44e9e-144">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="44e9e-145">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="44e9e-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="44e9e-146">Calificadores: WmiDataId (9)</span><span class="sxs-lookup"><span data-stu-id="44e9e-146">Qualifiers: WmiDataId(9)</span></span>
</dt> </dl>

<span data-ttu-id="44e9e-147">Número de secuencia.</span><span class="sxs-lookup"><span data-stu-id="44e9e-147">Sequence number.</span></span>

</dd> <dt>

<span data-ttu-id="44e9e-148">tamaño</span><span class="sxs-lookup"><span data-stu-id="44e9e-148">size</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44e9e-149">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="44e9e-149">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="44e9e-150">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="44e9e-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="44e9e-151">Calificadores: WmiDataId (2)</span><span class="sxs-lookup"><span data-stu-id="44e9e-151">Qualifiers: WmiDataId(2)</span></span>
</dt> </dl>

<span data-ttu-id="44e9e-152">Tamaño del paquete.</span><span class="sxs-lookup"><span data-stu-id="44e9e-152">Size of the packet.</span></span>

</dd> <dt>

<span data-ttu-id="44e9e-153">deportivo</span><span class="sxs-lookup"><span data-stu-id="44e9e-153">sport</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44e9e-154">Tipo de datos: **objeto**</span><span class="sxs-lookup"><span data-stu-id="44e9e-154">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="44e9e-155">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="44e9e-155">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="44e9e-156">Calificadores: WmiDataId (6), extensión ("puerto")</span><span class="sxs-lookup"><span data-stu-id="44e9e-156">Qualifiers: WmiDataId(6), Extension("Port")</span></span>
</dt> </dl>

<span data-ttu-id="44e9e-157">Número de puerto de origen.</span><span class="sxs-lookup"><span data-stu-id="44e9e-157">Source port number.</span></span>

</dd> <dt>

<span data-ttu-id="44e9e-158">**startime**</span><span class="sxs-lookup"><span data-stu-id="44e9e-158">**startime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44e9e-159">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="44e9e-159">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="44e9e-160">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="44e9e-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="44e9e-161">Calificadores: WmiDataId (7)</span><span class="sxs-lookup"><span data-stu-id="44e9e-161">Qualifiers: WmiDataId(7)</span></span>
</dt> </dl>

<span data-ttu-id="44e9e-162">Iniciar hora de solicitud de envío.</span><span class="sxs-lookup"><span data-stu-id="44e9e-162">Start send request time.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="44e9e-163">Requisitos</span><span class="sxs-lookup"><span data-stu-id="44e9e-163">Requirements</span></span>



| <span data-ttu-id="44e9e-164">Requisito</span><span class="sxs-lookup"><span data-stu-id="44e9e-164">Requirement</span></span> | <span data-ttu-id="44e9e-165">Value</span><span class="sxs-lookup"><span data-stu-id="44e9e-165">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="44e9e-166">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="44e9e-166">Minimum supported client</span></span><br/> | <span data-ttu-id="44e9e-167">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="44e9e-167">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="44e9e-168">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="44e9e-168">Minimum supported server</span></span><br/> | <span data-ttu-id="44e9e-169">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="44e9e-169">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="44e9e-170">Vea también</span><span class="sxs-lookup"><span data-stu-id="44e9e-170">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44e9e-171">**Luego**</span><span class="sxs-lookup"><span data-stu-id="44e9e-171">**TcpIp**</span></span>](tcpip.md)
</dt> </dl>

 

 




