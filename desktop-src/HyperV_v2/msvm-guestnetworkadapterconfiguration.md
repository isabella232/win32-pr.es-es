---
description: Representa la configuración de un adaptador de red en el sistema operativo invitado.
ms.assetid: 154d4a0f-0c57-496a-a351-6caa74011544
title: Msvm_GuestNetworkAdapterConfiguration (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_GuestNetworkAdapterConfiguration
- Msvm_GuestNetworkAdapterConfiguration.InstanceID
- Msvm_GuestNetworkAdapterConfiguration.ProtocolIFType
- Msvm_GuestNetworkAdapterConfiguration.DHCPEnabled
- Msvm_GuestNetworkAdapterConfiguration.IPAddresses
- Msvm_GuestNetworkAdapterConfiguration.Subnets
- Msvm_GuestNetworkAdapterConfiguration.DefaultGateways
- Msvm_GuestNetworkAdapterConfiguration.DNSServers
- Msvm_GuestNetworkAdapterConfiguration.IPAddressOrigins
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: ce5738bca4563aa77678cac2b7e33f5c4d5323e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154596"
---
# <a name="msvm_guestnetworkadapterconfiguration-class"></a><span data-ttu-id="cb131-103">MSVM \_ GuestNetworkAdapterConfiguration (clase)</span><span class="sxs-lookup"><span data-stu-id="cb131-103">Msvm\_GuestNetworkAdapterConfiguration class</span></span>

<span data-ttu-id="cb131-104">Representa la configuración de un adaptador de red en el sistema operativo invitado.</span><span class="sxs-lookup"><span data-stu-id="cb131-104">Represents the configuration of a network adapter within the guest operating system.</span></span>

<span data-ttu-id="cb131-105">La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="cb131-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="cb131-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="cb131-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_GuestNetworkAdapterConfiguration
{
  string  InstanceID;
  uint16  ProtocolIFType;
  boolean DHCPEnabled;
  string  IPAddresses[];
  string  Subnets[];
  string  DefaultGateways[];
  string  DNSServers[];
  UINT16  IPAddressOrigins[];
};
```

## <a name="members"></a><span data-ttu-id="cb131-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="cb131-107">Members</span></span>

<span data-ttu-id="cb131-108">La clase **MSVM \_ GuestNetworkAdapterConfiguration** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="cb131-108">The **Msvm\_GuestNetworkAdapterConfiguration** class has these types of members:</span></span>

-   [<span data-ttu-id="cb131-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="cb131-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="cb131-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="cb131-110">Properties</span></span>

<span data-ttu-id="cb131-111">La clase **MSVM \_ GuestNetworkAdapterConfiguration** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="cb131-111">The **Msvm\_GuestNetworkAdapterConfiguration** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="cb131-112">**DefaultGateways**</span><span class="sxs-lookup"><span data-stu-id="cb131-112">**DefaultGateways**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cb131-113">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="cb131-113">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="cb131-114">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="cb131-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cb131-115">Calificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado")</span><span class="sxs-lookup"><span data-stu-id="cb131-115">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="cb131-116">Matriz de cadenas que contienen las puertas de enlace IP predeterminadas configuradas en el adaptador de red en el sistema operativo invitado.</span><span class="sxs-lookup"><span data-stu-id="cb131-116">An array of strings that contain the default IP gateways configured on the network adapter within the guest operating system.</span></span> <span data-ttu-id="cb131-117">El número máximo de puertas de enlace de IP predeterminadas que se pueden configurar en un único adaptador de red es cinco.</span><span class="sxs-lookup"><span data-stu-id="cb131-117">The maximum number of default IP gateways that may be configured on a single network adapter is five.</span></span>

</dd> <dt>

<span data-ttu-id="cb131-118">**DHCPEnabled**</span><span class="sxs-lookup"><span data-stu-id="cb131-118">**DHCPEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cb131-119">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="cb131-119">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="cb131-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="cb131-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cb131-121">Especifica si DHCP está habilitado en el adaptador de red en el sistema operativo invitado.</span><span class="sxs-lookup"><span data-stu-id="cb131-121">Specifies whether DHCP is enabled on the network adapter within the guest operating system.</span></span>

</dd> <dt>

<span data-ttu-id="cb131-122">**DNSServers**</span><span class="sxs-lookup"><span data-stu-id="cb131-122">**DNSServers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cb131-123">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="cb131-123">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="cb131-124">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="cb131-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cb131-125">Calificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado")</span><span class="sxs-lookup"><span data-stu-id="cb131-125">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="cb131-126">Matriz de cadenas que contienen los servidores DNS configurados en el adaptador de red en el sistema operativo invitado.</span><span class="sxs-lookup"><span data-stu-id="cb131-126">An array of strings that contain the DNS servers configured on the network adapter within the guest operating system.</span></span>

</dd> <dt>

<span data-ttu-id="cb131-127">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="cb131-127">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cb131-128">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="cb131-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cb131-129">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="cb131-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cb131-130">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="cb131-130">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="cb131-131">Identificador único de este objeto.</span><span class="sxs-lookup"><span data-stu-id="cb131-131">The unique identifier for this object.</span></span>

</dd> <dt>

<span data-ttu-id="cb131-132">**IPAddresses**</span><span class="sxs-lookup"><span data-stu-id="cb131-132">**IPAddresses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cb131-133">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="cb131-133">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="cb131-134">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="cb131-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cb131-135">Calificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado")</span><span class="sxs-lookup"><span data-stu-id="cb131-135">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="cb131-136">Matriz de cadenas que contienen las direcciones IP configuradas en el adaptador de red dentro del sistema operativo invitado.</span><span class="sxs-lookup"><span data-stu-id="cb131-136">An array of strings that contain the IP addresses configured on the network adapter within the guest operating system.</span></span>

</dd> <dt>

<span data-ttu-id="cb131-137">**IPAddressOrigins**</span><span class="sxs-lookup"><span data-stu-id="cb131-137">**IPAddressOrigins**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cb131-138">Tipo de datos: matriz **UINT16**</span><span class="sxs-lookup"><span data-stu-id="cb131-138">Data type: **UINT16** array</span></span>
</dt> <dt>

<span data-ttu-id="cb131-139">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="cb131-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cb131-140">Calificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado")</span><span class="sxs-lookup"><span data-stu-id="cb131-140">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="cb131-141">El origen de las direcciones IP configuradas en el adaptador de red en el sistema operativo invitado.</span><span class="sxs-lookup"><span data-stu-id="cb131-141">The source of the IP addresses configured on the network adapter within the guest operating system.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="cb131-142">**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="cb131-142">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="cb131-143">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="cb131-143">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Static"></span><span id="static"></span><span id="STATIC"></span>

<span data-ttu-id="cb131-144">**Static** (2)</span><span class="sxs-lookup"><span data-stu-id="cb131-144">**Static** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="cb131-145">**ProtocolIFType**</span><span class="sxs-lookup"><span data-stu-id="cb131-145">**ProtocolIFType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cb131-146">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="cb131-146">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="cb131-147">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="cb131-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cb131-148">Identifica los protocolos IP a los que se aplica la configuración especificada por esta instancia.</span><span class="sxs-lookup"><span data-stu-id="cb131-148">Identifies the IP protocols that the settings specified by this instance apply to.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="cb131-149">**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="cb131-149">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="cb131-150">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="cb131-150">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="IPv4"></span><span id="ipv4"></span><span id="IPV4"></span>

<span data-ttu-id="cb131-151">**IPv4** (4096)</span><span class="sxs-lookup"><span data-stu-id="cb131-151">**IPv4** (4096)</span></span>


</dt> <dd></dd> <dt>

<span id="IPv6"></span><span id="ipv6"></span><span id="IPV6"></span>

<span data-ttu-id="cb131-152">**IPv6** (4097)</span><span class="sxs-lookup"><span data-stu-id="cb131-152">**IPv6** (4097)</span></span>


</dt> <dd></dd> <dt>

<span id="IPv4_v6"></span><span id="ipv4_v6"></span><span id="IPV4_V6"></span>

<span data-ttu-id="cb131-153">**IPv4/V6** (4098)</span><span class="sxs-lookup"><span data-stu-id="cb131-153">**IPv4/v6** (4098)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="cb131-154">**Subredes**</span><span class="sxs-lookup"><span data-stu-id="cb131-154">**Subnets**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cb131-155">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="cb131-155">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="cb131-156">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="cb131-156">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cb131-157">Calificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado")</span><span class="sxs-lookup"><span data-stu-id="cb131-157">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="cb131-158">Matriz de cadenas que contiene las subredes configuradas en el adaptador de red en el sistema operativo invitado.</span><span class="sxs-lookup"><span data-stu-id="cb131-158">An array of strings that contain the subnets configured on the network adapter within the guest operating system.</span></span> <span data-ttu-id="cb131-159">Cada elemento de esta matriz se aplica al elemento correspondiente de la matriz **IPAddresses** .</span><span class="sxs-lookup"><span data-stu-id="cb131-159">Each element in this array applies to the corresponding element in the **IPAddresses** array.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="cb131-160">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cb131-160">Requirements</span></span>



| <span data-ttu-id="cb131-161">Requisito</span><span class="sxs-lookup"><span data-stu-id="cb131-161">Requirement</span></span> | <span data-ttu-id="cb131-162">Value</span><span class="sxs-lookup"><span data-stu-id="cb131-162">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cb131-163">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cb131-163">Minimum supported client</span></span><br/> | <span data-ttu-id="cb131-164">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="cb131-164">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="cb131-165">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cb131-165">Minimum supported server</span></span><br/> | <span data-ttu-id="cb131-166">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="cb131-166">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="cb131-167">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="cb131-167">Namespace</span></span><br/>                | <span data-ttu-id="cb131-168">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="cb131-168">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="cb131-169">MOF</span><span class="sxs-lookup"><span data-stu-id="cb131-169">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cb131-170"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="cb131-170"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="cb131-171">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="cb131-171">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cb131-172"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="cb131-172"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

