---
description: La \_ clase AssociatedSupplyCurrentSensor de CIM asocia una fuente de alimentación con un sensor actual (amperaje) que supervisa la frecuencia de entrada.
ms.assetid: bed4714f-ecf4-4c53-b231-c8fac673371f
ms.tgt_platform: multiple
title: CIM_AssociatedSupplyCurrentSensor (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_AssociatedSupplyCurrentSensor
- CIM_AssociatedSupplyCurrentSensor.Dependent
- CIM_AssociatedSupplyCurrentSensor.Antecedent
- CIM_AssociatedSupplyCurrentSensor.MonitoringRange
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 70a88d87c68b36db5bd44413e3c68940db44f29b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275037"
---
# <a name="cim_associatedsupplycurrentsensor-class"></a><span data-ttu-id="1dd63-103">\_Clase AssociatedSupplyCurrentSensor de CIM</span><span class="sxs-lookup"><span data-stu-id="1dd63-103">CIM\_AssociatedSupplyCurrentSensor class</span></span>

<span data-ttu-id="1dd63-104">La **clase \_ AssociatedSupplyCurrentSensor de CIM** asocia una fuente de alimentación con un sensor actual (amperaje) que supervisa la frecuencia de entrada.</span><span class="sxs-lookup"><span data-stu-id="1dd63-104">The **CIM\_AssociatedSupplyCurrentSensor** class associates a power supply with a current (amperage) sensor that monitors its input frequency.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="1dd63-105">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="1dd63-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="1dd63-106">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="1dd63-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="1dd63-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="1dd63-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="1dd63-108">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="1dd63-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="1dd63-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1dd63-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{29B273F2-E3D3-11d2-8601-0000F8102E5F}"), AMENDMENT]
class CIM_AssociatedSupplyCurrentSensor : CIM_AssociatedSensor
{
  CIM_PowerSupply   REF Dependent;
  CIM_CurrentSensor REF Antecedent;
  uint16                MonitoringRange;
};
```

## <a name="members"></a><span data-ttu-id="1dd63-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="1dd63-110">Members</span></span>

<span data-ttu-id="1dd63-111">La clase **CIM \_ AssociatedSupplyCurrentSensor** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="1dd63-111">The **CIM\_AssociatedSupplyCurrentSensor** class has these types of members:</span></span>

-   [<span data-ttu-id="1dd63-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="1dd63-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1dd63-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="1dd63-113">Properties</span></span>

<span data-ttu-id="1dd63-114">La clase **CIM \_ AssociatedSupplyCurrentSensor** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="1dd63-114">The **CIM\_AssociatedSupplyCurrentSensor** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1dd63-115">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="1dd63-115">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1dd63-116">Tipo de datos: **CIM \_ CurrentSensor**</span><span class="sxs-lookup"><span data-stu-id="1dd63-116">Data type: **CIM\_CurrentSensor**</span></span>
</dt> <dt>

<span data-ttu-id="1dd63-117">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1dd63-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1dd63-118">Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente")</span><span class="sxs-lookup"><span data-stu-id="1dd63-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="1dd63-119">[**\_ CurrentSensor CIM**](cim-currentsensor.md) que describe el sensor actual.</span><span class="sxs-lookup"><span data-stu-id="1dd63-119">A [**CIM\_CurrentSensor**](cim-currentsensor.md) that describes the current sensor.</span></span>

</dd> <dt>

<span data-ttu-id="1dd63-120">**Dependientes**</span><span class="sxs-lookup"><span data-stu-id="1dd63-120">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1dd63-121">Tipo de datos: sistema de sistema **CIM \_**</span><span class="sxs-lookup"><span data-stu-id="1dd63-121">Data type: **CIM\_PowerSupply**</span></span>
</dt> <dt>

<span data-ttu-id="1dd63-122">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1dd63-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1dd63-123">Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependiente")</span><span class="sxs-lookup"><span data-stu-id="1dd63-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="1dd63-124">Alimentación [**de \_ CIM**](cim-powersupply.md) que describe la fuente de alimentación asociada al sensor actual.</span><span class="sxs-lookup"><span data-stu-id="1dd63-124">A [**CIM\_PowerSupply**](cim-powersupply.md) that describes the power supply associated with the current sensor.</span></span>

</dd> <dt>

<span data-ttu-id="1dd63-125">**MonitoringRange**</span><span class="sxs-lookup"><span data-stu-id="1dd63-125">**MonitoringRange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1dd63-126">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1dd63-126">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1dd63-127">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1dd63-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1dd63-128">Indica el intervalo de frecuencia de entrada de la fuente de alimentación medido por el sensor asociado.</span><span class="sxs-lookup"><span data-stu-id="1dd63-128">Indicates the power supply input frequency range measured by the associated sensor.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="1dd63-129"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="1dd63-129"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="1dd63-130"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="1dd63-130"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Range_1"></span><span id="range_1"></span><span id="RANGE_1"></span>

<span data-ttu-id="1dd63-131"><span id="Range_1"></span><span id="range_1"></span><span id="RANGE_1"></span>**Intervalo 1** (2)</span><span class="sxs-lookup"><span data-stu-id="1dd63-131"><span id="Range_1"></span><span id="range_1"></span><span id="RANGE_1"></span>**Range 1** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Range_2"></span><span id="range_2"></span><span id="RANGE_2"></span>

<span data-ttu-id="1dd63-132"><span id="Range_2"></span><span id="range_2"></span><span id="RANGE_2"></span>**Intervalo 2** (3)</span><span class="sxs-lookup"><span data-stu-id="1dd63-132"><span id="Range_2"></span><span id="range_2"></span><span id="RANGE_2"></span>**Range 2** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Both_Range_1_and_2"></span><span id="both_range_1_and_2"></span><span id="BOTH_RANGE_1_AND_2"></span>

<span data-ttu-id="1dd63-133"><span id="Both_Range_1_and_2"></span><span id="both_range_1_and_2"></span><span id="BOTH_RANGE_1_AND_2"></span>**Rango 1 y 2** (4)</span><span class="sxs-lookup"><span data-stu-id="1dd63-133"><span id="Both_Range_1_and_2"></span><span id="both_range_1_and_2"></span><span id="BOTH_RANGE_1_AND_2"></span>**Both Range 1 and 2** (4)</span></span>


</dt> <dd>

<span data-ttu-id="1dd63-134">Rango 1 y 2</span><span class="sxs-lookup"><span data-stu-id="1dd63-134">Range 1 and 2</span></span>

</dd> </dl>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1dd63-135">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1dd63-135">Remarks</span></span>

<span data-ttu-id="1dd63-136">La clase **CIM \_ AssociatedSupplyCurrentSensor** se deriva de [**\_ AssociatedSensor de CIM**](cim-associatedsensor.md).</span><span class="sxs-lookup"><span data-stu-id="1dd63-136">The **CIM\_AssociatedSupplyCurrentSensor** class is derived from [**CIM\_AssociatedSensor**](cim-associatedsensor.md).</span></span>

<span data-ttu-id="1dd63-137">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="1dd63-137">WMI does not implement this class.</span></span>

<span data-ttu-id="1dd63-138">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="1dd63-138">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="1dd63-139">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="1dd63-139">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="1dd63-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1dd63-140">Requirements</span></span>



| <span data-ttu-id="1dd63-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="1dd63-141">Requirement</span></span> | <span data-ttu-id="1dd63-142">Value</span><span class="sxs-lookup"><span data-stu-id="1dd63-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1dd63-143">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1dd63-143">Minimum supported client</span></span><br/> | <span data-ttu-id="1dd63-144">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1dd63-144">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="1dd63-145">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1dd63-145">Minimum supported server</span></span><br/> | <span data-ttu-id="1dd63-146">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1dd63-146">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="1dd63-147">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="1dd63-147">Namespace</span></span><br/>                | <span data-ttu-id="1dd63-148">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="1dd63-148">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="1dd63-149">MOF</span><span class="sxs-lookup"><span data-stu-id="1dd63-149">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1dd63-150"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1dd63-150"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="1dd63-151">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="1dd63-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1dd63-152"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1dd63-152"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1dd63-153">Vea también</span><span class="sxs-lookup"><span data-stu-id="1dd63-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1dd63-154">**\_ASSOCIATEDSENSOR CIM**</span><span class="sxs-lookup"><span data-stu-id="1dd63-154">**CIM\_AssociatedSensor**</span></span>](cim-associatedsensor.md)
</dt> </dl>

 

