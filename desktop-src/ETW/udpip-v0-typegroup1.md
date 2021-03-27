---
description: Esta clase es la clase de tipo de evento para eventos UDP/IP. La siguiente sintaxis se simplifica desde el código MOF.
ms.assetid: 834a761a-089b-4b93-9a6a-a1edf752b582
title: UdpIp_V0_TypeGroup1 (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UdpIp_V0_TypeGroup1
- UdpIp_V0_TypeGroup1.context
- UdpIp_V0_TypeGroup1.saddr
- UdpIp_V0_TypeGroup1.sport
- UdpIp_V0_TypeGroup1.size
- UdpIp_V0_TypeGroup1.daddr
- UdpIp_V0_TypeGroup1.dport
- UdpIp_V0_TypeGroup1.dsize
api_type:
- NA
api_location: ''
ms.openlocfilehash: 2813476bc2c820d1872e787dc047fafccd3b7d52
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002573"
---
# <a name="udpip_v0_typegroup1-class"></a><span data-ttu-id="97208-104">UdpIp \_ V0 \_ TypeGroup1 (clase)</span><span class="sxs-lookup"><span data-stu-id="97208-104">UdpIp\_V0\_TypeGroup1 class</span></span>

<span data-ttu-id="97208-105">Esta clase es la clase de tipo de evento para eventos UDP/IP.</span><span class="sxs-lookup"><span data-stu-id="97208-105">This class is the event type class for UDP/IP events.</span></span>

<span data-ttu-id="97208-106">La siguiente sintaxis se simplifica desde el código MOF.</span><span class="sxs-lookup"><span data-stu-id="97208-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="97208-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="97208-107">Syntax</span></span>

``` syntax
[EventType{10, 11}, EventTypeName{"Send", "Recv"}]
class UdpIp_V0_TypeGroup1 : UdpIp_V0
{
  uint32 context;
  object saddr;
  object sport;
  uint16 size;
  object daddr;
  object dport;
  uint16 dsize;
};
```

## <a name="members"></a><span data-ttu-id="97208-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="97208-108">Members</span></span>

<span data-ttu-id="97208-109">La clase **UdpIp \_ V0 \_ TypeGroup1** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="97208-109">The **UdpIp\_V0\_TypeGroup1** class has these types of members:</span></span>

-   [<span data-ttu-id="97208-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="97208-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="97208-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="97208-111">Properties</span></span>

<span data-ttu-id="97208-112">La clase **UdpIp \_ V0 \_ TypeGroup1** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="97208-112">The **UdpIp\_V0\_TypeGroup1** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="97208-113">context</span><span class="sxs-lookup"><span data-stu-id="97208-113">context</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97208-114">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="97208-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="97208-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="97208-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="97208-116">Calificadores: WmiDataId (1), puntero</span><span class="sxs-lookup"><span data-stu-id="97208-116">Qualifiers: WmiDataId(1), pointer</span></span>
</dt> </dl>

<span data-ttu-id="97208-117">Identificador de proceso del objeto de dirección que ha realizado o recibido la solicitud.</span><span class="sxs-lookup"><span data-stu-id="97208-117">Process identifier for the Address Object that made or received the request.</span></span>

</dd> <dt>

<span data-ttu-id="97208-118">daddr</span><span class="sxs-lookup"><span data-stu-id="97208-118">daddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97208-119">Tipo de datos: **objeto**</span><span class="sxs-lookup"><span data-stu-id="97208-119">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="97208-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="97208-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="97208-121">Calificadores: WmiDataId (5), extensión ("DirIP")</span><span class="sxs-lookup"><span data-stu-id="97208-121">Qualifiers: WmiDataId(5), Extension("IPAddr")</span></span>
</dt> </dl>

<span data-ttu-id="97208-122">Dirección IP de destino.</span><span class="sxs-lookup"><span data-stu-id="97208-122">Destination IP address.</span></span>

</dd> <dt>

<span data-ttu-id="97208-123">dport</span><span class="sxs-lookup"><span data-stu-id="97208-123">dport</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97208-124">Tipo de datos: **objeto**</span><span class="sxs-lookup"><span data-stu-id="97208-124">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="97208-125">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="97208-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="97208-126">Calificadores: WmiDataId (6), extensión ("puerto")</span><span class="sxs-lookup"><span data-stu-id="97208-126">Qualifiers: WmiDataId(6), Extension("Port")</span></span>
</dt> </dl>

<span data-ttu-id="97208-127">Número de puerto de destino.</span><span class="sxs-lookup"><span data-stu-id="97208-127">Destination port number.</span></span>

</dd> <dt>

<span data-ttu-id="97208-128">dsize</span><span class="sxs-lookup"><span data-stu-id="97208-128">dsize</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97208-129">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="97208-129">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="97208-130">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="97208-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="97208-131">Calificadores: WmiDataId (7)</span><span class="sxs-lookup"><span data-stu-id="97208-131">Qualifiers: WmiDataId(7)</span></span>
</dt> </dl>

<span data-ttu-id="97208-132">Tamaño del paquete de destino.</span><span class="sxs-lookup"><span data-stu-id="97208-132">Size of the destination packet.</span></span>

</dd> <dt>

<span data-ttu-id="97208-133">saddr</span><span class="sxs-lookup"><span data-stu-id="97208-133">saddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97208-134">Tipo de datos: **objeto**</span><span class="sxs-lookup"><span data-stu-id="97208-134">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="97208-135">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="97208-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="97208-136">Calificadores: WmiDataId (2), extensión ("DirIP")</span><span class="sxs-lookup"><span data-stu-id="97208-136">Qualifiers: WmiDataId(2), Extension("IPAddr")</span></span>
</dt> </dl>

<span data-ttu-id="97208-137">Dirección IP de origen.</span><span class="sxs-lookup"><span data-stu-id="97208-137">Source IP address.</span></span>

</dd> <dt>

<span data-ttu-id="97208-138">tamaño</span><span class="sxs-lookup"><span data-stu-id="97208-138">size</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97208-139">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="97208-139">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="97208-140">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="97208-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="97208-141">Calificadores: WmiDataId (4)</span><span class="sxs-lookup"><span data-stu-id="97208-141">Qualifiers: WmiDataId(4)</span></span>
</dt> </dl>

<span data-ttu-id="97208-142">Tamaño del paquete de origen.</span><span class="sxs-lookup"><span data-stu-id="97208-142">Size of the source packet.</span></span>

</dd> <dt>

<span data-ttu-id="97208-143">deportivo</span><span class="sxs-lookup"><span data-stu-id="97208-143">sport</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97208-144">Tipo de datos: **objeto**</span><span class="sxs-lookup"><span data-stu-id="97208-144">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="97208-145">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="97208-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="97208-146">Calificadores: WmiDataId (3), extensión ("puerto")</span><span class="sxs-lookup"><span data-stu-id="97208-146">Qualifiers: WmiDataId(3), Extension("Port")</span></span>
</dt> </dl>

<span data-ttu-id="97208-147">Número de puerto de origen.</span><span class="sxs-lookup"><span data-stu-id="97208-147">Source port number.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="97208-148">Requisitos</span><span class="sxs-lookup"><span data-stu-id="97208-148">Requirements</span></span>



| <span data-ttu-id="97208-149">Requisito</span><span class="sxs-lookup"><span data-stu-id="97208-149">Requirement</span></span> | <span data-ttu-id="97208-150">Value</span><span class="sxs-lookup"><span data-stu-id="97208-150">Value</span></span> |
|-------------------------------------|---------------------------------------------|
| <span data-ttu-id="97208-151">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="97208-151">Minimum supported client</span></span><br/> | <span data-ttu-id="97208-152">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="97208-152">Windows XP \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="97208-153">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="97208-153">Minimum supported server</span></span><br/> | <span data-ttu-id="97208-154">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="97208-154">None supported</span></span><br/>                   |



## <a name="see-also"></a><span data-ttu-id="97208-155">Vea también</span><span class="sxs-lookup"><span data-stu-id="97208-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="97208-156">**UdpIp \_ v0**</span><span class="sxs-lookup"><span data-stu-id="97208-156">**UdpIp\_V0**</span></span>](udpip-v0.md)
</dt> </dl>

 

 




