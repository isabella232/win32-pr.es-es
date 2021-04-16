---
description: Representa la configuración para el servicio de migración del sistema virtual en un host.
ms.assetid: 56711134-9a4a-49bd-8a0e-ce679b959adf
title: Msvm_VirtualSystemMigrationServiceSettingData (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemMigrationServiceSettingData
- Msvm_VirtualSystemMigrationServiceSettingData.InstanceID
- Msvm_VirtualSystemMigrationServiceSettingData.Caption
- Msvm_VirtualSystemMigrationServiceSettingData.Description
- Msvm_VirtualSystemMigrationServiceSettingData.ElementName
- Msvm_VirtualSystemMigrationServiceSettingData.EnableVirtualSystemMigration
- Msvm_VirtualSystemMigrationServiceSettingData.MaximumActiveVirtualSystemMigration
- Msvm_VirtualSystemMigrationServiceSettingData.MaximumActiveStorageMigration
- Msvm_VirtualSystemMigrationServiceSettingData.AuthenticationType
- Msvm_VirtualSystemMigrationServiceSettingData.EnableCompression
- Msvm_VirtualSystemMigrationServiceSettingData.EnableSmbTransport
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 8c8685e468d60983408c52a985169c61be91f632
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666327"
---
# <a name="msvm_virtualsystemmigrationservicesettingdata-class"></a><span data-ttu-id="3a53a-103">MSVM \_ VirtualSystemMigrationServiceSettingData (clase)</span><span class="sxs-lookup"><span data-stu-id="3a53a-103">Msvm\_VirtualSystemMigrationServiceSettingData class</span></span>

<span data-ttu-id="3a53a-104">Representa la configuración para el servicio de migración del sistema virtual en un host.</span><span class="sxs-lookup"><span data-stu-id="3a53a-104">Represents the settings for the virtual system migration service on a host.</span></span> <span data-ttu-id="3a53a-105">Las propiedades de esta clase no se pueden modificar directamente.</span><span class="sxs-lookup"><span data-stu-id="3a53a-105">The properties for this class cannot be modified directly.</span></span> <span data-ttu-id="3a53a-106">El cliente debe llamar al método **MSVM \_ VirtualSystemMigrationService. ModifyServiceSettings** para modificar cualquiera de estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="3a53a-106">The client must call the **Msvm\_VirtualSystemMigrationService.ModifyServiceSettings** method to modify any of these properties.</span></span>

<span data-ttu-id="3a53a-107">La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="3a53a-107">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="3a53a-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3a53a-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualSystemMigrationServiceSettingData : CIM_SettingData
{
  string  InstanceID;
  string  Caption;
  string  Description;
  string  ElementName;
  boolean EnableVirtualSystemMigration;
  uint32  MaximumActiveVirtualSystemMigration;
  uint32  MaximumActiveStorageMigration;
  uint32  AuthenticationType;
  boolean EnableCompression = True;
  boolean EnableSmbTransport = False;
};
```

## <a name="members"></a><span data-ttu-id="3a53a-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="3a53a-109">Members</span></span>

<span data-ttu-id="3a53a-110">La clase **MSVM \_ VirtualSystemMigrationServiceSettingData** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="3a53a-110">The **Msvm\_VirtualSystemMigrationServiceSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="3a53a-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="3a53a-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3a53a-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="3a53a-112">Properties</span></span>

<span data-ttu-id="3a53a-113">La clase **MSVM \_ VirtualSystemMigrationServiceSettingData** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="3a53a-113">The **Msvm\_VirtualSystemMigrationServiceSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3a53a-114">**AuthenticationType**</span><span class="sxs-lookup"><span data-stu-id="3a53a-114">**AuthenticationType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a53a-115">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3a53a-115">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3a53a-116">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3a53a-116">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3a53a-117">Especifica el mecanismo de autenticación usado para las conexiones de red de migración del sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="3a53a-117">Specifies the authentication mechanism used for virtual system migration network connections.</span></span> <span data-ttu-id="3a53a-118">Se trata de una propiedad de solo lectura, pero se puede cambiar mediante el método [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmigrationservice.md) de la clase [**MSVM \_ VirtualSystemMigrationService**](msvm-virtualsystemmigrationservice.md) .</span><span class="sxs-lookup"><span data-stu-id="3a53a-118">This is a read-only property, but it can be changed by using the [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmigrationservice.md) method of the [**Msvm\_VirtualSystemMigrationService**](msvm-virtualsystemmigrationservice.md) class.</span></span>

<dt>

<span id="CredSSP"></span><span id="credssp"></span><span id="CREDSSP"></span>

<span data-ttu-id="3a53a-119">**CredSSP** (0)</span><span class="sxs-lookup"><span data-stu-id="3a53a-119">**CredSSP** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Kerberos"></span><span id="kerberos"></span><span id="KERBEROS"></span>

<span data-ttu-id="3a53a-120">**Kerberos** (1)</span><span class="sxs-lookup"><span data-stu-id="3a53a-120">**Kerberos** (1)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="3a53a-121">**Caption**</span><span class="sxs-lookup"><span data-stu-id="3a53a-121">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a53a-122">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="3a53a-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3a53a-123">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3a53a-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3a53a-124">Breve descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="3a53a-124">A short description of the object.</span></span> <span data-ttu-id="3a53a-125">Esta propiedad se hereda de la clase [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) .</span><span class="sxs-lookup"><span data-stu-id="3a53a-125">This property is inherited from the [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) class.</span></span>

</dd> <dt>

<span data-ttu-id="3a53a-126">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="3a53a-126">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a53a-127">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="3a53a-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3a53a-128">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3a53a-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3a53a-129">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="3a53a-129">A description of the object.</span></span> <span data-ttu-id="3a53a-130">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="3a53a-130">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="3a53a-131">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="3a53a-131">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a53a-132">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="3a53a-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3a53a-133">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3a53a-133">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3a53a-134">Nombre para mostrar del objeto.</span><span class="sxs-lookup"><span data-stu-id="3a53a-134">A display name for the object.</span></span> <span data-ttu-id="3a53a-135">Esta propiedad se hereda del [**\_ SettingData de CIM**](/previous-versions//cc136911(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="3a53a-135">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="3a53a-136">**EnableCompression**</span><span class="sxs-lookup"><span data-stu-id="3a53a-136">**EnableCompression**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a53a-137">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="3a53a-137">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3a53a-138">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="3a53a-138">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="3a53a-139">Indica si la compresión del tráfico de migración en vivo está habilitada o deshabilitada.</span><span class="sxs-lookup"><span data-stu-id="3a53a-139">Indicates whether compression of live migration traffic is enabled or disabled.</span></span> <span data-ttu-id="3a53a-140">True indica que está habilitado.</span><span class="sxs-lookup"><span data-stu-id="3a53a-140">True indicates enabled.</span></span>

<span data-ttu-id="3a53a-141">Se trata de una propiedad de solo lectura, pero se puede cambiar mediante el método [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) de la clase [**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="3a53a-141">This is a read-only property, but it can be changed by using the [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

<span data-ttu-id="3a53a-142">**Windows 8.1:** Este valor no se admite hasta Windows 8.1 y Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="3a53a-142">**Windows 8.1:** This value is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span>

</dd> <dt>

<span data-ttu-id="3a53a-143">**EnableSmbTransport**</span><span class="sxs-lookup"><span data-stu-id="3a53a-143">**EnableSmbTransport**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a53a-144">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="3a53a-144">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3a53a-145">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="3a53a-145">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="3a53a-146">Indica si el uso de SMB como un tipo de transporte para transferir el estado de la máquina virtual entre los hosts de Hyper-V durante la migración del sistema virtual está habilitado o deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="3a53a-146">Indicates whether use of SMB as a transport type for transferring VM state between the Hyper-V hosts during virtual system migration is enabled or disabled.</span></span> <span data-ttu-id="3a53a-147">**True** indica que está habilitado.</span><span class="sxs-lookup"><span data-stu-id="3a53a-147">**True** indicates enabled.</span></span> <span data-ttu-id="3a53a-148">Se consigue un mayor rendimiento si las NIC RDMA están configuradas para el transporte SMB durante la migración en vivo de máquinas virtuales.</span><span class="sxs-lookup"><span data-stu-id="3a53a-148">A higher performance is achieved if RDMA NICs are configured for SMB transport during VM live migration.</span></span> <span data-ttu-id="3a53a-149">Si el valor de **EnableSmbTransport** es true, se omite el valor de **EnableCompression** .</span><span class="sxs-lookup"><span data-stu-id="3a53a-149">If **EnableSmbTransport** value is true, the value of **EnableCompression** is ignored.</span></span>

<span data-ttu-id="3a53a-150">Se trata de una propiedad de solo lectura, pero se puede cambiar mediante el método [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) de la clase [**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="3a53a-150">This is a read-only property, but it can be changed by using the [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

<span data-ttu-id="3a53a-151">**Windows 8.1:** Este valor no se admite hasta Windows 8.1 y Windows Server 2012 R2.</span><span class="sxs-lookup"><span data-stu-id="3a53a-151">**Windows 8.1:** This value is not supported until Windows 8.1 and Windows Server 2012 R2.</span></span>

</dd> <dt>

<span data-ttu-id="3a53a-152">**EnableVirtualSystemMigration**</span><span class="sxs-lookup"><span data-stu-id="3a53a-152">**EnableVirtualSystemMigration**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a53a-153">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="3a53a-153">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3a53a-154">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3a53a-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3a53a-155">Especifica si la migración del sistema virtual está habilitada o deshabilitada.</span><span class="sxs-lookup"><span data-stu-id="3a53a-155">Specifies whether virtual system migration is enabled or disabled.</span></span> <span data-ttu-id="3a53a-156">La migración de almacenamiento siempre está habilitada.</span><span class="sxs-lookup"><span data-stu-id="3a53a-156">Storage migration is always enabled.</span></span> <span data-ttu-id="3a53a-157">Se trata de una propiedad de solo lectura, pero se puede cambiar mediante el método [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmigrationservice.md) de la clase [**MSVM \_ VirtualSystemMigrationService**](msvm-virtualsystemmigrationservice.md) .</span><span class="sxs-lookup"><span data-stu-id="3a53a-157">This is a read-only property, but it can be changed by using the [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmigrationservice.md) method of the [**Msvm\_VirtualSystemMigrationService**](msvm-virtualsystemmigrationservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="3a53a-158">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="3a53a-158">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a53a-159">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="3a53a-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3a53a-160">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3a53a-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3a53a-161">Calificadores: **clave**</span><span class="sxs-lookup"><span data-stu-id="3a53a-161">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="3a53a-162">Identifica de forma única una instancia de esta clase.</span><span class="sxs-lookup"><span data-stu-id="3a53a-162">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="3a53a-163">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="3a53a-163">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="3a53a-164">**MaximumActiveStorageMigration**</span><span class="sxs-lookup"><span data-stu-id="3a53a-164">**MaximumActiveStorageMigration**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a53a-165">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3a53a-165">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3a53a-166">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3a53a-166">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3a53a-167">Especifica el número máximo de migraciones de almacenamiento activas permitidas.</span><span class="sxs-lookup"><span data-stu-id="3a53a-167">Specifies the maximum number of active storage migrations allowed.</span></span> <span data-ttu-id="3a53a-168">Se trata de una propiedad de solo lectura, pero se puede cambiar mediante el método [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmigrationservice.md) de la clase [**MSVM \_ VirtualSystemMigrationService**](msvm-virtualsystemmigrationservice.md) .</span><span class="sxs-lookup"><span data-stu-id="3a53a-168">This is a read-only property, but it can be changed by using the [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmigrationservice.md) method of the [**Msvm\_VirtualSystemMigrationService**](msvm-virtualsystemmigrationservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="3a53a-169">**MaximumActiveVirtualSystemMigration**</span><span class="sxs-lookup"><span data-stu-id="3a53a-169">**MaximumActiveVirtualSystemMigration**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a53a-170">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3a53a-170">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3a53a-171">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3a53a-171">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3a53a-172">Especifica el número máximo de migraciones de sistema virtuales activas permitidas.</span><span class="sxs-lookup"><span data-stu-id="3a53a-172">Specifies the maximum number of active virtual system migrations allowed.</span></span> <span data-ttu-id="3a53a-173">Se trata de una propiedad de solo lectura, pero se puede cambiar mediante el método [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmigrationservice.md) de la clase [**MSVM \_ VirtualSystemMigrationService**](msvm-virtualsystemmigrationservice.md) .</span><span class="sxs-lookup"><span data-stu-id="3a53a-173">This is a read-only property, but it can be changed by using the [**ModifyServiceSettings**](modifyservicesettings-msvm-virtualsystemmigrationservice.md) method of the [**Msvm\_VirtualSystemMigrationService**](msvm-virtualsystemmigrationservice.md) class.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3a53a-174">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3a53a-174">Requirements</span></span>



| <span data-ttu-id="3a53a-175">Requisito</span><span class="sxs-lookup"><span data-stu-id="3a53a-175">Requirement</span></span> | <span data-ttu-id="3a53a-176">Value</span><span class="sxs-lookup"><span data-stu-id="3a53a-176">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3a53a-177">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3a53a-177">Minimum supported client</span></span><br/> | <span data-ttu-id="3a53a-178">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="3a53a-178">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="3a53a-179">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3a53a-179">Minimum supported server</span></span><br/> | <span data-ttu-id="3a53a-180">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="3a53a-180">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="3a53a-181">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="3a53a-181">Namespace</span></span><br/>                | <span data-ttu-id="3a53a-182">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="3a53a-182">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="3a53a-183">MOF</span><span class="sxs-lookup"><span data-stu-id="3a53a-183">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3a53a-184"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3a53a-184"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="3a53a-185">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="3a53a-185">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3a53a-186"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="3a53a-186"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="3a53a-187">Vea también</span><span class="sxs-lookup"><span data-stu-id="3a53a-187">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a53a-188">**SettingData de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="3a53a-188">**CIM\_SettingData**</span></span>](cim-settingdata.md)
</dt> <dt>

[<span data-ttu-id="3a53a-189">**ModifyServiceSettings**</span><span class="sxs-lookup"><span data-stu-id="3a53a-189">**ModifyServiceSettings**</span></span>](modifyservicesettings-msvm-virtualsystemmigrationservice.md)
</dt> </dl>

 

