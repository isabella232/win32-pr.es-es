---
description: 'UdpIp_V1_TypeGroup1 clase : esta clase es la clase de tipo de evento para eventos UDP/IP. La sintaxis siguiente se simplifica a partir del código MOF.'
ms.assetid: c0ef6679-3852-4992-9fc2-114620eae14e
title: UdpIp_V1_TypeGroup1 clase
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
ms.openlocfilehash: d7dadaac3d418d2351f9e27c694309deb373615e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105413"
---
# <a name="udpip_v1_typegroup1-class"></a><span data-ttu-id="cc547-104">UdpIp \_ V1 \_ TypeGroup1 (clase)</span><span class="sxs-lookup"><span data-stu-id="cc547-104">UdpIp\_V1\_TypeGroup1 class</span></span>

<span data-ttu-id="cc547-105">Esta clase es la clase de tipo de evento para eventos UDP/IP.</span><span class="sxs-lookup"><span data-stu-id="cc547-105">This class is the event type class for UDP/IP events.</span></span>

<span data-ttu-id="cc547-106">La sintaxis siguiente se simplifica a partir del código MOF.</span><span class="sxs-lookup"><span data-stu-id="cc547-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="cc547-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="cc547-107">Syntax</span></span>

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

## <a name="members"></a><span data-ttu-id="cc547-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="cc547-108">Members</span></span>

<span data-ttu-id="cc547-109">La **clase UdpIp \_ V1 \_ TypeGroup1** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="cc547-109">The **UdpIp\_V1\_TypeGroup1** class has these types of members:</span></span>

-   [<span data-ttu-id="cc547-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="cc547-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="cc547-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="cc547-111">Properties</span></span>

<span data-ttu-id="cc547-112">La **clase \_ \_ TypeGroup1 UdpIp V1** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="cc547-112">The **UdpIp\_V1\_TypeGroup1** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="cc547-113">dr</span><span class="sxs-lookup"><span data-stu-id="cc547-113">daddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cc547-114">Tipo de datos: **objeto**</span><span class="sxs-lookup"><span data-stu-id="cc547-114">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="cc547-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="cc547-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cc547-116">Calificadores: WmiDataId(3), Extension("IPAddr")</span><span class="sxs-lookup"><span data-stu-id="cc547-116">Qualifiers: WmiDataId(3), Extension("IPAddr")</span></span>
</dt> </dl>

<span data-ttu-id="cc547-117">Dirección IP de destino.</span><span class="sxs-lookup"><span data-stu-id="cc547-117">Destination IP address.</span></span>

</dd> <dt>

<span data-ttu-id="cc547-118">dport</span><span class="sxs-lookup"><span data-stu-id="cc547-118">dport</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cc547-119">Tipo de datos: **objeto**</span><span class="sxs-lookup"><span data-stu-id="cc547-119">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="cc547-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="cc547-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cc547-121">Calificadores: WmiDataId(5), Extension("Port")</span><span class="sxs-lookup"><span data-stu-id="cc547-121">Qualifiers: WmiDataId(5), Extension("Port")</span></span>
</dt> </dl>

<span data-ttu-id="cc547-122">Número de puerto de destino.</span><span class="sxs-lookup"><span data-stu-id="cc547-122">Destination port number.</span></span>

</dd> <dt>

<span data-ttu-id="cc547-123">PID</span><span class="sxs-lookup"><span data-stu-id="cc547-123">PID</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cc547-124">Tipo de datos: **uint32**</span><span class="sxs-lookup"><span data-stu-id="cc547-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="cc547-125">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="cc547-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cc547-126">Calificadores: WmiDataId(1)</span><span class="sxs-lookup"><span data-stu-id="cc547-126">Qualifiers: WmiDataId(1)</span></span>
</dt> </dl>

<span data-ttu-id="cc547-127">Identificador del proceso asociado a la solicitud.</span><span class="sxs-lookup"><span data-stu-id="cc547-127">Identifier of the process associated with the request.</span></span>

</dd> <dt>

<span data-ttu-id="cc547-128">saddr</span><span class="sxs-lookup"><span data-stu-id="cc547-128">saddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cc547-129">Tipo de datos: **objeto**</span><span class="sxs-lookup"><span data-stu-id="cc547-129">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="cc547-130">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="cc547-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cc547-131">Calificadores: WmiDataId(4), Extension("IPAddr")</span><span class="sxs-lookup"><span data-stu-id="cc547-131">Qualifiers: WmiDataId(4), Extension("IPAddr")</span></span>
</dt> </dl>

<span data-ttu-id="cc547-132">Dirección IP de origen.</span><span class="sxs-lookup"><span data-stu-id="cc547-132">Source IP address.</span></span>

</dd> <dt>

<span data-ttu-id="cc547-133">tamaño</span><span class="sxs-lookup"><span data-stu-id="cc547-133">size</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cc547-134">Tipo de datos: **uint32**</span><span class="sxs-lookup"><span data-stu-id="cc547-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="cc547-135">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="cc547-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cc547-136">Calificadores: WmiDataId(2)</span><span class="sxs-lookup"><span data-stu-id="cc547-136">Qualifiers: WmiDataId(2)</span></span>
</dt> </dl>

<span data-ttu-id="cc547-137">Tamaño del paquete.</span><span class="sxs-lookup"><span data-stu-id="cc547-137">Size of the packet.</span></span>

</dd> <dt>

<span data-ttu-id="cc547-138">Deporte</span><span class="sxs-lookup"><span data-stu-id="cc547-138">sport</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cc547-139">Tipo de datos: **objeto**</span><span class="sxs-lookup"><span data-stu-id="cc547-139">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="cc547-140">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="cc547-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cc547-141">Calificadores: WmiDataId(6), Extension("Port")</span><span class="sxs-lookup"><span data-stu-id="cc547-141">Qualifiers: WmiDataId(6), Extension("Port")</span></span>
</dt> </dl>

<span data-ttu-id="cc547-142">Número de puerto de origen.</span><span class="sxs-lookup"><span data-stu-id="cc547-142">Source port number.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="cc547-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cc547-143">Requirements</span></span>



| <span data-ttu-id="cc547-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="cc547-144">Requirement</span></span> | <span data-ttu-id="cc547-145">Valor</span><span class="sxs-lookup"><span data-stu-id="cc547-145">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="cc547-146">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cc547-146">Minimum supported client</span></span><br/> | <span data-ttu-id="cc547-147">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="cc547-147">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="cc547-148">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cc547-148">Minimum supported server</span></span><br/> | <span data-ttu-id="cc547-149">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="cc547-149">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="cc547-150">Consulte también</span><span class="sxs-lookup"><span data-stu-id="cc547-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cc547-151">**UdpIp \_ V1**</span><span class="sxs-lookup"><span data-stu-id="cc547-151">**UdpIp\_V1**</span></span>](udpip-v1.md)
</dt> <dt>

[<span data-ttu-id="cc547-152">**UdpIp**</span><span class="sxs-lookup"><span data-stu-id="cc547-152">**UdpIp**</span></span>](udpip.md)
</dt> </dl>

 

 




