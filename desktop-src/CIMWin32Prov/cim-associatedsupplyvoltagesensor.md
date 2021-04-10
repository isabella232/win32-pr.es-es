---
description: Asocia una fuente de alimentación a un sensor de voltaje que supervisa su voltaje de entrada.
ms.assetid: 4164320e-8362-4ce2-9949-f14669278bd8
ms.tgt_platform: multiple
title: CIM_AssociatedSupplyVoltageSensor (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_AssociatedSupplyVoltageSensor
- CIM_AssociatedSupplyVoltageSensor.Dependent
- CIM_AssociatedSupplyVoltageSensor.Antecedent
- CIM_AssociatedSupplyVoltageSensor.MonitoringRange
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: ce597fb9e170b63335c56e30f8f8c4ddb30af66c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153290"
---
# <a name="cim_associatedsupplyvoltagesensor-class"></a><span data-ttu-id="2b96c-103">\_Clase AssociatedSupplyVoltageSensor de CIM</span><span class="sxs-lookup"><span data-stu-id="2b96c-103">CIM\_AssociatedSupplyVoltageSensor class</span></span>

<span data-ttu-id="2b96c-104">La **clase \_ AssociatedSupplyVoltageSensor de CIM** asocia una fuente de alimentación con un sensor de voltaje que supervisa su voltaje de entrada.</span><span class="sxs-lookup"><span data-stu-id="2b96c-104">The **CIM\_AssociatedSupplyVoltageSensor** class associates a power supply with a voltage sensor that monitors its input voltage.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2b96c-105">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="2b96c-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="2b96c-106">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="2b96c-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="2b96c-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="2b96c-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="2b96c-108">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="2b96c-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="2b96c-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2b96c-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{327ABD78-E3D3-11d2-8601-0000F8102E5F}"), AMENDMENT]
class CIM_AssociatedSupplyVoltageSensor : CIM_AssociatedSensor
{
  CIM_PowerSupply   REF Dependent;
  CIM_VoltageSensor REF Antecedent;
  uint16                MonitoringRange;
};
```

## <a name="members"></a><span data-ttu-id="2b96c-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="2b96c-110">Members</span></span>

<span data-ttu-id="2b96c-111">La clase **CIM \_ AssociatedSupplyVoltageSensor** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="2b96c-111">The **CIM\_AssociatedSupplyVoltageSensor** class has these types of members:</span></span>

-   [<span data-ttu-id="2b96c-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="2b96c-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2b96c-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="2b96c-113">Properties</span></span>

<span data-ttu-id="2b96c-114">La clase **CIM \_ AssociatedSupplyVoltageSensor** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="2b96c-114">The **CIM\_AssociatedSupplyVoltageSensor** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2b96c-115">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="2b96c-115">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b96c-116">Tipo de datos: **CIM \_ VoltageSensor**</span><span class="sxs-lookup"><span data-stu-id="2b96c-116">Data type: **CIM\_VoltageSensor**</span></span>
</dt> <dt>

<span data-ttu-id="2b96c-117">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2b96c-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2b96c-118">Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente")</span><span class="sxs-lookup"><span data-stu-id="2b96c-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="2b96c-119">Un [**\_ VoltageSensor de CIM**](cim-voltagesensor.md) que describe el sensor de voltaje.</span><span class="sxs-lookup"><span data-stu-id="2b96c-119">A [**CIM\_VoltageSensor**](cim-voltagesensor.md) that describes the voltage sensor.</span></span>

</dd> <dt>

<span data-ttu-id="2b96c-120">**Dependientes**</span><span class="sxs-lookup"><span data-stu-id="2b96c-120">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b96c-121">Tipo de datos: sistema de sistema **CIM \_**</span><span class="sxs-lookup"><span data-stu-id="2b96c-121">Data type: **CIM\_PowerSupply**</span></span>
</dt> <dt>

<span data-ttu-id="2b96c-122">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2b96c-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2b96c-123">Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependiente")</span><span class="sxs-lookup"><span data-stu-id="2b96c-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="2b96c-124">Una alimentación de [**CIM \_**](cim-powersupply.md) que describe la fuente de alimentación asociada al sensor de voltaje.</span><span class="sxs-lookup"><span data-stu-id="2b96c-124">A [**CIM\_PowerSupply**](cim-powersupply.md) that describes the power supply associated with the voltage sensor.</span></span>

</dd> <dt>

<span data-ttu-id="2b96c-125">**MonitoringRange**</span><span class="sxs-lookup"><span data-stu-id="2b96c-125">**MonitoringRange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2b96c-126">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2b96c-126">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2b96c-127">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2b96c-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2b96c-128">Indica el intervalo de voltaje de entrada de la fuente de alimentación medido por el sensor asociado.</span><span class="sxs-lookup"><span data-stu-id="2b96c-128">Indicates the power supply's input voltage range measured by the associated sensor.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="2b96c-129"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="2b96c-129"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="2b96c-130"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="2b96c-130"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Range_1"></span><span id="range_1"></span><span id="RANGE_1"></span>

<span data-ttu-id="2b96c-131"><span id="Range_1"></span><span id="range_1"></span><span id="RANGE_1"></span>**Intervalo 1** (2)</span><span class="sxs-lookup"><span data-stu-id="2b96c-131"><span id="Range_1"></span><span id="range_1"></span><span id="RANGE_1"></span>**Range 1** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Range_2"></span><span id="range_2"></span><span id="RANGE_2"></span>

<span data-ttu-id="2b96c-132"><span id="Range_2"></span><span id="range_2"></span><span id="RANGE_2"></span>**Intervalo 2** (3)</span><span class="sxs-lookup"><span data-stu-id="2b96c-132"><span id="Range_2"></span><span id="range_2"></span><span id="RANGE_2"></span>**Range 2** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Both_Range_1_and_2"></span><span id="both_range_1_and_2"></span><span id="BOTH_RANGE_1_AND_2"></span>

<span data-ttu-id="2b96c-133"><span id="Both_Range_1_and_2"></span><span id="both_range_1_and_2"></span><span id="BOTH_RANGE_1_AND_2"></span>**Rango 1 y 2** (4)</span><span class="sxs-lookup"><span data-stu-id="2b96c-133"><span id="Both_Range_1_and_2"></span><span id="both_range_1_and_2"></span><span id="BOTH_RANGE_1_AND_2"></span>**Both Range 1 and 2** (4)</span></span>


</dt> <dd>

<span data-ttu-id="2b96c-134">Rango 1 y 2</span><span class="sxs-lookup"><span data-stu-id="2b96c-134">Range 1 and 2</span></span>

</dd> </dl>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2b96c-135">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2b96c-135">Remarks</span></span>

<span data-ttu-id="2b96c-136">La clase **CIM \_ AssociatedSupplyVoltageSensor** se deriva de [**\_ AssociatedSensor de CIM**](cim-associatedsensor.md).</span><span class="sxs-lookup"><span data-stu-id="2b96c-136">The **CIM\_AssociatedSupplyVoltageSensor** class is derived from [**CIM\_AssociatedSensor**](cim-associatedsensor.md).</span></span>

<span data-ttu-id="2b96c-137">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="2b96c-137">WMI does not implement this class.</span></span>

<span data-ttu-id="2b96c-138">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="2b96c-138">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="2b96c-139">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="2b96c-139">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="2b96c-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2b96c-140">Requirements</span></span>



| <span data-ttu-id="2b96c-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="2b96c-141">Requirement</span></span> | <span data-ttu-id="2b96c-142">Value</span><span class="sxs-lookup"><span data-stu-id="2b96c-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2b96c-143">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2b96c-143">Minimum supported client</span></span><br/> | <span data-ttu-id="2b96c-144">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2b96c-144">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="2b96c-145">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2b96c-145">Minimum supported server</span></span><br/> | <span data-ttu-id="2b96c-146">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2b96c-146">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="2b96c-147">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="2b96c-147">Namespace</span></span><br/>                | <span data-ttu-id="2b96c-148">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="2b96c-148">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="2b96c-149">MOF</span><span class="sxs-lookup"><span data-stu-id="2b96c-149">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2b96c-150"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2b96c-150"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="2b96c-151">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="2b96c-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2b96c-152"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2b96c-152"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2b96c-153">Vea también</span><span class="sxs-lookup"><span data-stu-id="2b96c-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b96c-154">**\_ASSOCIATEDSENSOR CIM**</span><span class="sxs-lookup"><span data-stu-id="2b96c-154">**CIM\_AssociatedSensor**</span></span>](cim-associatedsensor.md)
</dt> </dl>

 

