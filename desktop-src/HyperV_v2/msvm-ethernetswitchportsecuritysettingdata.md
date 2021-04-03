---
description: Representa los datos de configuración de la característica de seguridad.
ms.assetid: 98e0de24-ccdc-4fc7-86a5-b68d454fde9d
title: Msvm_EthernetSwitchPortSecuritySettingData (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchPortSecuritySettingData
- Msvm_EthernetSwitchPortSecuritySettingData.InstanceID
- Msvm_EthernetSwitchPortSecuritySettingData.Caption
- Msvm_EthernetSwitchPortSecuritySettingData.Description
- Msvm_EthernetSwitchPortSecuritySettingData.ElementName
- Msvm_EthernetSwitchPortSecuritySettingData.AllowMacSpoofing
- Msvm_EthernetSwitchPortSecuritySettingData.EnableDhcpGuard
- Msvm_EthernetSwitchPortSecuritySettingData.EnableRouterGuard
- Msvm_EthernetSwitchPortSecuritySettingData.MonitorMode
- Msvm_EthernetSwitchPortSecuritySettingData.MonitorSession
- Msvm_EthernetSwitchPortSecuritySettingData.AllowIeeePriorityTag
- Msvm_EthernetSwitchPortSecuritySettingData.VirtualSubnetId
- Msvm_EthernetSwitchPortSecuritySettingData.AllowTeaming
- Msvm_EthernetSwitchPortSecuritySettingData.TeamName
- Msvm_EthernetSwitchPortSecuritySettingData.TeamNumber
- Msvm_EthernetSwitchPortSecuritySettingData.EnableFixSpeed10G
- Msvm_EthernetSwitchPortSecuritySettingData.Reserved
- Msvm_EthernetSwitchPortSecuritySettingData.DynamicIPAddressLimit
- Msvm_EthernetSwitchPortSecuritySettingData.StormLimit
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 8d37913f015a3ffbfaa751a7bbb10f79cea2fb39
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913886"
---
# <a name="msvm_ethernetswitchportsecuritysettingdata-class"></a><span data-ttu-id="03f77-103">MSVM \_ EthernetSwitchPortSecuritySettingData (clase)</span><span class="sxs-lookup"><span data-stu-id="03f77-103">Msvm\_EthernetSwitchPortSecuritySettingData class</span></span>

<span data-ttu-id="03f77-104">Representa los datos de configuración de la característica de seguridad.</span><span class="sxs-lookup"><span data-stu-id="03f77-104">Represents the security feature setting data.</span></span>

<span data-ttu-id="03f77-105">La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="03f77-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="03f77-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="03f77-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), UUID("776E0BA7-94A1-41C8-8F28-951F524251B5"), ExtensionId("11EC6134-128A-4A23-B12F-164184B48348"), InterfaceVersion("3"), InterfaceRevision("0"), DisplayName("Ethernet Switch Port Security Settings"), AMENDMENT]
class Msvm_EthernetSwitchPortSecuritySettingData : Msvm_EthernetSwitchPortFeatureSettingData
{
  string  InstanceID;
  string  Caption = "Ethernet Switch Port Security Settings";
  string  Description = "Represents the security feature setting data.";
  string  ElementName = "Ethernet Switch Port Security Settings";
  boolean AllowMacSpoofing = FALSE;
  boolean EnableDhcpGuard = FALSE;
  boolean EnableRouterGuard = FALSE;
  uint8   MonitorMode = 0;
  uint8   MonitorSession = 0;
  boolean AllowIeeePriorityTag = FALSE;
  uint32  VirtualSubnetId = 0;
  boolean AllowTeaming = FALSE;
  string  TeamName = ;
  uint32  TeamNumber = 0;
  boolean EnableFixSpeed10G = FALSE;
  boolean Reserved = FALSE;
  uint32  DynamicIPAddressLimit = 0;
  uint32  StormLimit = 0;
};
```

## <a name="members"></a><span data-ttu-id="03f77-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="03f77-107">Members</span></span>

<span data-ttu-id="03f77-108">La clase **MSVM \_ EthernetSwitchPortSecuritySettingData** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="03f77-108">The **Msvm\_EthernetSwitchPortSecuritySettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="03f77-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="03f77-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="03f77-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="03f77-110">Properties</span></span>

<span data-ttu-id="03f77-111">La clase **MSVM \_ EthernetSwitchPortSecuritySettingData** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="03f77-111">The **Msvm\_EthernetSwitchPortSecuritySettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="03f77-112">**AllowIeeePriorityTag**</span><span class="sxs-lookup"><span data-stu-id="03f77-112">**AllowIeeePriorityTag**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03f77-113">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="03f77-113">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="03f77-114">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="03f77-114">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="03f77-115">Calificadores: **WmiDataId** (6), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="03f77-115">Qualifiers: **WmiDataId** (6), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="03f77-116">Especifica si el tráfico hacia o desde el puerto conserva la información de 802.1 P.</span><span class="sxs-lookup"><span data-stu-id="03f77-116">Specifies whether traffic to/from the port retains 802.1P information.</span></span> <span data-ttu-id="03f77-117">Contiene **true** si el tráfico hacia o desde el puerto conserva la información de 802.1 p o **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="03f77-117">Contains **True** if traffic to/from the port retains 802.1P information or **False** otherwise.</span></span> <span data-ttu-id="03f77-118">El valor predeterminado es **False**.</span><span class="sxs-lookup"><span data-stu-id="03f77-118">The default value is **False**.</span></span>

</dd> <dt>

<span data-ttu-id="03f77-119">**AllowMacSpoofing**</span><span class="sxs-lookup"><span data-stu-id="03f77-119">**AllowMacSpoofing**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03f77-120">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="03f77-120">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="03f77-121">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="03f77-121">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="03f77-122">Calificadores: **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="03f77-122">Qualifiers: **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="03f77-123">Indica si el puerto permitirá la suplantación de direcciones MAC.</span><span class="sxs-lookup"><span data-stu-id="03f77-123">Indicates whether the port will allow MAC spoofing.</span></span> <span data-ttu-id="03f77-124">Si esta propiedad es **true**, el puerto permitirá la suplantación de direcciones MAC.</span><span class="sxs-lookup"><span data-stu-id="03f77-124">If this property is **True**, the port will allow MAC addresses to be spoofed.</span></span> <span data-ttu-id="03f77-125">Se permiten todos los valores de dirección MAC de unidifusión válidos.</span><span class="sxs-lookup"><span data-stu-id="03f77-125">All valid unicast MAC address values are allowed.</span></span> <span data-ttu-id="03f77-126">Si esta propiedad es **false**, el puerto solo permitirá el uso de direcciones MAC que estén configuradas en la administración de Hyper-V.</span><span class="sxs-lookup"><span data-stu-id="03f77-126">If this property is **False**, the port will only allow MAC addresses that are configured within Hyper-V management to be used.</span></span> <span data-ttu-id="03f77-127">El valor predeterminado es **False**.</span><span class="sxs-lookup"><span data-stu-id="03f77-127">The default value is **False**.</span></span>

</dd> <dt>

<span data-ttu-id="03f77-128">**AllowTeaming**</span><span class="sxs-lookup"><span data-stu-id="03f77-128">**AllowTeaming**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03f77-129">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="03f77-129">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="03f77-130">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="03f77-130">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="03f77-131">Calificadores: **WmiDataId** (8), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="03f77-131">Qualifiers: **WmiDataId** (8), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="03f77-132">Indica si las NIC conectadas al puerto pueden formar parte de un equipo.</span><span class="sxs-lookup"><span data-stu-id="03f77-132">Indicates whether the NICs connected to the port can be part of a team.</span></span> <span data-ttu-id="03f77-133">Esto solo se aplica a las NIC conectadas a máquinas virtuales.</span><span class="sxs-lookup"><span data-stu-id="03f77-133">This applies only to NICs connected to virtual machines.</span></span> <span data-ttu-id="03f77-134">Contiene **true** si se permite la formación de equipos NIC o **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="03f77-134">Contains **True** if NIC teaming is allowed or **False** otherwise.</span></span> <span data-ttu-id="03f77-135">El valor predeterminado es **False**.</span><span class="sxs-lookup"><span data-stu-id="03f77-135">The default value is **False**.</span></span>

</dd> <dt>

<span data-ttu-id="03f77-136">**Caption**</span><span class="sxs-lookup"><span data-stu-id="03f77-136">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03f77-137">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="03f77-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="03f77-138">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="03f77-138">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="03f77-139">Breve descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="03f77-139">A short description of the object.</span></span> <span data-ttu-id="03f77-140">Esta propiedad se hereda de [**la \_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)y siempre se establece en "configuración de seguridad del puerto de conmutador Ethernet".</span><span class="sxs-lookup"><span data-stu-id="03f77-140">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Ethernet Switch Port Security Settings".</span></span>

</dd> <dt>

<span data-ttu-id="03f77-141">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="03f77-141">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03f77-142">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="03f77-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="03f77-143">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="03f77-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="03f77-144">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="03f77-144">A description of the object.</span></span> <span data-ttu-id="03f77-145">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)y siempre está establecida en "representa los datos de configuración de la característica de seguridad".</span><span class="sxs-lookup"><span data-stu-id="03f77-145">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Represents the security feature setting data.".</span></span>

</dd> <dt>

<span data-ttu-id="03f77-146">**DynamicIPAddressLimit**</span><span class="sxs-lookup"><span data-stu-id="03f77-146">**DynamicIPAddressLimit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03f77-147">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="03f77-147">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="03f77-148">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="03f77-148">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="03f77-149">Calificadores: **WmiDataId** (12), **InterfaceVersion** (2), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="03f77-149">Qualifiers: **WmiDataId** (12), **InterfaceVersion** (2), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="03f77-150">Define el límite para el número de direcciones IP dinámicas conocidas.</span><span class="sxs-lookup"><span data-stu-id="03f77-150">Defines the limit for number of Dynamic IP addresses learned.</span></span> <span data-ttu-id="03f77-151">El valor predeterminado es none.</span><span class="sxs-lookup"><span data-stu-id="03f77-151">Default is none.</span></span>

</dd> <dt>

<span data-ttu-id="03f77-152">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="03f77-152">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03f77-153">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="03f77-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="03f77-154">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="03f77-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="03f77-155">Nombre para mostrar del objeto.</span><span class="sxs-lookup"><span data-stu-id="03f77-155">A display name for the object.</span></span> <span data-ttu-id="03f77-156">Esta propiedad se hereda de [**la \_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)y siempre se establece en "configuración de seguridad del puerto de conmutador Ethernet".</span><span class="sxs-lookup"><span data-stu-id="03f77-156">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Ethernet Switch Port Security Settings".</span></span>

</dd> <dt>

<span data-ttu-id="03f77-157">**EnableDhcpGuard**</span><span class="sxs-lookup"><span data-stu-id="03f77-157">**EnableDhcpGuard**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03f77-158">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="03f77-158">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="03f77-159">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="03f77-159">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="03f77-160">Calificadores: **WmiDataId** (2), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="03f77-160">Qualifiers: **WmiDataId** (2), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="03f77-161">Especifica si las ofertas DHCP están bloqueadas en el puerto.</span><span class="sxs-lookup"><span data-stu-id="03f77-161">Specifies whether DHCP offers are blocked from the port.</span></span> <span data-ttu-id="03f77-162">Contiene **true** si las ofertas de DHCP están bloqueadas en el puerto o **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="03f77-162">Contains **True** if DHCP offers are blocked from the port or **False** otherwise.</span></span> <span data-ttu-id="03f77-163">El valor predeterminado es **False**.</span><span class="sxs-lookup"><span data-stu-id="03f77-163">The default value is **False**.</span></span>

</dd> <dt>

<span data-ttu-id="03f77-164">**EnableFixSpeed10G**</span><span class="sxs-lookup"><span data-stu-id="03f77-164">**EnableFixSpeed10G**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03f77-165">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="03f77-165">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="03f77-166">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="03f77-166">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="03f77-167">Calificadores: **WmiDataId** (14), **InterfaceVersion** (3), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="03f77-167">Qualifiers: **WmiDataId** (14), **InterfaceVersion** (3), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="03f77-168">Establézcalo en TRUE si la velocidad fija 10G está habilitada, de lo contrario, FALSE.</span><span class="sxs-lookup"><span data-stu-id="03f77-168">Set to TRUE if Fixed Speed 10G is enabled else FALSE.</span></span> <span data-ttu-id="03f77-169">El valor predeterminado es FALSE.</span><span class="sxs-lookup"><span data-stu-id="03f77-169">Default value is FALSE.</span></span>

> [!Note]  
> <span data-ttu-id="03f77-170">Propiedad agregada en Windows 10.</span><span class="sxs-lookup"><span data-stu-id="03f77-170">Property added in Windows 10.</span></span>

 

</dd> <dt>

<span data-ttu-id="03f77-171">**EnableRouterGuard**</span><span class="sxs-lookup"><span data-stu-id="03f77-171">**EnableRouterGuard**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03f77-172">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="03f77-172">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="03f77-173">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="03f77-173">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="03f77-174">Calificadores: **WmiDataId** (3), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="03f77-174">Qualifiers: **WmiDataId** (3), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="03f77-175">Especifica si los anuncios de enrutador y las redirecciones de enrutador se bloquean desde el puerto.</span><span class="sxs-lookup"><span data-stu-id="03f77-175">Specifies whether router advertisements and router redirects are blocked from the port.</span></span> <span data-ttu-id="03f77-176">Contiene **true** si los anuncios de enrutador y las redirecciones de enrutador están bloqueados en el puerto o **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="03f77-176">Contains **True** if router advertisements and router redirects are blocked from the port or **False** otherwise.</span></span> <span data-ttu-id="03f77-177">El valor predeterminado es **False**.</span><span class="sxs-lookup"><span data-stu-id="03f77-177">The default value is **False**.</span></span>

</dd> <dt>

<span data-ttu-id="03f77-178">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="03f77-178">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03f77-179">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="03f77-179">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="03f77-180">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="03f77-180">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="03f77-181">Calificadores: **clave**</span><span class="sxs-lookup"><span data-stu-id="03f77-181">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="03f77-182">Identifica de forma única una instancia de esta clase.</span><span class="sxs-lookup"><span data-stu-id="03f77-182">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="03f77-183">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="03f77-183">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="03f77-184">**MonitorMode**</span><span class="sxs-lookup"><span data-stu-id="03f77-184">**MonitorMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03f77-185">Tipo de datos: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="03f77-185">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="03f77-186">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="03f77-186">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="03f77-187">Calificadores: **WmiDataId** (4), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="03f77-187">Qualifiers: **WmiDataId** (4), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="03f77-188">Indica el modo de monitor del puerto.</span><span class="sxs-lookup"><span data-stu-id="03f77-188">This indicates the monitor mode of the port.</span></span>

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="03f77-189">**Ninguno** (0)</span><span class="sxs-lookup"><span data-stu-id="03f77-189">**None** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Destination"></span><span id="destination"></span><span id="DESTINATION"></span>

<span data-ttu-id="03f77-190">**Destino** (1)</span><span class="sxs-lookup"><span data-stu-id="03f77-190">**Destination** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Source"></span><span id="source"></span><span id="SOURCE"></span>

<span data-ttu-id="03f77-191">**Origen** (2)</span><span class="sxs-lookup"><span data-stu-id="03f77-191">**Source** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="03f77-192">**MonitorSession**</span><span class="sxs-lookup"><span data-stu-id="03f77-192">**MonitorSession**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03f77-193">Tipo de datos: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="03f77-193">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="03f77-194">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="03f77-194">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="03f77-195">Calificadores: **WmiDataId** (5), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="03f77-195">Qualifiers: **WmiDataId** (5), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="03f77-196">Especifica el identificador de la sesión de monitor a la que pertenece este puerto.</span><span class="sxs-lookup"><span data-stu-id="03f77-196">Specifies the identifier of the monitor session this port belongs to.</span></span>

</dd> <dt>

<span data-ttu-id="03f77-197">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="03f77-197">**Reserved**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03f77-198">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="03f77-198">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="03f77-199">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="03f77-199">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="03f77-200">Calificadores: [**desusados**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("sin valor"), **WmiDataId** (13), **InterfaceVersion** (3), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="03f77-200">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("No value"), **WmiDataId** (13), **InterfaceVersion** (3), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="03f77-201">Reservado</span><span class="sxs-lookup"><span data-stu-id="03f77-201">Reserved</span></span>

> [!Note]  
> <span data-ttu-id="03f77-202">Propiedad agregada en Windows 10.</span><span class="sxs-lookup"><span data-stu-id="03f77-202">Property added in Windows 10.</span></span>

 

</dd> <dt>

<span data-ttu-id="03f77-203">**StormLimit**</span><span class="sxs-lookup"><span data-stu-id="03f77-203">**StormLimit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03f77-204">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="03f77-204">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="03f77-205">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="03f77-205">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="03f77-206">Calificadores: **WmiDataId** (11), **InterfaceVersion** (2), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="03f77-206">Qualifiers: **WmiDataId** (11), **InterfaceVersion** (2), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="03f77-207">Define el límite de paquetes por segundo para el tráfico de difusión y multidifusión.</span><span class="sxs-lookup"><span data-stu-id="03f77-207">Defines the packets per second limit for broadcast and multicast traffic.</span></span> <span data-ttu-id="03f77-208">El valor predeterminado es none.</span><span class="sxs-lookup"><span data-stu-id="03f77-208">Default is none.</span></span>

</dd> <dt>

<span data-ttu-id="03f77-209">**TeamName**</span><span class="sxs-lookup"><span data-stu-id="03f77-209">**TeamName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03f77-210">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="03f77-210">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="03f77-211">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="03f77-211">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="03f77-212">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (127), **WmiDataId** (9), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="03f77-212">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (127), **WmiDataId** (9), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="03f77-213">Reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="03f77-213">Reserved for future use.</span></span>

</dd> <dt>

<span data-ttu-id="03f77-214">**TeamNumber**</span><span class="sxs-lookup"><span data-stu-id="03f77-214">**TeamNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03f77-215">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="03f77-215">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="03f77-216">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="03f77-216">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="03f77-217">Calificadores: **WmiDataId** (10), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="03f77-217">Qualifiers: **WmiDataId** (10), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="03f77-218">Reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="03f77-218">Reserved for future use.</span></span>

</dd> <dt>

<span data-ttu-id="03f77-219">**VirtualSubnetId**</span><span class="sxs-lookup"><span data-stu-id="03f77-219">**VirtualSubnetId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03f77-220">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="03f77-220">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="03f77-221">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="03f77-221">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="03f77-222">Calificadores: **WmiDataId** (7), **InterfaceVersion** (1), **InterfaceRevision** (0), [**MinValue**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**MaxValue**](/windows/desktop/WmiSdk/standard-qualifiers) (16777215)</span><span class="sxs-lookup"><span data-stu-id="03f77-222">Qualifiers: **WmiDataId** (7), **InterfaceVersion** (1), **InterfaceRevision** (0), [**MinValue**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**MaxValue**](/windows/desktop/WmiSdk/standard-qualifiers) (16777215)</span></span>
</dt> </dl>

<span data-ttu-id="03f77-223">Especifica el identificador de la subred virtual de la que es miembro el puerto.</span><span class="sxs-lookup"><span data-stu-id="03f77-223">Specifies the identifier of the virtual subnet that the port is a member of.</span></span> <span data-ttu-id="03f77-224">El valor predeterminado es none.</span><span class="sxs-lookup"><span data-stu-id="03f77-224">The default is none.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="03f77-225">Requisitos</span><span class="sxs-lookup"><span data-stu-id="03f77-225">Requirements</span></span>



| <span data-ttu-id="03f77-226">Requisito</span><span class="sxs-lookup"><span data-stu-id="03f77-226">Requirement</span></span> | <span data-ttu-id="03f77-227">Value</span><span class="sxs-lookup"><span data-stu-id="03f77-227">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="03f77-228">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="03f77-228">Minimum supported client</span></span><br/> | <span data-ttu-id="03f77-229">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="03f77-229">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="03f77-230">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="03f77-230">Minimum supported server</span></span><br/> | <span data-ttu-id="03f77-231">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="03f77-231">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="03f77-232">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="03f77-232">Namespace</span></span><br/>                | <span data-ttu-id="03f77-233">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="03f77-233">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="03f77-234">MOF</span><span class="sxs-lookup"><span data-stu-id="03f77-234">MOF</span></span><br/>                      | <dl> <span data-ttu-id="03f77-235"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="03f77-235"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="03f77-236">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="03f77-236">DLL</span></span><br/>                      | <dl> <span data-ttu-id="03f77-237"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="03f77-237"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

