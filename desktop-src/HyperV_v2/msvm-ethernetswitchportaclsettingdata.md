---
description: Representa la lista de control de acceso (ACL) para la configuración del puerto del conmutador.
ms.assetid: c0d6dfa1-017c-4e66-9ee3-425182d84231
title: Msvm_EthernetSwitchPortAclSettingData (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchPortAclSettingData
- Msvm_EthernetSwitchPortAclSettingData.InstanceID
- Msvm_EthernetSwitchPortAclSettingData.Caption
- Msvm_EthernetSwitchPortAclSettingData.Description
- Msvm_EthernetSwitchPortAclSettingData.ElementName
- Msvm_EthernetSwitchPortAclSettingData.Name
- Msvm_EthernetSwitchPortAclSettingData.Direction
- Msvm_EthernetSwitchPortAclSettingData.Applicability
- Msvm_EthernetSwitchPortAclSettingData.AclType
- Msvm_EthernetSwitchPortAclSettingData.Action
- Msvm_EthernetSwitchPortAclSettingData.LocalAddress
- Msvm_EthernetSwitchPortAclSettingData.LocalAddressPrefixLength
- Msvm_EthernetSwitchPortAclSettingData.RemoteAddress
- Msvm_EthernetSwitchPortAclSettingData.RemoteAddressPrefixLength
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 92735718e339a0caf33910dec703276aea946a67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105689582"
---
# <a name="msvm_ethernetswitchportaclsettingdata-class"></a><span data-ttu-id="0308c-103">MSVM \_ EthernetSwitchPortAclSettingData (clase)</span><span class="sxs-lookup"><span data-stu-id="0308c-103">Msvm\_EthernetSwitchPortAclSettingData class</span></span>

<span data-ttu-id="0308c-104">Representa la lista de control de acceso (ACL) para la configuración del puerto del conmutador.</span><span class="sxs-lookup"><span data-stu-id="0308c-104">Represents the access control list (ACL) for switch port settings.</span></span>

<span data-ttu-id="0308c-105">La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="0308c-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="0308c-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0308c-106">Syntax</span></span>

``` syntax
[Dynamic, UUID("998BEF4A-5D55-492A-9C43-8B2F5EAE9F2B"), ExtensionId("11EC6134-128A-4A23-B12F-164184B48348"), Provider("VmmsWmiInstanceAndMethodProvider"), InterfaceVersion("1"), InterfaceRevision("0"), DisplayName("Ethernet Switch Port ACL Settings"), AMENDMENT]
class Msvm_EthernetSwitchPortAclSettingData : Msvm_EthernetSwitchPortFeatureSettingData
{
  string InstanceID;
  string Caption = "Ethernet Switch Port ACL Settings";
  string Description = "Represents the base class for switch port settings.";
  string ElementName = "Ethernet Switch Port ACL Settings";
  string Name = "";
  uint8  Direction = 0;
  uint8  Applicability = 0;
  uint8  AclType = 0;
  uint8  Action = 0;
  string LocalAddress = "";
  uint8  LocalAddressPrefixLength = 0;
  string RemoteAddress = length = 0;
  uint8  RemoteAddressPrefixLength = 0;
};
```

## <a name="members"></a><span data-ttu-id="0308c-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="0308c-107">Members</span></span>

<span data-ttu-id="0308c-108">La clase **MSVM \_ EthernetSwitchPortAclSettingData** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="0308c-108">The **Msvm\_EthernetSwitchPortAclSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="0308c-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="0308c-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0308c-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="0308c-110">Properties</span></span>

<span data-ttu-id="0308c-111">La clase **MSVM \_ EthernetSwitchPortAclSettingData** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="0308c-111">The **Msvm\_EthernetSwitchPortAclSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0308c-112">**AclType**</span><span class="sxs-lookup"><span data-stu-id="0308c-112">**AclType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0308c-113">Tipo de datos: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="0308c-113">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="0308c-114">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="0308c-114">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="0308c-115">Calificadores: **WmiDataId** (4), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="0308c-115">Qualifiers: **WmiDataId** (4), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="0308c-116">Indica el tipo de extremo de ACL.</span><span class="sxs-lookup"><span data-stu-id="0308c-116">This indicates the type of ACL endpoint.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="0308c-117">**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="0308c-117">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="MAC_Acl"></span><span id="mac_acl"></span><span id="MAC_ACL"></span>

<span data-ttu-id="0308c-118">**ACL de Mac** (1)</span><span class="sxs-lookup"><span data-stu-id="0308c-118">**MAC Acl** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="IPv4_Acl"></span><span id="ipv4_acl"></span><span id="IPV4_ACL"></span>

<span data-ttu-id="0308c-119">**ACL IPv4** (2)</span><span class="sxs-lookup"><span data-stu-id="0308c-119">**IPv4 Acl** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="IPv6_Acl"></span><span id="ipv6_acl"></span><span id="IPV6_ACL"></span>

<span data-ttu-id="0308c-120">**ACL de IPv6** (3)</span><span class="sxs-lookup"><span data-stu-id="0308c-120">**IPv6 Acl** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="0308c-121">**Acción**</span><span class="sxs-lookup"><span data-stu-id="0308c-121">**Action**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0308c-122">Tipo de datos: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="0308c-122">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="0308c-123">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="0308c-123">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="0308c-124">Calificadores: **WmiDataId** (5), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="0308c-124">Qualifiers: **WmiDataId** (5), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="0308c-125">Indica la acción de la ACL.</span><span class="sxs-lookup"><span data-stu-id="0308c-125">This indicates the action of the ACL.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="0308c-126">**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="0308c-126">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Allow"></span><span id="allow"></span><span id="ALLOW"></span>

<span data-ttu-id="0308c-127">**Permitir** (1)</span><span class="sxs-lookup"><span data-stu-id="0308c-127">**Allow** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Deny"></span><span id="deny"></span><span id="DENY"></span>

<span data-ttu-id="0308c-128">**Denegar** (2)</span><span class="sxs-lookup"><span data-stu-id="0308c-128">**Deny** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Meter"></span><span id="meter"></span><span id="METER"></span>

<span data-ttu-id="0308c-129">**Medidor** (3)</span><span class="sxs-lookup"><span data-stu-id="0308c-129">**Meter** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="0308c-130">**Aplicabilidad**</span><span class="sxs-lookup"><span data-stu-id="0308c-130">**Applicability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0308c-131">Tipo de datos: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="0308c-131">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="0308c-132">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="0308c-132">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="0308c-133">Calificadores: **WmiDataId** (3), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="0308c-133">Qualifiers: **WmiDataId** (3), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="0308c-134">Indica si la ACL se aplica al punto de conexión local o remoto.</span><span class="sxs-lookup"><span data-stu-id="0308c-134">This indicates whether the ACL applies to the local or remote endpoint.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="0308c-135">**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="0308c-135">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Local"></span><span id="local"></span><span id="LOCAL"></span>

<span data-ttu-id="0308c-136">**Local** (1)</span><span class="sxs-lookup"><span data-stu-id="0308c-136">**Local** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Remote"></span><span id="remote"></span><span id="REMOTE"></span>

<span data-ttu-id="0308c-137">**Remoto** (2)</span><span class="sxs-lookup"><span data-stu-id="0308c-137">**Remote** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="0308c-138">**Caption**</span><span class="sxs-lookup"><span data-stu-id="0308c-138">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0308c-139">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="0308c-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0308c-140">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0308c-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0308c-141">Breve descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="0308c-141">A short description of the object.</span></span> <span data-ttu-id="0308c-142">Esta propiedad se hereda de [**la \_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)y siempre se establece en "configuración de ACL del puerto de conmutador Ethernet".</span><span class="sxs-lookup"><span data-stu-id="0308c-142">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Ethernet Switch Port ACL Settings".</span></span>

</dd> <dt>

<span data-ttu-id="0308c-143">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="0308c-143">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0308c-144">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="0308c-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0308c-145">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0308c-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0308c-146">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="0308c-146">A description of the object.</span></span> <span data-ttu-id="0308c-147">Esta propiedad se hereda de [**la \_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)y siempre se establece en "representa la clase base para la configuración del puerto del conmutador".</span><span class="sxs-lookup"><span data-stu-id="0308c-147">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Represents the base class for switch port settings.".</span></span>

</dd> <dt>

<span data-ttu-id="0308c-148">**Dirección**</span><span class="sxs-lookup"><span data-stu-id="0308c-148">**Direction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0308c-149">Tipo de datos: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="0308c-149">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="0308c-150">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="0308c-150">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="0308c-151">Calificadores: **WmiDataId** (2), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="0308c-151">Qualifiers: **WmiDataId** (2), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="0308c-152">Indica si la ACL se aplica a la dirección de entrada o de salida.</span><span class="sxs-lookup"><span data-stu-id="0308c-152">This indicates whether the ACL applies to ingress or egress direction.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="0308c-153">**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="0308c-153">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Incoming"></span><span id="incoming"></span><span id="INCOMING"></span>

<span data-ttu-id="0308c-154">**Entrante** (1)</span><span class="sxs-lookup"><span data-stu-id="0308c-154">**Incoming** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Outgoing"></span><span id="outgoing"></span><span id="OUTGOING"></span>

<span data-ttu-id="0308c-155">**Saliente** (2)</span><span class="sxs-lookup"><span data-stu-id="0308c-155">**Outgoing** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="0308c-156">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="0308c-156">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0308c-157">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="0308c-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0308c-158">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0308c-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0308c-159">Nombre para mostrar del objeto.</span><span class="sxs-lookup"><span data-stu-id="0308c-159">A display name for the object.</span></span> <span data-ttu-id="0308c-160">Esta propiedad se hereda de [**la \_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)y siempre se establece en "configuración de ACL del puerto de conmutador Ethernet".</span><span class="sxs-lookup"><span data-stu-id="0308c-160">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Ethernet Switch Port ACL Settings".</span></span>

</dd> <dt>

<span data-ttu-id="0308c-161">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="0308c-161">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0308c-162">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="0308c-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0308c-163">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0308c-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0308c-164">Calificadores: **clave**</span><span class="sxs-lookup"><span data-stu-id="0308c-164">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="0308c-165">Identifica de forma única una instancia de esta clase.</span><span class="sxs-lookup"><span data-stu-id="0308c-165">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="0308c-166">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="0308c-166">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="0308c-167">**LocalAddress**</span><span class="sxs-lookup"><span data-stu-id="0308c-167">**LocalAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0308c-168">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="0308c-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0308c-169">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="0308c-169">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="0308c-170">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (40), **WmiDataId** (6), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="0308c-170">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (40), **WmiDataId** (6), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="0308c-171">Dirección local de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="0308c-171">The local address of the virtual machine.</span></span> <span data-ttu-id="0308c-172">Puede ser una dirección IPv4, IPv6 o MAC.</span><span class="sxs-lookup"><span data-stu-id="0308c-172">This can be an IPv4, IPv6, or a MAC address.</span></span>

</dd> <dt>

<span data-ttu-id="0308c-173">**LocalAddressPrefixLength**</span><span class="sxs-lookup"><span data-stu-id="0308c-173">**LocalAddressPrefixLength**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0308c-174">Tipo de datos: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="0308c-174">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="0308c-175">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="0308c-175">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="0308c-176">Calificadores: **WmiDataId** (7), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="0308c-176">Qualifiers: **WmiDataId** (7), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="0308c-177">La longitud del prefijo de dirección local.</span><span class="sxs-lookup"><span data-stu-id="0308c-177">The local address prefix length.</span></span>

</dd> <dt>

<span data-ttu-id="0308c-178">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="0308c-178">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0308c-179">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="0308c-179">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0308c-180">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="0308c-180">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="0308c-181">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="0308c-181">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="0308c-182">Nombre para mostrar de la ACL.</span><span class="sxs-lookup"><span data-stu-id="0308c-182">The display name of the ACL.</span></span>

</dd> <dt>

<span data-ttu-id="0308c-183">**RemoteAddress**</span><span class="sxs-lookup"><span data-stu-id="0308c-183">**RemoteAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0308c-184">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="0308c-184">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0308c-185">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="0308c-185">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="0308c-186">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (40), **WmiDataId** (8), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="0308c-186">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (40), **WmiDataId** (8), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="0308c-187">La dirección remota de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="0308c-187">The remote address of the virtual machine.</span></span> <span data-ttu-id="0308c-188">Puede ser IPv4, IPv6 o una dirección MAC.</span><span class="sxs-lookup"><span data-stu-id="0308c-188">This can be IPv4, IPv6, or a MAC address.</span></span>

</dd> <dt>

<span data-ttu-id="0308c-189">**RemoteAddressPrefixLength**</span><span class="sxs-lookup"><span data-stu-id="0308c-189">**RemoteAddressPrefixLength**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0308c-190">Tipo de datos: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="0308c-190">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="0308c-191">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="0308c-191">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="0308c-192">Calificadores: **WmiDataId** (9), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="0308c-192">Qualifiers: **WmiDataId** (9), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="0308c-193">La longitud del prefijo de la dirección remota.</span><span class="sxs-lookup"><span data-stu-id="0308c-193">The remote address prefix length.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0308c-194">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0308c-194">Requirements</span></span>



| <span data-ttu-id="0308c-195">Requisito</span><span class="sxs-lookup"><span data-stu-id="0308c-195">Requirement</span></span> | <span data-ttu-id="0308c-196">Value</span><span class="sxs-lookup"><span data-stu-id="0308c-196">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0308c-197">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0308c-197">Minimum supported client</span></span><br/> | <span data-ttu-id="0308c-198">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="0308c-198">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="0308c-199">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0308c-199">Minimum supported server</span></span><br/> | <span data-ttu-id="0308c-200">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="0308c-200">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="0308c-201">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="0308c-201">Namespace</span></span><br/>                | <span data-ttu-id="0308c-202">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="0308c-202">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="0308c-203">MOF</span><span class="sxs-lookup"><span data-stu-id="0308c-203">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0308c-204"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0308c-204"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="0308c-205">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="0308c-205">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0308c-206"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="0308c-206"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

