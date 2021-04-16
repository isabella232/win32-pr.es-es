---
description: Representa las capacidades de un \_ objeto VirtualSystemMigrationService de CIM.
ms.assetid: 5fe3a10b-c075-4c45-838d-0b5c2e491584
title: CIM_VirtualSystemMigrationCapabilities (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemMigrationCapabilities
- CIM_VirtualSystemMigrationCapabilities.SynchronousMethodsSupported
- CIM_VirtualSystemMigrationCapabilities.AsynchronousMethodsSupported
- CIM_VirtualSystemMigrationCapabilities.DestinationHostFormatsSupported
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 1a9a9a0a0f8e9ea344c7a37ad1168dcb5e059093
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104545219"
---
# <a name="cim_virtualsystemmigrationcapabilities-class"></a><span data-ttu-id="664fa-103">\_Clase VirtualSystemMigrationCapabilities de CIM</span><span class="sxs-lookup"><span data-stu-id="664fa-103">CIM\_VirtualSystemMigrationCapabilities class</span></span>

<span data-ttu-id="664fa-104">Representa las capacidades de un [**objeto \_ VirtualSystemMigrationService de CIM**](cim-virtualsystemmigrationservice.md) .</span><span class="sxs-lookup"><span data-stu-id="664fa-104">Represents the capabilities of a [**CIM\_VirtualSystemMigrationService**](cim-virtualsystemmigrationservice.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="664fa-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="664fa-105">Syntax</span></span>

``` syntax
[Experimental, Abstract, Version("2.17.0"), UMLPackagePath("CIM::System::Virtualization"), AMENDMENT]
class CIM_VirtualSystemMigrationCapabilities : CIM_Capabilities
{
  uint16 SynchronousMethodsSupported[];
  uint16 AsynchronousMethodsSupported[];
  uint16 DestinationHostFormatsSupported[];
};
```

## <a name="members"></a><span data-ttu-id="664fa-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="664fa-106">Members</span></span>

<span data-ttu-id="664fa-107">La clase **CIM \_ VirtualSystemMigrationCapabilities** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="664fa-107">The **CIM\_VirtualSystemMigrationCapabilities** class has these types of members:</span></span>

-   [<span data-ttu-id="664fa-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="664fa-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="664fa-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="664fa-109">Properties</span></span>

<span data-ttu-id="664fa-110">La clase **CIM \_ VirtualSystemMigrationCapabilities** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="664fa-110">The **CIM\_VirtualSystemMigrationCapabilities** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="664fa-111">**AsynchronousMethodsSupported**</span><span class="sxs-lookup"><span data-stu-id="664fa-111">**AsynchronousMethodsSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="664fa-112">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="664fa-112">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="664fa-113">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="664fa-113">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="664fa-114">Una matriz que indica los [**métodos \_ VirtualSystemMigrationService de CIM**](cim-virtualsystemmigrationservice.md) que se admiten para las operaciones asincrónicas.</span><span class="sxs-lookup"><span data-stu-id="664fa-114">An array that indicates the [**CIM\_VirtualSystemMigrationService**](cim-virtualsystemmigrationservice.md) methods that are supported for asynchronous operations.</span></span>

<dt>

<span id="MigrateVirtualSystemToHostSupported"></span><span id="migratevirtualsystemtohostsupported"></span><span id="MIGRATEVIRTUALSYSTEMTOHOSTSUPPORTED"></span>

<span data-ttu-id="664fa-115">**MigrateVirtualSystemToHostSupported** (2)</span><span class="sxs-lookup"><span data-stu-id="664fa-115">**MigrateVirtualSystemToHostSupported** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="MigrateVirtualSystemToSystemSupported"></span><span id="migratevirtualsystemtosystemsupported"></span><span id="MIGRATEVIRTUALSYSTEMTOSYSTEMSUPPORTED"></span>

<span data-ttu-id="664fa-116">**MigrateVirtualSystemToSystemSupported** (3)</span><span class="sxs-lookup"><span data-stu-id="664fa-116">**MigrateVirtualSystemToSystemSupported** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="664fa-117">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="664fa-117">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="664fa-118">**DestinationHostFormatsSupported**</span><span class="sxs-lookup"><span data-stu-id="664fa-118">**DestinationHostFormatsSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="664fa-119">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="664fa-119">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="664fa-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="664fa-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="664fa-121">Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ VirtualSystemMigrationService**](cim-virtualsystemmigrationservice.md).**MigrateVirtualSystemToHost (DestinationHost)**","**CIM \_ VirtualSystemMigrationService**.**CheckVirtualSystemIsMigratableToHost (DestinationHost)**")</span><span class="sxs-lookup"><span data-stu-id="664fa-121">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_VirtualSystemMigrationService**](cim-virtualsystemmigrationservice.md).**MigrateVirtualSystemToHost(DestinationHost)**", "**CIM\_VirtualSystemMigrationService**.**CheckVirtualSystemIsMigratableToHost(DestinationHost)**")</span></span>
</dt> </dl>

<span data-ttu-id="664fa-122">Una matriz que contiene los formatos admitidos para el parámetro *DestinationHost* de los métodos [**MigrateVirtualSystemToHost**](cim-virtualsystemmigrationservice-migratevirtualsystemtohost.md) y [**CheckVirtualSystemIsMigratableToHost**](cim-virtualsystemmigrationservice-checkvirtualsystemismigratabletohost.md) para el objeto [**\_ VirtualSystemMigrationService de CIM**](cim-virtualsystemmigrationservice.md) .</span><span class="sxs-lookup"><span data-stu-id="664fa-122">An array that contains the supported formats for the *DestinationHost* parameter of the [**MigrateVirtualSystemToHost**](cim-virtualsystemmigrationservice-migratevirtualsystemtohost.md) and [**CheckVirtualSystemIsMigratableToHost**](cim-virtualsystemmigrationservice-checkvirtualsystemismigratabletohost.md) methods for the [**CIM\_VirtualSystemMigrationService**](cim-virtualsystemmigrationservice.md) object.</span></span>

<dt>

<span id="DomainNameFormatSupported"></span><span id="domainnameformatsupported"></span><span id="DOMAINNAMEFORMATSUPPORTED"></span>

<span data-ttu-id="664fa-123"><span id="DomainNameFormatSupported"></span><span id="domainnameformatsupported"></span><span id="DOMAINNAMEFORMATSUPPORTED"></span>**DomainNameFormatSupported** (2)</span><span class="sxs-lookup"><span data-stu-id="664fa-123"><span id="DomainNameFormatSupported"></span><span id="domainnameformatsupported"></span><span id="DOMAINNAMEFORMATSUPPORTED"></span>**DomainNameFormatSupported** (2)</span></span>


</dt> <dd>

<span data-ttu-id="664fa-124">Compatibilidad con el formato de texto de nombre de dominio según RFC 1035.</span><span class="sxs-lookup"><span data-stu-id="664fa-124">Support of the Domain Name text format according to RFC 1035.</span></span>

</dd> <dt>

<span id="IPv4DottedDecimalFormatSupported"></span><span id="ipv4dotteddecimalformatsupported"></span><span id="IPV4DOTTEDDECIMALFORMATSUPPORTED"></span>

<span data-ttu-id="664fa-125"><span id="IPv4DottedDecimalFormatSupported"></span><span id="ipv4dotteddecimalformatsupported"></span><span id="IPV4DOTTEDDECIMALFORMATSUPPORTED"></span>**IPv4DottedDecimalFormatSupported** (3)</span><span class="sxs-lookup"><span data-stu-id="664fa-125"><span id="IPv4DottedDecimalFormatSupported"></span><span id="ipv4dotteddecimalformatsupported"></span><span id="IPV4DOTTEDDECIMALFORMATSUPPORTED"></span>**IPv4DottedDecimalFormatSupported** (3)</span></span>


</dt> <dd>

<span data-ttu-id="664fa-126">Compatibilidad con el formato decimal con puntos de IPv4 según RFC 1208.</span><span class="sxs-lookup"><span data-stu-id="664fa-126">Support of the IPv4 dotted decimal format according to RFC 1208.</span></span>

</dd> <dt>

<span id="IPv6TextFormatSupported"></span><span id="ipv6textformatsupported"></span><span id="IPV6TEXTFORMATSUPPORTED"></span>

<span data-ttu-id="664fa-127"><span id="IPv6TextFormatSupported"></span><span id="ipv6textformatsupported"></span><span id="IPV6TEXTFORMATSUPPORTED"></span>**IPv6TextFormatSupported** (4)</span><span class="sxs-lookup"><span data-stu-id="664fa-127"><span id="IPv6TextFormatSupported"></span><span id="ipv6textformatsupported"></span><span id="IPV6TEXTFORMATSUPPORTED"></span>**IPv6TextFormatSupported** (4)</span></span>


</dt> <dd>

<span data-ttu-id="664fa-128">Compatibilidad con el formato de texto IPv6 según RFC 4291</span><span class="sxs-lookup"><span data-stu-id="664fa-128">Support of the IPv6 text format according to RFC 4291</span></span>

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="664fa-129"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="664fa-129"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="664fa-130">**SynchronousMethodsSupported**</span><span class="sxs-lookup"><span data-stu-id="664fa-130">**SynchronousMethodsSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="664fa-131">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="664fa-131">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="664fa-132">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="664fa-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="664fa-133">Una matriz que indica los [**métodos \_ VirtualSystemMigrationService de CIM**](cim-virtualsystemmigrationservice.md) que se admiten para las operaciones sincrónicas.</span><span class="sxs-lookup"><span data-stu-id="664fa-133">An array that indicates the [**CIM\_VirtualSystemMigrationService**](cim-virtualsystemmigrationservice.md) methods that are supported for synchronous operations.</span></span>

<span data-ttu-id="664fa-134">Enumeración de los identificadores de método cuya implementación puede ser sincrónica; es decir, la operación se puede completar inmediatamente y, por tanto, es posible que el método no devuelva un trabajo.</span><span class="sxs-lookup"><span data-stu-id="664fa-134">Enumeration of method identifiers whose implementation may be synchronous; that is, the operation may complete immediately and therefore the method may not return a job.</span></span>

<dt>

<span id="MigrateVirtualSystemToHostSupported"></span><span id="migratevirtualsystemtohostsupported"></span><span id="MIGRATEVIRTUALSYSTEMTOHOSTSUPPORTED"></span>

<span data-ttu-id="664fa-135">**MigrateVirtualSystemToHostSupported** (2)</span><span class="sxs-lookup"><span data-stu-id="664fa-135">**MigrateVirtualSystemToHostSupported** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="MigrateVirtualSystemToSystemSupported"></span><span id="migratevirtualsystemtosystemsupported"></span><span id="MIGRATEVIRTUALSYSTEMTOSYSTEMSUPPORTED"></span>

<span data-ttu-id="664fa-136">**MigrateVirtualSystemToSystemSupported** (3)</span><span class="sxs-lookup"><span data-stu-id="664fa-136">**MigrateVirtualSystemToSystemSupported** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="CheckVirtualSystemIsMigratableToHostSupported"></span><span id="checkvirtualsystemismigratabletohostsupported"></span><span id="CHECKVIRTUALSYSTEMISMIGRATABLETOHOSTSUPPORTED"></span>

<span data-ttu-id="664fa-137">**CheckVirtualSystemIsMigratableToHostSupported** (4)</span><span class="sxs-lookup"><span data-stu-id="664fa-137">**CheckVirtualSystemIsMigratableToHostSupported** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="CheckVirtualSystemIsMigratableToSystemSupported"></span><span id="checkvirtualsystemismigratabletosystemsupported"></span><span id="CHECKVIRTUALSYSTEMISMIGRATABLETOSYSTEMSUPPORTED"></span>

<span data-ttu-id="664fa-138">**CheckVirtualSystemIsMigratableToSystemSupported** (5)</span><span class="sxs-lookup"><span data-stu-id="664fa-138">**CheckVirtualSystemIsMigratableToSystemSupported** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="664fa-139">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="664fa-139">**DMTF Reserved** (..)</span></span>


<span data-ttu-id="664fa-140"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="664fa-140"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="664fa-141">Requisitos</span><span class="sxs-lookup"><span data-stu-id="664fa-141">Requirements</span></span>



| <span data-ttu-id="664fa-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="664fa-142">Requirement</span></span> | <span data-ttu-id="664fa-143">Value</span><span class="sxs-lookup"><span data-stu-id="664fa-143">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="664fa-144">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="664fa-144">Minimum supported client</span></span><br/> | <span data-ttu-id="664fa-145">Windows 8</span><span class="sxs-lookup"><span data-stu-id="664fa-145">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="664fa-146">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="664fa-146">Minimum supported server</span></span><br/> | <span data-ttu-id="664fa-147">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="664fa-147">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="664fa-148">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="664fa-148">Namespace</span></span><br/>                | <span data-ttu-id="664fa-149">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="664fa-149">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="664fa-150">MOF</span><span class="sxs-lookup"><span data-stu-id="664fa-150">MOF</span></span><br/>                      | <dl> <span data-ttu-id="664fa-151"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="664fa-151"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="664fa-152">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="664fa-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="664fa-153"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="664fa-153"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="664fa-154">Vea también</span><span class="sxs-lookup"><span data-stu-id="664fa-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="664fa-155">**Capacidades de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="664fa-155">**CIM\_Capabilities**</span></span>](cim-capabilities.md)
</dt> </dl>

 

