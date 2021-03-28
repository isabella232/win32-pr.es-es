---
description: Esta clase es la clase de tipo de evento para eventos UDP/IP. La siguiente sintaxis se simplifica desde el código MOF.
ms.assetid: c0ef6679-3852-4992-9fc2-114620eae14e
title: UdpIp_V1_TypeGroup1 (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UdpIp_V1_TypeGroup1
- UdpIp_V1_TypeGroup1.PID
- UdpIp_V1_TypeGroup1.size
- UdpIp_V1_TypeGroup1.daddr
- UdpIp_V1_TypeGroup1.saddr
- UdpIp_V1_TypeGroup1.dport
- UdpIp_V1_TypeGroup1.sport
api_type:
- NA
api_location: ''
ms.openlocfilehash: 58f7506aefa79c3bc9136d2e3e76d662f545a921
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984214"
---
# <a name="udpip_v1_typegroup1-class"></a><span data-ttu-id="7a971-104">UdpIp \_ v1 \_ TypeGroup1 (clase)</span><span class="sxs-lookup"><span data-stu-id="7a971-104">UdpIp\_V1\_TypeGroup1 class</span></span>

<span data-ttu-id="7a971-105">Esta clase es la clase de tipo de evento para eventos UDP/IP.</span><span class="sxs-lookup"><span data-stu-id="7a971-105">This class is the event type class for UDP/IP events.</span></span>

<span data-ttu-id="7a971-106">La siguiente sintaxis se simplifica desde el código MOF.</span><span class="sxs-lookup"><span data-stu-id="7a971-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="7a971-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7a971-107">Syntax</span></span>

``` syntax
[EventType{10, 11}, EventTypeName{"Send", "Recv"}]
class UdpIp_V1_TypeGroup1 : UdpIp_V1
{
  uint32 PID;
  uint32 size;
  object daddr;
  object saddr;
  object dport;
  object sport;
};
```

## <a name="members"></a><span data-ttu-id="7a971-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="7a971-108">Members</span></span>

<span data-ttu-id="7a971-109">La **clase \_ \_ TypeGroup1 de UdpIp v1** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="7a971-109">The **UdpIp\_V1\_TypeGroup1** class has these types of members:</span></span>

-   [<span data-ttu-id="7a971-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="7a971-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7a971-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="7a971-111">Properties</span></span>

<span data-ttu-id="7a971-112">La **clase \_ \_ TypeGroup1 de UdpIp v1** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="7a971-112">The **UdpIp\_V1\_TypeGroup1** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7a971-113">daddr</span><span class="sxs-lookup"><span data-stu-id="7a971-113">daddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7a971-114">Tipo de datos: **objeto**</span><span class="sxs-lookup"><span data-stu-id="7a971-114">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="7a971-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7a971-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7a971-116">Calificadores: WmiDataId (3), extensión ("DirIP")</span><span class="sxs-lookup"><span data-stu-id="7a971-116">Qualifiers: WmiDataId(3), Extension("IPAddr")</span></span>
</dt> </dl>

<span data-ttu-id="7a971-117">Dirección IP de destino.</span><span class="sxs-lookup"><span data-stu-id="7a971-117">Destination IP address.</span></span>

</dd> <dt>

<span data-ttu-id="7a971-118">dport</span><span class="sxs-lookup"><span data-stu-id="7a971-118">dport</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7a971-119">Tipo de datos: **objeto**</span><span class="sxs-lookup"><span data-stu-id="7a971-119">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="7a971-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7a971-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7a971-121">Calificadores: WmiDataId (5), extensión ("puerto")</span><span class="sxs-lookup"><span data-stu-id="7a971-121">Qualifiers: WmiDataId(5), Extension("Port")</span></span>
</dt> </dl>

<span data-ttu-id="7a971-122">Número de puerto de destino.</span><span class="sxs-lookup"><span data-stu-id="7a971-122">Destination port number.</span></span>

</dd> <dt>

<span data-ttu-id="7a971-123">PID</span><span class="sxs-lookup"><span data-stu-id="7a971-123">PID</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7a971-124">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7a971-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7a971-125">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7a971-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7a971-126">Calificadores: WmiDataId (1)</span><span class="sxs-lookup"><span data-stu-id="7a971-126">Qualifiers: WmiDataId(1)</span></span>
</dt> </dl>

<span data-ttu-id="7a971-127">Identificador del proceso asociado a la solicitud.</span><span class="sxs-lookup"><span data-stu-id="7a971-127">Identifier of the process associated with the request.</span></span>

</dd> <dt>

<span data-ttu-id="7a971-128">saddr</span><span class="sxs-lookup"><span data-stu-id="7a971-128">saddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7a971-129">Tipo de datos: **objeto**</span><span class="sxs-lookup"><span data-stu-id="7a971-129">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="7a971-130">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7a971-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7a971-131">Calificadores: WmiDataId (4), extensión ("DirIP")</span><span class="sxs-lookup"><span data-stu-id="7a971-131">Qualifiers: WmiDataId(4), Extension("IPAddr")</span></span>
</dt> </dl>

<span data-ttu-id="7a971-132">Dirección IP de origen.</span><span class="sxs-lookup"><span data-stu-id="7a971-132">Source IP address.</span></span>

</dd> <dt>

<span data-ttu-id="7a971-133">tamaño</span><span class="sxs-lookup"><span data-stu-id="7a971-133">size</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7a971-134">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7a971-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7a971-135">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7a971-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7a971-136">Calificadores: WmiDataId (2)</span><span class="sxs-lookup"><span data-stu-id="7a971-136">Qualifiers: WmiDataId(2)</span></span>
</dt> </dl>

<span data-ttu-id="7a971-137">Tamaño del paquete.</span><span class="sxs-lookup"><span data-stu-id="7a971-137">Size of the packet.</span></span>

</dd> <dt>

<span data-ttu-id="7a971-138">deportivo</span><span class="sxs-lookup"><span data-stu-id="7a971-138">sport</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7a971-139">Tipo de datos: **objeto**</span><span class="sxs-lookup"><span data-stu-id="7a971-139">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="7a971-140">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7a971-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7a971-141">Calificadores: WmiDataId (6), extensión ("puerto")</span><span class="sxs-lookup"><span data-stu-id="7a971-141">Qualifiers: WmiDataId(6), Extension("Port")</span></span>
</dt> </dl>

<span data-ttu-id="7a971-142">Número de puerto de origen.</span><span class="sxs-lookup"><span data-stu-id="7a971-142">Source port number.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7a971-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7a971-143">Requirements</span></span>



| <span data-ttu-id="7a971-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="7a971-144">Requirement</span></span> | <span data-ttu-id="7a971-145">Value</span><span class="sxs-lookup"><span data-stu-id="7a971-145">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="7a971-146">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7a971-146">Minimum supported client</span></span><br/> | <span data-ttu-id="7a971-147">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="7a971-147">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="7a971-148">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7a971-148">Minimum supported server</span></span><br/> | <span data-ttu-id="7a971-149">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="7a971-149">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7a971-150">Vea también</span><span class="sxs-lookup"><span data-stu-id="7a971-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a971-151">**UdpIp \_ v1**</span><span class="sxs-lookup"><span data-stu-id="7a971-151">**UdpIp\_V1**</span></span>](udpip-v1.md)
</dt> <dt>

[<span data-ttu-id="7a971-152">**UdpIp**</span><span class="sxs-lookup"><span data-stu-id="7a971-152">**UdpIp**</span></span>](udpip.md)
</dt> </dl>

 

 




