---
description: Esta clase es la clase de tipo de evento para los eventos de envío de TCP/IP IPv4. La siguiente sintaxis se simplifica desde el código MOF.
ms.assetid: 51a61257-fcbf-4724-80e4-12bdf45b359e
title: TcpIp_SendIPV4 (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TcpIp_SendIPV4
- TcpIp_SendIPV4.PID
- TcpIp_SendIPV4.size
- TcpIp_SendIPV4.daddr
- TcpIp_SendIPV4.saddr
- TcpIp_SendIPV4.dport
- TcpIp_SendIPV4.sport
- TcpIp_SendIPV4.startime
- TcpIp_SendIPV4.endtime
- TcpIp_SendIPV4.seqnum
- TcpIp_SendIPV4.connid
api_type:
- NA
api_location: ''
ms.openlocfilehash: a255c8a262c53e6dad4654946171fc19a43c6f5f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001496"
---
# <a name="tcpip_sendipv4-class"></a><span data-ttu-id="61bb7-104">\_Clase SendIPV4 de TCPIP</span><span class="sxs-lookup"><span data-stu-id="61bb7-104">TcpIp\_SendIPV4 class</span></span>

<span data-ttu-id="61bb7-105">Esta clase es la clase de tipo de evento para los eventos de envío de TCP/IP IPv4.</span><span class="sxs-lookup"><span data-stu-id="61bb7-105">This class is the event type class for IPv4 TCP/IP send events.</span></span>

<span data-ttu-id="61bb7-106">La siguiente sintaxis se simplifica desde el código MOF.</span><span class="sxs-lookup"><span data-stu-id="61bb7-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="61bb7-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="61bb7-107">Syntax</span></span>

``` syntax
[EventType{10}, EventTypeName{"SendIPV4"}]
class TcpIp_SendIPV4 : TcpIp
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

## <a name="members"></a><span data-ttu-id="61bb7-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="61bb7-108">Members</span></span>

<span data-ttu-id="61bb7-109">La **clase \_ SendIPV4 de TCPIP** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="61bb7-109">The **TcpIp\_SendIPV4** class has these types of members:</span></span>

-   [<span data-ttu-id="61bb7-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="61bb7-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="61bb7-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="61bb7-111">Properties</span></span>

<span data-ttu-id="61bb7-112">La **clase \_ SendIPV4 de TCPIP** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="61bb7-112">The **TcpIp\_SendIPV4** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="61bb7-113">connid</span><span class="sxs-lookup"><span data-stu-id="61bb7-113">connid</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61bb7-114">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="61bb7-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="61bb7-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="61bb7-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="61bb7-116">Calificadores: WmiDataId (10), puntero</span><span class="sxs-lookup"><span data-stu-id="61bb7-116">Qualifiers: WmiDataId(10), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="61bb7-117">Un identificador de conexión único para correlacionar los eventos que pertenecen a la misma conexión.</span><span class="sxs-lookup"><span data-stu-id="61bb7-117">A unique connection identifier to correlate events belonging to the same connection.</span></span>

</dd> <dt>

<span data-ttu-id="61bb7-118">daddr</span><span class="sxs-lookup"><span data-stu-id="61bb7-118">daddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61bb7-119">Tipo de datos: **objeto**</span><span class="sxs-lookup"><span data-stu-id="61bb7-119">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="61bb7-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="61bb7-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="61bb7-121">Calificadores: WmiDataId (3), extensión ("IPAddrV4")</span><span class="sxs-lookup"><span data-stu-id="61bb7-121">Qualifiers: WmiDataId(3), Extension("IPAddrV4")</span></span>
</dt> </dl>

<span data-ttu-id="61bb7-122">Dirección IP de destino.</span><span class="sxs-lookup"><span data-stu-id="61bb7-122">Destination IP address.</span></span>

</dd> <dt>

<span data-ttu-id="61bb7-123">dport</span><span class="sxs-lookup"><span data-stu-id="61bb7-123">dport</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61bb7-124">Tipo de datos: **objeto**</span><span class="sxs-lookup"><span data-stu-id="61bb7-124">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="61bb7-125">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="61bb7-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="61bb7-126">Calificadores: WmiDataId (5), extensión ("puerto")</span><span class="sxs-lookup"><span data-stu-id="61bb7-126">Qualifiers: WmiDataId(5), Extension("Port")</span></span>
</dt> </dl>

<span data-ttu-id="61bb7-127">Número de puerto de destino.</span><span class="sxs-lookup"><span data-stu-id="61bb7-127">Destination port number.</span></span>

</dd> <dt>

<span data-ttu-id="61bb7-128">**EndTime**</span><span class="sxs-lookup"><span data-stu-id="61bb7-128">**endtime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61bb7-129">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="61bb7-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="61bb7-130">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="61bb7-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="61bb7-131">Calificadores: WmiDataId (8)</span><span class="sxs-lookup"><span data-stu-id="61bb7-131">Qualifiers: WmiDataId(8)</span></span>
</dt> </dl>

<span data-ttu-id="61bb7-132">Fin del tiempo de solicitud de envío.</span><span class="sxs-lookup"><span data-stu-id="61bb7-132">End send request time.</span></span>

</dd> <dt>

<span data-ttu-id="61bb7-133">PID</span><span class="sxs-lookup"><span data-stu-id="61bb7-133">PID</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61bb7-134">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="61bb7-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="61bb7-135">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="61bb7-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="61bb7-136">Calificadores: WmiDataId (1)</span><span class="sxs-lookup"><span data-stu-id="61bb7-136">Qualifiers: WmiDataId(1)</span></span>
</dt> </dl>

<span data-ttu-id="61bb7-137">Identificador del proceso asociado a la solicitud.</span><span class="sxs-lookup"><span data-stu-id="61bb7-137">Identifier of the process associated with the request.</span></span>

</dd> <dt>

<span data-ttu-id="61bb7-138">saddr</span><span class="sxs-lookup"><span data-stu-id="61bb7-138">saddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61bb7-139">Tipo de datos: **objeto**</span><span class="sxs-lookup"><span data-stu-id="61bb7-139">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="61bb7-140">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="61bb7-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="61bb7-141">Calificadores: WmiDataId (4), extensión ("IPAddrV4")</span><span class="sxs-lookup"><span data-stu-id="61bb7-141">Qualifiers: WmiDataId(4), Extension("IPAddrV4")</span></span>
</dt> </dl>

<span data-ttu-id="61bb7-142">Dirección IP de origen.</span><span class="sxs-lookup"><span data-stu-id="61bb7-142">Source IP address.</span></span>

</dd> <dt>

<span data-ttu-id="61bb7-143">seqnum</span><span class="sxs-lookup"><span data-stu-id="61bb7-143">seqnum</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61bb7-144">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="61bb7-144">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="61bb7-145">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="61bb7-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="61bb7-146">Calificadores: WmiDataId (9)</span><span class="sxs-lookup"><span data-stu-id="61bb7-146">Qualifiers: WmiDataId(9)</span></span>
</dt> </dl>

<span data-ttu-id="61bb7-147">Número de secuencia.</span><span class="sxs-lookup"><span data-stu-id="61bb7-147">Sequence number.</span></span>

</dd> <dt>

<span data-ttu-id="61bb7-148">tamaño</span><span class="sxs-lookup"><span data-stu-id="61bb7-148">size</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61bb7-149">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="61bb7-149">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="61bb7-150">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="61bb7-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="61bb7-151">Calificadores: WmiDataId (2)</span><span class="sxs-lookup"><span data-stu-id="61bb7-151">Qualifiers: WmiDataId(2)</span></span>
</dt> </dl>

<span data-ttu-id="61bb7-152">Tamaño del paquete.</span><span class="sxs-lookup"><span data-stu-id="61bb7-152">Size of the packet.</span></span>

</dd> <dt>

<span data-ttu-id="61bb7-153">deportivo</span><span class="sxs-lookup"><span data-stu-id="61bb7-153">sport</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61bb7-154">Tipo de datos: **objeto**</span><span class="sxs-lookup"><span data-stu-id="61bb7-154">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="61bb7-155">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="61bb7-155">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="61bb7-156">Calificadores: WmiDataId (6), extensión ("puerto")</span><span class="sxs-lookup"><span data-stu-id="61bb7-156">Qualifiers: WmiDataId(6), Extension("Port")</span></span>
</dt> </dl>

<span data-ttu-id="61bb7-157">Número de puerto de origen.</span><span class="sxs-lookup"><span data-stu-id="61bb7-157">Source port number.</span></span>

</dd> <dt>

<span data-ttu-id="61bb7-158">**startime**</span><span class="sxs-lookup"><span data-stu-id="61bb7-158">**startime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="61bb7-159">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="61bb7-159">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="61bb7-160">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="61bb7-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="61bb7-161">Calificadores: WmiDataId (7)</span><span class="sxs-lookup"><span data-stu-id="61bb7-161">Qualifiers: WmiDataId(7)</span></span>
</dt> </dl>

<span data-ttu-id="61bb7-162">Iniciar hora de solicitud de envío.</span><span class="sxs-lookup"><span data-stu-id="61bb7-162">Start send request time.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="61bb7-163">Requisitos</span><span class="sxs-lookup"><span data-stu-id="61bb7-163">Requirements</span></span>



| <span data-ttu-id="61bb7-164">Requisito</span><span class="sxs-lookup"><span data-stu-id="61bb7-164">Requirement</span></span> | <span data-ttu-id="61bb7-165">Value</span><span class="sxs-lookup"><span data-stu-id="61bb7-165">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="61bb7-166">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="61bb7-166">Minimum supported client</span></span><br/> | <span data-ttu-id="61bb7-167">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="61bb7-167">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="61bb7-168">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="61bb7-168">Minimum supported server</span></span><br/> | <span data-ttu-id="61bb7-169">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="61bb7-169">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="61bb7-170">Vea también</span><span class="sxs-lookup"><span data-stu-id="61bb7-170">See also</span></span>

<dl> <dt>

[<span data-ttu-id="61bb7-171">**Luego**</span><span class="sxs-lookup"><span data-stu-id="61bb7-171">**TcpIp**</span></span>](tcpip.md)
</dt> </dl>

 

 




