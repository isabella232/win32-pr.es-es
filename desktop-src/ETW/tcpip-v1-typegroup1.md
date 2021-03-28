---
description: Esta clase es la clase de tipo de evento para los eventos TCP/IP. La siguiente sintaxis se simplifica desde el código MOF.
ms.assetid: 1cde7e37-52da-4108-90ce-7647a5653f65
title: TcpIp_V1_TypeGroup1 (clase)
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
ms.openlocfilehash: fcd5f19eafa5308ef369a211559c6c464427b168
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984778"
---
# <a name="tcpip_v1_typegroup1-class"></a><span data-ttu-id="f1bf0-104">TcpIp \_ v1 ( \_ clase TypeGroup1)</span><span class="sxs-lookup"><span data-stu-id="f1bf0-104">TcpIp\_V1\_TypeGroup1 class</span></span>

<span data-ttu-id="f1bf0-105">Esta clase es la clase de tipo de evento para los eventos TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="f1bf0-105">This class is the event type class for TCP/IP events.</span></span>

<span data-ttu-id="f1bf0-106">La siguiente sintaxis se simplifica desde el código MOF.</span><span class="sxs-lookup"><span data-stu-id="f1bf0-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="f1bf0-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f1bf0-107">Syntax</span></span>

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

## <a name="members"></a><span data-ttu-id="f1bf0-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="f1bf0-108">Members</span></span>

<span data-ttu-id="f1bf0-109">La **clase \_ \_ TypeGroup1 de TCPIP v1** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="f1bf0-109">The **TcpIp\_V1\_TypeGroup1** class has these types of members:</span></span>

-   [<span data-ttu-id="f1bf0-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f1bf0-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f1bf0-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f1bf0-111">Properties</span></span>

<span data-ttu-id="f1bf0-112">La **clase \_ \_ TypeGroup1 de TCPIP v1** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="f1bf0-112">The **TcpIp\_V1\_TypeGroup1** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f1bf0-113">daddr</span><span class="sxs-lookup"><span data-stu-id="f1bf0-113">daddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1bf0-114">Tipo de datos: **objeto**</span><span class="sxs-lookup"><span data-stu-id="f1bf0-114">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="f1bf0-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f1bf0-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1bf0-116">Calificadores: WmiDataId (3), extensión ("DirIP")</span><span class="sxs-lookup"><span data-stu-id="f1bf0-116">Qualifiers: WmiDataId(3), Extension("IPAddr")</span></span>
</dt> </dl>

<span data-ttu-id="f1bf0-117">Dirección IP de destino.</span><span class="sxs-lookup"><span data-stu-id="f1bf0-117">Destination IP address.</span></span>

</dd> <dt>

<span data-ttu-id="f1bf0-118">dport</span><span class="sxs-lookup"><span data-stu-id="f1bf0-118">dport</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1bf0-119">Tipo de datos: **objeto**</span><span class="sxs-lookup"><span data-stu-id="f1bf0-119">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="f1bf0-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f1bf0-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1bf0-121">Calificadores: WmiDataId (5), extensión ("puerto")</span><span class="sxs-lookup"><span data-stu-id="f1bf0-121">Qualifiers: WmiDataId(5), Extension("Port")</span></span>
</dt> </dl>

<span data-ttu-id="f1bf0-122">Número de puerto de destino.</span><span class="sxs-lookup"><span data-stu-id="f1bf0-122">Destination port number.</span></span>

</dd> <dt>

<span data-ttu-id="f1bf0-123">PID</span><span class="sxs-lookup"><span data-stu-id="f1bf0-123">PID</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1bf0-124">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f1bf0-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f1bf0-125">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f1bf0-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1bf0-126">Calificadores: WmiDataId (1)</span><span class="sxs-lookup"><span data-stu-id="f1bf0-126">Qualifiers: WmiDataId(1)</span></span>
</dt> </dl>

<span data-ttu-id="f1bf0-127">Identificador del proceso asociado a la solicitud.</span><span class="sxs-lookup"><span data-stu-id="f1bf0-127">Identifier of the process associated with the request.</span></span>

</dd> <dt>

<span data-ttu-id="f1bf0-128">saddr</span><span class="sxs-lookup"><span data-stu-id="f1bf0-128">saddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1bf0-129">Tipo de datos: **objeto**</span><span class="sxs-lookup"><span data-stu-id="f1bf0-129">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="f1bf0-130">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f1bf0-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1bf0-131">Calificadores: WmiDataId (4), extensión ("DirIP")</span><span class="sxs-lookup"><span data-stu-id="f1bf0-131">Qualifiers: WmiDataId(4), Extension("IPAddr")</span></span>
</dt> </dl>

<span data-ttu-id="f1bf0-132">Dirección IP de origen.</span><span class="sxs-lookup"><span data-stu-id="f1bf0-132">Source IP address.</span></span>

</dd> <dt>

<span data-ttu-id="f1bf0-133">tamaño</span><span class="sxs-lookup"><span data-stu-id="f1bf0-133">size</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1bf0-134">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f1bf0-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f1bf0-135">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f1bf0-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1bf0-136">Calificadores: WmiDataId (2)</span><span class="sxs-lookup"><span data-stu-id="f1bf0-136">Qualifiers: WmiDataId(2)</span></span>
</dt> </dl>

<span data-ttu-id="f1bf0-137">Tamaño del paquete.</span><span class="sxs-lookup"><span data-stu-id="f1bf0-137">Size of the packet.</span></span>

</dd> <dt>

<span data-ttu-id="f1bf0-138">deportivo</span><span class="sxs-lookup"><span data-stu-id="f1bf0-138">sport</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1bf0-139">Tipo de datos: **objeto**</span><span class="sxs-lookup"><span data-stu-id="f1bf0-139">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="f1bf0-140">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f1bf0-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1bf0-141">Calificadores: WmiDataId (6), extensión ("puerto")</span><span class="sxs-lookup"><span data-stu-id="f1bf0-141">Qualifiers: WmiDataId(6), Extension("Port")</span></span>
</dt> </dl>

<span data-ttu-id="f1bf0-142">Número de puerto de origen.</span><span class="sxs-lookup"><span data-stu-id="f1bf0-142">Source port number.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f1bf0-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f1bf0-143">Requirements</span></span>



| <span data-ttu-id="f1bf0-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="f1bf0-144">Requirement</span></span> | <span data-ttu-id="f1bf0-145">Value</span><span class="sxs-lookup"><span data-stu-id="f1bf0-145">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="f1bf0-146">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f1bf0-146">Minimum supported client</span></span><br/> | <span data-ttu-id="f1bf0-147">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="f1bf0-147">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="f1bf0-148">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f1bf0-148">Minimum supported server</span></span><br/> | <span data-ttu-id="f1bf0-149">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="f1bf0-149">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f1bf0-150">Vea también</span><span class="sxs-lookup"><span data-stu-id="f1bf0-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1bf0-151">**TcpIp \_ v1**</span><span class="sxs-lookup"><span data-stu-id="f1bf0-151">**TcpIp\_V1**</span></span>](tcpip-v1.md)
</dt> </dl>

 

 




