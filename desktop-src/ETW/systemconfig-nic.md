---
description: Esta clase es la clase de tipo de evento para los eventos de configuración de tarjeta de interfaz de red. La siguiente sintaxis se simplifica desde el código MOF.
ms.assetid: 66b2c116-810e-489d-ad5e-f9c09902005b
title: SystemConfig_NIC (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_NIC
- SystemConfig_NIC.PhysicalAddr
- SystemConfig_NIC.PhysicalAddrLen
- SystemConfig_NIC.Ipv4Index
- SystemConfig_NIC.Ipv6Index
- SystemConfig_NIC.NICDescription
- SystemConfig_NIC.IpAddresses
- SystemConfig_NIC.DnsServerAddresses
api_type:
- NA
api_location: ''
ms.openlocfilehash: 63d522eee993f0766554eb9bc4fb09d842e9cd8f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001175"
---
# <a name="systemconfig_nic-class"></a><span data-ttu-id="7be23-104">\_Clase SystemConfig NIC</span><span class="sxs-lookup"><span data-stu-id="7be23-104">SystemConfig\_NIC class</span></span>

<span data-ttu-id="7be23-105">Esta clase es la clase de tipo de evento para los eventos de configuración de tarjeta de interfaz de red.</span><span class="sxs-lookup"><span data-stu-id="7be23-105">This class is the event type class for network interface card configuration events.</span></span>

<span data-ttu-id="7be23-106">La siguiente sintaxis se simplifica desde el código MOF.</span><span class="sxs-lookup"><span data-stu-id="7be23-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="7be23-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7be23-107">Syntax</span></span>

``` syntax
[EventType(13), EventTypeName("NIC")]
class SystemConfig_NIC : SystemConfig
{
  uint64 PhysicalAddr;
  uint32 PhysicalAddrLen;
  uint32 Ipv4Index;
  uint32 Ipv6Index;
  string NICDescription;
  string IpAddresses;
  string DnsServerAddresses;
};
```

## <a name="members"></a><span data-ttu-id="7be23-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="7be23-108">Members</span></span>

<span data-ttu-id="7be23-109">La **clase \_ NIC SystemConfig** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="7be23-109">The **SystemConfig\_NIC** class has these types of members:</span></span>

-   [<span data-ttu-id="7be23-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="7be23-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7be23-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="7be23-111">Properties</span></span>

<span data-ttu-id="7be23-112">La clase **SystemConfig \_ NIC** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="7be23-112">The **SystemConfig\_NIC** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7be23-113">DnsServerAddresses</span><span class="sxs-lookup"><span data-stu-id="7be23-113">DnsServerAddresses</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7be23-114">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="7be23-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7be23-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7be23-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7be23-116">Calificadores: WmiDataId (7), StringTermination ("NullTerminated"), Format ("w")</span><span class="sxs-lookup"><span data-stu-id="7be23-116">Qualifiers: WmiDataId(7), StringTermination("NullTerminated"), Format("w")</span></span>
</dt> </dl>

<span data-ttu-id="7be23-117">Direcciones IP que se van a usar en la consulta de servidores DNS.</span><span class="sxs-lookup"><span data-stu-id="7be23-117">IP addresses to be used in querying for DNS servers.</span></span> <span data-ttu-id="7be23-118">La lista de direcciones está delimitada por comas.</span><span class="sxs-lookup"><span data-stu-id="7be23-118">The list of addresses is comma-delimited.</span></span>

</dd> <dt>

<span data-ttu-id="7be23-119">IpAddresses</span><span class="sxs-lookup"><span data-stu-id="7be23-119">IpAddresses</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7be23-120">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="7be23-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7be23-121">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7be23-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7be23-122">Calificadores: WmiDataId (6), StringTermination ("NullTerminated"), Format ("w")</span><span class="sxs-lookup"><span data-stu-id="7be23-122">Qualifiers: WmiDataId(6), StringTermination("NullTerminated"), Format("w")</span></span>
</dt> </dl>

<span data-ttu-id="7be23-123">Direcciones IP asociadas a la tarjeta de interfaz de red.</span><span class="sxs-lookup"><span data-stu-id="7be23-123">IP addresses associated with the network interface card.</span></span> <span data-ttu-id="7be23-124">La lista de direcciones está delimitada por comas.</span><span class="sxs-lookup"><span data-stu-id="7be23-124">The list of addresses is comma-delimited.</span></span>

</dd> <dt>

<span data-ttu-id="7be23-125">Ipv4Index</span><span class="sxs-lookup"><span data-stu-id="7be23-125">Ipv4Index</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7be23-126">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7be23-126">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7be23-127">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7be23-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7be23-128">Calificadores: WmiDataId (3)</span><span class="sxs-lookup"><span data-stu-id="7be23-128">Qualifiers: WmiDataId(3)</span></span>
</dt> </dl>

<span data-ttu-id="7be23-129">Índice de adaptador para NIC IPv4.</span><span class="sxs-lookup"><span data-stu-id="7be23-129">Adapter index for IPv4 NIC.</span></span> <span data-ttu-id="7be23-130">El índice del adaptador puede cambiar cuando un adaptador está deshabilitado y habilitado, o en otras circunstancias, y no debe considerarse persistente.</span><span class="sxs-lookup"><span data-stu-id="7be23-130">The adapter index may change when an adapter is disabled and then enabled, or under other circumstances, and should not be considered persistent.</span></span>

</dd> <dt>

<span data-ttu-id="7be23-131">Ipv6Index</span><span class="sxs-lookup"><span data-stu-id="7be23-131">Ipv6Index</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7be23-132">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7be23-132">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7be23-133">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7be23-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7be23-134">Calificadores: WmiDataId (4)</span><span class="sxs-lookup"><span data-stu-id="7be23-134">Qualifiers: WmiDataId(4)</span></span>
</dt> </dl>

<span data-ttu-id="7be23-135">Índice de adaptador para NIC IPv6.</span><span class="sxs-lookup"><span data-stu-id="7be23-135">Adapter index for IPv6 NIC.</span></span> <span data-ttu-id="7be23-136">El índice del adaptador puede cambiar cuando un adaptador está deshabilitado y habilitado, o en otras circunstancias, y no debe considerarse persistente.</span><span class="sxs-lookup"><span data-stu-id="7be23-136">The adapter index may change when an adapter is disabled and then enabled, or under other circumstances, and should not be considered persistent.</span></span>

</dd> <dt>

<span data-ttu-id="7be23-137">NICDescription</span><span class="sxs-lookup"><span data-stu-id="7be23-137">NICDescription</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7be23-138">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="7be23-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7be23-139">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7be23-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7be23-140">Calificadores: WmiDataId (5), StringTermination ("NullTerminated"), Format ("w")</span><span class="sxs-lookup"><span data-stu-id="7be23-140">Qualifiers: WmiDataId(5), StringTermination("NullTerminated"), Format("w")</span></span>
</dt> </dl>

<span data-ttu-id="7be23-141">Descripción del adaptador.</span><span class="sxs-lookup"><span data-stu-id="7be23-141">Description of the adapter.</span></span>

</dd> <dt>

<span data-ttu-id="7be23-142">PhysicalAddr</span><span class="sxs-lookup"><span data-stu-id="7be23-142">PhysicalAddr</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7be23-143">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="7be23-143">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="7be23-144">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7be23-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7be23-145">Calificadores: WmiDataId (1), Format ("x")</span><span class="sxs-lookup"><span data-stu-id="7be23-145">Qualifiers: WmiDataId(1), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="7be23-146">Dirección de hardware del adaptador.</span><span class="sxs-lookup"><span data-stu-id="7be23-146">Hardware address for the adapter.</span></span>

</dd> <dt>

<span data-ttu-id="7be23-147">PhysicalAddrLen</span><span class="sxs-lookup"><span data-stu-id="7be23-147">PhysicalAddrLen</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7be23-148">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7be23-148">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7be23-149">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7be23-149">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7be23-150">Calificadores: WmiDataId (2)</span><span class="sxs-lookup"><span data-stu-id="7be23-150">Qualifiers: WmiDataId(2)</span></span>
</dt> </dl>

<span data-ttu-id="7be23-151">Longitud de la dirección de hardware para el adaptador.</span><span class="sxs-lookup"><span data-stu-id="7be23-151">Length of the hardware address for the adapter.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7be23-152">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7be23-152">Requirements</span></span>



| <span data-ttu-id="7be23-153">Requisito</span><span class="sxs-lookup"><span data-stu-id="7be23-153">Requirement</span></span> | <span data-ttu-id="7be23-154">Value</span><span class="sxs-lookup"><span data-stu-id="7be23-154">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="7be23-155">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7be23-155">Minimum supported client</span></span><br/> | <span data-ttu-id="7be23-156">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="7be23-156">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="7be23-157">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7be23-157">Minimum supported server</span></span><br/> | <span data-ttu-id="7be23-158">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="7be23-158">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7be23-159">Vea también</span><span class="sxs-lookup"><span data-stu-id="7be23-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7be23-160">**SystemConfig**</span><span class="sxs-lookup"><span data-stu-id="7be23-160">**SystemConfig**</span></span>](systemconfig.md)
</dt> </dl>

 

 




