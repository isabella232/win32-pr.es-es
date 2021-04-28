---
description: 'TcpIp_V0_TypeGroup1 clase : esta clase es la clase de tipo de evento para eventos TCP/IP. La sintaxis siguiente se simplifica a partir del código MOF.'
ms.assetid: 007f0744-8b74-4c57-85bc-f6bdb20bffa7
title: TcpIp_V0_TypeGroup1 clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TcpIp_V0_TypeGroup1
- TcpIp_V0_TypeGroup1.daddr
- TcpIp_V0_TypeGroup1.saddr
- TcpIp_V0_TypeGroup1.dport
- TcpIp_V0_TypeGroup1.sport
- TcpIp_V0_TypeGroup1.size
- TcpIp_V0_TypeGroup1.PID
api_type:
- NA
api_location: ''
ms.openlocfilehash: 96df2214aff9b5be6f10a1f08f6e6ea2e015c6b5
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105793"
---
# <a name="tcpip_v0_typegroup1-class"></a><span data-ttu-id="79700-104">Clase \_ TypeGroup1 de TcpIp V0 \_</span><span class="sxs-lookup"><span data-stu-id="79700-104">TcpIp\_V0\_TypeGroup1 class</span></span>

<span data-ttu-id="79700-105">Esta clase es la clase de tipo de evento para eventos TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="79700-105">This class is the event type class for TCP/IP events.</span></span>

<span data-ttu-id="79700-106">La sintaxis siguiente se simplifica a partir del código MOF.</span><span class="sxs-lookup"><span data-stu-id="79700-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="79700-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="79700-107">Syntax</span></span>

``` syntax
[EventType{10, 11, 12, 13, 14, 15}, EventTypeName{"Send", "Recv", "Connect", "Disconnect", "Retransmit", "Accept"}]
class TcpIp_V0_TypeGroup1 : TcpIp_V0
{
  object daddr;
  object saddr;
  object dport;
  object sport;
  uint32 size;
  uint32 PID;
};
```

## <a name="members"></a><span data-ttu-id="79700-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="79700-108">Members</span></span>

<span data-ttu-id="79700-109">La **clase \_ \_ TypeGroup1 de TcpIp V0** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="79700-109">The **TcpIp\_V0\_TypeGroup1** class has these types of members:</span></span>

-   [<span data-ttu-id="79700-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="79700-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="79700-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="79700-111">Properties</span></span>

<span data-ttu-id="79700-112">La **clase \_ \_ TypeGroup1 de TcpIp V0** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="79700-112">The **TcpIp\_V0\_TypeGroup1** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="79700-113">dr</span><span class="sxs-lookup"><span data-stu-id="79700-113">daddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79700-114">Tipo de datos: **objeto**</span><span class="sxs-lookup"><span data-stu-id="79700-114">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="79700-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="79700-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="79700-116">Calificadores: WmiDataId(1), Extension("IPAddr")</span><span class="sxs-lookup"><span data-stu-id="79700-116">Qualifiers: WmiDataId(1), Extension("IPAddr")</span></span>
</dt> </dl>

<span data-ttu-id="79700-117">Dirección IP de destino.</span><span class="sxs-lookup"><span data-stu-id="79700-117">Destination IP address.</span></span>

</dd> <dt>

<span data-ttu-id="79700-118">dport</span><span class="sxs-lookup"><span data-stu-id="79700-118">dport</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79700-119">Tipo de datos: **objeto**</span><span class="sxs-lookup"><span data-stu-id="79700-119">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="79700-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="79700-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="79700-121">Calificadores: WmiDataId(3), Extension("Port")</span><span class="sxs-lookup"><span data-stu-id="79700-121">Qualifiers: WmiDataId(3), Extension("Port")</span></span>
</dt> </dl>

<span data-ttu-id="79700-122">Número de puerto de destino.</span><span class="sxs-lookup"><span data-stu-id="79700-122">Destination port number.</span></span>

</dd> <dt>

<span data-ttu-id="79700-123">PID</span><span class="sxs-lookup"><span data-stu-id="79700-123">PID</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79700-124">Tipo de datos: **uint32**</span><span class="sxs-lookup"><span data-stu-id="79700-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="79700-125">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="79700-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="79700-126">Calificadores: WmiDataId(6)</span><span class="sxs-lookup"><span data-stu-id="79700-126">Qualifiers: WmiDataId(6)</span></span>
</dt> </dl>

<span data-ttu-id="79700-127">Identificador del proceso asociado a la solicitud.</span><span class="sxs-lookup"><span data-stu-id="79700-127">Identifier of the process associated with the request.</span></span>

</dd> <dt>

<span data-ttu-id="79700-128">saddr</span><span class="sxs-lookup"><span data-stu-id="79700-128">saddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79700-129">Tipo de datos: **objeto**</span><span class="sxs-lookup"><span data-stu-id="79700-129">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="79700-130">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="79700-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="79700-131">Calificadores: WmiDataId(2), Extension("IPAddr")</span><span class="sxs-lookup"><span data-stu-id="79700-131">Qualifiers: WmiDataId(2), Extension("IPAddr")</span></span>
</dt> </dl>

<span data-ttu-id="79700-132">Dirección IP de origen.</span><span class="sxs-lookup"><span data-stu-id="79700-132">Source IP address.</span></span>

</dd> <dt>

<span data-ttu-id="79700-133">tamaño</span><span class="sxs-lookup"><span data-stu-id="79700-133">size</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79700-134">Tipo de datos: **uint32**</span><span class="sxs-lookup"><span data-stu-id="79700-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="79700-135">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="79700-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="79700-136">Calificadores: WmiDataId(5)</span><span class="sxs-lookup"><span data-stu-id="79700-136">Qualifiers: WmiDataId(5)</span></span>
</dt> </dl>

<span data-ttu-id="79700-137">Tamaño del paquete.</span><span class="sxs-lookup"><span data-stu-id="79700-137">Size of the packet.</span></span>

</dd> <dt>

<span data-ttu-id="79700-138">Deporte</span><span class="sxs-lookup"><span data-stu-id="79700-138">sport</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="79700-139">Tipo de datos: **objeto**</span><span class="sxs-lookup"><span data-stu-id="79700-139">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="79700-140">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="79700-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="79700-141">Calificadores: WmiDataId(4), Extension("Port")</span><span class="sxs-lookup"><span data-stu-id="79700-141">Qualifiers: WmiDataId(4), Extension("Port")</span></span>
</dt> </dl>

<span data-ttu-id="79700-142">Número de puerto de origen.</span><span class="sxs-lookup"><span data-stu-id="79700-142">Source port number.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="79700-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="79700-143">Requirements</span></span>



| <span data-ttu-id="79700-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="79700-144">Requirement</span></span> | <span data-ttu-id="79700-145">Valor</span><span class="sxs-lookup"><span data-stu-id="79700-145">Value</span></span> |
|-------------------------------------|---------------------------------------------|
| <span data-ttu-id="79700-146">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="79700-146">Minimum supported client</span></span><br/> | <span data-ttu-id="79700-147">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="79700-147">Windows XP \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="79700-148">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="79700-148">Minimum supported server</span></span><br/> | <span data-ttu-id="79700-149">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="79700-149">None supported</span></span><br/>                   |



## <a name="see-also"></a><span data-ttu-id="79700-150">Consulte también</span><span class="sxs-lookup"><span data-stu-id="79700-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="79700-151">**TcpIp \_ V0**</span><span class="sxs-lookup"><span data-stu-id="79700-151">**TcpIp\_V0**</span></span>](tcpip-v0.md)
</dt> </dl>

 

 




