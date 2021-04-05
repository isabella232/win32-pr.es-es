---
description: La \_ clase de asociación CIM ServiceAccessBySAP representa los puntos de acceso de un servicio. Por ejemplo, se puede tener acceso a una impresora a través de los puntos de acceso de servicio (SAP, Macintosh o Windows), que pueden hospedarse en sistemas diferentes.
ms.assetid: 68311a56-b034-4a30-a885-74a745a738d8
ms.tgt_platform: multiple
title: CIM_ServiceAccessBySAP (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ServiceAccessBySAP
- CIM_ServiceAccessBySAP.Dependent
- CIM_ServiceAccessBySAP.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: e34b2af50a6475461ae4d39d156d26143fcb75f5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104000556"
---
# <a name="cim_serviceaccessbysap-class"></a><span data-ttu-id="9803f-104">\_Clase ServiceAccessBySAP de CIM</span><span class="sxs-lookup"><span data-stu-id="9803f-104">CIM\_ServiceAccessBySAP class</span></span>

<span data-ttu-id="9803f-105">La clase de asociación **CIM \_ ServiceAccessBySAP** representa los puntos de acceso de un servicio.</span><span class="sxs-lookup"><span data-stu-id="9803f-105">The **CIM\_ServiceAccessBySAP** association class represents the access points for a service.</span></span> <span data-ttu-id="9803f-106">Por ejemplo, se puede tener acceso a una impresora a través de los puntos de acceso de servicio (SAP, Macintosh o Windows), que pueden hospedarse en sistemas diferentes.</span><span class="sxs-lookup"><span data-stu-id="9803f-106">For example, a printer can be accessed by NetWare, Macintosh, or Windows service access points (SAPs), which are potentially hosted on different systems.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="9803f-107">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="9803f-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="9803f-108">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="9803f-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="9803f-109">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="9803f-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="9803f-110">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="9803f-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="9803f-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9803f-111">Syntax</span></span>

``` syntax
[UUID("{714C00BA-DB37-11d2-85FC-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_ServiceAccessBySAP : CIM_Dependency
{
  CIM_ServiceAccessPoint REF Dependent;
  CIM_Service            REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="9803f-112">Miembros</span><span class="sxs-lookup"><span data-stu-id="9803f-112">Members</span></span>

<span data-ttu-id="9803f-113">La clase **CIM \_ ServiceAccessBySAP** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="9803f-113">The **CIM\_ServiceAccessBySAP** class has these types of members:</span></span>

-   [<span data-ttu-id="9803f-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="9803f-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9803f-115">Propiedades</span><span class="sxs-lookup"><span data-stu-id="9803f-115">Properties</span></span>

<span data-ttu-id="9803f-116">La clase **CIM \_ ServiceAccessBySAP** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="9803f-116">The **CIM\_ServiceAccessBySAP** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9803f-117">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="9803f-117">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9803f-118">Tipo de datos **: \_ servicio CIM**</span><span class="sxs-lookup"><span data-stu-id="9803f-118">Data type: **CIM\_Service**</span></span>
</dt> <dt>

<span data-ttu-id="9803f-119">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9803f-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9803f-120">Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente")</span><span class="sxs-lookup"><span data-stu-id="9803f-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="9803f-121">Un [**\_ servicio CIM**](cim-service.md) que describe el servicio.</span><span class="sxs-lookup"><span data-stu-id="9803f-121">A [**CIM\_Service**](cim-service.md) that describes the service.</span></span>

</dd> <dt>

<span data-ttu-id="9803f-122">**Dependientes**</span><span class="sxs-lookup"><span data-stu-id="9803f-122">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9803f-123">Tipo de datos: **CIM \_ punto**</span><span class="sxs-lookup"><span data-stu-id="9803f-123">Data type: **CIM\_ServiceAccessPoint**</span></span>
</dt> <dt>

<span data-ttu-id="9803f-124">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9803f-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9803f-125">Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependiente")</span><span class="sxs-lookup"><span data-stu-id="9803f-125">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="9803f-126">Un [**\_ punto de CIM**](cim-serviceaccesspoint.md) que describe un punto de acceso para un servicio.</span><span class="sxs-lookup"><span data-stu-id="9803f-126">A [**CIM\_ServiceAccessPoint**](cim-serviceaccesspoint.md) that describes an access point for a service.</span></span> <span data-ttu-id="9803f-127">Los puntos de acceso dependen de esta relación, ya que no tienen ninguna función sin un servicio correspondiente.</span><span class="sxs-lookup"><span data-stu-id="9803f-127">Access points are dependent in this relationship since they have no function without a corresponding service.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9803f-128">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9803f-128">Remarks</span></span>

<span data-ttu-id="9803f-129">La clase **CIM \_ ServiceAccessBySAP** se deriva de [**la \_ dependencia CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="9803f-129">The **CIM\_ServiceAccessBySAP** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="9803f-130">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="9803f-130">WMI does not implement this class.</span></span> <span data-ttu-id="9803f-131">Para las clases WMI que se derivan de **\_ ServiceAccessBySAP CIM**, vea [clases Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="9803f-131">For WMI classes that are derived from **CIM\_ServiceAccessBySAP**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="9803f-132">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="9803f-132">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="9803f-133">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="9803f-133">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="9803f-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9803f-134">Requirements</span></span>



| <span data-ttu-id="9803f-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="9803f-135">Requirement</span></span> | <span data-ttu-id="9803f-136">Value</span><span class="sxs-lookup"><span data-stu-id="9803f-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9803f-137">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9803f-137">Minimum supported client</span></span><br/> | <span data-ttu-id="9803f-138">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9803f-138">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="9803f-139">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9803f-139">Minimum supported server</span></span><br/> | <span data-ttu-id="9803f-140">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9803f-140">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="9803f-141">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="9803f-141">Namespace</span></span><br/>                | <span data-ttu-id="9803f-142">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="9803f-142">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="9803f-143">MOF</span><span class="sxs-lookup"><span data-stu-id="9803f-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9803f-144"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9803f-144"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="9803f-145">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="9803f-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9803f-146"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9803f-146"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9803f-147">Vea también</span><span class="sxs-lookup"><span data-stu-id="9803f-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9803f-148">**Dependencia de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="9803f-148">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

