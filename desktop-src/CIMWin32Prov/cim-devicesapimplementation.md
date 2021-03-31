---
description: La \_ clase CIM DeviceSAPImplementation representa una asociación entre un punto de acceso de servicio (SAP) y cómo se implementa.
ms.assetid: 6c059507-bfc0-4630-9b39-9c4bae2bf138
ms.tgt_platform: multiple
title: CIM_DeviceSAPImplementation (clase) (proveedores WMI de CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DeviceSAPImplementation
- CIM_DeviceSAPImplementation.Dependent
- CIM_DeviceSAPImplementation.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: eadc1e42427c06717c7b0d7a13aba8a2a71ccddb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807675"
---
# <a name="cim_devicesapimplementation-class-cimwin32-wmi-providers"></a><span data-ttu-id="7d912-103">CIM_DeviceSAPImplementation (clase) (proveedores WMI de CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="7d912-103">CIM_DeviceSAPImplementation class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="7d912-104">La clase **CIM \_ DeviceSAPImplementation** representa una asociación entre un punto de acceso de servicio (SAP) y cómo se implementa.</span><span class="sxs-lookup"><span data-stu-id="7d912-104">The **CIM\_DeviceSAPImplementation** class represents an association between a service access point (SAP) and how it is implemented.</span></span> <span data-ttu-id="7d912-105">Cuando muchos dispositivos lógicos están asociados a un SAP, los elementos funcionan conjuntamente para proporcionar el punto de acceso.</span><span class="sxs-lookup"><span data-stu-id="7d912-105">When many logical devices are associated with one SAP, the elements operate in conjunction to provide the access point.</span></span> <span data-ttu-id="7d912-106">Si existen implementaciones diferentes de un SAP, cada implementación da como resultado la creación de instancias individuales del objeto SAP.</span><span class="sxs-lookup"><span data-stu-id="7d912-106">If different implementations of a SAP exist, each implementation results in individual instantiations of the SAP object.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="7d912-107">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="7d912-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="7d912-108">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="7d912-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="7d912-109">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="7d912-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="7d912-110">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="7d912-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="7d912-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7d912-111">Syntax</span></span>

``` syntax
[UUID("{1BE949DA-DB36-11d2-85FC-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_DeviceSAPImplementation : CIM_Dependency
{
  CIM_ServiceAccessPoint REF Dependent;
  CIM_LogicalDevice      REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="7d912-112">Miembros</span><span class="sxs-lookup"><span data-stu-id="7d912-112">Members</span></span>

<span data-ttu-id="7d912-113">La clase **CIM \_ DeviceSAPImplementation** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="7d912-113">The **CIM\_DeviceSAPImplementation** class has these types of members:</span></span>

-   [<span data-ttu-id="7d912-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="7d912-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7d912-115">Propiedades</span><span class="sxs-lookup"><span data-stu-id="7d912-115">Properties</span></span>

<span data-ttu-id="7d912-116">La clase **CIM \_ DeviceSAPImplementation** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="7d912-116">The **CIM\_DeviceSAPImplementation** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7d912-117">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="7d912-117">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7d912-118">Tipo de datos **: \_ LogicalDevice de CIM**</span><span class="sxs-lookup"><span data-stu-id="7d912-118">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="7d912-119">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7d912-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7d912-120">Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente")</span><span class="sxs-lookup"><span data-stu-id="7d912-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="7d912-121">Un [**\_ LogicalDevice de CIM**](cim-logicaldevice.md) que describe el dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="7d912-121">A [**CIM\_LogicalDevice**](cim-logicaldevice.md) that describes the logical device.</span></span>

</dd> <dt>

<span data-ttu-id="7d912-122">**Dependientes**</span><span class="sxs-lookup"><span data-stu-id="7d912-122">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7d912-123">Tipo de datos: **CIM \_ punto**</span><span class="sxs-lookup"><span data-stu-id="7d912-123">Data type: **CIM\_ServiceAccessPoint**</span></span>
</dt> <dt>

<span data-ttu-id="7d912-124">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7d912-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7d912-125">Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependiente")</span><span class="sxs-lookup"><span data-stu-id="7d912-125">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="7d912-126">Un [**\_ punto de CIM**](cim-serviceaccesspoint.md) que describe el punto de acceso al servicio implementado mediante el dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="7d912-126">A [**CIM\_ServiceAccessPoint**](cim-serviceaccesspoint.md) that describes the service access point implemented using the logical device.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7d912-127">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7d912-127">Remarks</span></span>

<span data-ttu-id="7d912-128">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="7d912-128">WMI does not implement this class.</span></span>

<span data-ttu-id="7d912-129">La clase **CIM \_ DeviceSAPImplementation** se deriva de [**la \_ dependencia CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="7d912-129">The **CIM\_DeviceSAPImplementation** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="7d912-130">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="7d912-130">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="7d912-131">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="7d912-131">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="7d912-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7d912-132">Requirements</span></span>



| <span data-ttu-id="7d912-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="7d912-133">Requirement</span></span> | <span data-ttu-id="7d912-134">Value</span><span class="sxs-lookup"><span data-stu-id="7d912-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7d912-135">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7d912-135">Minimum supported client</span></span><br/> | <span data-ttu-id="7d912-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7d912-136">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="7d912-137">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7d912-137">Minimum supported server</span></span><br/> | <span data-ttu-id="7d912-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7d912-138">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="7d912-139">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="7d912-139">Namespace</span></span><br/>                | <span data-ttu-id="7d912-140">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="7d912-140">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="7d912-141">MOF</span><span class="sxs-lookup"><span data-stu-id="7d912-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7d912-142"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7d912-142"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="7d912-143">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="7d912-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7d912-144"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7d912-144"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7d912-145">Vea también</span><span class="sxs-lookup"><span data-stu-id="7d912-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7d912-146">**Dependencia de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="7d912-146">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

