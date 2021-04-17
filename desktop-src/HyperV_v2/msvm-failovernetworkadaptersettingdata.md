---
description: Representa la configuración de un adaptador de red en el sistema operativo invitado, que se aplicará en el momento de una conmutación por error.
ms.assetid: d7f2d471-7328-4181-b94e-b9127814706e
title: Msvm_FailoverNetworkAdapterSettingData (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_FailoverNetworkAdapterSettingData
- Msvm_FailoverNetworkAdapterSettingData.InstanceID
- Msvm_FailoverNetworkAdapterSettingData.Caption
- Msvm_FailoverNetworkAdapterSettingData.Description
- Msvm_FailoverNetworkAdapterSettingData.ElementName
- Msvm_FailoverNetworkAdapterSettingData.ProtocolIFType
- Msvm_FailoverNetworkAdapterSettingData.DHCPEnabled
- Msvm_FailoverNetworkAdapterSettingData.IPAddresses
- Msvm_FailoverNetworkAdapterSettingData.Subnets
- Msvm_FailoverNetworkAdapterSettingData.DefaultGateways
- Msvm_FailoverNetworkAdapterSettingData.DNSServers
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: d4989c43dda823be13d604e3ac9b575b62f2f9da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666622"
---
# <a name="msvm_failovernetworkadaptersettingdata-class"></a><span data-ttu-id="22a24-103">MSVM \_ FailoverNetworkAdapterSettingData (clase)</span><span class="sxs-lookup"><span data-stu-id="22a24-103">Msvm\_FailoverNetworkAdapterSettingData class</span></span>

<span data-ttu-id="22a24-104">Representa la configuración de un adaptador de red en el sistema operativo invitado, que se aplicará en el momento de una conmutación por error.</span><span class="sxs-lookup"><span data-stu-id="22a24-104">Represents the settings for a network adapter within the guest operating system, which will be applied at the time of a failover.</span></span>

<span data-ttu-id="22a24-105">La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="22a24-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="22a24-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="22a24-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_FailoverNetworkAdapterSettingData : CIM_SettingData
{
  string  InstanceID;
  string  Caption;
  string  Description;
  string  ElementName;
  uint16  ProtocolIFType;
  boolean DHCPEnabled;
  string  IPAddresses[];
  string  Subnets[];
  string  DefaultGateways[];
  string  DNSServers[];
};
```

## <a name="members"></a><span data-ttu-id="22a24-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="22a24-107">Members</span></span>

<span data-ttu-id="22a24-108">La clase **MSVM \_ FailoverNetworkAdapterSettingData** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="22a24-108">The **Msvm\_FailoverNetworkAdapterSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="22a24-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="22a24-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="22a24-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="22a24-110">Properties</span></span>

<span data-ttu-id="22a24-111">La clase **MSVM \_ FailoverNetworkAdapterSettingData** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="22a24-111">The **Msvm\_FailoverNetworkAdapterSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="22a24-112">**Caption**</span><span class="sxs-lookup"><span data-stu-id="22a24-112">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22a24-113">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="22a24-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="22a24-114">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="22a24-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="22a24-115">Breve descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="22a24-115">A short description of the object.</span></span> <span data-ttu-id="22a24-116">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)y siempre se establece en **null**.</span><span class="sxs-lookup"><span data-stu-id="22a24-116">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="22a24-117">**DefaultGateways**</span><span class="sxs-lookup"><span data-stu-id="22a24-117">**DefaultGateways**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22a24-118">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="22a24-118">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="22a24-119">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="22a24-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="22a24-120">Calificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado")</span><span class="sxs-lookup"><span data-stu-id="22a24-120">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="22a24-121">Matriz de cadenas que especifican las puertas de enlace IP predeterminadas configuradas en el adaptador de red en el sistema operativo invitado.</span><span class="sxs-lookup"><span data-stu-id="22a24-121">An array of strings that specify the default IP gateways configured on the network adapter within the guest operating system.</span></span> <span data-ttu-id="22a24-122">El número máximo de puertas de enlace de IP predeterminadas que se pueden configurar en un único adaptador de red es cinco.</span><span class="sxs-lookup"><span data-stu-id="22a24-122">The maximum number of default IP gateways that may be configured on a single network adapter is five.</span></span>

</dd> <dt>

<span data-ttu-id="22a24-123">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="22a24-123">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22a24-124">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="22a24-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="22a24-125">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="22a24-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="22a24-126">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="22a24-126">A description of the object.</span></span> <span data-ttu-id="22a24-127">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)y siempre se establece en **null**.</span><span class="sxs-lookup"><span data-stu-id="22a24-127">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="22a24-128">**DHCPEnabled**</span><span class="sxs-lookup"><span data-stu-id="22a24-128">**DHCPEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22a24-129">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="22a24-129">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="22a24-130">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="22a24-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="22a24-131">Especifica si DHCP está habilitado en la interfaz IPv4 del adaptador de red en el sistema operativo invitado.</span><span class="sxs-lookup"><span data-stu-id="22a24-131">Specifies whether DHCP is enabled on the IPv4 interface of the network adapter within the guest operating system.</span></span>

</dd> <dt>

<span data-ttu-id="22a24-132">**DNSServers**</span><span class="sxs-lookup"><span data-stu-id="22a24-132">**DNSServers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22a24-133">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="22a24-133">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="22a24-134">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="22a24-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="22a24-135">Calificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado")</span><span class="sxs-lookup"><span data-stu-id="22a24-135">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="22a24-136">Matriz de cadenas que especifican los servidores DNS configurados en el adaptador de red en el sistema operativo invitado.</span><span class="sxs-lookup"><span data-stu-id="22a24-136">An array of strings that specify the DNS servers configured on the network adapter within the guest operating system.</span></span>

</dd> <dt>

<span data-ttu-id="22a24-137">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="22a24-137">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22a24-138">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="22a24-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="22a24-139">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="22a24-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="22a24-140">Nombre para mostrar del objeto.</span><span class="sxs-lookup"><span data-stu-id="22a24-140">A display name for the object.</span></span> <span data-ttu-id="22a24-141">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)y siempre se establece en **null**.</span><span class="sxs-lookup"><span data-stu-id="22a24-141">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="22a24-142">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="22a24-142">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22a24-143">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="22a24-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="22a24-144">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="22a24-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="22a24-145">Calificadores: **clave**</span><span class="sxs-lookup"><span data-stu-id="22a24-145">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="22a24-146">Identifica de forma única una instancia de esta clase.</span><span class="sxs-lookup"><span data-stu-id="22a24-146">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="22a24-147">Esta propiedad se hereda del [**\_ SettingData de CIM**](/previous-versions//cc136911(v=vs.85))y siempre se establece en **null**.</span><span class="sxs-lookup"><span data-stu-id="22a24-147">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="22a24-148">**IPAddresses**</span><span class="sxs-lookup"><span data-stu-id="22a24-148">**IPAddresses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22a24-149">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="22a24-149">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="22a24-150">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="22a24-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="22a24-151">Calificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado")</span><span class="sxs-lookup"><span data-stu-id="22a24-151">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="22a24-152">Matriz de cadenas que especifican las direcciones IP configuradas en el adaptador de red en el sistema operativo invitado.</span><span class="sxs-lookup"><span data-stu-id="22a24-152">An array of strings that specify the IP addresses configured on the network adapter within the guest operating system.</span></span>

</dd> <dt>

<span data-ttu-id="22a24-153">**ProtocolIFType**</span><span class="sxs-lookup"><span data-stu-id="22a24-153">**ProtocolIFType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22a24-154">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="22a24-154">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="22a24-155">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="22a24-155">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="22a24-156">Identifica los protocolos de Internet a los que se aplica la configuración especificada por esta instancia.</span><span class="sxs-lookup"><span data-stu-id="22a24-156">Identifies the Internet protocols that the settings specified by this instance apply to.</span></span> <span data-ttu-id="22a24-157">Debe ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="22a24-157">This must be one of the following values.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="22a24-158"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="22a24-158"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="22a24-159"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="22a24-159"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="IPv4"></span><span id="ipv4"></span><span id="IPV4"></span>

<span data-ttu-id="22a24-160"><span id="IPv4"></span><span id="ipv4"></span><span id="IPV4"></span>**IPv4** (4096)</span><span class="sxs-lookup"><span data-stu-id="22a24-160"><span id="IPv4"></span><span id="ipv4"></span><span id="IPV4"></span>**IPv4** (4096)</span></span>


</dt> <dd></dd> <dt>

<span id="IPv6"></span><span id="ipv6"></span><span id="IPV6"></span>

<span data-ttu-id="22a24-161"><span id="IPv6"></span><span id="ipv6"></span><span id="IPV6"></span>**IPv6** (4097)</span><span class="sxs-lookup"><span data-stu-id="22a24-161"><span id="IPv6"></span><span id="ipv6"></span><span id="IPV6"></span>**IPv6** (4097)</span></span>


</dt> <dd></dd> <dt>

<span id="IPv4_v6"></span><span id="ipv4_v6"></span><span id="IPV4_V6"></span>

<span data-ttu-id="22a24-162"><span id="IPv4_v6"></span><span id="ipv4_v6"></span><span id="IPV4_V6"></span>**IPv4/V6** (4098)</span><span class="sxs-lookup"><span data-stu-id="22a24-162"><span id="IPv4_v6"></span><span id="ipv4_v6"></span><span id="IPV4_V6"></span>**IPv4/v6** (4098)</span></span>


</dt> <dd>

<span data-ttu-id="22a24-163">IPv4/IPv6</span><span class="sxs-lookup"><span data-stu-id="22a24-163">IPv4/IPv6</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="22a24-164">**Subredes**</span><span class="sxs-lookup"><span data-stu-id="22a24-164">**Subnets**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22a24-165">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="22a24-165">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="22a24-166">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="22a24-166">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="22a24-167">Calificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado")</span><span class="sxs-lookup"><span data-stu-id="22a24-167">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="22a24-168">Matriz de cadenas que especifican las subredes configuradas en el adaptador de red en el sistema operativo invitado.</span><span class="sxs-lookup"><span data-stu-id="22a24-168">An array of strings that specify the subnets configured on the network adapter within the guest operating system.</span></span> <span data-ttu-id="22a24-169">Cada elemento de esta matriz se aplica al elemento correspondiente de la matriz **IPAddresses** .</span><span class="sxs-lookup"><span data-stu-id="22a24-169">Each element in this array applies to the corresponding element in the **IPAddresses** array.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="22a24-170">Requisitos</span><span class="sxs-lookup"><span data-stu-id="22a24-170">Requirements</span></span>



| <span data-ttu-id="22a24-171">Requisito</span><span class="sxs-lookup"><span data-stu-id="22a24-171">Requirement</span></span> | <span data-ttu-id="22a24-172">Value</span><span class="sxs-lookup"><span data-stu-id="22a24-172">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="22a24-173">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="22a24-173">Minimum supported client</span></span><br/> | <span data-ttu-id="22a24-174">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="22a24-174">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="22a24-175">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="22a24-175">Minimum supported server</span></span><br/> | <span data-ttu-id="22a24-176">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="22a24-176">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="22a24-177">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="22a24-177">Namespace</span></span><br/>                | <span data-ttu-id="22a24-178">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="22a24-178">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="22a24-179">MOF</span><span class="sxs-lookup"><span data-stu-id="22a24-179">MOF</span></span><br/>                      | <dl> <span data-ttu-id="22a24-180"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="22a24-180"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="22a24-181">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="22a24-181">DLL</span></span><br/>                      | <dl> <span data-ttu-id="22a24-182"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="22a24-182"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

