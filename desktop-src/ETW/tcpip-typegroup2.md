---
description: Esta clase es la clase de tipo de evento para la conexión TCP/IP de IPv4 y los eventos Accept. La siguiente sintaxis se simplifica desde el código MOF.
ms.assetid: a9b33ceb-7d50-4cd7-8224-0b2cf895b3b4
title: TcpIp_TypeGroup2 (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TcpIp_TypeGroup2
- TcpIp_TypeGroup2.PID
- TcpIp_TypeGroup2.size
- TcpIp_TypeGroup2.daddr
- TcpIp_TypeGroup2.saddr
- TcpIp_TypeGroup2.dport
- TcpIp_TypeGroup2.sport
- TcpIp_TypeGroup2.mss
- TcpIp_TypeGroup2.sackopt
- TcpIp_TypeGroup2.tsopt
- TcpIp_TypeGroup2.wsopt
- TcpIp_TypeGroup2.rcvwin
- TcpIp_TypeGroup2.rcvwinscale
- TcpIp_TypeGroup2.sndwinscale
- TcpIp_TypeGroup2.seqnum
- TcpIp_TypeGroup2.connid
api_type:
- NA
api_location: ''
ms.openlocfilehash: 398b6b0e2b7e4684481f13f73bdd94ef4cd76829
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104544318"
---
# <a name="tcpip_typegroup2-class"></a><span data-ttu-id="d6dfd-104">\_Clase TypeGroup2 de TCPIP</span><span class="sxs-lookup"><span data-stu-id="d6dfd-104">TcpIp\_TypeGroup2 class</span></span>

<span data-ttu-id="d6dfd-105">Esta clase es la clase de tipo de evento para la conexión TCP/IP de IPv4 y los eventos Accept.</span><span class="sxs-lookup"><span data-stu-id="d6dfd-105">This class is the event type class for IPv4 TCP/IP connect and accept events.</span></span>

<span data-ttu-id="d6dfd-106">La siguiente sintaxis se simplifica desde el código MOF.</span><span class="sxs-lookup"><span data-stu-id="d6dfd-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="d6dfd-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d6dfd-107">Syntax</span></span>

``` syntax
[EventType{12, 15}, EventTypeName{"ConnectIPV4", "AcceptIPV4"}]
class TcpIp_TypeGroup2 : TcpIp
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

## <a name="members"></a><span data-ttu-id="d6dfd-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="d6dfd-108">Members</span></span>

<span data-ttu-id="d6dfd-109">La **clase \_ TypeGroup2 de TCPIP** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="d6dfd-109">The **TcpIp\_TypeGroup2** class has these types of members:</span></span>

-   [<span data-ttu-id="d6dfd-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d6dfd-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d6dfd-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d6dfd-111">Properties</span></span>

<span data-ttu-id="d6dfd-112">La **clase \_ TypeGroup2 de TCPIP** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="d6dfd-112">The **TcpIp\_TypeGroup2** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d6dfd-113">**connid**</span><span class="sxs-lookup"><span data-stu-id="d6dfd-113">**connid**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d6dfd-114">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d6dfd-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d6dfd-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d6dfd-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d6dfd-116">Calificadores: **WmiDataId (15)**, **puntero**</span><span class="sxs-lookup"><span data-stu-id="d6dfd-116">Qualifiers: **WmiDataId(15)**, **Pointer**</span></span>
</dt> </dl>

<span data-ttu-id="d6dfd-117">Un identificador de conexión único para correlacionar los eventos que pertenecen a la misma conexión.</span><span class="sxs-lookup"><span data-stu-id="d6dfd-117">A unique connection identifier to correlate events belonging to the same connection.</span></span>

</dd> <dt>

<span data-ttu-id="d6dfd-118">**daddr**</span><span class="sxs-lookup"><span data-stu-id="d6dfd-118">**daddr**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d6dfd-119">Tipo de datos: **objeto**</span><span class="sxs-lookup"><span data-stu-id="d6dfd-119">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="d6dfd-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d6dfd-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d6dfd-121">Calificadores: **WmiDataId (3)**, **extensión ("IPAddrV4")**</span><span class="sxs-lookup"><span data-stu-id="d6dfd-121">Qualifiers: **WmiDataId(3)**, **Extension("IPAddrV4")**</span></span>
</dt> </dl>

<span data-ttu-id="d6dfd-122">Dirección IP de destino.</span><span class="sxs-lookup"><span data-stu-id="d6dfd-122">Destination IP address.</span></span>

</dd> <dt>

<span data-ttu-id="d6dfd-123">**dport**</span><span class="sxs-lookup"><span data-stu-id="d6dfd-123">**dport**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d6dfd-124">Tipo de datos: **objeto**</span><span class="sxs-lookup"><span data-stu-id="d6dfd-124">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="d6dfd-125">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d6dfd-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d6dfd-126">Calificadores: **WmiDataId (5)**, **extensión ("puerto")**</span><span class="sxs-lookup"><span data-stu-id="d6dfd-126">Qualifiers: **WmiDataId(5)**, **Extension("Port")**</span></span>
</dt> </dl>

<span data-ttu-id="d6dfd-127">Número de puerto de destino.</span><span class="sxs-lookup"><span data-stu-id="d6dfd-127">Destination port number.</span></span>

</dd> <dt>

<span data-ttu-id="d6dfd-128">**MSS**</span><span class="sxs-lookup"><span data-stu-id="d6dfd-128">**mss**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d6dfd-129">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d6dfd-129">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d6dfd-130">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d6dfd-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d6dfd-131">Calificadores: **WmiDataId (7)**</span><span class="sxs-lookup"><span data-stu-id="d6dfd-131">Qualifiers: **WmiDataId(7)**</span></span>
</dt> </dl>

<span data-ttu-id="d6dfd-132">Tamaño máximo del segmento.</span><span class="sxs-lookup"><span data-stu-id="d6dfd-132">Maximum segment size.</span></span>

</dd> <dt>

<span data-ttu-id="d6dfd-133">**ID**</span><span class="sxs-lookup"><span data-stu-id="d6dfd-133">**PID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d6dfd-134">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d6dfd-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d6dfd-135">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d6dfd-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d6dfd-136">Calificadores: **WmiDataId (1)**</span><span class="sxs-lookup"><span data-stu-id="d6dfd-136">Qualifiers: **WmiDataId(1)**</span></span>
</dt> </dl>

<span data-ttu-id="d6dfd-137">Identificador del proceso asociado a la solicitud.</span><span class="sxs-lookup"><span data-stu-id="d6dfd-137">Identifier of the process associated with the request.</span></span>

</dd> <dt>

<span data-ttu-id="d6dfd-138">**rcvwin**</span><span class="sxs-lookup"><span data-stu-id="d6dfd-138">**rcvwin**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d6dfd-139">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d6dfd-139">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d6dfd-140">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d6dfd-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d6dfd-141">Calificadores: **WmiDataId (11)**</span><span class="sxs-lookup"><span data-stu-id="d6dfd-141">Qualifiers: **WmiDataId(11)**</span></span>
</dt> </dl>

<span data-ttu-id="d6dfd-142">Tamaño de la ventana de recepción de TCP.</span><span class="sxs-lookup"><span data-stu-id="d6dfd-142">TCP Receive Window size.</span></span>

</dd> <dt>

<span data-ttu-id="d6dfd-143">**rcvwinscale**</span><span class="sxs-lookup"><span data-stu-id="d6dfd-143">**rcvwinscale**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d6dfd-144">Tipo de datos: **sint16**</span><span class="sxs-lookup"><span data-stu-id="d6dfd-144">Data type: **sint16**</span></span>
</dt> <dt>

<span data-ttu-id="d6dfd-145">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d6dfd-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d6dfd-146">Calificadores: **WmiDataId (12)**</span><span class="sxs-lookup"><span data-stu-id="d6dfd-146">Qualifiers: **WmiDataId(12)**</span></span>
</dt> </dl>

<span data-ttu-id="d6dfd-147">Factor de escala de la ventana de recepción de TCP.</span><span class="sxs-lookup"><span data-stu-id="d6dfd-147">TCP Receive Window Scaling factor.</span></span>

</dd> <dt>

<span data-ttu-id="d6dfd-148">**sackopt**</span><span class="sxs-lookup"><span data-stu-id="d6dfd-148">**sackopt**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d6dfd-149">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d6dfd-149">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d6dfd-150">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d6dfd-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d6dfd-151">Calificadores: **WmiDataId (8)**</span><span class="sxs-lookup"><span data-stu-id="d6dfd-151">Qualifiers: **WmiDataId(8)**</span></span>
</dt> </dl>

<span data-ttu-id="d6dfd-152">Opción de confirmación selectiva (SACK) en el encabezado TCP.</span><span class="sxs-lookup"><span data-stu-id="d6dfd-152">Selective Acknowledgment (SACK) option in TCP header.</span></span>

</dd> <dt>

<span data-ttu-id="d6dfd-153">**saddr**</span><span class="sxs-lookup"><span data-stu-id="d6dfd-153">**saddr**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d6dfd-154">Tipo de datos: **objeto**</span><span class="sxs-lookup"><span data-stu-id="d6dfd-154">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="d6dfd-155">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d6dfd-155">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d6dfd-156">Calificadores: **WmiDataId (4)**, **extensión ("IPAddrV4")**</span><span class="sxs-lookup"><span data-stu-id="d6dfd-156">Qualifiers: **WmiDataId(4)**, **Extension("IPAddrV4")**</span></span>
</dt> </dl>

<span data-ttu-id="d6dfd-157">Dirección IP de origen.</span><span class="sxs-lookup"><span data-stu-id="d6dfd-157">Source IP address.</span></span>

</dd> <dt>

<span data-ttu-id="d6dfd-158">**seqnum**</span><span class="sxs-lookup"><span data-stu-id="d6dfd-158">**seqnum**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d6dfd-159">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d6dfd-159">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d6dfd-160">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d6dfd-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d6dfd-161">Calificadores: **WmiDataId (14)**</span><span class="sxs-lookup"><span data-stu-id="d6dfd-161">Qualifiers: **WmiDataId(14)**</span></span>
</dt> </dl>

<span data-ttu-id="d6dfd-162">Número de secuencia.</span><span class="sxs-lookup"><span data-stu-id="d6dfd-162">Sequence number.</span></span>

</dd> <dt>

<span data-ttu-id="d6dfd-163">**size**</span><span class="sxs-lookup"><span data-stu-id="d6dfd-163">**size**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d6dfd-164">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d6dfd-164">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d6dfd-165">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d6dfd-165">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d6dfd-166">Calificadores: **WmiDataId (2)**</span><span class="sxs-lookup"><span data-stu-id="d6dfd-166">Qualifiers: **WmiDataId(2)**</span></span>
</dt> </dl>

<span data-ttu-id="d6dfd-167">Tamaño del paquete.</span><span class="sxs-lookup"><span data-stu-id="d6dfd-167">Size of the packet.</span></span>

</dd> <dt>

<span data-ttu-id="d6dfd-168">**sndwinscale**</span><span class="sxs-lookup"><span data-stu-id="d6dfd-168">**sndwinscale**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d6dfd-169">Tipo de datos: **sint16**</span><span class="sxs-lookup"><span data-stu-id="d6dfd-169">Data type: **sint16**</span></span>
</dt> <dt>

<span data-ttu-id="d6dfd-170">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d6dfd-170">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d6dfd-171">Calificadores: **WmiDataId (13)**</span><span class="sxs-lookup"><span data-stu-id="d6dfd-171">Qualifiers: **WmiDataId(13)**</span></span>
</dt> </dl>

<span data-ttu-id="d6dfd-172">Factor de escala de la ventana de envío TCP.</span><span class="sxs-lookup"><span data-stu-id="d6dfd-172">TCP Send Window Scaling factor.</span></span>

</dd> <dt>

<span data-ttu-id="d6dfd-173">**deportivo**</span><span class="sxs-lookup"><span data-stu-id="d6dfd-173">**sport**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d6dfd-174">Tipo de datos: **objeto**</span><span class="sxs-lookup"><span data-stu-id="d6dfd-174">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="d6dfd-175">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d6dfd-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d6dfd-176">Calificadores: **WmiDataId (6)**, **extensión ("puerto")**</span><span class="sxs-lookup"><span data-stu-id="d6dfd-176">Qualifiers: **WmiDataId(6)**, **Extension("Port")**</span></span>
</dt> </dl>

<span data-ttu-id="d6dfd-177">Número de puerto de origen.</span><span class="sxs-lookup"><span data-stu-id="d6dfd-177">Source port number.</span></span>

</dd> <dt>

<span data-ttu-id="d6dfd-178">**tsopt**</span><span class="sxs-lookup"><span data-stu-id="d6dfd-178">**tsopt**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d6dfd-179">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d6dfd-179">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d6dfd-180">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d6dfd-180">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d6dfd-181">Calificadores: **WmiDataId (9)**</span><span class="sxs-lookup"><span data-stu-id="d6dfd-181">Qualifiers: **WmiDataId(9)**</span></span>
</dt> </dl>

<span data-ttu-id="d6dfd-182">Opción de marca de tiempo en el encabezado TCP.</span><span class="sxs-lookup"><span data-stu-id="d6dfd-182">Time Stamp option in TCP header.</span></span>

</dd> <dt>

<span data-ttu-id="d6dfd-183">**wsopt**</span><span class="sxs-lookup"><span data-stu-id="d6dfd-183">**wsopt**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d6dfd-184">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d6dfd-184">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d6dfd-185">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d6dfd-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d6dfd-186">Calificadores: **WmiDataId (10)**</span><span class="sxs-lookup"><span data-stu-id="d6dfd-186">Qualifiers: **WmiDataId(10)**</span></span>
</dt> </dl>

<span data-ttu-id="d6dfd-187">Opción de escala de ventana en el encabezado TCP.</span><span class="sxs-lookup"><span data-stu-id="d6dfd-187">Window Scale option in TCP header.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d6dfd-188">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d6dfd-188">Requirements</span></span>



| <span data-ttu-id="d6dfd-189">Requisito</span><span class="sxs-lookup"><span data-stu-id="d6dfd-189">Requirement</span></span> | <span data-ttu-id="d6dfd-190">Value</span><span class="sxs-lookup"><span data-stu-id="d6dfd-190">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="d6dfd-191">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d6dfd-191">Minimum supported client</span></span><br/> | <span data-ttu-id="d6dfd-192">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="d6dfd-192">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="d6dfd-193">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d6dfd-193">Minimum supported server</span></span><br/> | <span data-ttu-id="d6dfd-194">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="d6dfd-194">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d6dfd-195">Vea también</span><span class="sxs-lookup"><span data-stu-id="d6dfd-195">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d6dfd-196">**Luego**</span><span class="sxs-lookup"><span data-stu-id="d6dfd-196">**TcpIp**</span></span>](tcpip.md)
</dt> </dl>

 

 




