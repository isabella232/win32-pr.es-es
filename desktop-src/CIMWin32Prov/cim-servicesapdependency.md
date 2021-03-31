---
description: La \_ clase CIM ServiceSAPDependency representa una asociación entre un servicio y un punto de acceso de servicio (SAP), que indica que el servicio utiliza el SAP al que se hace referencia para proporcionar su funcionalidad.
ms.assetid: cf5a8b9b-a38e-4173-861c-e417fbea6016
ms.tgt_platform: multiple
title: CIM_ServiceSAPDependency (clase) (proveedores WMI de CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ServiceSAPDependency
- CIM_ServiceSAPDependency.Dependent
- CIM_ServiceSAPDependency.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: e47283c962b377b70bc14efe998752d9009796df
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153050"
---
# <a name="cim_servicesapdependency-class-cimwin32-wmi-providers"></a><span data-ttu-id="091dc-103">CIM_ServiceSAPDependency (clase) (proveedores WMI de CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="091dc-103">CIM_ServiceSAPDependency class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="091dc-104">La clase **CIM \_ ServiceSAPDependency** representa una asociación entre un servicio y un punto de acceso de servicio (SAP), que indica que el servicio utiliza el SAP al que se hace referencia para proporcionar su funcionalidad.</span><span class="sxs-lookup"><span data-stu-id="091dc-104">The **CIM\_ServiceSAPDependency** class represents an association between a service and a service access point (SAP), which indicates that the referenced SAP is used by the service to provide its functionality.</span></span> <span data-ttu-id="091dc-105">Por ejemplo, los servicios de arranque pueden invocar los servicios de disco BIOS (interrupciones) para que funcionen.</span><span class="sxs-lookup"><span data-stu-id="091dc-105">For example, boot services can invoke BIOS disk services (interrupts) to function.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="091dc-106">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="091dc-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="091dc-107">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="091dc-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="091dc-108">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="091dc-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="091dc-109">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="091dc-109">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="091dc-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="091dc-110">Syntax</span></span>

``` syntax
[UUID("{652E2D58-DB37-11d2-85FC-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_ServiceSAPDependency : CIM_Dependency
{
  CIM_Service            REF Dependent;
  CIM_ServiceAccessPoint REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="091dc-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="091dc-111">Members</span></span>

<span data-ttu-id="091dc-112">La clase **CIM \_ ServiceSAPDependency** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="091dc-112">The **CIM\_ServiceSAPDependency** class has these types of members:</span></span>

-   [<span data-ttu-id="091dc-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="091dc-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="091dc-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="091dc-114">Properties</span></span>

<span data-ttu-id="091dc-115">La clase **CIM \_ ServiceSAPDependency** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="091dc-115">The **CIM\_ServiceSAPDependency** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="091dc-116">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="091dc-116">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="091dc-117">Tipo de datos: **CIM \_ punto**</span><span class="sxs-lookup"><span data-stu-id="091dc-117">Data type: **CIM\_ServiceAccessPoint**</span></span>
</dt> <dt>

<span data-ttu-id="091dc-118">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="091dc-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="091dc-119">Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente")</span><span class="sxs-lookup"><span data-stu-id="091dc-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="091dc-120">Un [**\_ punto de CIM**](cim-serviceaccesspoint.md) que describe el punto de acceso al servicio requerido.</span><span class="sxs-lookup"><span data-stu-id="091dc-120">A [**CIM\_ServiceAccessPoint**](cim-serviceaccesspoint.md) that describes the required service access point.</span></span>

</dd> <dt>

<span data-ttu-id="091dc-121">**Dependientes**</span><span class="sxs-lookup"><span data-stu-id="091dc-121">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="091dc-122">Tipo de datos **: \_ servicio CIM**</span><span class="sxs-lookup"><span data-stu-id="091dc-122">Data type: **CIM\_Service**</span></span>
</dt> <dt>

<span data-ttu-id="091dc-123">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="091dc-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="091dc-124">Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependiente")</span><span class="sxs-lookup"><span data-stu-id="091dc-124">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="091dc-125">Un [**\_ servicio CIM**](cim-service.md) que describe el servicio que depende de un SAP subyacente.</span><span class="sxs-lookup"><span data-stu-id="091dc-125">A [**CIM\_Service**](cim-service.md) that describes the service that is dependent on an underlying SAP.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="091dc-126">Observaciones</span><span class="sxs-lookup"><span data-stu-id="091dc-126">Remarks</span></span>

<span data-ttu-id="091dc-127">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="091dc-127">WMI does not implement this class.</span></span>

<span data-ttu-id="091dc-128">La clase **CIM \_ ServiceSAPDependency** se deriva de [**la \_ dependencia CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="091dc-128">The **CIM\_ServiceSAPDependency** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="091dc-129">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="091dc-129">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="091dc-130">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="091dc-130">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="091dc-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="091dc-131">Requirements</span></span>



| <span data-ttu-id="091dc-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="091dc-132">Requirement</span></span> | <span data-ttu-id="091dc-133">Value</span><span class="sxs-lookup"><span data-stu-id="091dc-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="091dc-134">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="091dc-134">Minimum supported client</span></span><br/> | <span data-ttu-id="091dc-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="091dc-135">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="091dc-136">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="091dc-136">Minimum supported server</span></span><br/> | <span data-ttu-id="091dc-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="091dc-137">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="091dc-138">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="091dc-138">Namespace</span></span><br/>                | <span data-ttu-id="091dc-139">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="091dc-139">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="091dc-140">MOF</span><span class="sxs-lookup"><span data-stu-id="091dc-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="091dc-141"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="091dc-141"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="091dc-142">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="091dc-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="091dc-143"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="091dc-143"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="091dc-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="091dc-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="091dc-145">**Dependencia de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="091dc-145">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

