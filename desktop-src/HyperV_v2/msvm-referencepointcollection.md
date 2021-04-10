---
description: Representa una colección de puntos de referencia del sistema virtual.
ms.assetid: dc293f94-a683-468f-af05-ba99824d773e
title: Msvm_ReferencePointCollection (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReferencePointCollection
- Msvm_ReferencePointCollection.CollectionID
- Msvm_ReferencePointCollection.ElementName
- Msvm_ReferencePointCollection.ReferencePointType
- Msvm_ReferencePointCollection.ConsistencyLevel
- Msvm_ReferencePointCollection.VirtualSystemCollectionId
- Msvm_ReferencePointCollection.HasAssociatedLog
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 570590221ee8568d78e150fec3c359365c8434cd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910142"
---
# <a name="msvm_referencepointcollection-class"></a><span data-ttu-id="bc406-103">MSVM \_ ReferencePointCollection (clase)</span><span class="sxs-lookup"><span data-stu-id="bc406-103">Msvm\_ReferencePointCollection class</span></span>

<span data-ttu-id="bc406-104">Representa una colección de puntos de referencia del sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="bc406-104">Represents a collection of virtual system reference points.</span></span>

<span data-ttu-id="bc406-105">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="bc406-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="bc406-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bc406-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ReferencePointCollection : CIM_Collection
{
  string  CollectionID;
  string  ElementName;
  uint16  ReferencePointType;
  uint16  ConsistencyLevel;
  string  VirtualSystemCollectionId;
  boolean HasAssociatedLog;
};
```

## <a name="members"></a><span data-ttu-id="bc406-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="bc406-107">Members</span></span>

<span data-ttu-id="bc406-108">La clase **MSVM \_ ReferencePointCollection** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="bc406-108">The **Msvm\_ReferencePointCollection** class has these types of members:</span></span>

-   [<span data-ttu-id="bc406-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="bc406-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="bc406-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="bc406-110">Properties</span></span>

<span data-ttu-id="bc406-111">La clase **MSVM \_ ReferencePointCollection** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="bc406-111">The **Msvm\_ReferencePointCollection** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="bc406-112">**Recopilación**</span><span class="sxs-lookup"><span data-stu-id="bc406-112">**CollectionID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc406-113">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="bc406-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bc406-114">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="bc406-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bc406-115">Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("CollectionID"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="bc406-115">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CollectionID"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="bc406-116">Identificación única del objeto de colección.</span><span class="sxs-lookup"><span data-stu-id="bc406-116">The unique identification of the collection object.</span></span>

</dd> <dt>

<span data-ttu-id="bc406-117">**ConsistencyLevel**</span><span class="sxs-lookup"><span data-stu-id="bc406-117">**ConsistencyLevel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc406-118">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="bc406-118">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="bc406-119">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="bc406-119">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="bc406-120">Nivel de coherencia del punto de referencia.</span><span class="sxs-lookup"><span data-stu-id="bc406-120">Consistency level of the reference point.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="bc406-121"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="bc406-121"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Crash_Consistent"></span><span id="crash_consistent"></span><span id="CRASH_CONSISTENT"></span>

<span data-ttu-id="bc406-122"><span id="Crash_Consistent"></span><span id="crash_consistent"></span><span id="CRASH_CONSISTENT"></span>**Coherencia de bloqueos** (1)</span><span class="sxs-lookup"><span data-stu-id="bc406-122"><span id="Crash_Consistent"></span><span id="crash_consistent"></span><span id="CRASH_CONSISTENT"></span>**Crash Consistent** (1)</span></span>


</dt> <dd>

<span data-ttu-id="bc406-123">El punto de referencia indica un punto en el tiempo en el que el sistema virtual se encontraba en un estado coherente con el bloqueo.</span><span class="sxs-lookup"><span data-stu-id="bc406-123">The reference point indicates a point in time when the virtual system was in crash consistent state.</span></span>

</dd> <dt>

<span id="Application_Consistent"></span><span id="application_consistent"></span><span id="APPLICATION_CONSISTENT"></span>

<span data-ttu-id="bc406-124"><span id="Application_Consistent"></span><span id="application_consistent"></span><span id="APPLICATION_CONSISTENT"></span>**Coherente** con la aplicación (2)</span><span class="sxs-lookup"><span data-stu-id="bc406-124"><span id="Application_Consistent"></span><span id="application_consistent"></span><span id="APPLICATION_CONSISTENT"></span>**Application Consistent** (2)</span></span>


</dt> <dd>

<span data-ttu-id="bc406-125">El punto de referencia indica un punto en el tiempo en el que el sistema virtual estuvo en un estado coherente con la aplicación.</span><span class="sxs-lookup"><span data-stu-id="bc406-125">The reference point indicates a point in time when the virtual system was in application consistent state.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="bc406-126">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="bc406-126">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc406-127">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="bc406-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bc406-128">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="bc406-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bc406-129">Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("ElementName")</span><span class="sxs-lookup"><span data-stu-id="bc406-129">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("ElementName")</span></span>
</dt> </dl>

<span data-ttu-id="bc406-130">Nombre definido por el usuario para la colección.</span><span class="sxs-lookup"><span data-stu-id="bc406-130">An user-defined name for the collection.</span></span> <span data-ttu-id="bc406-131">Tenga en cuenta que no se garantiza que sea único.</span><span class="sxs-lookup"><span data-stu-id="bc406-131">Note this is not guaranteed to be unique.</span></span>

</dd> <dt>

<span data-ttu-id="bc406-132">**HasAssociatedLog**</span><span class="sxs-lookup"><span data-stu-id="bc406-132">**HasAssociatedLog**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc406-133">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="bc406-133">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="bc406-134">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="bc406-134">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="bc406-135">**true** si todos los puntos de referencia de miembro tienen registros asociados.</span><span class="sxs-lookup"><span data-stu-id="bc406-135">**true** if all the member reference points have associated logs.</span></span> <span data-ttu-id="bc406-136">Esto solo es válido para los puntos de referencia basados en el registro.</span><span class="sxs-lookup"><span data-stu-id="bc406-136">This is valid only for log based reference points.</span></span> <span data-ttu-id="bc406-137">En el caso de los puntos de referencia basados en RCT, **HasAssociatedLog** se establece en **false**.</span><span class="sxs-lookup"><span data-stu-id="bc406-137">For RCT based reference points, **HasAssociatedLog** is set to **false**.</span></span> <span data-ttu-id="bc406-138">En el caso de los puntos de referencia basados en el registro, una vez descartado el registro, **HasAssociatedLog** se convierte en **false**.</span><span class="sxs-lookup"><span data-stu-id="bc406-138">For log based reference points, once the log is discarded **HasAssociatedLog** becomes **false**.</span></span>

</dd> <dt>

<span data-ttu-id="bc406-139">**ReferencePointType**</span><span class="sxs-lookup"><span data-stu-id="bc406-139">**ReferencePointType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc406-140">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="bc406-140">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="bc406-141">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="bc406-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bc406-142">Calificadores: [ **en**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="bc406-142">Qualifiers: [**In**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="bc406-143">Indica el tipo del punto de referencia.</span><span class="sxs-lookup"><span data-stu-id="bc406-143">Indicates the type of the reference point.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="bc406-144"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="bc406-144"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Log_based"></span><span id="log_based"></span><span id="LOG_BASED"></span>

<span data-ttu-id="bc406-145"><span id="Log_based"></span><span id="log_based"></span><span id="LOG_BASED"></span>**Basado en el registro** (1)</span><span class="sxs-lookup"><span data-stu-id="bc406-145"><span id="Log_based"></span><span id="log_based"></span><span id="LOG_BASED"></span>**Log based** (1)</span></span>


</dt> <dd>

<span data-ttu-id="bc406-146">Seguimiento del registro de réplica de Hyper-V.</span><span class="sxs-lookup"><span data-stu-id="bc406-146">Hyper-V replica log tracking.</span></span>

</dd> <dt>

<span id="RCT_based"></span><span id="rct_based"></span><span id="RCT_BASED"></span>

<span data-ttu-id="bc406-147"><span id="RCT_based"></span><span id="rct_based"></span><span id="RCT_BASED"></span>**RCT basado** (2)</span><span class="sxs-lookup"><span data-stu-id="bc406-147"><span id="RCT_based"></span><span id="rct_based"></span><span id="RCT_BASED"></span>**RCT based** (2)</span></span>


</dt> <dd>

<span data-ttu-id="bc406-148">Basado en Change Tracking resistente de los discos virtuales.</span><span class="sxs-lookup"><span data-stu-id="bc406-148">Based on Resilient Change Tracking of virtual disks.</span></span>

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="bc406-149"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="bc406-149"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>

<span data-ttu-id="bc406-150"><span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>**Específico del proveedor** (32768... 65535)</span><span class="sxs-lookup"><span data-stu-id="bc406-150"><span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>**Vendor Specific** (32768..65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="bc406-151">**VirtualSystemCollectionId**</span><span class="sxs-lookup"><span data-stu-id="bc406-151">**VirtualSystemCollectionId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc406-152">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="bc406-152">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bc406-153">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="bc406-153">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bc406-154">Calificadores: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**MSVM \_ VirtualSystemCollection**](msvm-virtualsystemcollection.md).**CollectionID**")</span><span class="sxs-lookup"><span data-stu-id="bc406-154">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**Msvm\_VirtualSystemCollection**](msvm-virtualsystemcollection.md).**CollectionID**")</span></span>
</dt> </dl>

<span data-ttu-id="bc406-155">Identificador del [**\_ VirtualSystemCollection de MSVM**](msvm-virtualsystemcollection.md) al que pertenece este punto de referencia.</span><span class="sxs-lookup"><span data-stu-id="bc406-155">The identifier of the [**Msvm\_VirtualSystemCollection**](msvm-virtualsystemcollection.md) to which this reference point belongs.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="bc406-156">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bc406-156">Requirements</span></span>



| <span data-ttu-id="bc406-157">Requisito</span><span class="sxs-lookup"><span data-stu-id="bc406-157">Requirement</span></span> | <span data-ttu-id="bc406-158">Value</span><span class="sxs-lookup"><span data-stu-id="bc406-158">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bc406-159">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bc406-159">Minimum supported client</span></span><br/> | <span data-ttu-id="bc406-160">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="bc406-160">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="bc406-161">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bc406-161">Minimum supported server</span></span><br/> | <span data-ttu-id="bc406-162">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="bc406-162">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="bc406-163">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="bc406-163">Namespace</span></span><br/>                | <span data-ttu-id="bc406-164">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="bc406-164">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="bc406-165">MOF</span><span class="sxs-lookup"><span data-stu-id="bc406-165">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bc406-166"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="bc406-166"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="bc406-167">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="bc406-167">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bc406-168"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="bc406-168"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="bc406-169">Vea también</span><span class="sxs-lookup"><span data-stu-id="bc406-169">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc406-170">**\_Colección CIM**</span><span class="sxs-lookup"><span data-stu-id="bc406-170">**CIM\_Collection**</span></span>](cim-collection.md)
</dt> </dl>

 

