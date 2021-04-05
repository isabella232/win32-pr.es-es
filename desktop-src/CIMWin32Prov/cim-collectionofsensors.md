---
description: La \_ Asociación CollectionOfSensors de CIM representa los sensores binarios que componen el sensor de múltiples Estados.
ms.assetid: d9494716-bb4e-4aa2-9e3b-e865360c740f
ms.tgt_platform: multiple
title: CIM_CollectionOfSensors (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_CollectionOfSensors
- CIM_CollectionOfSensors.PartComponent
- CIM_CollectionOfSensors.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 06f33d3b55c2c35526495d492b0f063fee9c1a0c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104000666"
---
# <a name="cim_collectionofsensors-class"></a><span data-ttu-id="d1caa-103">\_Clase CollectionOfSensors de CIM</span><span class="sxs-lookup"><span data-stu-id="d1caa-103">CIM\_CollectionOfSensors class</span></span>

<span data-ttu-id="d1caa-104">La **Asociación \_ CollectionOfSensors de CIM** representa los sensores binarios que componen el sensor de múltiples Estados.</span><span class="sxs-lookup"><span data-stu-id="d1caa-104">The **CIM\_CollectionOfSensors** association represents the binary sensors that make up the multistate sensor.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d1caa-105">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="d1caa-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="d1caa-106">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="d1caa-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="d1caa-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="d1caa-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="d1caa-108">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="d1caa-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="d1caa-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d1caa-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{A2ABF536-DB35-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_CollectionOfSensors : CIM_Component
{
  CIM_BinarySensor     REF PartComponent;
  CIM_MultiStateSensor REF GroupComponent;
};
```

## <a name="members"></a><span data-ttu-id="d1caa-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="d1caa-110">Members</span></span>

<span data-ttu-id="d1caa-111">La clase **CIM \_ CollectionOfSensors** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="d1caa-111">The **CIM\_CollectionOfSensors** class has these types of members:</span></span>

-   [<span data-ttu-id="d1caa-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d1caa-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d1caa-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d1caa-113">Properties</span></span>

<span data-ttu-id="d1caa-114">La clase **CIM \_ CollectionOfSensors** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="d1caa-114">The **CIM\_CollectionOfSensors** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d1caa-115">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="d1caa-115">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1caa-116">Tipo de datos: **CIM \_ MultiStateSensor**</span><span class="sxs-lookup"><span data-stu-id="d1caa-116">Data type: **CIM\_MultiStateSensor**</span></span>
</dt> <dt>

<span data-ttu-id="d1caa-117">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d1caa-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1caa-118">Calificadores: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span><span class="sxs-lookup"><span data-stu-id="d1caa-118">Qualifiers: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span></span>
</dt> </dl>

<span data-ttu-id="d1caa-119">Un [**\_ MultiStateSensor de CIM**](cim-multistatesensor.md) que describe el sensor de varios Estados.</span><span class="sxs-lookup"><span data-stu-id="d1caa-119">A [**CIM\_MultiStateSensor**](cim-multistatesensor.md) that describes the multi-state sensor.</span></span>

</dd> <dt>

<span data-ttu-id="d1caa-120">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="d1caa-120">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1caa-121">Tipo de datos: **CIM \_ BinarySensor**</span><span class="sxs-lookup"><span data-stu-id="d1caa-121">Data type: **CIM\_BinarySensor**</span></span>
</dt> <dt>

<span data-ttu-id="d1caa-122">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d1caa-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1caa-123">Calificadores: [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (2), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="d1caa-123">Qualifiers: [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (2), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="d1caa-124">Un [**\_ BinarySensor de CIM**](cim-binarysensor.md) que describe un sensor binario que forma parte del sensor de varios Estados.</span><span class="sxs-lookup"><span data-stu-id="d1caa-124">A [**CIM\_BinarySensor**](cim-binarysensor.md) that describes a binary sensor that is part of the multi-state sensor.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d1caa-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d1caa-125">Remarks</span></span>

<span data-ttu-id="d1caa-126">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="d1caa-126">WMI does not implement this class.</span></span>

<span data-ttu-id="d1caa-127">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="d1caa-127">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="d1caa-128">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="d1caa-128">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="d1caa-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d1caa-129">Requirements</span></span>



| <span data-ttu-id="d1caa-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="d1caa-130">Requirement</span></span> | <span data-ttu-id="d1caa-131">Value</span><span class="sxs-lookup"><span data-stu-id="d1caa-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d1caa-132">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d1caa-132">Minimum supported client</span></span><br/> | <span data-ttu-id="d1caa-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d1caa-133">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d1caa-134">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d1caa-134">Minimum supported server</span></span><br/> | <span data-ttu-id="d1caa-135">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d1caa-135">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d1caa-136">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="d1caa-136">Namespace</span></span><br/>                | <span data-ttu-id="d1caa-137">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="d1caa-137">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="d1caa-138">MOF</span><span class="sxs-lookup"><span data-stu-id="d1caa-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d1caa-139"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d1caa-139"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="d1caa-140">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d1caa-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d1caa-141"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d1caa-141"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d1caa-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="d1caa-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1caa-143">**\_Componente CIM**</span><span class="sxs-lookup"><span data-stu-id="d1caa-143">**CIM\_Component**</span></span>](cim-component.md)
</dt> </dl>

 

