---
description: 'TcpIp_V1_TypeGroup1 clase : esta clase es la clase de tipo de evento para eventos TCP/IP. La sintaxis siguiente se simplifica a partir del código MOF.'
ms.assetid: 1cde7e37-52da-4108-90ce-7647a5653f65
title: TcpIp_V1_TypeGroup1 clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TcpIp_V1_TypeGroup1
- TcpIp_V1_TypeGroup1.PID
- TcpIp_V1_TypeGroup1.size
- TcpIp_V1_TypeGroup1.daddr
- TcpIp_V1_TypeGroup1.saddr
- TcpIp_V1_TypeGroup1.dport
- TcpIp_V1_TypeGroup1.sport
api_type:
- NA
api_location: ''
ms.openlocfilehash: 831dfdc228e2c8e128f328784046e833b0b45a39
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105763"
---
# <a name="tcpip_v1_typegroup1-class"></a><span data-ttu-id="15374-104">Clase \_ TypeGroup1 de TcpIp \_ V1</span><span class="sxs-lookup"><span data-stu-id="15374-104">TcpIp\_V1\_TypeGroup1 class</span></span>

<span data-ttu-id="15374-105">Esta clase es la clase de tipo de evento para eventos TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="15374-105">This class is the event type class for TCP/IP events.</span></span>

<span data-ttu-id="15374-106">La sintaxis siguiente se simplifica a partir del código MOF.</span><span class="sxs-lookup"><span data-stu-id="15374-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="15374-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="15374-107">Syntax</span></span>

``` syntax
[EventType{10, 11, 12, 13, 14, 15, 16}, EventTypeName{"Send", "Recv", "Connect", "Disconnect", "Retransmit", "Accept", "Reconnect"}]
class TcpIp_V1_TypeGroup1 : TcpIp_V1
{
  uint32 PID;
  uint32 size;
  object daddr;
  object saddr;
  object dport;
  object sport;
};
```

## <a name="members"></a><span data-ttu-id="15374-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="15374-108">Members</span></span>

<span data-ttu-id="15374-109">La **clase \_ \_ TypeGroup1 de TcpIp V1** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="15374-109">The **TcpIp\_V1\_TypeGroup1** class has these types of members:</span></span>

-   [<span data-ttu-id="15374-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="15374-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="15374-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="15374-111">Properties</span></span>

<span data-ttu-id="15374-112">La **clase \_ \_ TypeGroup1 de TcpIp V1** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="15374-112">The **TcpIp\_V1\_TypeGroup1** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="15374-113">dr</span><span class="sxs-lookup"><span data-stu-id="15374-113">daddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15374-114">Tipo de datos: **objeto**</span><span class="sxs-lookup"><span data-stu-id="15374-114">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="15374-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="15374-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="15374-116">Calificadores: WmiDataId(3), Extension("IPAddr")</span><span class="sxs-lookup"><span data-stu-id="15374-116">Qualifiers: WmiDataId(3), Extension("IPAddr")</span></span>
</dt> </dl>

<span data-ttu-id="15374-117">Dirección IP de destino.</span><span class="sxs-lookup"><span data-stu-id="15374-117">Destination IP address.</span></span>

</dd> <dt>

<span data-ttu-id="15374-118">dport</span><span class="sxs-lookup"><span data-stu-id="15374-118">dport</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15374-119">Tipo de datos: **objeto**</span><span class="sxs-lookup"><span data-stu-id="15374-119">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="15374-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="15374-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="15374-121">Calificadores: WmiDataId(5), Extension("Port")</span><span class="sxs-lookup"><span data-stu-id="15374-121">Qualifiers: WmiDataId(5), Extension("Port")</span></span>
</dt> </dl>

<span data-ttu-id="15374-122">Número de puerto de destino.</span><span class="sxs-lookup"><span data-stu-id="15374-122">Destination port number.</span></span>

</dd> <dt>

<span data-ttu-id="15374-123">PID</span><span class="sxs-lookup"><span data-stu-id="15374-123">PID</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15374-124">Tipo de datos: **uint32**</span><span class="sxs-lookup"><span data-stu-id="15374-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="15374-125">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="15374-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="15374-126">Calificadores: WmiDataId(1)</span><span class="sxs-lookup"><span data-stu-id="15374-126">Qualifiers: WmiDataId(1)</span></span>
</dt> </dl>

<span data-ttu-id="15374-127">Identificador del proceso asociado a la solicitud.</span><span class="sxs-lookup"><span data-stu-id="15374-127">Identifier of the process associated with the request.</span></span>

</dd> <dt>

<span data-ttu-id="15374-128">saddr</span><span class="sxs-lookup"><span data-stu-id="15374-128">saddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15374-129">Tipo de datos: **objeto**</span><span class="sxs-lookup"><span data-stu-id="15374-129">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="15374-130">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="15374-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="15374-131">Calificadores: WmiDataId(4), Extension("IPAddr")</span><span class="sxs-lookup"><span data-stu-id="15374-131">Qualifiers: WmiDataId(4), Extension("IPAddr")</span></span>
</dt> </dl>

<span data-ttu-id="15374-132">Dirección IP de origen.</span><span class="sxs-lookup"><span data-stu-id="15374-132">Source IP address.</span></span>

</dd> <dt>

<span data-ttu-id="15374-133">tamaño</span><span class="sxs-lookup"><span data-stu-id="15374-133">size</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15374-134">Tipo de datos: **uint32**</span><span class="sxs-lookup"><span data-stu-id="15374-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="15374-135">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="15374-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="15374-136">Calificadores: WmiDataId(2)</span><span class="sxs-lookup"><span data-stu-id="15374-136">Qualifiers: WmiDataId(2)</span></span>
</dt> </dl>

<span data-ttu-id="15374-137">Tamaño del paquete.</span><span class="sxs-lookup"><span data-stu-id="15374-137">Size of the packet.</span></span>

</dd> <dt>

<span data-ttu-id="15374-138">Deporte</span><span class="sxs-lookup"><span data-stu-id="15374-138">sport</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15374-139">Tipo de datos: **objeto**</span><span class="sxs-lookup"><span data-stu-id="15374-139">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="15374-140">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="15374-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="15374-141">Calificadores: WmiDataId(6), Extension("Port")</span><span class="sxs-lookup"><span data-stu-id="15374-141">Qualifiers: WmiDataId(6), Extension("Port")</span></span>
</dt> </dl>

<span data-ttu-id="15374-142">Número de puerto de origen.</span><span class="sxs-lookup"><span data-stu-id="15374-142">Source port number.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="15374-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="15374-143">Requirements</span></span>



| <span data-ttu-id="15374-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="15374-144">Requirement</span></span> | <span data-ttu-id="15374-145">Valor</span><span class="sxs-lookup"><span data-stu-id="15374-145">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="15374-146">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="15374-146">Minimum supported client</span></span><br/> | <span data-ttu-id="15374-147">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="15374-147">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="15374-148">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="15374-148">Minimum supported server</span></span><br/> | <span data-ttu-id="15374-149">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="15374-149">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="15374-150">Consulte también</span><span class="sxs-lookup"><span data-stu-id="15374-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15374-151">**TcpIp \_ V1**</span><span class="sxs-lookup"><span data-stu-id="15374-151">**TcpIp\_V1**</span></span>](tcpip-v1.md)
</dt> </dl>

 

 




