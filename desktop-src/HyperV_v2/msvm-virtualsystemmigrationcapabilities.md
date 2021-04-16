---
description: Define los medios por los que un cliente puede detectar los métodos proporcionados por el servicio de migración y el intervalo válido de datos de configuración de migración del sistema virtual.
ms.assetid: 704fa81d-54a4-4d12-9b85-8836581d2784
title: Msvm_VirtualSystemMigrationCapabilities (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemMigrationCapabilities
- Msvm_VirtualSystemMigrationCapabilities.InstanceID
- Msvm_VirtualSystemMigrationCapabilities.Caption
- Msvm_VirtualSystemMigrationCapabilities.Description
- Msvm_VirtualSystemMigrationCapabilities.ElementName
- Msvm_VirtualSystemMigrationCapabilities.SynchronousMethodsSupported
- Msvm_VirtualSystemMigrationCapabilities.AsynchronousMethodsSupported
- Msvm_VirtualSystemMigrationCapabilities.DestinationHostFormatsSupported
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: c89e898cbf861d2bc3643e43a8bd9089062a2d32
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540283"
---
# <a name="msvm_virtualsystemmigrationcapabilities-class"></a><span data-ttu-id="abb41-103">MSVM \_ VirtualSystemMigrationCapabilities (clase)</span><span class="sxs-lookup"><span data-stu-id="abb41-103">Msvm\_VirtualSystemMigrationCapabilities class</span></span>

<span data-ttu-id="abb41-104">Define los medios por los que un cliente puede detectar los métodos proporcionados por el servicio de migración y el intervalo válido de datos de configuración de migración del sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="abb41-104">Defines the means by which a client can discover the methods provided by the migration service, and valid range of virtual system migration setting data.</span></span> <span data-ttu-id="abb41-105">El **objeto \_ VirtualSystemMigrationCapabilities MSVM** está asociado a [**objetos \_ MSVM VirtualSystemMigrationSettingData**](msvm-virtualsystemmigrationsettingdata.md) .</span><span class="sxs-lookup"><span data-stu-id="abb41-105">The **Msvm\_VirtualSystemMigrationCapabilities** object is associated with [**Msvm\_VirtualSystemMigrationSettingData**](msvm-virtualsystemmigrationsettingdata.md) objects.</span></span> <span data-ttu-id="abb41-106">Estas asociaciones definen el intervalo válido de servicios de migración disponible.</span><span class="sxs-lookup"><span data-stu-id="abb41-106">These associations define the valid range of migration services available.</span></span>

<span data-ttu-id="abb41-107">La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="abb41-107">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="abb41-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="abb41-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualSystemMigrationCapabilities : CIM_VirtualSystemMigrationCapabilities
{
  string InstanceID;
  string Caption = "Migration Capabilities";
  string Description = "Virtual System Migration Capabilities";
  string ElementName;
  uint16 SynchronousMethodsSupported[];
  uint16 AsynchronousMethodsSupported[];
  uint16 DestinationHostFormatsSupported[];
};
```

## <a name="members"></a><span data-ttu-id="abb41-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="abb41-109">Members</span></span>

<span data-ttu-id="abb41-110">La clase **MSVM \_ VirtualSystemMigrationCapabilities** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="abb41-110">The **Msvm\_VirtualSystemMigrationCapabilities** class has these types of members:</span></span>

-   [<span data-ttu-id="abb41-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="abb41-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="abb41-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="abb41-112">Properties</span></span>

<span data-ttu-id="abb41-113">La clase **MSVM \_ VirtualSystemMigrationCapabilities** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="abb41-113">The **Msvm\_VirtualSystemMigrationCapabilities** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="abb41-114">**AsynchronousMethodsSupported**</span><span class="sxs-lookup"><span data-stu-id="abb41-114">**AsynchronousMethodsSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="abb41-115">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="abb41-115">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="abb41-116">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="abb41-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="abb41-117">Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("AsynchronousMethodsSupported")</span><span class="sxs-lookup"><span data-stu-id="abb41-117">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("AsynchronousMethodsSupported")</span></span>
</dt> </dl>

<span data-ttu-id="abb41-118">Identifica los métodos cuya implementación puede ser asincrónica; es decir, la operación no se completará inmediatamente y devolverá un trabajo.</span><span class="sxs-lookup"><span data-stu-id="abb41-118">Identifies the methods whose implementation may be asynchronous; that is, the operation will not be completed immediately and will return a job.</span></span> <span data-ttu-id="abb41-119">Esta propiedad se hereda de **\_ VirtualSystemMigrationCapabilities CIM**.</span><span class="sxs-lookup"><span data-stu-id="abb41-119">This property is inherited from **CIM\_VirtualSystemMigrationCapabilities**.</span></span>

<dt>

<span id="MigrateVirtualSystemToHostSupported"></span><span id="migratevirtualsystemtohostsupported"></span><span id="MIGRATEVIRTUALSYSTEMTOHOSTSUPPORTED"></span>

<span data-ttu-id="abb41-120">**MigrateVirtualSystemToHostSupported** (2)</span><span class="sxs-lookup"><span data-stu-id="abb41-120">**MigrateVirtualSystemToHostSupported** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="MigrateVirtualSystemToSystemSupported"></span><span id="migratevirtualsystemtosystemsupported"></span><span id="MIGRATEVIRTUALSYSTEMTOSYSTEMSUPPORTED"></span>

<span data-ttu-id="abb41-121">**MigrateVirtualSystemToSystemSupported** (3)</span><span class="sxs-lookup"><span data-stu-id="abb41-121">**MigrateVirtualSystemToSystemSupported** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="CheckVirtualSystemIsMigratableSupported"></span><span id="checkvirtualsystemismigratablesupported"></span><span id="CHECKVIRTUALSYSTEMISMIGRATABLESUPPORTED"></span>

<span data-ttu-id="abb41-122">**CheckVirtualSystemIsMigratableSupported** (32768)</span><span class="sxs-lookup"><span data-stu-id="abb41-122">**CheckVirtualSystemIsMigratableSupported** (32768)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="abb41-123">**Caption**</span><span class="sxs-lookup"><span data-stu-id="abb41-123">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="abb41-124">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="abb41-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="abb41-125">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="abb41-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="abb41-126">Breve descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="abb41-126">A short description of the object.</span></span> <span data-ttu-id="abb41-127">Esta propiedad se hereda de [**la \_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)y siempre se establece en "capacidades de migración".</span><span class="sxs-lookup"><span data-stu-id="abb41-127">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Migration Capabilities".</span></span>

</dd> <dt>

<span data-ttu-id="abb41-128">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="abb41-128">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="abb41-129">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="abb41-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="abb41-130">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="abb41-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="abb41-131">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="abb41-131">A description of the object.</span></span> <span data-ttu-id="abb41-132">Esta propiedad se hereda de [**la \_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)y siempre se establece en "capacidades de migración del sistema virtual".</span><span class="sxs-lookup"><span data-stu-id="abb41-132">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Virtual System Migration Capabilities".</span></span>

</dd> <dt>

<span data-ttu-id="abb41-133">**DestinationHostFormatsSupported**</span><span class="sxs-lookup"><span data-stu-id="abb41-133">**DestinationHostFormatsSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="abb41-134">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="abb41-134">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="abb41-135">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="abb41-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="abb41-136">Matriz de formatos de nombre que se admiten para el parámetro *DestinationHost* de los métodos [**MigrateVirtualSystemToHost**](migratevirtualsystemtohost-msvm-virtualsystemmigrationservice.md) y [**CheckVirtualSystemIsMigratable**](checkvirtualsystemismigratable-msvm-virtualsystemmigrationservice.md) .</span><span class="sxs-lookup"><span data-stu-id="abb41-136">An array of name formats that are supported for the *DestinationHost* parameter of the [**MigrateVirtualSystemToHost**](migratevirtualsystemtohost-msvm-virtualsystemmigrationservice.md) and [**CheckVirtualSystemIsMigratable**](checkvirtualsystemismigratable-msvm-virtualsystemmigrationservice.md) methods.</span></span> <span data-ttu-id="abb41-137">Esta propiedad se hereda de **\_ VirtualSystemMigrationCapabilities CIM**.</span><span class="sxs-lookup"><span data-stu-id="abb41-137">This property is inherited from **CIM\_VirtualSystemMigrationCapabilities**.</span></span>



| <span data-ttu-id="abb41-138">Value</span><span class="sxs-lookup"><span data-stu-id="abb41-138">Value</span></span>                                                                                                                                                                                                                                                                                                                           | <span data-ttu-id="abb41-139">Significado</span><span class="sxs-lookup"><span data-stu-id="abb41-139">Meaning</span></span>                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <span id="DomainNameFormatSupported"></span><span id="domainnameformatsupported"></span><span id="DOMAINNAMEFORMATSUPPORTED"></span><dl> <span data-ttu-id="abb41-140"><dt>**DomainNameFormatSupported**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="abb41-140"><dt>**DomainNameFormatSupported**</dt> <dt>2</dt></span></span> </dl>                             | <span data-ttu-id="abb41-141">Compatibilidad con el formato de nombre de dominio según RFC 10353.</span><span class="sxs-lookup"><span data-stu-id="abb41-141">Support of the domain name format according to RFC 10353.</span></span><br/>         |
| <span id="IPv4DottedDecimalFormatSupported"></span><span id="ipv4dotteddecimalformatsupported"></span><span id="IPV4DOTTEDDECIMALFORMATSUPPORTED"></span><dl> <span data-ttu-id="abb41-142"><dt>**IPv4DottedDecimalFormatSupported**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="abb41-142"><dt>**IPv4DottedDecimalFormatSupported**</dt> <dt>3</dt></span></span> </dl> | <span data-ttu-id="abb41-143">Compatibilidad con el formato decimal con puntos de IPv4 según RFC 12084.</span><span class="sxs-lookup"><span data-stu-id="abb41-143">Support of the IPv4 dotted decimal format according to RFC 12084.</span></span><br/> |
| <span id="IPv6TextFormatSupported"></span><span id="ipv6textformatsupported"></span><span id="IPV6TEXTFORMATSUPPORTED"></span><dl> <span data-ttu-id="abb41-144"><dt>**IPv6TextFormatSupported**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="abb41-144"><dt>**IPv6TextFormatSupported**</dt> <dt>4</dt></span></span> </dl>                                     | <span data-ttu-id="abb41-145">Compatibilidad con el formato de texto IPv6 según RFC 4291.</span><span class="sxs-lookup"><span data-stu-id="abb41-145">Support of the IPv6 text format according to RFC 4291.</span></span><br/>            |



 

</dd> <dt>

<span data-ttu-id="abb41-146">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="abb41-146">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="abb41-147">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="abb41-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="abb41-148">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="abb41-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="abb41-149">Nombre para mostrar del objeto.</span><span class="sxs-lookup"><span data-stu-id="abb41-149">A display name for the object.</span></span> <span data-ttu-id="abb41-150">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="abb41-150">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="abb41-151">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="abb41-151">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="abb41-152">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="abb41-152">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="abb41-153">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="abb41-153">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="abb41-154">Calificadores: **clave**</span><span class="sxs-lookup"><span data-stu-id="abb41-154">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="abb41-155">Identifica de forma única una instancia de esta clase.</span><span class="sxs-lookup"><span data-stu-id="abb41-155">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="abb41-156">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="abb41-156">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="abb41-157">**SynchronousMethodsSupported**</span><span class="sxs-lookup"><span data-stu-id="abb41-157">**SynchronousMethodsSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="abb41-158">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="abb41-158">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="abb41-159">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="abb41-159">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="abb41-160">Identifica los métodos cuya implementación puede ser sincrónica; es decir, la operación se completará inmediatamente y no devolverá un trabajo.</span><span class="sxs-lookup"><span data-stu-id="abb41-160">Identifies the methods whose implementation may be synchronous; that is, the operation will be completed immediately and will not return a job.</span></span> <span data-ttu-id="abb41-161">Esta propiedad se hereda de **\_ VirtualSystemMigrationCapabilities CIM**.</span><span class="sxs-lookup"><span data-stu-id="abb41-161">This property is inherited from **CIM\_VirtualSystemMigrationCapabilities**.</span></span>

<dl> <dt>

<span data-ttu-id="abb41-162"><span id="MigrateVirtualSystemToHostSupported"></span><span id="migratevirtualsystemtohostsupported"></span><span id="MIGRATEVIRTUALSYSTEMTOHOSTSUPPORTED"></span>**MigrateVirtualSystemToHostSupported** (2)</span><span class="sxs-lookup"><span data-stu-id="abb41-162"><span id="MigrateVirtualSystemToHostSupported"></span><span id="migratevirtualsystemtohostsupported"></span><span id="MIGRATEVIRTUALSYSTEMTOHOSTSUPPORTED"></span>**MigrateVirtualSystemToHostSupported** (2)</span></span>
</dt> <dt>

<span data-ttu-id="abb41-163"><span id="MigrateVirtualSystemToSystemSupported"></span><span id="migratevirtualsystemtosystemsupported"></span><span id="MIGRATEVIRTUALSYSTEMTOSYSTEMSUPPORTED"></span>**MigrateVirtualSystemToSystemSupported** (3)</span><span class="sxs-lookup"><span data-stu-id="abb41-163"><span id="MigrateVirtualSystemToSystemSupported"></span><span id="migratevirtualsystemtosystemsupported"></span><span id="MIGRATEVIRTUALSYSTEMTOSYSTEMSUPPORTED"></span>**MigrateVirtualSystemToSystemSupported** (3)</span></span>
</dt> <dt>

<span data-ttu-id="abb41-164"><span id="CheckVirtualSystemIsMigratableToHostSupported"></span><span id="checkvirtualsystemismigratabletohostsupported"></span><span id="CHECKVIRTUALSYSTEMISMIGRATABLETOHOSTSUPPORTED"></span>**CheckVirtualSystemIsMigratableToHostSupported** (4)</span><span class="sxs-lookup"><span data-stu-id="abb41-164"><span id="CheckVirtualSystemIsMigratableToHostSupported"></span><span id="checkvirtualsystemismigratabletohostsupported"></span><span id="CHECKVIRTUALSYSTEMISMIGRATABLETOHOSTSUPPORTED"></span>**CheckVirtualSystemIsMigratableToHostSupported** (4)</span></span>
</dt> <dt>

<span data-ttu-id="abb41-165"><span id="CheckVirtualSystemIsMigratableToSystemSupported"></span><span id="checkvirtualsystemismigratabletosystemsupported"></span><span id="CHECKVIRTUALSYSTEMISMIGRATABLETOSYSTEMSUPPORTED"></span>**CheckVirtualSystemIsMigratableToSystemSupported** (5)</span><span class="sxs-lookup"><span data-stu-id="abb41-165"><span id="CheckVirtualSystemIsMigratableToSystemSupported"></span><span id="checkvirtualsystemismigratabletosystemsupported"></span><span id="CHECKVIRTUALSYSTEMISMIGRATABLETOSYSTEMSUPPORTED"></span>**CheckVirtualSystemIsMigratableToSystemSupported** (5)</span></span>
</dt> <dt>

<span data-ttu-id="abb41-166"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF reservado** (..</span><span class="sxs-lookup"><span data-stu-id="abb41-166"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF Reserved** (..</span></span> <span data-ttu-id="abb41-167">)</span><span class="sxs-lookup"><span data-stu-id="abb41-167">)</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="abb41-168">Requisitos</span><span class="sxs-lookup"><span data-stu-id="abb41-168">Requirements</span></span>



| <span data-ttu-id="abb41-169">Requisito</span><span class="sxs-lookup"><span data-stu-id="abb41-169">Requirement</span></span> | <span data-ttu-id="abb41-170">Value</span><span class="sxs-lookup"><span data-stu-id="abb41-170">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="abb41-171">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="abb41-171">Minimum supported client</span></span><br/> | <span data-ttu-id="abb41-172">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="abb41-172">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="abb41-173">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="abb41-173">Minimum supported server</span></span><br/> | <span data-ttu-id="abb41-174">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="abb41-174">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="abb41-175">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="abb41-175">Namespace</span></span><br/>                | <span data-ttu-id="abb41-176">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="abb41-176">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="abb41-177">MOF</span><span class="sxs-lookup"><span data-stu-id="abb41-177">MOF</span></span><br/>                      | <dl> <span data-ttu-id="abb41-178"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="abb41-178"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="abb41-179">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="abb41-179">DLL</span></span><br/>                      | <dl> <span data-ttu-id="abb41-180"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="abb41-180"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

