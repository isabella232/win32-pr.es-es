---
description: La \_ clase BootServiceAccessBySAP de CIM asocia un servicio de arranque y sus puntos de acceso.
ms.assetid: 993469dd-fb9c-4d21-99e0-03c4b19eb7fd
ms.tgt_platform: multiple
title: CIM_BootServiceAccessBySAP (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_BootServiceAccessBySAP
- CIM_BootServiceAccessBySAP.Dependent
- CIM_BootServiceAccessBySAP.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 90548be52defbcf3419d6c7defc21395da5cfbfe
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807615"
---
# <a name="cim_bootserviceaccessbysap-class"></a><span data-ttu-id="180d2-103">\_Clase BootServiceAccessBySAP de CIM</span><span class="sxs-lookup"><span data-stu-id="180d2-103">CIM\_BootServiceAccessBySAP class</span></span>

<span data-ttu-id="180d2-104">La **clase \_ BootServiceAccessBySAP de CIM** asocia un servicio de arranque y sus puntos de acceso.</span><span class="sxs-lookup"><span data-stu-id="180d2-104">The **CIM\_BootServiceAccessBySAP** class associates a boot service and its access points.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="180d2-105">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="180d2-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="180d2-106">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="180d2-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="180d2-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="180d2-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="180d2-108">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="180d2-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="180d2-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="180d2-109">Syntax</span></span>

``` syntax
[UUID("{6EDF1DD2-DB35-11d2-85FC-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_BootServiceAccessBySAP : CIM_ServiceAccessBySAP
{
  CIM_BootSAP     REF Dependent;
  CIM_BootService REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="180d2-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="180d2-110">Members</span></span>

<span data-ttu-id="180d2-111">La clase **CIM \_ BootServiceAccessBySAP** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="180d2-111">The **CIM\_BootServiceAccessBySAP** class has these types of members:</span></span>

-   [<span data-ttu-id="180d2-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="180d2-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="180d2-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="180d2-113">Properties</span></span>

<span data-ttu-id="180d2-114">La clase **CIM \_ BootServiceAccessBySAP** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="180d2-114">The **CIM\_BootServiceAccessBySAP** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="180d2-115">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="180d2-115">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="180d2-116">Tipo de datos: **CIM \_ BootService**</span><span class="sxs-lookup"><span data-stu-id="180d2-116">Data type: **CIM\_BootService**</span></span>
</dt> <dt>

<span data-ttu-id="180d2-117">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="180d2-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="180d2-118">Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente")</span><span class="sxs-lookup"><span data-stu-id="180d2-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="180d2-119">Un [**\_ BootService de CIM**](cim-bootservice.md) que describe el servicio de arranque.</span><span class="sxs-lookup"><span data-stu-id="180d2-119">A [**CIM\_BootService**](cim-bootservice.md) that describes the boot service.</span></span>

</dd> <dt>

<span data-ttu-id="180d2-120">**Dependientes**</span><span class="sxs-lookup"><span data-stu-id="180d2-120">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="180d2-121">Tipo de datos: **CIM \_ BootSAP**</span><span class="sxs-lookup"><span data-stu-id="180d2-121">Data type: **CIM\_BootSAP**</span></span>
</dt> <dt>

<span data-ttu-id="180d2-122">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="180d2-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="180d2-123">Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependiente")</span><span class="sxs-lookup"><span data-stu-id="180d2-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="180d2-124">Un [**\_ BootSAP de CIM**](cim-bootsap.md) que describe un punto de acceso para el servicio de arranque.</span><span class="sxs-lookup"><span data-stu-id="180d2-124">A [**CIM\_BootSAP**](cim-bootsap.md) that describes an access point for the boot service.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="180d2-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="180d2-125">Remarks</span></span>

<span data-ttu-id="180d2-126">La clase **CIM \_ BootServiceAccessBySAP** se deriva de [**\_ ServiceAccessBySAP de CIM**](cim-serviceaccessbysap.md).</span><span class="sxs-lookup"><span data-stu-id="180d2-126">The **CIM\_BootServiceAccessBySAP** class is derived from [**CIM\_ServiceAccessBySAP**](cim-serviceaccessbysap.md).</span></span>

<span data-ttu-id="180d2-127">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="180d2-127">WMI does not implement this class.</span></span>

<span data-ttu-id="180d2-128">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="180d2-128">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="180d2-129">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="180d2-129">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="180d2-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="180d2-130">Requirements</span></span>



| <span data-ttu-id="180d2-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="180d2-131">Requirement</span></span> | <span data-ttu-id="180d2-132">Value</span><span class="sxs-lookup"><span data-stu-id="180d2-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="180d2-133">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="180d2-133">Minimum supported client</span></span><br/> | <span data-ttu-id="180d2-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="180d2-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="180d2-135">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="180d2-135">Minimum supported server</span></span><br/> | <span data-ttu-id="180d2-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="180d2-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="180d2-137">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="180d2-137">Namespace</span></span><br/>                | <span data-ttu-id="180d2-138">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="180d2-138">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="180d2-139">MOF</span><span class="sxs-lookup"><span data-stu-id="180d2-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="180d2-140"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="180d2-140"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="180d2-141">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="180d2-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="180d2-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="180d2-142"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="180d2-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="180d2-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="180d2-144">**\_SERVICEACCESSBYSAP CIM**</span><span class="sxs-lookup"><span data-stu-id="180d2-144">**CIM\_ServiceAccessBySAP**</span></span>](cim-serviceaccessbysap.md)
</dt> </dl>

 

