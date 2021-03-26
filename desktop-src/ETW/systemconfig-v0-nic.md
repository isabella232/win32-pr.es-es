---
description: Esta clase es la clase de tipo de evento para los eventos de configuración de tarjeta de interfaz de red.
ms.assetid: 1cae611b-fb6a-4416-8fd4-0c882e8aa5e6
title: SystemConfig_V0_NIC (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_V0_NIC
- SystemConfig_V0_NIC.NICName
- SystemConfig_V0_NIC.Index
- SystemConfig_V0_NIC.PhysicalAddrLen
- SystemConfig_V0_NIC.PhysicalAddr
- SystemConfig_V0_NIC.Size
- SystemConfig_V0_NIC.IpAddress
- SystemConfig_V0_NIC.SubnetMask
- SystemConfig_V0_NIC.DhcpServer
- SystemConfig_V0_NIC.Gateway
- SystemConfig_V0_NIC.PrimaryWinsServer
- SystemConfig_V0_NIC.SecondaryWinsServer
- SystemConfig_V0_NIC.DnsServer1
- SystemConfig_V0_NIC.DnsServer2
- SystemConfig_V0_NIC.DnsServer3
- SystemConfig_V0_NIC.DnsServer4
- SystemConfig_V0_NIC.Data
api_type:
- NA
api_location: ''
ms.openlocfilehash: 040c409564c0ad37e5208c1e91962d3f04de5fc4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985935"
---
# <a name="systemconfig_v0_nic-class"></a><span data-ttu-id="7a2c9-103">\_Clase SystemConfig V0 \_ NIC</span><span class="sxs-lookup"><span data-stu-id="7a2c9-103">SystemConfig\_V0\_NIC class</span></span>

<span data-ttu-id="7a2c9-104">Esta clase es la clase de tipo de evento para los eventos de configuración de tarjeta de interfaz de red.</span><span class="sxs-lookup"><span data-stu-id="7a2c9-104">This class is the event type class for network interface card configuration events.</span></span>

<span data-ttu-id="7a2c9-105">La siguiente sintaxis se simplifica desde el código MOF.</span><span class="sxs-lookup"><span data-stu-id="7a2c9-105">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="7a2c9-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7a2c9-106">Syntax</span></span>

``` syntax
[EventType(13), EventTypeName("NIC")]
class SystemConfig_V0_NIC : SystemConfig_V0
{
  char16 NICName[];
  uint32 Index;
  uint32 PhysicalAddrLen;
  char16 PhysicalAddr;
  uint32 Size;
  sint32 IpAddress;
  sint32 SubnetMask;
  sint32 DhcpServer;
  sint32 Gateway;
  sint32 PrimaryWinsServer;
  sint32 SecondaryWinsServer;
  sint32 DnsServer1;
  sint32 DnsServer2;
  sint32 DnsServer3;
  sint32 DnsServer4;
  uint32 Data;
};
```

## <a name="members"></a><span data-ttu-id="7a2c9-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="7a2c9-107">Members</span></span>

<span data-ttu-id="7a2c9-108">La clase **SystemConfig \_ V0 \_ NIC** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="7a2c9-108">The **SystemConfig\_V0\_NIC** class has these types of members:</span></span>

-   [<span data-ttu-id="7a2c9-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="7a2c9-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7a2c9-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="7a2c9-110">Properties</span></span>

<span data-ttu-id="7a2c9-111">La clase **SystemConfig \_ V0 \_ NIC** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="7a2c9-111">The **SystemConfig\_V0\_NIC** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7a2c9-112">**Data**</span><span class="sxs-lookup"><span data-stu-id="7a2c9-112">**Data**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7a2c9-113">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7a2c9-113">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7a2c9-114">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7a2c9-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7a2c9-115">Calificadores: **WmiDataId** (16)</span><span class="sxs-lookup"><span data-stu-id="7a2c9-115">Qualifiers: **WmiDataId** (16)</span></span>
</dt> </dl>

<span data-ttu-id="7a2c9-116">Campo de datos.</span><span class="sxs-lookup"><span data-stu-id="7a2c9-116">Data field.</span></span>

</dd> <dt>

<span data-ttu-id="7a2c9-117">**DhcpServer**</span><span class="sxs-lookup"><span data-stu-id="7a2c9-117">**DhcpServer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7a2c9-118">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="7a2c9-118">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="7a2c9-119">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7a2c9-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7a2c9-120">Calificadores: **WmiDataId** (8)</span><span class="sxs-lookup"><span data-stu-id="7a2c9-120">Qualifiers: **WmiDataId** (8)</span></span>
</dt> </dl>

<span data-ttu-id="7a2c9-121">Dirección IP del servidor del Protocolo de configuración dinámica de host (DHCP).</span><span class="sxs-lookup"><span data-stu-id="7a2c9-121">IP address of the dynamic host configuration protocol (DHCP) server.</span></span> <span data-ttu-id="7a2c9-122">Un valor de 255.255.255.255 indica que no se pudo establecer contacto con el servidor DHCP o está en proceso de alcanzarse.</span><span class="sxs-lookup"><span data-stu-id="7a2c9-122">A value of 255.255.255.255 indicates the DHCP server could not be reached, or is in the process of being reached.</span></span> <span data-ttu-id="7a2c9-123">Cada byte de sint32 representa una de las cuatro partes de la dirección IP (P1. P2. P3. P4).</span><span class="sxs-lookup"><span data-stu-id="7a2c9-123">Each byte of the sint32 represents one of the four parts of the IP address (p1.p2.p3.p4).</span></span> <span data-ttu-id="7a2c9-124">El byte de orden inferior contiene el valor de P1, el siguiente byte contiene el valor de P2, etc.</span><span class="sxs-lookup"><span data-stu-id="7a2c9-124">The low-order byte contains the value for p1, the next byte contains the value for p2, and so on.</span></span>

</dd> <dt>

<span data-ttu-id="7a2c9-125">**DnsServer1**</span><span class="sxs-lookup"><span data-stu-id="7a2c9-125">**DnsServer1**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7a2c9-126">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="7a2c9-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="7a2c9-127">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7a2c9-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7a2c9-128">Calificadores: **WmiDataId** (12)</span><span class="sxs-lookup"><span data-stu-id="7a2c9-128">Qualifiers: **WmiDataId** (12)</span></span>
</dt> </dl>

<span data-ttu-id="7a2c9-129">Primeras direcciones IP de servidor que se van a usar en la consulta de servidores DNS.</span><span class="sxs-lookup"><span data-stu-id="7a2c9-129">First server IP addresses to be used in querying for DNS servers.</span></span> <span data-ttu-id="7a2c9-130">Cada byte de sint32 representa una de las cuatro partes de la dirección IP (P1. P2. P3. P4).</span><span class="sxs-lookup"><span data-stu-id="7a2c9-130">Each byte of the sint32 represents one of the four parts of the IP address (p1.p2.p3.p4).</span></span> <span data-ttu-id="7a2c9-131">El byte de orden inferior contiene el valor de P1, el siguiente byte contiene el valor de P2, etc.</span><span class="sxs-lookup"><span data-stu-id="7a2c9-131">The low-order byte contains the value for p1, the next byte contains the value for p2, and so on.</span></span>

</dd> <dt>

<span data-ttu-id="7a2c9-132">**DnsServer2**</span><span class="sxs-lookup"><span data-stu-id="7a2c9-132">**DnsServer2**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7a2c9-133">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="7a2c9-133">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="7a2c9-134">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7a2c9-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7a2c9-135">Calificadores: **WmiDataId** (13)</span><span class="sxs-lookup"><span data-stu-id="7a2c9-135">Qualifiers: **WmiDataId** (13)</span></span>
</dt> </dl>

<span data-ttu-id="7a2c9-136">Segundas direcciones IP de servidor que se van a usar en la consulta de servidores DNS.</span><span class="sxs-lookup"><span data-stu-id="7a2c9-136">Second server IP addresses to be used in querying for DNS servers.</span></span> <span data-ttu-id="7a2c9-137">Cada byte de sint32 representa una de las cuatro partes de la dirección IP (P1. P2. P3. P4).</span><span class="sxs-lookup"><span data-stu-id="7a2c9-137">Each byte of the sint32 represents one of the four parts of the IP address (p1.p2.p3.p4).</span></span> <span data-ttu-id="7a2c9-138">El byte de orden inferior contiene el valor de P1, el siguiente byte contiene el valor de P2, etc.</span><span class="sxs-lookup"><span data-stu-id="7a2c9-138">The low-order byte contains the value for p1, the next byte contains the value for p2, and so on.</span></span>

</dd> <dt>

<span data-ttu-id="7a2c9-139">**DnsServer3**</span><span class="sxs-lookup"><span data-stu-id="7a2c9-139">**DnsServer3**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7a2c9-140">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="7a2c9-140">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="7a2c9-141">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7a2c9-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7a2c9-142">Calificadores: **WmiDataId** (14)</span><span class="sxs-lookup"><span data-stu-id="7a2c9-142">Qualifiers: **WmiDataId** (14)</span></span>
</dt> </dl>

<span data-ttu-id="7a2c9-143">Direcciones IP de tercer servidor que se van a usar en la consulta de servidores DNS.</span><span class="sxs-lookup"><span data-stu-id="7a2c9-143">Third server IP addresses to be used in querying for DNS servers.</span></span> <span data-ttu-id="7a2c9-144">Cada byte de sint32 representa una de las cuatro partes de la dirección IP (P1. P2. P3. P4).</span><span class="sxs-lookup"><span data-stu-id="7a2c9-144">Each byte of the sint32 represents one of the four parts of the IP address (p1.p2.p3.p4).</span></span> <span data-ttu-id="7a2c9-145">El byte de orden inferior contiene el valor de P1, el siguiente byte contiene el valor de P2, etc.</span><span class="sxs-lookup"><span data-stu-id="7a2c9-145">The low-order byte contains the value for p1, the next byte contains the value for p2, and so on.</span></span>

</dd> <dt>

<span data-ttu-id="7a2c9-146">**DnsServer4**</span><span class="sxs-lookup"><span data-stu-id="7a2c9-146">**DnsServer4**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7a2c9-147">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="7a2c9-147">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="7a2c9-148">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7a2c9-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7a2c9-149">Calificadores: **WmiDataId** (15)</span><span class="sxs-lookup"><span data-stu-id="7a2c9-149">Qualifiers: **WmiDataId** (15)</span></span>
</dt> </dl>

<span data-ttu-id="7a2c9-150">Cuarta direcciones IP de servidor que se van a usar en la consulta de servidores DNS.</span><span class="sxs-lookup"><span data-stu-id="7a2c9-150">Fourth server IP addresses to be used in querying for DNS servers.</span></span> <span data-ttu-id="7a2c9-151">Cada byte de sint32 representa una de las cuatro partes de la dirección IP (P1. P2. P3. P4).</span><span class="sxs-lookup"><span data-stu-id="7a2c9-151">Each byte of the sint32 represents one of the four parts of the IP address (p1.p2.p3.p4).</span></span> <span data-ttu-id="7a2c9-152">El byte de orden inferior contiene el valor de P1, el siguiente byte contiene el valor de P2, etc.</span><span class="sxs-lookup"><span data-stu-id="7a2c9-152">The low-order byte contains the value for p1, the next byte contains the value for p2, and so on.</span></span>

</dd> <dt>

<span data-ttu-id="7a2c9-153">**Puerta de enlace**</span><span class="sxs-lookup"><span data-stu-id="7a2c9-153">**Gateway**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7a2c9-154">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="7a2c9-154">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="7a2c9-155">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7a2c9-155">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7a2c9-156">Calificadores: **WmiDataId** (9)</span><span class="sxs-lookup"><span data-stu-id="7a2c9-156">Qualifiers: **WmiDataId** (9)</span></span>
</dt> </dl>

<span data-ttu-id="7a2c9-157">Dirección IP de la puerta de enlace predeterminada que utiliza el sistema del equipo.</span><span class="sxs-lookup"><span data-stu-id="7a2c9-157">IP address of default gateway that the computer system uses.</span></span> <span data-ttu-id="7a2c9-158">Cada byte de sint32 representa una de las cuatro partes de la dirección IP (P1. P2. P3. P4).</span><span class="sxs-lookup"><span data-stu-id="7a2c9-158">Each byte of the sint32 represents one of the four parts of the IP address (p1.p2.p3.p4).</span></span> <span data-ttu-id="7a2c9-159">El byte de orden inferior contiene el valor de P1, el siguiente byte contiene el valor de P2, etc.</span><span class="sxs-lookup"><span data-stu-id="7a2c9-159">The low-order byte contains the value for p1, the next byte contains the value for p2, and so on.</span></span>

</dd> <dt>

<span data-ttu-id="7a2c9-160">**Index**</span><span class="sxs-lookup"><span data-stu-id="7a2c9-160">**Index**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7a2c9-161">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7a2c9-161">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7a2c9-162">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7a2c9-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7a2c9-163">Calificadores: **WmiDataId** (2)</span><span class="sxs-lookup"><span data-stu-id="7a2c9-163">Qualifiers: **WmiDataId** (2)</span></span>
</dt> </dl>

<span data-ttu-id="7a2c9-164">Índice del adaptador.</span><span class="sxs-lookup"><span data-stu-id="7a2c9-164">Adapter index.</span></span> <span data-ttu-id="7a2c9-165">El índice del adaptador puede cambiar cuando un adaptador está deshabilitado y habilitado, o en otras circunstancias, y no debe considerarse persistente.</span><span class="sxs-lookup"><span data-stu-id="7a2c9-165">The adapter index may change when an adapter is disabled and then enabled, or under other circumstances, and should not be considered persistent.</span></span>

</dd> <dt>

<span data-ttu-id="7a2c9-166">**IpAddress**</span><span class="sxs-lookup"><span data-stu-id="7a2c9-166">**IpAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7a2c9-167">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="7a2c9-167">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="7a2c9-168">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7a2c9-168">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7a2c9-169">Calificadores: **WmiDataId** (6)</span><span class="sxs-lookup"><span data-stu-id="7a2c9-169">Qualifiers: **WmiDataId** (6)</span></span>
</dt> </dl>

<span data-ttu-id="7a2c9-170">Direcciones IP asociadas a la tarjeta de interfaz de red.</span><span class="sxs-lookup"><span data-stu-id="7a2c9-170">IP addresses associated with the network interface card.</span></span> <span data-ttu-id="7a2c9-171">Cada byte de sint32 representa una de las cuatro partes de la dirección IP (P1. P2. P3. P4).</span><span class="sxs-lookup"><span data-stu-id="7a2c9-171">Each byte of the sint32 represents one of the four parts of the IP address (p1.p2.p3.p4).</span></span> <span data-ttu-id="7a2c9-172">El byte de orden inferior contiene el valor de P1, el siguiente byte contiene el valor de P2, etc.</span><span class="sxs-lookup"><span data-stu-id="7a2c9-172">The low-order byte contains the value for p1, the next byte contains the value for p2, and so on.</span></span>

</dd> <dt>

<span data-ttu-id="7a2c9-173">**NICName**</span><span class="sxs-lookup"><span data-stu-id="7a2c9-173">**NICName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7a2c9-174">Tipo de datos: matriz **char16**</span><span class="sxs-lookup"><span data-stu-id="7a2c9-174">Data type: **char16** array</span></span>
</dt> <dt>

<span data-ttu-id="7a2c9-175">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7a2c9-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7a2c9-176">Calificadores: **WmiDataId** (1), **Max** (256)</span><span class="sxs-lookup"><span data-stu-id="7a2c9-176">Qualifiers: **WmiDataId** (1), **Max** (256)</span></span>
</dt> </dl>

<span data-ttu-id="7a2c9-177">Nombre de la tarjeta de interfaz de red.</span><span class="sxs-lookup"><span data-stu-id="7a2c9-177">Name of the network interface card.</span></span>

</dd> <dt>

<span data-ttu-id="7a2c9-178">**PhysicalAddr**</span><span class="sxs-lookup"><span data-stu-id="7a2c9-178">**PhysicalAddr**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7a2c9-179">Tipo de datos: **char16**</span><span class="sxs-lookup"><span data-stu-id="7a2c9-179">Data type: **char16**</span></span>
</dt> <dt>

<span data-ttu-id="7a2c9-180">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7a2c9-180">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7a2c9-181">Calificadores: **WmiDataId** (4), **Max** (8)</span><span class="sxs-lookup"><span data-stu-id="7a2c9-181">Qualifiers: **WmiDataId** (4), **Max** (8)</span></span>
</dt> </dl>

<span data-ttu-id="7a2c9-182">Dirección de hardware del adaptador.</span><span class="sxs-lookup"><span data-stu-id="7a2c9-182">Hardware address for the adapter.</span></span>

</dd> <dt>

<span data-ttu-id="7a2c9-183">**PhysicalAddrLen**</span><span class="sxs-lookup"><span data-stu-id="7a2c9-183">**PhysicalAddrLen**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7a2c9-184">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7a2c9-184">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7a2c9-185">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7a2c9-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7a2c9-186">Calificadores: **WmiDataId** (3)</span><span class="sxs-lookup"><span data-stu-id="7a2c9-186">Qualifiers: **WmiDataId** (3)</span></span>
</dt> </dl>

<span data-ttu-id="7a2c9-187">Longitud de la dirección de hardware para el adaptador.</span><span class="sxs-lookup"><span data-stu-id="7a2c9-187">Length of the hardware address for the adapter.</span></span>

</dd> <dt>

<span data-ttu-id="7a2c9-188">**PrimaryWinsServer**</span><span class="sxs-lookup"><span data-stu-id="7a2c9-188">**PrimaryWinsServer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7a2c9-189">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="7a2c9-189">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="7a2c9-190">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7a2c9-190">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7a2c9-191">Calificadores: **WmiDataId** (10)</span><span class="sxs-lookup"><span data-stu-id="7a2c9-191">Qualifiers: **WmiDataId** (10)</span></span>
</dt> </dl>

<span data-ttu-id="7a2c9-192">Dirección IP del servidor WINS principal.</span><span class="sxs-lookup"><span data-stu-id="7a2c9-192">IP address for the primary WINS server.</span></span> <span data-ttu-id="7a2c9-193">Cada byte de sint32 representa una de las cuatro partes de la dirección IP (P1. P2. P3. P4).</span><span class="sxs-lookup"><span data-stu-id="7a2c9-193">Each byte of the sint32 represents one of the four parts of the IP address (p1.p2.p3.p4).</span></span> <span data-ttu-id="7a2c9-194">El byte de orden inferior contiene el valor de P1, el siguiente byte contiene el valor de P2, etc.</span><span class="sxs-lookup"><span data-stu-id="7a2c9-194">The low-order byte contains the value for p1, the next byte contains the value for p2, and so on.</span></span>

</dd> <dt>

<span data-ttu-id="7a2c9-195">**SecondaryWinsServer**</span><span class="sxs-lookup"><span data-stu-id="7a2c9-195">**SecondaryWinsServer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7a2c9-196">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="7a2c9-196">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="7a2c9-197">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7a2c9-197">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7a2c9-198">Calificadores: **WmiDataId** (11)</span><span class="sxs-lookup"><span data-stu-id="7a2c9-198">Qualifiers: **WmiDataId** (11)</span></span>
</dt> </dl>

<span data-ttu-id="7a2c9-199">Dirección IP del servidor WINS secundario.</span><span class="sxs-lookup"><span data-stu-id="7a2c9-199">IP address for the secondary WINS server.</span></span> <span data-ttu-id="7a2c9-200">Cada byte de sint32 representa una de las cuatro partes de la dirección IP (P1. P2. P3. P4).</span><span class="sxs-lookup"><span data-stu-id="7a2c9-200">Each byte of the sint32 represents one of the four parts of the IP address (p1.p2.p3.p4).</span></span> <span data-ttu-id="7a2c9-201">El byte de orden inferior contiene el valor de P1, el siguiente byte contiene el valor de P2, etc.</span><span class="sxs-lookup"><span data-stu-id="7a2c9-201">The low-order byte contains the value for p1, the next byte contains the value for p2, and so on.</span></span>

</dd> <dt>

<span data-ttu-id="7a2c9-202">**Tamaño**</span><span class="sxs-lookup"><span data-stu-id="7a2c9-202">**Size**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7a2c9-203">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7a2c9-203">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7a2c9-204">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7a2c9-204">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7a2c9-205">Calificadores: **WmiDataId** (5)</span><span class="sxs-lookup"><span data-stu-id="7a2c9-205">Qualifiers: **WmiDataId** (5)</span></span>
</dt> </dl>

<span data-ttu-id="7a2c9-206">Tamaño, en bytes, de la propiedad de datos.</span><span class="sxs-lookup"><span data-stu-id="7a2c9-206">Size, in bytes, of the Data property.</span></span>

</dd> <dt>

<span data-ttu-id="7a2c9-207">**SubnetMask**</span><span class="sxs-lookup"><span data-stu-id="7a2c9-207">**SubnetMask**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7a2c9-208">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="7a2c9-208">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="7a2c9-209">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7a2c9-209">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7a2c9-210">Calificadores: **WmiDataId** (7)</span><span class="sxs-lookup"><span data-stu-id="7a2c9-210">Qualifiers: **WmiDataId** (7)</span></span>
</dt> </dl>

<span data-ttu-id="7a2c9-211">Máscara de subred asociada a la tarjeta de interfaz de red.</span><span class="sxs-lookup"><span data-stu-id="7a2c9-211">Subnet mask associated with the network interface card.</span></span> <span data-ttu-id="7a2c9-212">Cada byte de sint32 representa una de las cuatro partes de la dirección IP (P1. P2. P3. P4).</span><span class="sxs-lookup"><span data-stu-id="7a2c9-212">Each byte of the sint32 represents one of the four parts of the IP address (p1.p2.p3.p4).</span></span> <span data-ttu-id="7a2c9-213">El byte de orden inferior contiene el valor de P1, el siguiente byte contiene el valor de P2, etc.</span><span class="sxs-lookup"><span data-stu-id="7a2c9-213">The low-order byte contains the value for p1, the next byte contains the value for p2, and so on.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7a2c9-214">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7a2c9-214">Requirements</span></span>



| <span data-ttu-id="7a2c9-215">Requisito</span><span class="sxs-lookup"><span data-stu-id="7a2c9-215">Requirement</span></span> | <span data-ttu-id="7a2c9-216">Value</span><span class="sxs-lookup"><span data-stu-id="7a2c9-216">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="7a2c9-217">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7a2c9-217">Minimum supported client</span></span><br/> | <span data-ttu-id="7a2c9-218">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="7a2c9-218">None supported</span></span><br/>                            |
| <span data-ttu-id="7a2c9-219">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7a2c9-219">Minimum supported server</span></span><br/> | <span data-ttu-id="7a2c9-220">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="7a2c9-220">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7a2c9-221">Vea también</span><span class="sxs-lookup"><span data-stu-id="7a2c9-221">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a2c9-222">**SystemConfig \_ v0**</span><span class="sxs-lookup"><span data-stu-id="7a2c9-222">**SystemConfig\_V0**</span></span>](systemconfig-v0.md)
</dt> </dl>

 

 




