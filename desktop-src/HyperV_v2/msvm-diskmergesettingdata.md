---
description: Representa el estado de configuración de la combinación de discos para una máquina virtual.
ms.assetid: b4c0afeb-ce37-4eec-8aba-0d74115c463f
title: Msvm_DiskMergeSettingData (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_DiskMergeSettingData
- Msvm_DiskMergeSettingData.InstanceID
- Msvm_DiskMergeSettingData.Caption
- Msvm_DiskMergeSettingData.Description
- Msvm_DiskMergeSettingData.ElementName
- Msvm_DiskMergeSettingData.EnabledState
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: fe702c382fb0636579a8ab1355bfd1299657b214
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668424"
---
# <a name="msvm_diskmergesettingdata-class"></a><span data-ttu-id="7d6a7-103">MSVM \_ DiskMergeSettingData (clase)</span><span class="sxs-lookup"><span data-stu-id="7d6a7-103">Msvm\_DiskMergeSettingData class</span></span>

<span data-ttu-id="7d6a7-104">Representa el estado de configuración de la combinación de discos para una máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="7d6a7-104">Represents the configuration state of the disk merge settings for a virtual machine.</span></span>

<span data-ttu-id="7d6a7-105">La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="7d6a7-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="7d6a7-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7d6a7-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_DiskMergeSettingData : CIM_SettingData
{
  string InstanceID = "Microsoft:GUID\DeviceSpecificData";
  string Caption = "Disk Merge Setting Data";
  string Description = "Microsoft Disk Merge Setting Data";
  string ElementName = "Disk Merge Setting Data";
  uint32 EnabledState = 1;
};
```

## <a name="members"></a><span data-ttu-id="7d6a7-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="7d6a7-107">Members</span></span>

<span data-ttu-id="7d6a7-108">La clase **MSVM \_ DiskMergeSettingData** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="7d6a7-108">The **Msvm\_DiskMergeSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="7d6a7-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="7d6a7-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7d6a7-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="7d6a7-110">Properties</span></span>

<span data-ttu-id="7d6a7-111">La clase **MSVM \_ DiskMergeSettingData** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="7d6a7-111">The **Msvm\_DiskMergeSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7d6a7-112">**Caption**</span><span class="sxs-lookup"><span data-stu-id="7d6a7-112">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7d6a7-113">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="7d6a7-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7d6a7-114">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7d6a7-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7d6a7-115">Breve descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="7d6a7-115">A short description of the object.</span></span> <span data-ttu-id="7d6a7-116">Esta propiedad se hereda de la clase de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) y siempre se establece en "datos de configuración de combinación de discos".</span><span class="sxs-lookup"><span data-stu-id="7d6a7-116">This property is inherited from the [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) class and is always set to "Disk Merge Setting Data".</span></span>

</dd> <dt>

<span data-ttu-id="7d6a7-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="7d6a7-117">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7d6a7-118">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="7d6a7-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7d6a7-119">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7d6a7-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7d6a7-120">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="7d6a7-120">A description of the object.</span></span> <span data-ttu-id="7d6a7-121">Esta propiedad se hereda de [**la \_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)y siempre se establece en "datos de configuración de combinación de discos de Microsoft".</span><span class="sxs-lookup"><span data-stu-id="7d6a7-121">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Microsoft Disk Merge Setting Data".</span></span>

</dd> <dt>

<span data-ttu-id="7d6a7-122">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="7d6a7-122">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7d6a7-123">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="7d6a7-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7d6a7-124">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7d6a7-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7d6a7-125">Nombre para mostrar del objeto.</span><span class="sxs-lookup"><span data-stu-id="7d6a7-125">A display name for the object.</span></span> <span data-ttu-id="7d6a7-126">Esta propiedad se hereda del [**\_ SettingData de CIM**](/previous-versions//cc136911(v=vs.85))y siempre se establece en "datos de configuración de combinación de discos".</span><span class="sxs-lookup"><span data-stu-id="7d6a7-126">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)), and it is always set to "Disk Merge Setting Data".</span></span> <span data-ttu-id="7d6a7-127">Al cambiar esta propiedad, se cambiará la propiedad **ElementName** del derivado de [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) asociado.</span><span class="sxs-lookup"><span data-stu-id="7d6a7-127">Changing this property will change the **ElementName** property of the associated [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) derivative.</span></span>

<span data-ttu-id="7d6a7-128">Se trata de una propiedad de solo lectura, pero se puede cambiar mediante el método [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) de la clase [**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .</span><span class="sxs-lookup"><span data-stu-id="7d6a7-128">This is a read-only property, but it can be changed by using the [**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualsystemmanagementservice.md) method of the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="7d6a7-129">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="7d6a7-129">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7d6a7-130">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7d6a7-130">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7d6a7-131">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7d6a7-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7d6a7-132">Especifica el estado habilitado de la funcionalidad de combinación de discos.</span><span class="sxs-lookup"><span data-stu-id="7d6a7-132">Specifies the enabled state of the disk merge functionality.</span></span>

<dt>

<span id="Temporarily_disabled"></span><span id="temporarily_disabled"></span><span id="TEMPORARILY_DISABLED"></span>

<span data-ttu-id="7d6a7-133">**Deshabilitado temporalmente** (0)</span><span class="sxs-lookup"><span data-stu-id="7d6a7-133">**Temporarily disabled** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="7d6a7-134">**Habilitado** (1)</span><span class="sxs-lookup"><span data-stu-id="7d6a7-134">**Enabled** (1)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="7d6a7-135">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="7d6a7-135">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7d6a7-136">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="7d6a7-136">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7d6a7-137">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7d6a7-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7d6a7-138">Calificadores: **clave**</span><span class="sxs-lookup"><span data-stu-id="7d6a7-138">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="7d6a7-139">Identifica de forma única una instancia de esta clase.</span><span class="sxs-lookup"><span data-stu-id="7d6a7-139">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="7d6a7-140">Esta propiedad se hereda del [**\_ SettingData de CIM**](/previous-versions//cc136911(v=vs.85)) y siempre se establece en "Microsoft:*GUID* \\ *DeviceSpecificData*".</span><span class="sxs-lookup"><span data-stu-id="7d6a7-140">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)) and is always set to "Microsoft:*GUID*\\*DeviceSpecificData*".</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7d6a7-141">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7d6a7-141">Requirements</span></span>



| <span data-ttu-id="7d6a7-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="7d6a7-142">Requirement</span></span> | <span data-ttu-id="7d6a7-143">Value</span><span class="sxs-lookup"><span data-stu-id="7d6a7-143">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7d6a7-144">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7d6a7-144">Minimum supported client</span></span><br/> | <span data-ttu-id="7d6a7-145">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="7d6a7-145">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="7d6a7-146">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7d6a7-146">Minimum supported server</span></span><br/> | <span data-ttu-id="7d6a7-147">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="7d6a7-147">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="7d6a7-148">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="7d6a7-148">Namespace</span></span><br/>                | <span data-ttu-id="7d6a7-149">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="7d6a7-149">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="7d6a7-150">MOF</span><span class="sxs-lookup"><span data-stu-id="7d6a7-150">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7d6a7-151"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7d6a7-151"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="7d6a7-152">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="7d6a7-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7d6a7-153"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="7d6a7-153"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

