---
description: La \_ clase CIM DeviceServiceImplementation representa una asociación entre un servicio y cómo se implementa.
ms.assetid: 5e2e3975-8338-4bf4-8c73-5be4b93fa2c8
ms.tgt_platform: multiple
title: CIM_DeviceServiceImplementation (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DeviceServiceImplementation
- CIM_DeviceServiceImplementation.Dependent
- CIM_DeviceServiceImplementation.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: ae96d94c95ddda684dbb4d17a2d8eb52fc6ffd4b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104000691"
---
# <a name="cim_deviceserviceimplementation-class"></a><span data-ttu-id="d33fd-103">\_Clase DeviceServiceImplementation de CIM</span><span class="sxs-lookup"><span data-stu-id="d33fd-103">CIM\_DeviceServiceImplementation class</span></span>

<span data-ttu-id="d33fd-104">La clase **CIM \_ DeviceServiceImplementation** representa una asociación entre un servicio y cómo se implementa.</span><span class="sxs-lookup"><span data-stu-id="d33fd-104">The **CIM\_DeviceServiceImplementation** class represents an association between a service and how it is implemented.</span></span> <span data-ttu-id="d33fd-105">Cuando hay varios dispositivos asociados a un servicio, los elementos funcionan conjuntamente para proporcionar el servicio.</span><span class="sxs-lookup"><span data-stu-id="d33fd-105">When multiple devices are associated with one service, the elements operate in conjunction to provide the service.</span></span> <span data-ttu-id="d33fd-106">Si existen implementaciones diferentes de un servicio, cada implementación tiene como resultado la creación de instancias individuales del objeto de servicio.</span><span class="sxs-lookup"><span data-stu-id="d33fd-106">If different implementations of a service exist, each implementation results in individual instantiations of the service object.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d33fd-107">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="d33fd-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="d33fd-108">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="d33fd-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="d33fd-109">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="d33fd-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="d33fd-110">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="d33fd-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="d33fd-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d33fd-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{290FC242-DB36-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_DeviceServiceImplementation : CIM_Dependency
{
  CIM_Service       REF Dependent;
  CIM_LogicalDevice REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="d33fd-112">Miembros</span><span class="sxs-lookup"><span data-stu-id="d33fd-112">Members</span></span>

<span data-ttu-id="d33fd-113">La clase **CIM \_ DeviceServiceImplementation** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="d33fd-113">The **CIM\_DeviceServiceImplementation** class has these types of members:</span></span>

-   [<span data-ttu-id="d33fd-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d33fd-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d33fd-115">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d33fd-115">Properties</span></span>

<span data-ttu-id="d33fd-116">La clase **CIM \_ DeviceServiceImplementation** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="d33fd-116">The **CIM\_DeviceServiceImplementation** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d33fd-117">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="d33fd-117">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d33fd-118">Tipo de datos **: \_ LogicalDevice de CIM**</span><span class="sxs-lookup"><span data-stu-id="d33fd-118">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="d33fd-119">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d33fd-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d33fd-120">Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente")</span><span class="sxs-lookup"><span data-stu-id="d33fd-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="d33fd-121">Un [**\_ LogicalDevice de CIM**](cim-logicaldevice.md) que describe el dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="d33fd-121">A [**CIM\_LogicalDevice**](cim-logicaldevice.md) that describes the logical device.</span></span>

</dd> <dt>

<span data-ttu-id="d33fd-122">**Dependientes**</span><span class="sxs-lookup"><span data-stu-id="d33fd-122">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d33fd-123">Tipo de datos **: \_ servicio CIM**</span><span class="sxs-lookup"><span data-stu-id="d33fd-123">Data type: **CIM\_Service**</span></span>
</dt> <dt>

<span data-ttu-id="d33fd-124">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d33fd-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d33fd-125">Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependiente")</span><span class="sxs-lookup"><span data-stu-id="d33fd-125">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="d33fd-126">Un [**\_ servicio CIM**](cim-service.md) que describe el servicio implementado mediante el dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="d33fd-126">A [**CIM\_Service**](cim-service.md) that describes the service implemented using the logical device.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d33fd-127">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d33fd-127">Remarks</span></span>

<span data-ttu-id="d33fd-128">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="d33fd-128">WMI does not implement this class.</span></span>

<span data-ttu-id="d33fd-129">La clase **CIM \_ DeviceServiceImplementation** se deriva de [**la \_ dependencia CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="d33fd-129">The **CIM\_DeviceServiceImplementation** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="d33fd-130">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="d33fd-130">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="d33fd-131">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="d33fd-131">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="d33fd-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d33fd-132">Requirements</span></span>



| <span data-ttu-id="d33fd-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="d33fd-133">Requirement</span></span> | <span data-ttu-id="d33fd-134">Value</span><span class="sxs-lookup"><span data-stu-id="d33fd-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d33fd-135">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d33fd-135">Minimum supported client</span></span><br/> | <span data-ttu-id="d33fd-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d33fd-136">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d33fd-137">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d33fd-137">Minimum supported server</span></span><br/> | <span data-ttu-id="d33fd-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d33fd-138">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d33fd-139">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="d33fd-139">Namespace</span></span><br/>                | <span data-ttu-id="d33fd-140">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="d33fd-140">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="d33fd-141">MOF</span><span class="sxs-lookup"><span data-stu-id="d33fd-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d33fd-142"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d33fd-142"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="d33fd-143">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d33fd-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d33fd-144"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d33fd-144"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d33fd-145">Vea también</span><span class="sxs-lookup"><span data-stu-id="d33fd-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d33fd-146">**Dependencia de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="d33fd-146">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

