---
description: Exportar los datos de configuración que se van a pasar al método ExportSnapshot de la \_ clase MSVM CollectionSnapshotService.
ms.assetid: 03b448ed-72bc-485e-bb31-4445c53baa1c
title: Msvm_CollectionSnapshotExportSettingData (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionSnapshotExportSettingData
- Msvm_CollectionSnapshotExportSettingData.CopyVmStorage
- Msvm_CollectionSnapshotExportSettingData.DifferentialBackupBase
- Msvm_CollectionSnapshotExportSettingData.BackupIntent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 3e146fe2e2af17223e792d86cff16bf1c4149dd6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666473"
---
# <a name="msvm_collectionsnapshotexportsettingdata-class"></a><span data-ttu-id="e8a37-103">MSVM \_ CollectionSnapshotExportSettingData (clase)</span><span class="sxs-lookup"><span data-stu-id="e8a37-103">Msvm\_CollectionSnapshotExportSettingData class</span></span>

<span data-ttu-id="e8a37-104">Exportar los datos de configuración que se van a pasar al método ExportSnapshot de la clase [**MSVM \_ CollectionSnapshotService**](msvm-collectionsnapshotservice.md) .</span><span class="sxs-lookup"><span data-stu-id="e8a37-104">Export setting data to be passed in to the ExportSnapshot method of [**Msvm\_CollectionSnapshotService**](msvm-collectionsnapshotservice.md) class.</span></span>

<span data-ttu-id="e8a37-105">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="e8a37-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="e8a37-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e8a37-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_CollectionSnapshotExportSettingData : CIM_SettingData
{
  boolean CopyVmStorage;
  string  DifferentialBackupBase;
  uint16  BackupIntent;
};
```

## <a name="members"></a><span data-ttu-id="e8a37-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="e8a37-107">Members</span></span>

<span data-ttu-id="e8a37-108">La clase **MSVM \_ CollectionSnapshotExportSettingData** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="e8a37-108">The **Msvm\_CollectionSnapshotExportSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="e8a37-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="e8a37-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e8a37-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="e8a37-110">Properties</span></span>

<span data-ttu-id="e8a37-111">La clase **MSVM \_ CollectionSnapshotExportSettingData** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="e8a37-111">The **Msvm\_CollectionSnapshotExportSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e8a37-112">**BackupIntent**</span><span class="sxs-lookup"><span data-stu-id="e8a37-112">**BackupIntent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8a37-113">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e8a37-113">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e8a37-114">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="e8a37-114">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="e8a37-115">Indica la intención de usar los conjuntos de copia de seguridad exportados:</span><span class="sxs-lookup"><span data-stu-id="e8a37-115">Indicates the intent how the exported backup sets would be used:</span></span>

<dt>

<span id="BackupIntentPreserveChain"></span><span id="backupintentpreservechain"></span><span id="BACKUPINTENTPRESERVECHAIN"></span>

<span data-ttu-id="e8a37-116"><span id="BackupIntentPreserveChain"></span><span id="backupintentpreservechain"></span><span id="BACKUPINTENTPRESERVECHAIN"></span>**BackupIntentPreserveChain** (1)</span><span class="sxs-lookup"><span data-stu-id="e8a37-116"><span id="BackupIntentPreserveChain"></span><span id="backupintentpreservechain"></span><span id="BACKUPINTENTPRESERVECHAIN"></span>**BackupIntentPreserveChain** (1)</span></span>


</dt> <dd>

<span data-ttu-id="e8a37-117">Todos los conjuntos de copia de seguridad completos y diferenciales exportados se conservarán tal como están.</span><span class="sxs-lookup"><span data-stu-id="e8a37-117">All exported full and differential backup sets would be preserved as they are.</span></span>

</dd> <dt>

<span id="BackupIntentMerge"></span><span id="backupintentmerge"></span><span id="BACKUPINTENTMERGE"></span>

<span data-ttu-id="e8a37-118"><span id="BackupIntentMerge"></span><span id="backupintentmerge"></span><span id="BACKUPINTENTMERGE"></span>**BackupIntentMerge** (2)</span><span class="sxs-lookup"><span data-stu-id="e8a37-118"><span id="BackupIntentMerge"></span><span id="backupintentmerge"></span><span id="BACKUPINTENTMERGE"></span>**BackupIntentMerge** (2)</span></span>


</dt> <dd>

<span data-ttu-id="e8a37-119">Los conjuntos de copia de seguridad completos y diferenciales exportados se combinarán para sintetizar los conjuntos de copia de seguridad completos.</span><span class="sxs-lookup"><span data-stu-id="e8a37-119">The exported full and differential backup sets would be merged to synthesize full backup sets.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="e8a37-120">**CopyVmStorage**</span><span class="sxs-lookup"><span data-stu-id="e8a37-120">**CopyVmStorage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8a37-121">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="e8a37-121">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e8a37-122">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="e8a37-122">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="e8a37-123">Si es **true**, el almacenamiento de la máquina virtual se copiará cuando se exporte la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="e8a37-123">if **true**, the VM storage will be copied when the VM is exported.</span></span> <span data-ttu-id="e8a37-124">En caso contrario, **false.**</span><span class="sxs-lookup"><span data-stu-id="e8a37-124">Otherwise, **false.**</span></span>

</dd> <dt>

<span data-ttu-id="e8a37-125">**DifferentialBackupBase**</span><span class="sxs-lookup"><span data-stu-id="e8a37-125">**DifferentialBackupBase**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8a37-126">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="e8a37-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e8a37-127">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="e8a37-127">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="e8a37-128">Base para la exportación diferencial.</span><span class="sxs-lookup"><span data-stu-id="e8a37-128">Base for differential export.</span></span> <span data-ttu-id="e8a37-129">Se trata de una ruta de acceso a una instancia de [**MSVM \_ ReferencePointCollection**](msvm-referencepointcollection.md) que representa el punto de referencia, o la ruta de acceso a una instancia de [**MSVM \_ SnapshotCollection**](msvm-snapshotcollection.md) que representa la instantánea que se va a usar como base para la exportación diferencial.</span><span class="sxs-lookup"><span data-stu-id="e8a37-129">This is either path to an [**Msvm\_ReferencePointCollection**](msvm-referencepointcollection.md) instance that represents the reference point, or path to an [**Msvm\_SnapshotCollection**](msvm-snapshotcollection.md) instance that represents the snapshot to be used as a base for differential export.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e8a37-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e8a37-130">Requirements</span></span>



| <span data-ttu-id="e8a37-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="e8a37-131">Requirement</span></span> | <span data-ttu-id="e8a37-132">Value</span><span class="sxs-lookup"><span data-stu-id="e8a37-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e8a37-133">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e8a37-133">Minimum supported client</span></span><br/> | <span data-ttu-id="e8a37-134">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="e8a37-134">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="e8a37-135">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e8a37-135">Minimum supported server</span></span><br/> | <span data-ttu-id="e8a37-136">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="e8a37-136">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="e8a37-137">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="e8a37-137">Namespace</span></span><br/>                | <span data-ttu-id="e8a37-138">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="e8a37-138">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="e8a37-139">MOF</span><span class="sxs-lookup"><span data-stu-id="e8a37-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e8a37-140"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e8a37-140"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="e8a37-141">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="e8a37-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e8a37-142"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="e8a37-142"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="e8a37-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="e8a37-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8a37-144">**SettingData de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="e8a37-144">**CIM\_SettingData**</span></span>](cim-settingdata.md)
</dt> </dl>

 

 




