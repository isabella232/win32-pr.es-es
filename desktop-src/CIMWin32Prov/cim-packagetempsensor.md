---
description: La \_ Asociación PackageTempSensor de CIM representa la relación en la que un sensor de temperatura se instala a menudo en un paquete, como un chasis o un bastidor, para supervisar el entorno del paquete.
ms.assetid: 79f2c4d1-5e1a-4c5f-9ef4-0c8bc3926a13
ms.tgt_platform: multiple
title: CIM_PackageTempSensor (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PackageTempSensor
- CIM_PackageTempSensor.Dependent
- CIM_PackageTempSensor.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 28c3fa3ba569a2bf3101d62734bb9e4d5372fcf0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153154"
---
# <a name="cim_packagetempsensor-class"></a><span data-ttu-id="3923a-103">\_Clase PackageTempSensor de CIM</span><span class="sxs-lookup"><span data-stu-id="3923a-103">CIM\_PackageTempSensor class</span></span>

<span data-ttu-id="3923a-104">La **Asociación \_ PackageTempSensor de CIM** representa la relación en la que un sensor de temperatura se instala a menudo en un paquete, como un chasis o un bastidor, para supervisar el entorno del paquete.</span><span class="sxs-lookup"><span data-stu-id="3923a-104">The **CIM\_PackageTempSensor** association represents the relationship in which a temperature sensor is often installed in a package, such as a chassis or a rack, to monitor the package's environment.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="3923a-105">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="3923a-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="3923a-106">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="3923a-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="3923a-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="3923a-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="3923a-108">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="3923a-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="3923a-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3923a-109">Syntax</span></span>

``` syntax
[Abstract, Aggregation, UUID("{FAF76B8F-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_PackageTempSensor : CIM_Dependency
{
  CIM_PhysicalPackage   REF Dependent;
  CIM_TemperatureSensor REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="3923a-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="3923a-110">Members</span></span>

<span data-ttu-id="3923a-111">La clase **CIM \_ PackageTempSensor** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="3923a-111">The **CIM\_PackageTempSensor** class has these types of members:</span></span>

-   [<span data-ttu-id="3923a-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="3923a-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3923a-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="3923a-113">Properties</span></span>

<span data-ttu-id="3923a-114">La clase **CIM \_ PackageTempSensor** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="3923a-114">The **CIM\_PackageTempSensor** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3923a-115">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="3923a-115">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3923a-116">Tipo de datos: **CIM \_ TemperatureSensor**</span><span class="sxs-lookup"><span data-stu-id="3923a-116">Data type: **CIM\_TemperatureSensor**</span></span>
</dt> <dt>

<span data-ttu-id="3923a-117">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3923a-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3923a-118">Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente")</span><span class="sxs-lookup"><span data-stu-id="3923a-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="3923a-119">Un [**\_ TemperatureSensor de CIM**](cim-temperaturesensor.md) que describe el sensor de temperatura para el paquete.</span><span class="sxs-lookup"><span data-stu-id="3923a-119">A [**CIM\_TemperatureSensor**](cim-temperaturesensor.md) describing the temperature sensor for the package.</span></span>

</dd> <dt>

<span data-ttu-id="3923a-120">**Dependientes**</span><span class="sxs-lookup"><span data-stu-id="3923a-120">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3923a-121">Tipo de datos: **CIM \_ PhysicalPackage**</span><span class="sxs-lookup"><span data-stu-id="3923a-121">Data type: **CIM\_PhysicalPackage**</span></span>
</dt> <dt>

<span data-ttu-id="3923a-122">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3923a-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3923a-123">Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependiente")</span><span class="sxs-lookup"><span data-stu-id="3923a-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="3923a-124">Un [**\_ PhysicalPackage de CIM**](cim-physicalpackage.md) que describe el paquete físico cuyo entorno se supervisa.</span><span class="sxs-lookup"><span data-stu-id="3923a-124">A [**CIM\_PhysicalPackage**](cim-physicalpackage.md) describing the physical package whose environment is monitored.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3923a-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3923a-125">Remarks</span></span>

<span data-ttu-id="3923a-126">**CIM \_ PackageTempSensor** se deriva de [**la \_ dependencia CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="3923a-126">**CIM\_PackageTempSensor** is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="3923a-127">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="3923a-127">WMI does not implement this class.</span></span>

<span data-ttu-id="3923a-128">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="3923a-128">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="3923a-129">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="3923a-129">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="3923a-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3923a-130">Requirements</span></span>



| <span data-ttu-id="3923a-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="3923a-131">Requirement</span></span> | <span data-ttu-id="3923a-132">Value</span><span class="sxs-lookup"><span data-stu-id="3923a-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3923a-133">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3923a-133">Minimum supported client</span></span><br/> | <span data-ttu-id="3923a-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3923a-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="3923a-135">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3923a-135">Minimum supported server</span></span><br/> | <span data-ttu-id="3923a-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3923a-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="3923a-137">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="3923a-137">Namespace</span></span><br/>                | <span data-ttu-id="3923a-138">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="3923a-138">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="3923a-139">MOF</span><span class="sxs-lookup"><span data-stu-id="3923a-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3923a-140"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3923a-140"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="3923a-141">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="3923a-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3923a-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3923a-142"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3923a-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="3923a-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3923a-144">**Dependencia de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="3923a-144">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

