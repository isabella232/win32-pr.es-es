---
description: Proporciona información adicional que se va a usar con el método CreateSnapshot de la \_ clase VirtualSystemSnapshotService de MSVM.
ms.assetid: d4a025c4-6a3c-4ae0-8f2c-421c1aa1eb23
title: Msvm_VirtualSystemSnapshotSettingData (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemSnapshotSettingData
- Msvm_VirtualSystemSnapshotSettingData.ConsistencyLevel
- Msvm_VirtualSystemSnapshotSettingData.IgnoreNonSnapshottableDisks
- Msvm_VirtualSystemSnapshotSettingData.GuestBackupType
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 32ab52da97e9fcc943c3a70548bb6b1a6d7994a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423687"
---
# <a name="msvm_virtualsystemsnapshotsettingdata-class"></a><span data-ttu-id="60e79-103">MSVM \_ VirtualSystemSnapshotSettingData (clase)</span><span class="sxs-lookup"><span data-stu-id="60e79-103">Msvm\_VirtualSystemSnapshotSettingData class</span></span>

<span data-ttu-id="60e79-104">Proporciona información adicional que se va a usar con el método [**CreateSnapshot**](cim-virtualsystemsnapshotservice-createsnapshot.md) de la clase [**\_ VirtualSystemSnapshotService de MSVM**](msvm-virtualsystemsnapshotservice.md) .</span><span class="sxs-lookup"><span data-stu-id="60e79-104">Provides additional information to be used with the [**CreateSnapshot**](cim-virtualsystemsnapshotservice-createsnapshot.md) method of the [**Msvm\_VirtualSystemSnapshotService**](msvm-virtualsystemsnapshotservice.md) class.</span></span>

<span data-ttu-id="60e79-105">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="60e79-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="60e79-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="60e79-106">Syntax</span></span>

``` syntax
[AMENDMENT]
class Msvm_VirtualSystemSnapshotSettingData : CIM_SettingData
{
  uint8   ConsistencyLevel;
  boolean IgnoreNonSnapshottableDisks;
  uint8   GuestBackupType;
};
```

## <a name="members"></a><span data-ttu-id="60e79-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="60e79-107">Members</span></span>

<span data-ttu-id="60e79-108">La clase **MSVM \_ VirtualSystemSnapshotSettingData** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="60e79-108">The **Msvm\_VirtualSystemSnapshotSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="60e79-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="60e79-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="60e79-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="60e79-110">Properties</span></span>

<span data-ttu-id="60e79-111">La clase **MSVM \_ VirtualSystemSnapshotSettingData** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="60e79-111">The **Msvm\_VirtualSystemSnapshotSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="60e79-112">**ConsistencyLevel**</span><span class="sxs-lookup"><span data-stu-id="60e79-112">**ConsistencyLevel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60e79-113">Tipo de datos: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="60e79-113">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="60e79-114">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="60e79-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="60e79-115">El nivel de coherencia de la instantánea.</span><span class="sxs-lookup"><span data-stu-id="60e79-115">The consistency level of the snapshot.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="60e79-116">**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="60e79-116">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Application_Consistent"></span><span id="application_consistent"></span><span id="APPLICATION_CONSISTENT"></span>

<span data-ttu-id="60e79-117">**Coherente** con la aplicación (1)</span><span class="sxs-lookup"><span data-stu-id="60e79-117">**Application Consistent** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Crash_Consistent"></span><span id="crash_consistent"></span><span id="CRASH_CONSISTENT"></span>

<span data-ttu-id="60e79-118">**Coherencia de bloqueos** (2)</span><span class="sxs-lookup"><span data-stu-id="60e79-118">**Crash Consistent** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="60e79-119">**GuestBackupType**</span><span class="sxs-lookup"><span data-stu-id="60e79-119">**GuestBackupType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60e79-120">Tipo de datos: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="60e79-120">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="60e79-121">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="60e79-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="60e79-122">Tipo de copia de seguridad que se va a usar en el invitado.</span><span class="sxs-lookup"><span data-stu-id="60e79-122">Backup type to be used inside the guest.</span></span>

> [!Note]  
> <span data-ttu-id="60e79-123">Propiedad agregada en Windows 10, versión 1703</span><span class="sxs-lookup"><span data-stu-id="60e79-123">Property added in Windows 10, version 1703</span></span>

 

<dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

<span data-ttu-id="60e79-124">**Undefined** (0)</span><span class="sxs-lookup"><span data-stu-id="60e79-124">**Undefined** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Full"></span><span id="full"></span><span id="FULL"></span>

<span data-ttu-id="60e79-125">**Full** (1)</span><span class="sxs-lookup"><span data-stu-id="60e79-125">**Full** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Copy"></span><span id="copy"></span><span id="COPY"></span>

<span data-ttu-id="60e79-126">**Copiar** (2)</span><span class="sxs-lookup"><span data-stu-id="60e79-126">**Copy** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="60e79-127">**IgnoreNonSnapshottableDisks**</span><span class="sxs-lookup"><span data-stu-id="60e79-127">**IgnoreNonSnapshottableDisks**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="60e79-128">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="60e79-128">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="60e79-129">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="60e79-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="60e79-130">Especifica si los discos que no son de snapshottable, como los discos de acceso directo y los discos Canal de fibra, se omitirán al crear la instantánea.</span><span class="sxs-lookup"><span data-stu-id="60e79-130">Specifies if non-snapshottable disks like passthrough disks and Fibre Channel Disks are to be ignored while creating the snapshot.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="60e79-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="60e79-131">Requirements</span></span>



| <span data-ttu-id="60e79-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="60e79-132">Requirement</span></span> | <span data-ttu-id="60e79-133">Value</span><span class="sxs-lookup"><span data-stu-id="60e79-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="60e79-134">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="60e79-134">Minimum supported client</span></span><br/> | <span data-ttu-id="60e79-135">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="60e79-135">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="60e79-136">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="60e79-136">Minimum supported server</span></span><br/> | <span data-ttu-id="60e79-137">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="60e79-137">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="60e79-138">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="60e79-138">Namespace</span></span><br/>                | <span data-ttu-id="60e79-139">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="60e79-139">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="60e79-140">MOF</span><span class="sxs-lookup"><span data-stu-id="60e79-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="60e79-141"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="60e79-141"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="60e79-142">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="60e79-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="60e79-143"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="60e79-143"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="60e79-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="60e79-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60e79-145">**SettingData de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="60e79-145">**CIM\_SettingData**</span></span>](cim-settingdata.md)
</dt> </dl>

 

 




