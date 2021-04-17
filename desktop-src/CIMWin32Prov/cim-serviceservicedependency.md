---
description: La \_ clase CIM ServiceServiceDependency representa una asociación entre dos servicios.
ms.assetid: 0fb43fb3-2c05-4762-b339-2dcc090ed38d
ms.tgt_platform: multiple
title: CIM_ServiceServiceDependency (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ServiceServiceDependency
- CIM_ServiceServiceDependency.Dependent
- CIM_ServiceServiceDependency.Antecedent
- CIM_ServiceServiceDependency.TypeOfDependency
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: fdc8ea1a3324395e5230ca6d47487b61c8c02ba9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659510"
---
# <a name="cim_serviceservicedependency-class"></a><span data-ttu-id="0fec5-103">\_Clase ServiceServiceDependency de CIM</span><span class="sxs-lookup"><span data-stu-id="0fec5-103">CIM\_ServiceServiceDependency class</span></span>

<span data-ttu-id="0fec5-104">La clase **CIM \_ ServiceServiceDependency** representa una asociación entre dos servicios.</span><span class="sxs-lookup"><span data-stu-id="0fec5-104">The **CIM\_ServiceServiceDependency** class represents an association between two services.</span></span> <span data-ttu-id="0fec5-105">El servicio asociado debe estar presente, debe haberse completado o debe estar ausente para que el otro servicio funcione.</span><span class="sxs-lookup"><span data-stu-id="0fec5-105">The associated service must be present, must have completed, or must be absent for the other service to function.</span></span> <span data-ttu-id="0fec5-106">Por ejemplo, los servicios de arranque pueden depender del BIOS, el disco y los servicios de inicialización subyacentes.</span><span class="sxs-lookup"><span data-stu-id="0fec5-106">For example, boot services can be dependent on underlying BIOS, disk, and initialization services.</span></span> <span data-ttu-id="0fec5-107">En el caso de los servicios de inicialización, el servicio de arranque depende de la finalización de los servicios de inicialización.</span><span class="sxs-lookup"><span data-stu-id="0fec5-107">For initialization services, the boot service is dependent on the initialization services completing.</span></span> <span data-ttu-id="0fec5-108">En el caso de los servicios de disco, los servicios de arranque pueden utilizar realmente los SAP de este servicio.</span><span class="sxs-lookup"><span data-stu-id="0fec5-108">For disk services, boot services can actually use the SAPs of this service.</span></span> <span data-ttu-id="0fec5-109">Esta dependencia de uso se modela en la [**Asociación \_ ServiceSAPDependency de CIM**](cim-servicesapdependency.md) .</span><span class="sxs-lookup"><span data-stu-id="0fec5-109">This usage dependency is modeled on the [**CIM\_ServiceSAPDependency**](cim-servicesapdependency.md) association.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0fec5-110">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="0fec5-110">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="0fec5-111">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="0fec5-111">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="0fec5-112">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="0fec5-112">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="0fec5-113">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="0fec5-113">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="0fec5-114">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0fec5-114">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C53B-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_ServiceServiceDependency : CIM_Dependency
{
  CIM_Service REF Dependent;
  CIM_Service REF Antecedent;
  uint16          TypeOfDependency;
};
```

## <a name="members"></a><span data-ttu-id="0fec5-115">Miembros</span><span class="sxs-lookup"><span data-stu-id="0fec5-115">Members</span></span>

<span data-ttu-id="0fec5-116">La clase **CIM \_ ServiceServiceDependency** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="0fec5-116">The **CIM\_ServiceServiceDependency** class has these types of members:</span></span>

-   [<span data-ttu-id="0fec5-117">Propiedades</span><span class="sxs-lookup"><span data-stu-id="0fec5-117">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0fec5-118">Propiedades</span><span class="sxs-lookup"><span data-stu-id="0fec5-118">Properties</span></span>

<span data-ttu-id="0fec5-119">La clase **CIM \_ ServiceServiceDependency** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="0fec5-119">The **CIM\_ServiceServiceDependency** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0fec5-120">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="0fec5-120">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0fec5-121">Tipo de datos **: \_ servicio CIM**</span><span class="sxs-lookup"><span data-stu-id="0fec5-121">Data type: **CIM\_Service**</span></span>
</dt> <dt>

<span data-ttu-id="0fec5-122">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0fec5-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0fec5-123">Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente")</span><span class="sxs-lookup"><span data-stu-id="0fec5-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="0fec5-124">Un [**\_ servicio CIM**](cim-service.md) que describe el servicio requerido.</span><span class="sxs-lookup"><span data-stu-id="0fec5-124">A [**CIM\_Service**](cim-service.md) that describes the required service.</span></span>

</dd> <dt>

<span data-ttu-id="0fec5-125">**Dependientes**</span><span class="sxs-lookup"><span data-stu-id="0fec5-125">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0fec5-126">Tipo de datos **: \_ servicio CIM**</span><span class="sxs-lookup"><span data-stu-id="0fec5-126">Data type: **CIM\_Service**</span></span>
</dt> <dt>

<span data-ttu-id="0fec5-127">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0fec5-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0fec5-128">Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependiente")</span><span class="sxs-lookup"><span data-stu-id="0fec5-128">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="0fec5-129">[**\_ Servicio CIM**](cim-service.md) que describe el servicio que depende de un servicio subyacente.</span><span class="sxs-lookup"><span data-stu-id="0fec5-129">A [**CIM\_Service**](cim-service.md) that describes the service that is dependent on an underlying service.</span></span>

</dd> <dt>

<span data-ttu-id="0fec5-130">**TypeOfDependency**</span><span class="sxs-lookup"><span data-stu-id="0fec5-130">**TypeOfDependency**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0fec5-131">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0fec5-131">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0fec5-132">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0fec5-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0fec5-133">Naturaleza de la dependencia entre servicios.</span><span class="sxs-lookup"><span data-stu-id="0fec5-133">Nature of the service-to-service dependency.</span></span> <span data-ttu-id="0fec5-134">Esta propiedad indica que el servicio asociado debe haber finalizado, debe iniciarse o no debe iniciarse para que el servicio funcione.</span><span class="sxs-lookup"><span data-stu-id="0fec5-134">This property indicates that the associated service must have completed, must be started, or must not be started for the service to function.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="0fec5-135"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="0fec5-135"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="0fec5-136"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="0fec5-136"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Service_Must_Have_Completed"></span><span id="service_must_have_completed"></span><span id="SERVICE_MUST_HAVE_COMPLETED"></span>

<span data-ttu-id="0fec5-137"><span id="Service_Must_Have_Completed"></span><span id="service_must_have_completed"></span><span id="SERVICE_MUST_HAVE_COMPLETED"></span>El **servicio debe haberse completado** (2)</span><span class="sxs-lookup"><span data-stu-id="0fec5-137"><span id="Service_Must_Have_Completed"></span><span id="service_must_have_completed"></span><span id="SERVICE_MUST_HAVE_COMPLETED"></span>**Service Must Have Completed** (2)</span></span>


</dt> <dd>

<span data-ttu-id="0fec5-138">El servicio debe haberse completado.</span><span class="sxs-lookup"><span data-stu-id="0fec5-138">Service must have completed.</span></span>

</dd> <dt>

<span id="Service_Must_Be_Started"></span><span id="service_must_be_started"></span><span id="SERVICE_MUST_BE_STARTED"></span>

<span data-ttu-id="0fec5-139"><span id="Service_Must_Be_Started"></span><span id="service_must_be_started"></span><span id="SERVICE_MUST_BE_STARTED"></span>El **servicio debe iniciarse** (3)</span><span class="sxs-lookup"><span data-stu-id="0fec5-139"><span id="Service_Must_Be_Started"></span><span id="service_must_be_started"></span><span id="SERVICE_MUST_BE_STARTED"></span>**Service Must Be Started** (3)</span></span>


</dt> <dd>

<span data-ttu-id="0fec5-140">Debe iniciarse el servicio.</span><span class="sxs-lookup"><span data-stu-id="0fec5-140">Service must be started.</span></span>

</dd> <dt>

<span id="Service_Must_Not_Be_Started"></span><span id="service_must_not_be_started"></span><span id="SERVICE_MUST_NOT_BE_STARTED"></span>

<span data-ttu-id="0fec5-141"><span id="Service_Must_Not_Be_Started"></span><span id="service_must_not_be_started"></span><span id="SERVICE_MUST_NOT_BE_STARTED"></span>**No se debe iniciar el servicio** (4)</span><span class="sxs-lookup"><span data-stu-id="0fec5-141"><span id="Service_Must_Not_Be_Started"></span><span id="service_must_not_be_started"></span><span id="SERVICE_MUST_NOT_BE_STARTED"></span>**Service Must Not Be Started** (4)</span></span>


</dt> <dd>

<span data-ttu-id="0fec5-142">No se debe iniciar el servicio.</span><span class="sxs-lookup"><span data-stu-id="0fec5-142">Service must not be started.</span></span>

</dd> </dl>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0fec5-143">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0fec5-143">Remarks</span></span>

<span data-ttu-id="0fec5-144">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="0fec5-144">WMI does not implement this class.</span></span> <span data-ttu-id="0fec5-145">Para las clases WMI derivadas de **CIM \_ ServiceServiceDependency**, vea [clases Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="0fec5-145">For WMI classes derived from **CIM\_ServiceServiceDependency**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="0fec5-146">La clase **CIM \_ ServiceServiceDependency** se deriva de [**la \_ dependencia CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="0fec5-146">The **CIM\_ServiceServiceDependency** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="0fec5-147">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="0fec5-147">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="0fec5-148">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="0fec5-148">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="0fec5-149">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0fec5-149">Requirements</span></span>



| <span data-ttu-id="0fec5-150">Requisito</span><span class="sxs-lookup"><span data-stu-id="0fec5-150">Requirement</span></span> | <span data-ttu-id="0fec5-151">Value</span><span class="sxs-lookup"><span data-stu-id="0fec5-151">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0fec5-152">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0fec5-152">Minimum supported client</span></span><br/> | <span data-ttu-id="0fec5-153">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0fec5-153">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="0fec5-154">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0fec5-154">Minimum supported server</span></span><br/> | <span data-ttu-id="0fec5-155">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0fec5-155">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="0fec5-156">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="0fec5-156">Namespace</span></span><br/>                | <span data-ttu-id="0fec5-157">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="0fec5-157">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="0fec5-158">MOF</span><span class="sxs-lookup"><span data-stu-id="0fec5-158">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0fec5-159"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0fec5-159"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="0fec5-160">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="0fec5-160">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0fec5-161"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0fec5-161"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0fec5-162">Vea también</span><span class="sxs-lookup"><span data-stu-id="0fec5-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0fec5-163">**Dependencia de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="0fec5-163">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

