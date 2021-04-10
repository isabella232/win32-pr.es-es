---
description: La \_ clase SAPSAPDependency de CIM es una asociación entre dos puntos de acceso de servicio (SAP), que indica que el segundo SAP es necesario para que el primer SAP se conecte con su servicio.
ms.assetid: ba5f47d9-ebe5-4dcb-8a6d-0974acf67385
ms.tgt_platform: multiple
title: CIM_SAPSAPDependency (clase) (proveedores WMI de CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SAPSAPDependency
- CIM_SAPSAPDependency.Dependent
- CIM_SAPSAPDependency.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b75cb397120ac2d4af041187f38f826e6b56be11
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103998194"
---
# <a name="cim_sapsapdependency-class-cimwin32-wmi-providers"></a><span data-ttu-id="85733-103">CIM_SAPSAPDependency (clase) (proveedores WMI de CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="85733-103">CIM_SAPSAPDependency class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="85733-104">La **clase \_ SAPSAPDependency de CIM** es una asociación entre dos puntos de acceso de servicio (SAP), que indica que el segundo SAP es necesario para que el primer SAP se conecte con su servicio.</span><span class="sxs-lookup"><span data-stu-id="85733-104">The **CIM\_SAPSAPDependency** class is an association between two service access points (SAPs), which indicates that the second SAP is required for the first SAP to connect with its service.</span></span> <span data-ttu-id="85733-105">Por ejemplo, para imprimir en una impresora de red, los puntos de acceso de la impresora local deben usar SAP relacionado con la red subyacente, o extremos de protocolo, para enviar la solicitud de impresión.</span><span class="sxs-lookup"><span data-stu-id="85733-105">For example, to print on a network printer, local printer access points must use underlying network-related SAPs, or protocol endpoints, to send the print request.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="85733-106">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="85733-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="85733-107">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="85733-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="85733-108">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="85733-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="85733-109">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="85733-109">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="85733-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="85733-110">Syntax</span></span>

``` syntax
[UUID("{422D175A-E3D5-11d2-8601-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_SAPSAPDependency : CIM_Dependency
{
  CIM_ServiceAccessPoint REF Dependent;
  CIM_ServiceAccessPoint REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="85733-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="85733-111">Members</span></span>

<span data-ttu-id="85733-112">La clase **CIM \_ SAPSAPDependency** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="85733-112">The **CIM\_SAPSAPDependency** class has these types of members:</span></span>

-   [<span data-ttu-id="85733-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="85733-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="85733-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="85733-114">Properties</span></span>

<span data-ttu-id="85733-115">La clase **CIM \_ SAPSAPDependency** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="85733-115">The **CIM\_SAPSAPDependency** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="85733-116">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="85733-116">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85733-117">Tipo de datos: **CIM \_ punto**</span><span class="sxs-lookup"><span data-stu-id="85733-117">Data type: **CIM\_ServiceAccessPoint**</span></span>
</dt> <dt>

<span data-ttu-id="85733-118">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="85733-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="85733-119">Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente")</span><span class="sxs-lookup"><span data-stu-id="85733-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="85733-120">Un [**\_ punto de CIM**](cim-serviceaccesspoint.md) que describe el punto de acceso al servicio requerido.</span><span class="sxs-lookup"><span data-stu-id="85733-120">A [**CIM\_ServiceAccessPoint**](cim-serviceaccesspoint.md) that describes the required service access point.</span></span>

</dd> <dt>

<span data-ttu-id="85733-121">**Dependientes**</span><span class="sxs-lookup"><span data-stu-id="85733-121">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="85733-122">Tipo de datos: **CIM \_ punto**</span><span class="sxs-lookup"><span data-stu-id="85733-122">Data type: **CIM\_ServiceAccessPoint**</span></span>
</dt> <dt>

<span data-ttu-id="85733-123">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="85733-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="85733-124">Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependiente")</span><span class="sxs-lookup"><span data-stu-id="85733-124">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="85733-125">Un [**\_ punto de CIM**](cim-serviceaccesspoint.md) que describe el punto de acceso al servicio que depende de un SAP subyacente.</span><span class="sxs-lookup"><span data-stu-id="85733-125">A [**CIM\_ServiceAccessPoint**](cim-serviceaccesspoint.md) that describes the service access point that is dependent on an underlying SAP.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="85733-126">Observaciones</span><span class="sxs-lookup"><span data-stu-id="85733-126">Remarks</span></span>

<span data-ttu-id="85733-127">La clase **CIM \_ SAPSAPDependency** se deriva de [**la \_ dependencia CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="85733-127">The **CIM\_SAPSAPDependency** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="85733-128">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="85733-128">WMI does not implement this class.</span></span>

<span data-ttu-id="85733-129">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="85733-129">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="85733-130">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="85733-130">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="85733-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="85733-131">Requirements</span></span>



| <span data-ttu-id="85733-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="85733-132">Requirement</span></span> | <span data-ttu-id="85733-133">Value</span><span class="sxs-lookup"><span data-stu-id="85733-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="85733-134">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="85733-134">Minimum supported client</span></span><br/> | <span data-ttu-id="85733-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="85733-135">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="85733-136">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="85733-136">Minimum supported server</span></span><br/> | <span data-ttu-id="85733-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="85733-137">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="85733-138">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="85733-138">Namespace</span></span><br/>                | <span data-ttu-id="85733-139">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="85733-139">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="85733-140">MOF</span><span class="sxs-lookup"><span data-stu-id="85733-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="85733-141"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="85733-141"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="85733-142">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="85733-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="85733-143"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="85733-143"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="85733-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="85733-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="85733-145">**Dependencia de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="85733-145">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

