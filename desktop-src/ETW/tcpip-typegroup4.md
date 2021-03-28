---
description: Esta clase es la clase de tipo de evento para la conexión TCP/IP IPv6 y los eventos Accept. La siguiente sintaxis se simplifica desde el código MOF.
ms.assetid: c6c0463a-0058-47cf-9235-d2b621f30fb4
title: TcpIp_TypeGroup4 (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TcpIp_TypeGroup4
- TcpIp_TypeGroup4.PID
- TcpIp_TypeGroup4.size
- TcpIp_TypeGroup4.daddr
- TcpIp_TypeGroup4.saddr
- TcpIp_TypeGroup4.dport
- TcpIp_TypeGroup4.sport
- TcpIp_TypeGroup4.mss
- TcpIp_TypeGroup4.sackopt
- TcpIp_TypeGroup4.tsopt
- TcpIp_TypeGroup4.wsopt
- TcpIp_TypeGroup4.rcvwin
- TcpIp_TypeGroup4.rcvwinscale
- TcpIp_TypeGroup4.sndwinscale
- TcpIp_TypeGroup4.seqnum
- TcpIp_TypeGroup4.connid
api_type:
- NA
api_location: ''
ms.openlocfilehash: 942e5897db6771c0c3a9df965e5e889eaf71c841
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103811839"
---
# <a name="tcpip_typegroup4-class"></a><span data-ttu-id="4eb3a-104">\_Clase TypeGroup4 de TCPIP</span><span class="sxs-lookup"><span data-stu-id="4eb3a-104">TcpIp\_TypeGroup4 class</span></span>

<span data-ttu-id="4eb3a-105">Esta clase es la clase de tipo de evento para la conexión TCP/IP IPv6 y los eventos Accept.</span><span class="sxs-lookup"><span data-stu-id="4eb3a-105">This class is the event type class for IPv6 TCP/IP connect and accept events.</span></span>

<span data-ttu-id="4eb3a-106">La siguiente sintaxis se simplifica desde el código MOF.</span><span class="sxs-lookup"><span data-stu-id="4eb3a-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="4eb3a-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4eb3a-107">Syntax</span></span>

``` syntax
[EventType{28, 31}, EventTypeName{"ConnectIPV6", "AcceptIPV6"}]
class TcpIp_TypeGroup4 : TcpIp
{
  uint32 PID;
  uint32 size;
  object daddr;
  object saddr;
  object dport;
  object sport;
  uint16 mss;
  uint16 sackopt;
  uint16 tsopt;
  uint16 wsopt;
  uint32 rcvwin;
  sint16 rcvwinscale;
  sint16 sndwinscale;
  uint32 seqnum;
  uint32 connid;
};
```

## <a name="members"></a><span data-ttu-id="4eb3a-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="4eb3a-108">Members</span></span>

<span data-ttu-id="4eb3a-109">La **clase \_ TypeGroup4 de TCPIP** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="4eb3a-109">The **TcpIp\_TypeGroup4** class has these types of members:</span></span>

-   [<span data-ttu-id="4eb3a-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="4eb3a-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4eb3a-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="4eb3a-111">Properties</span></span>

<span data-ttu-id="4eb3a-112">La **clase \_ TypeGroup4 de TCPIP** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="4eb3a-112">The **TcpIp\_TypeGroup4** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4eb3a-113">connid</span><span class="sxs-lookup"><span data-stu-id="4eb3a-113">connid</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4eb3a-114">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4eb3a-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4eb3a-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4eb3a-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4eb3a-116">Calificadores: WmiDataId (15), puntero</span><span class="sxs-lookup"><span data-stu-id="4eb3a-116">Qualifiers: WmiDataId(15), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="4eb3a-117">Un identificador de conexión único para correlacionar los eventos que pertenecen a la misma conexión.</span><span class="sxs-lookup"><span data-stu-id="4eb3a-117">A unique connection identifier to correlate events belonging to the same connection.</span></span>

</dd> <dt>

<span data-ttu-id="4eb3a-118">daddr</span><span class="sxs-lookup"><span data-stu-id="4eb3a-118">daddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4eb3a-119">Tipo de datos: **objeto**</span><span class="sxs-lookup"><span data-stu-id="4eb3a-119">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="4eb3a-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4eb3a-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4eb3a-121">Calificadores: WmiDataId (3), extensión ("IPAddrV6")</span><span class="sxs-lookup"><span data-stu-id="4eb3a-121">Qualifiers: WmiDataId(3), Extension("IPAddrV6")</span></span>
</dt> </dl>

<span data-ttu-id="4eb3a-122">Dirección IP de destino.</span><span class="sxs-lookup"><span data-stu-id="4eb3a-122">Destination IP address.</span></span>

</dd> <dt>

<span data-ttu-id="4eb3a-123">dport</span><span class="sxs-lookup"><span data-stu-id="4eb3a-123">dport</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4eb3a-124">Tipo de datos: **objeto**</span><span class="sxs-lookup"><span data-stu-id="4eb3a-124">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="4eb3a-125">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4eb3a-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4eb3a-126">Calificadores: WmiDataId (5), extensión ("puerto")</span><span class="sxs-lookup"><span data-stu-id="4eb3a-126">Qualifiers: WmiDataId(5), Extension("Port")</span></span>
</dt> </dl>

<span data-ttu-id="4eb3a-127">Número de puerto de destino.</span><span class="sxs-lookup"><span data-stu-id="4eb3a-127">Destination port number.</span></span>

</dd> <dt>

<span data-ttu-id="4eb3a-128">**MSS**</span><span class="sxs-lookup"><span data-stu-id="4eb3a-128">**mss**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4eb3a-129">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4eb3a-129">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4eb3a-130">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4eb3a-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4eb3a-131">Calificadores: WmiDataId (7)</span><span class="sxs-lookup"><span data-stu-id="4eb3a-131">Qualifiers: WmiDataId(7)</span></span>
</dt> </dl>

<span data-ttu-id="4eb3a-132">Tamaño máximo del segmento.</span><span class="sxs-lookup"><span data-stu-id="4eb3a-132">Maximum segment size.</span></span>

</dd> <dt>

<span data-ttu-id="4eb3a-133">PID</span><span class="sxs-lookup"><span data-stu-id="4eb3a-133">PID</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4eb3a-134">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4eb3a-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4eb3a-135">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4eb3a-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4eb3a-136">Calificadores: WmiDataId (1)</span><span class="sxs-lookup"><span data-stu-id="4eb3a-136">Qualifiers: WmiDataId(1)</span></span>
</dt> </dl>

<span data-ttu-id="4eb3a-137">Identificador del proceso asociado a la solicitud.</span><span class="sxs-lookup"><span data-stu-id="4eb3a-137">Identifier of the process associated with the request.</span></span>

</dd> <dt>

<span data-ttu-id="4eb3a-138">**rcvwin**</span><span class="sxs-lookup"><span data-stu-id="4eb3a-138">**rcvwin**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4eb3a-139">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4eb3a-139">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4eb3a-140">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4eb3a-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4eb3a-141">Calificadores: WmiDataId (11)</span><span class="sxs-lookup"><span data-stu-id="4eb3a-141">Qualifiers: WmiDataId(11)</span></span>
</dt> </dl>

<span data-ttu-id="4eb3a-142">Tamaño de la ventana de recepción de TCP.</span><span class="sxs-lookup"><span data-stu-id="4eb3a-142">TCP Receive Window size.</span></span>

</dd> <dt>

<span data-ttu-id="4eb3a-143">**rcvwinscale**</span><span class="sxs-lookup"><span data-stu-id="4eb3a-143">**rcvwinscale**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4eb3a-144">Tipo de datos: **sint16**</span><span class="sxs-lookup"><span data-stu-id="4eb3a-144">Data type: **sint16**</span></span>
</dt> <dt>

<span data-ttu-id="4eb3a-145">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4eb3a-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4eb3a-146">Calificadores: WmiDataId (12)</span><span class="sxs-lookup"><span data-stu-id="4eb3a-146">Qualifiers: WmiDataId(12)</span></span>
</dt> </dl>

<span data-ttu-id="4eb3a-147">Factor de escala de la ventana de recepción de TCP.</span><span class="sxs-lookup"><span data-stu-id="4eb3a-147">TCP Receive Window Scaling factor.</span></span>

</dd> <dt>

<span data-ttu-id="4eb3a-148">**sackopt**</span><span class="sxs-lookup"><span data-stu-id="4eb3a-148">**sackopt**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4eb3a-149">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4eb3a-149">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4eb3a-150">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4eb3a-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4eb3a-151">Calificadores: **WmiDataId** (8)</span><span class="sxs-lookup"><span data-stu-id="4eb3a-151">Qualifiers: **WmiDataId** (8)</span></span>
</dt> </dl>

<span data-ttu-id="4eb3a-152">Opción de confirmación selectiva (SACK) en el encabezado TCP.</span><span class="sxs-lookup"><span data-stu-id="4eb3a-152">Selective Acknowledgment (SACK) option in TCP header.</span></span>

</dd> <dt>

<span data-ttu-id="4eb3a-153">saddr</span><span class="sxs-lookup"><span data-stu-id="4eb3a-153">saddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4eb3a-154">Tipo de datos: **objeto**</span><span class="sxs-lookup"><span data-stu-id="4eb3a-154">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="4eb3a-155">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4eb3a-155">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4eb3a-156">Calificadores: WmiDataId (4), extensión ("IPAddrV6")</span><span class="sxs-lookup"><span data-stu-id="4eb3a-156">Qualifiers: WmiDataId(4), Extension("IPAddrV6")</span></span>
</dt> </dl>

<span data-ttu-id="4eb3a-157">Dirección IP de origen.</span><span class="sxs-lookup"><span data-stu-id="4eb3a-157">Source IP address.</span></span>

</dd> <dt>

<span data-ttu-id="4eb3a-158">seqnum</span><span class="sxs-lookup"><span data-stu-id="4eb3a-158">seqnum</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4eb3a-159">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4eb3a-159">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4eb3a-160">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4eb3a-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4eb3a-161">Calificadores: WmiDataId (14)</span><span class="sxs-lookup"><span data-stu-id="4eb3a-161">Qualifiers: WmiDataId(14)</span></span>
</dt> </dl>

<span data-ttu-id="4eb3a-162">Número de secuencia.</span><span class="sxs-lookup"><span data-stu-id="4eb3a-162">Sequence number.</span></span>

</dd> <dt>

<span data-ttu-id="4eb3a-163">tamaño</span><span class="sxs-lookup"><span data-stu-id="4eb3a-163">size</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4eb3a-164">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4eb3a-164">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4eb3a-165">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4eb3a-165">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4eb3a-166">Calificadores: WmiDataId (2)</span><span class="sxs-lookup"><span data-stu-id="4eb3a-166">Qualifiers: WmiDataId(2)</span></span>
</dt> </dl>

<span data-ttu-id="4eb3a-167">Tamaño del paquete.</span><span class="sxs-lookup"><span data-stu-id="4eb3a-167">Size of the packet.</span></span>

</dd> <dt>

<span data-ttu-id="4eb3a-168">**sndwinscale**</span><span class="sxs-lookup"><span data-stu-id="4eb3a-168">**sndwinscale**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4eb3a-169">Tipo de datos: **sint16**</span><span class="sxs-lookup"><span data-stu-id="4eb3a-169">Data type: **sint16**</span></span>
</dt> <dt>

<span data-ttu-id="4eb3a-170">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4eb3a-170">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4eb3a-171">Calificadores: WmiDataId (13)</span><span class="sxs-lookup"><span data-stu-id="4eb3a-171">Qualifiers: WmiDataId(13)</span></span>
</dt> </dl>

<span data-ttu-id="4eb3a-172">Factor de escala de la ventana de envío TCP.</span><span class="sxs-lookup"><span data-stu-id="4eb3a-172">TCP Send Window Scaling factor.</span></span>

</dd> <dt>

<span data-ttu-id="4eb3a-173">deportivo</span><span class="sxs-lookup"><span data-stu-id="4eb3a-173">sport</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4eb3a-174">Tipo de datos: **objeto**</span><span class="sxs-lookup"><span data-stu-id="4eb3a-174">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="4eb3a-175">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4eb3a-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4eb3a-176">Calificadores: WmiDataId (6), extensión ("puerto")</span><span class="sxs-lookup"><span data-stu-id="4eb3a-176">Qualifiers: WmiDataId(6), Extension("Port")</span></span>
</dt> </dl>

<span data-ttu-id="4eb3a-177">Número de puerto de origen.</span><span class="sxs-lookup"><span data-stu-id="4eb3a-177">Source port number.</span></span>

</dd> <dt>

<span data-ttu-id="4eb3a-178">**tsopt**</span><span class="sxs-lookup"><span data-stu-id="4eb3a-178">**tsopt**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4eb3a-179">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4eb3a-179">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4eb3a-180">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4eb3a-180">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4eb3a-181">Calificadores: WmiDataId (9)</span><span class="sxs-lookup"><span data-stu-id="4eb3a-181">Qualifiers: WmiDataId(9)</span></span>
</dt> </dl>

<span data-ttu-id="4eb3a-182">Opción de marca de tiempo en el encabezado TCP.</span><span class="sxs-lookup"><span data-stu-id="4eb3a-182">Time Stamp option in TCP header.</span></span>

</dd> <dt>

<span data-ttu-id="4eb3a-183">**wsopt**</span><span class="sxs-lookup"><span data-stu-id="4eb3a-183">**wsopt**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4eb3a-184">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4eb3a-184">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4eb3a-185">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4eb3a-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4eb3a-186">Calificadores: WmiDataId (10)</span><span class="sxs-lookup"><span data-stu-id="4eb3a-186">Qualifiers: WmiDataId(10)</span></span>
</dt> </dl>

<span data-ttu-id="4eb3a-187">Opción de escala de ventana en el encabezado TCP.</span><span class="sxs-lookup"><span data-stu-id="4eb3a-187">Window Scale option in TCP header.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4eb3a-188">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4eb3a-188">Requirements</span></span>



| <span data-ttu-id="4eb3a-189">Requisito</span><span class="sxs-lookup"><span data-stu-id="4eb3a-189">Requirement</span></span> | <span data-ttu-id="4eb3a-190">Value</span><span class="sxs-lookup"><span data-stu-id="4eb3a-190">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="4eb3a-191">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4eb3a-191">Minimum supported client</span></span><br/> | <span data-ttu-id="4eb3a-192">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="4eb3a-192">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="4eb3a-193">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4eb3a-193">Minimum supported server</span></span><br/> | <span data-ttu-id="4eb3a-194">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="4eb3a-194">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="4eb3a-195">Vea también</span><span class="sxs-lookup"><span data-stu-id="4eb3a-195">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4eb3a-196">**Luego**</span><span class="sxs-lookup"><span data-stu-id="4eb3a-196">**TcpIp**</span></span>](tcpip.md)
</dt> </dl>

 

 




