---
description: Describe las capacidades de la clase MSVM \_ ResourcePoolConfigurationService asociada.
ms.assetid: 3e6857f9-62a0-420b-8f1d-8aad685a7ff7
title: Msvm_ResourcePoolConfigurationCapabilities (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ResourcePoolConfigurationCapabilities
- Msvm_ResourcePoolConfigurationCapabilities.InstanceID
- Msvm_ResourcePoolConfigurationCapabilities.Caption
- Msvm_ResourcePoolConfigurationCapabilities.Description
- Msvm_ResourcePoolConfigurationCapabilities.ElementName
- Msvm_ResourcePoolConfigurationCapabilities.AsynchronousMethodsSupported
- Msvm_ResourcePoolConfigurationCapabilities.SynchronousMethodsSupported
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: b70d9e84e2c85d4c5b702a638982df0b47d62193
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910729"
---
# <a name="msvm_resourcepoolconfigurationcapabilities-class"></a><span data-ttu-id="409f6-103">MSVM \_ ResourcePoolConfigurationCapabilities (clase)</span><span class="sxs-lookup"><span data-stu-id="409f6-103">Msvm\_ResourcePoolConfigurationCapabilities class</span></span>

<span data-ttu-id="409f6-104">Describe las capacidades de la clase [**MSVM \_ ResourcePoolConfigurationService**](msvm-resourcepoolconfigurationservice.md) asociada.</span><span class="sxs-lookup"><span data-stu-id="409f6-104">Describes the capabilities of the associated [**Msvm\_ResourcePoolConfigurationService**](msvm-resourcepoolconfigurationservice.md) class.</span></span> <span data-ttu-id="409f6-105">Los clientes pueden usar instancias de esta clase para determinar qué métodos se admiten de forma sincrónica o asincrónica.</span><span class="sxs-lookup"><span data-stu-id="409f6-105">Clients can use instances of this class to determine which methods are supported synchronously or asynchronously.</span></span> <span data-ttu-id="409f6-106">El mismo método no debe estar en ambas listas.</span><span class="sxs-lookup"><span data-stu-id="409f6-106">The same method must not be in both lists.</span></span> <span data-ttu-id="409f6-107">Las implementaciones de método deben ser sincrónicas o asincrónicas.</span><span class="sxs-lookup"><span data-stu-id="409f6-107">Method implementations must either be synchronous or asynchronous.</span></span>

<span data-ttu-id="409f6-108">La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="409f6-108">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="409f6-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="409f6-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider")]
class Msvm_ResourcePoolConfigurationCapabilities : CIM_Capabilities
{
  string InstanceID;
  string Caption = "Resource Pool Configuration Capabilities";
  string Description = "Microsoft Resource Pool Configuration Capabilities";
  string ElementName = "Resource Pool Configuration Capabilities";
  uint32 AsynchronousMethodsSupported[];
  uint32 SynchronousMethodsSupported[];
};
```

## <a name="members"></a><span data-ttu-id="409f6-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="409f6-110">Members</span></span>

<span data-ttu-id="409f6-111">La clase **MSVM \_ ResourcePoolConfigurationCapabilities** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="409f6-111">The **Msvm\_ResourcePoolConfigurationCapabilities** class has these types of members:</span></span>

-   [<span data-ttu-id="409f6-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="409f6-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="409f6-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="409f6-113">Properties</span></span>

<span data-ttu-id="409f6-114">La clase **MSVM \_ ResourcePoolConfigurationCapabilities** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="409f6-114">The **Msvm\_ResourcePoolConfigurationCapabilities** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="409f6-115">**AsynchronousMethodsSupported**</span><span class="sxs-lookup"><span data-stu-id="409f6-115">**AsynchronousMethodsSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="409f6-116">Tipo de datos: **UInt32** array</span><span class="sxs-lookup"><span data-stu-id="409f6-116">Data type: **uint32** array</span></span>
</dt> <dt>

<span data-ttu-id="409f6-117">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="409f6-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="409f6-118">Una matriz de identificadores de método, cada uno de los cuales identifica un método de la clase [**MSVM \_ ResourcePoolConfigurationService**](msvm-resourcepoolconfigurationservice.md) que la implementación admite de forma asincrónica.</span><span class="sxs-lookup"><span data-stu-id="409f6-118">An array of method identifiers, each identifying a method of the [**Msvm\_ResourcePoolConfigurationService**](msvm-resourcepoolconfigurationservice.md) class that is supported asynchronously by the implementation.</span></span>

<dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="409f6-119">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="409f6-119">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="CreatePool_is_supported"></span><span id="createpool_is_supported"></span><span id="CREATEPOOL_IS_SUPPORTED"></span>

<span data-ttu-id="409f6-120">**Se admite createpool** (32768)</span><span class="sxs-lookup"><span data-stu-id="409f6-120">**CreatePool is supported** (32768)</span></span>


</dt> <dd></dd> <dt>

<span id="ChangePoolResources_is_supported"></span><span id="changepoolresources_is_supported"></span><span id="CHANGEPOOLRESOURCES_IS_SUPPORTED"></span>

<span data-ttu-id="409f6-121">**Se admite ChangePoolResources** (32769)</span><span class="sxs-lookup"><span data-stu-id="409f6-121">**ChangePoolResources is supported** (32769)</span></span>


</dt> <dd></dd> <dt>

<span id="ChangePoolSettings_is_supported"></span><span id="changepoolsettings_is_supported"></span><span id="CHANGEPOOLSETTINGS_IS_SUPPORTED"></span>

<span data-ttu-id="409f6-122">**Se admite ChangePoolSettings** (32770)</span><span class="sxs-lookup"><span data-stu-id="409f6-122">**ChangePoolSettings is supported** (32770)</span></span>


</dt> <dd></dd> <dt>

<span id="DeletePool_is_supported"></span><span id="deletepool_is_supported"></span><span id="DELETEPOOL_IS_SUPPORTED"></span>

<span data-ttu-id="409f6-123">**Se admite DeletePool** (32771)</span><span class="sxs-lookup"><span data-stu-id="409f6-123">**DeletePool is supported** (32771)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="409f6-124">**Proveedor reservado** (32772.. 65535)</span><span class="sxs-lookup"><span data-stu-id="409f6-124">**Vendor Reserved** (32772..65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="409f6-125">**Caption**</span><span class="sxs-lookup"><span data-stu-id="409f6-125">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="409f6-126">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="409f6-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="409f6-127">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="409f6-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="409f6-128">Breve descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="409f6-128">A short description of the object.</span></span> <span data-ttu-id="409f6-129">Esta propiedad se hereda de [**la \_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)y siempre se establece en "capacidades de configuración del grupo de recursos".</span><span class="sxs-lookup"><span data-stu-id="409f6-129">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Resource Pool Configuration Capabilities".</span></span>

</dd> <dt>

<span data-ttu-id="409f6-130">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="409f6-130">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="409f6-131">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="409f6-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="409f6-132">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="409f6-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="409f6-133">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="409f6-133">A description of the object.</span></span> <span data-ttu-id="409f6-134">Esta propiedad se hereda de [**la \_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)y siempre se establece en "capacidades de configuración del grupo de recursos de Microsoft".</span><span class="sxs-lookup"><span data-stu-id="409f6-134">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Microsoft Resource Pool Configuration Capabilities".</span></span>

</dd> <dt>

<span data-ttu-id="409f6-135">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="409f6-135">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="409f6-136">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="409f6-136">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="409f6-137">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="409f6-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="409f6-138">Nombre para mostrar del objeto.</span><span class="sxs-lookup"><span data-stu-id="409f6-138">A display name for the object.</span></span> <span data-ttu-id="409f6-139">Esta propiedad se hereda de [**la \_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)y siempre se establece en "capacidades de configuración del grupo de recursos".</span><span class="sxs-lookup"><span data-stu-id="409f6-139">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Resource Pool Configuration Capabilities".</span></span>

</dd> <dt>

<span data-ttu-id="409f6-140">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="409f6-140">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="409f6-141">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="409f6-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="409f6-142">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="409f6-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="409f6-143">Calificadores: **clave**</span><span class="sxs-lookup"><span data-stu-id="409f6-143">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="409f6-144">Identifica de forma única una instancia de esta clase.</span><span class="sxs-lookup"><span data-stu-id="409f6-144">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="409f6-145">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="409f6-145">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="409f6-146">**SynchronousMethodsSupported**</span><span class="sxs-lookup"><span data-stu-id="409f6-146">**SynchronousMethodsSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="409f6-147">Tipo de datos: **UInt32** array</span><span class="sxs-lookup"><span data-stu-id="409f6-147">Data type: **uint32** array</span></span>
</dt> <dt>

<span data-ttu-id="409f6-148">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="409f6-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="409f6-149">Una matriz de identificadores de método, cada uno de los cuales identifica un método de la clase [**MSVM \_ ResourcePoolConfigurationService**](msvm-resourcepoolconfigurationservice.md) que la implementación admite sincrónicamente.</span><span class="sxs-lookup"><span data-stu-id="409f6-149">An array of method identifiers, each identifying a method of the [**Msvm\_ResourcePoolConfigurationService**](msvm-resourcepoolconfigurationservice.md) class that is supported synchronously by the implementation.</span></span>

<dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="409f6-150">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="409f6-150">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="CreatePool_is_supported"></span><span id="createpool_is_supported"></span><span id="CREATEPOOL_IS_SUPPORTED"></span>

<span data-ttu-id="409f6-151">**Se admite createpool** (32768)</span><span class="sxs-lookup"><span data-stu-id="409f6-151">**CreatePool is supported** (32768)</span></span>


</dt> <dd></dd> <dt>

<span id="ChangePoolResources_is_supported"></span><span id="changepoolresources_is_supported"></span><span id="CHANGEPOOLRESOURCES_IS_SUPPORTED"></span>

<span data-ttu-id="409f6-152">**Se admite ChangePoolResources** (32769)</span><span class="sxs-lookup"><span data-stu-id="409f6-152">**ChangePoolResources is supported** (32769)</span></span>


</dt> <dd></dd> <dt>

<span id="ChangePoolSettings_is_supported"></span><span id="changepoolsettings_is_supported"></span><span id="CHANGEPOOLSETTINGS_IS_SUPPORTED"></span>

<span data-ttu-id="409f6-153">**Se admite ChangePoolSettings** (32770)</span><span class="sxs-lookup"><span data-stu-id="409f6-153">**ChangePoolSettings is supported** (32770)</span></span>


</dt> <dd></dd> <dt>

<span id="DeletePool_is_supported"></span><span id="deletepool_is_supported"></span><span id="DELETEPOOL_IS_SUPPORTED"></span>

<span data-ttu-id="409f6-154">**Se admite DeletePool** (32771)</span><span class="sxs-lookup"><span data-stu-id="409f6-154">**DeletePool is supported** (32771)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="409f6-155">**Proveedor reservado** (32772.. 65535)</span><span class="sxs-lookup"><span data-stu-id="409f6-155">**Vendor Reserved** (32772..65535)</span></span>


<span data-ttu-id="409f6-156"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="409f6-156"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="409f6-157">Requisitos</span><span class="sxs-lookup"><span data-stu-id="409f6-157">Requirements</span></span>



| <span data-ttu-id="409f6-158">Requisito</span><span class="sxs-lookup"><span data-stu-id="409f6-158">Requirement</span></span> | <span data-ttu-id="409f6-159">Value</span><span class="sxs-lookup"><span data-stu-id="409f6-159">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="409f6-160">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="409f6-160">Minimum supported client</span></span><br/> | <span data-ttu-id="409f6-161">\[Solo aplicaciones de escritorio Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="409f6-161">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="409f6-162">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="409f6-162">Minimum supported server</span></span><br/> | <span data-ttu-id="409f6-163">Solo aplicaciones de escritorio de Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="409f6-163">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="409f6-164">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="409f6-164">Namespace</span></span><br/>                | <span data-ttu-id="409f6-165">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="409f6-165">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="409f6-166">MOF</span><span class="sxs-lookup"><span data-stu-id="409f6-166">MOF</span></span><br/>                      | <dl> <span data-ttu-id="409f6-167"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="409f6-167"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="409f6-168">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="409f6-168">DLL</span></span><br/>                      | <dl> <span data-ttu-id="409f6-169"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="409f6-169"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

