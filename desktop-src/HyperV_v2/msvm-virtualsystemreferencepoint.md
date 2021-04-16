---
description: Representa un punto de referencia para un sistema virtual.
ms.assetid: b3ba4fa7-3b77-4a1d-ab8f-d38af12ab5dd
title: Msvm_VirtualSystemReferencePoint (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemReferencePoint
- Msvm_VirtualSystemReferencePoint.InstanceID
- Msvm_VirtualSystemReferencePoint.ReferencePointType
- Msvm_VirtualSystemReferencePoint.ConsistencyLevel
- Msvm_VirtualSystemReferencePoint.VirtualSystemIdentifier
- Msvm_VirtualSystemReferencePoint.HasAssociatedData
- Msvm_VirtualSystemReferencePoint.VirtualDiskIdentifiers
- Msvm_VirtualSystemReferencePoint.ResilientChangeTrackingIdentifiers
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: add160cf44a592462634704ddf783cd8f4084068
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "105670081"
---
# <a name="msvm_virtualsystemreferencepoint-class"></a><span data-ttu-id="46f46-103">MSVM \_ VirtualSystemReferencePoint (clase)</span><span class="sxs-lookup"><span data-stu-id="46f46-103">Msvm\_VirtualSystemReferencePoint class</span></span>

<span data-ttu-id="46f46-104">Representa un punto de referencia para un sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="46f46-104">Represents a reference point for a virtual system.</span></span>

<span data-ttu-id="46f46-105">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="46f46-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="46f46-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="46f46-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualSystemReferencePoint : CIM_ManagedElement
{
  string  InstanceID;
  uint16  ReferencePointType;
  uint16  ConsistencyLevel;
  string  VirtualSystemIdentifier;
  boolean HasAssociatedData;
  string  VirtualDiskIdentifiers[];
  string  ResilientChangeTrackingIdentifiers[];
};
```

## <a name="members"></a><span data-ttu-id="46f46-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="46f46-107">Members</span></span>

<span data-ttu-id="46f46-108">La clase **MSVM \_ VirtualSystemReferencePoint** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="46f46-108">The **Msvm\_VirtualSystemReferencePoint** class has these types of members:</span></span>

-   [<span data-ttu-id="46f46-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="46f46-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="46f46-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="46f46-110">Properties</span></span>

<span data-ttu-id="46f46-111">La clase **MSVM \_ VirtualSystemReferencePoint** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="46f46-111">The **Msvm\_VirtualSystemReferencePoint** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="46f46-112">**ConsistencyLevel**</span><span class="sxs-lookup"><span data-stu-id="46f46-112">**ConsistencyLevel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46f46-113">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="46f46-113">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="46f46-114">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="46f46-114">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="46f46-115">El nivel de coherencia del punto de referencia.</span><span class="sxs-lookup"><span data-stu-id="46f46-115">The consistency level of the reference point.</span></span>

<dt>

<span id="Application_Consistent"></span><span id="application_consistent"></span><span id="APPLICATION_CONSISTENT"></span>

<span data-ttu-id="46f46-116"><span id="Application_Consistent"></span><span id="application_consistent"></span><span id="APPLICATION_CONSISTENT"></span>**Coherente** con la aplicación (1)</span><span class="sxs-lookup"><span data-stu-id="46f46-116"><span id="Application_Consistent"></span><span id="application_consistent"></span><span id="APPLICATION_CONSISTENT"></span>**Application Consistent** (1)</span></span>


</dt> <dd>

<span data-ttu-id="46f46-117">El punto de referencia indica un punto en el tiempo en el que el sistema virtual estuvo en un estado coherente con la aplicación.</span><span class="sxs-lookup"><span data-stu-id="46f46-117">The reference point indicates a point in time when the virtual system was in application consistent state.</span></span>

</dd> <dt>

<span id="Crash_Consistent"></span><span id="crash_consistent"></span><span id="CRASH_CONSISTENT"></span>

<span data-ttu-id="46f46-118"><span id="Crash_Consistent"></span><span id="crash_consistent"></span><span id="CRASH_CONSISTENT"></span>**Coherencia de bloqueos** (2)</span><span class="sxs-lookup"><span data-stu-id="46f46-118"><span id="Crash_Consistent"></span><span id="crash_consistent"></span><span id="CRASH_CONSISTENT"></span>**Crash Consistent** (2)</span></span>


</dt> <dd>

<span data-ttu-id="46f46-119">El punto de referencia indica un punto en el tiempo en el que el sistema virtual se encontraba en un estado coherente con el bloqueo.</span><span class="sxs-lookup"><span data-stu-id="46f46-119">The reference point indicates a point in time when the virtual system was in crash consistent state.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="46f46-120">**HasAssociatedData**</span><span class="sxs-lookup"><span data-stu-id="46f46-120">**HasAssociatedData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46f46-121">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="46f46-121">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="46f46-122">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="46f46-122">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="46f46-123">Establézcalo en **true** si el punto de referencia tiene datos asociados.</span><span class="sxs-lookup"><span data-stu-id="46f46-123">Set to **true** if the reference point has associated data.</span></span> <span data-ttu-id="46f46-124">Esto solo es válido para los puntos de referencia basados en el registro.</span><span class="sxs-lookup"><span data-stu-id="46f46-124">This is valid only for log based reference points.</span></span> <span data-ttu-id="46f46-125">En el caso de los puntos de referencia basados en RCT, **HasAssociatedData** se establece en **false**.</span><span class="sxs-lookup"><span data-stu-id="46f46-125">For RCT-based reference points, **HasAssociatedData** is set to **false**.</span></span> <span data-ttu-id="46f46-126">En el caso de los puntos de referencia basados en el registro, una vez descartado el registro, **HasAssociatedData** se convierte en **false**.</span><span class="sxs-lookup"><span data-stu-id="46f46-126">For log based reference points, once the log is discarded **HasAssociatedData** becomes **false**.</span></span>

</dd> <dt>

<span data-ttu-id="46f46-127">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="46f46-127">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46f46-128">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="46f46-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="46f46-129">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="46f46-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="46f46-130">Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("InstanceID"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="46f46-130">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("InstanceID"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="46f46-131">Identificación única de un objeto de punto de referencia.</span><span class="sxs-lookup"><span data-stu-id="46f46-131">Unique identification of a reference point object.</span></span>

</dd> <dt>

<span data-ttu-id="46f46-132">**ReferencePointType**</span><span class="sxs-lookup"><span data-stu-id="46f46-132">**ReferencePointType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46f46-133">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="46f46-133">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="46f46-134">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="46f46-134">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="46f46-135">Indica el tipo del punto de referencia.</span><span class="sxs-lookup"><span data-stu-id="46f46-135">Indicates the type of the reference point.</span></span>

<dt>

<span id="Log_based"></span><span id="log_based"></span><span id="LOG_BASED"></span>

<span data-ttu-id="46f46-136"><span id="Log_based"></span><span id="log_based"></span><span id="LOG_BASED"></span>**Basado en el registro** (1)</span><span class="sxs-lookup"><span data-stu-id="46f46-136"><span id="Log_based"></span><span id="log_based"></span><span id="LOG_BASED"></span>**Log based** (1)</span></span>


</dt> <dd>

<span data-ttu-id="46f46-137">Seguimiento del registro de réplica de Hyper-V.</span><span class="sxs-lookup"><span data-stu-id="46f46-137">Hyper-V replica log tracking.</span></span>

</dd> <dt>

<span id="RCT_based"></span><span id="rct_based"></span><span id="RCT_BASED"></span>

<span data-ttu-id="46f46-138"><span id="RCT_based"></span><span id="rct_based"></span><span id="RCT_BASED"></span>**RCT basado** (2)</span><span class="sxs-lookup"><span data-stu-id="46f46-138"><span id="RCT_based"></span><span id="rct_based"></span><span id="RCT_BASED"></span>**RCT based** (2)</span></span>


</dt> <dd>

<span data-ttu-id="46f46-139">Basado en Change Tracking resistente de los discos virtuales.</span><span class="sxs-lookup"><span data-stu-id="46f46-139">Based on Resilient Change Tracking of virtual disks.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="46f46-140">**ResilientChangeTrackingIdentifiers**</span><span class="sxs-lookup"><span data-stu-id="46f46-140">**ResilientChangeTrackingIdentifiers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46f46-141">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="46f46-141">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="46f46-142">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="46f46-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="46f46-143">Una matriz de identificadores RCT correspondientes a los discos virtuales de la máquina virtual en el momento en que se creó este punto de referencia.</span><span class="sxs-lookup"><span data-stu-id="46f46-143">An array of RCT IDs corresponding to the virtual disks of the VM at the time this reference point was created.</span></span> <span data-ttu-id="46f46-144">Este campo solo es válido para los puntos de referencia basados en RCT.</span><span class="sxs-lookup"><span data-stu-id="46f46-144">This field is valid only for RCT-based reference points.</span></span>

</dd> <dt>

<span data-ttu-id="46f46-145">**VirtualDiskIdentifiers**</span><span class="sxs-lookup"><span data-stu-id="46f46-145">**VirtualDiskIdentifiers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46f46-146">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="46f46-146">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="46f46-147">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="46f46-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="46f46-148">Una matriz de identificadores de instancia de WMI que corresponden a los discos virtuales de la máquina virtual en el momento en que se creó este punto de referencia.</span><span class="sxs-lookup"><span data-stu-id="46f46-148">An array of WMI instance IDs corresponding to the virtual disks of the VM at the time this reference point was created.</span></span> <span data-ttu-id="46f46-149">Estos discos virtuales tienen identificadores RCT asociados.</span><span class="sxs-lookup"><span data-stu-id="46f46-149">These virtual disks have RCT IDs associated with them.</span></span>

</dd> <dt>

<span data-ttu-id="46f46-150">**Virtualsystemidentifer**</span><span class="sxs-lookup"><span data-stu-id="46f46-150">**VirtualSystemIdentifier**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46f46-151">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="46f46-151">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="46f46-152">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="46f46-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="46f46-153">Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ ComputerSystem**](cim-computersystem.md).**Nombre**")</span><span class="sxs-lookup"><span data-stu-id="46f46-153">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**Name**")</span></span>
</dt> </dl>

<span data-ttu-id="46f46-154">El nombre del [**\_ ComputerSystem de CIM**](cim-computersystem.md) al que pertenece este punto de referencia</span><span class="sxs-lookup"><span data-stu-id="46f46-154">The name of the [**CIM\_ComputerSystem**](cim-computersystem.md) to which this reference point belongs</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="46f46-155">Requisitos</span><span class="sxs-lookup"><span data-stu-id="46f46-155">Requirements</span></span>



| <span data-ttu-id="46f46-156">Requisito</span><span class="sxs-lookup"><span data-stu-id="46f46-156">Requirement</span></span> | <span data-ttu-id="46f46-157">Value</span><span class="sxs-lookup"><span data-stu-id="46f46-157">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="46f46-158">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="46f46-158">Minimum supported client</span></span><br/> | <span data-ttu-id="46f46-159">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="46f46-159">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="46f46-160">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="46f46-160">Minimum supported server</span></span><br/> | <span data-ttu-id="46f46-161">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="46f46-161">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="46f46-162">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="46f46-162">Namespace</span></span><br/>                | <span data-ttu-id="46f46-163">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="46f46-163">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="46f46-164">MOF</span><span class="sxs-lookup"><span data-stu-id="46f46-164">MOF</span></span><br/>                      | <dl> <span data-ttu-id="46f46-165"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="46f46-165"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="46f46-166">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="46f46-166">DLL</span></span><br/>                      | <dl> <span data-ttu-id="46f46-167"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="46f46-167"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="46f46-168">Vea también</span><span class="sxs-lookup"><span data-stu-id="46f46-168">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46f46-169">**ManagedElement de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="46f46-169">**CIM\_ManagedElement**</span></span>](cim-managedelement.md)
</dt> </dl>

 

