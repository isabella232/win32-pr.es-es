---
description: La \_ clase BIOSFeatureBIOSElements de CIM asocia una característica de BIOS y sus elementos de BIOS agregados.
ms.assetid: 84ebd6d0-af42-4e82-bad3-1f934789cbfe
ms.tgt_platform: multiple
title: CIM_BIOSFeatureBIOSElements (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_BIOSFeatureBIOSElements
- CIM_BIOSFeatureBIOSElements.PartComponent
- CIM_BIOSFeatureBIOSElements.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: a5a4eecea97b4d82fadcdc521d378b5b32d986b9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153286"
---
# <a name="cim_biosfeaturebioselements-class"></a><span data-ttu-id="12d98-103">\_Clase BIOSFeatureBIOSElements de CIM</span><span class="sxs-lookup"><span data-stu-id="12d98-103">CIM\_BIOSFeatureBIOSElements class</span></span>

<span data-ttu-id="12d98-104">La **clase \_ BIOSFeatureBIOSElements de CIM** asocia una característica de BIOS y sus elementos de BIOS agregados.</span><span class="sxs-lookup"><span data-stu-id="12d98-104">The **CIM\_BIOSFeatureBIOSElements** class associates a BIOS feature and its aggregated BIOS elements.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="12d98-105">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="12d98-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="12d98-106">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="12d98-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="12d98-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="12d98-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="12d98-108">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="12d98-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="12d98-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="12d98-109">Syntax</span></span>

``` syntax
[UUID("{42B2EC5C-DB35-11d2-85FC-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_BIOSFeatureBIOSElements : CIM_SoftwareFeatureSoftwareElements
{
  CIM_BIOSElement REF PartComponent;
  CIM_BIOSFeature REF GroupComponent;
};
```

## <a name="members"></a><span data-ttu-id="12d98-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="12d98-110">Members</span></span>

<span data-ttu-id="12d98-111">La clase **CIM \_ BIOSFeatureBIOSElements** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="12d98-111">The **CIM\_BIOSFeatureBIOSElements** class has these types of members:</span></span>

-   [<span data-ttu-id="12d98-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="12d98-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="12d98-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="12d98-113">Properties</span></span>

<span data-ttu-id="12d98-114">La clase **CIM \_ BIOSFeatureBIOSElements** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="12d98-114">The **CIM\_BIOSFeatureBIOSElements** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="12d98-115">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="12d98-115">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="12d98-116">Tipo de datos: **CIM \_ BIOSFeature**</span><span class="sxs-lookup"><span data-stu-id="12d98-116">Data type: **CIM\_BIOSFeature**</span></span>
</dt> <dt>

<span data-ttu-id="12d98-117">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="12d98-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="12d98-118">Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span><span class="sxs-lookup"><span data-stu-id="12d98-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span></span>
</dt> </dl>

<span data-ttu-id="12d98-119">Un [**\_ BIOSFeature de CIM**](cim-biosfeature.md) que describe la característica BIOS.</span><span class="sxs-lookup"><span data-stu-id="12d98-119">A [**CIM\_BIOSFeature**](cim-biosfeature.md) that describes the BIOS feature.</span></span>

</dd> <dt>

<span data-ttu-id="12d98-120">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="12d98-120">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="12d98-121">Tipo de datos: **CIM \_ BIOSElement**</span><span class="sxs-lookup"><span data-stu-id="12d98-121">Data type: **CIM\_BIOSElement**</span></span>
</dt> <dt>

<span data-ttu-id="12d98-122">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="12d98-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="12d98-123">Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="12d98-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="12d98-124">Un [**\_ BIOSElement de CIM**](cim-bioselement.md) que describe el elemento BIOS que implementa las funciones descritas por la característica BIOS.</span><span class="sxs-lookup"><span data-stu-id="12d98-124">A [**CIM\_BIOSElement**](cim-bioselement.md) that describes the BIOS element that implements the capabilities described by BIOS feature.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="12d98-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="12d98-125">Remarks</span></span>

<span data-ttu-id="12d98-126">La clase **CIM \_ BIOSFeatureBIOSElements** se deriva de [**\_ SoftwareFeatureSoftwareElements de CIM**](cim-softwarefeaturesoftwareelements.md).</span><span class="sxs-lookup"><span data-stu-id="12d98-126">The **CIM\_BIOSFeatureBIOSElements** class is derived from [**CIM\_SoftwareFeatureSoftwareElements**](cim-softwarefeaturesoftwareelements.md).</span></span>

<span data-ttu-id="12d98-127">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="12d98-127">WMI does not implement this class.</span></span>

<span data-ttu-id="12d98-128">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="12d98-128">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="12d98-129">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="12d98-129">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="12d98-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="12d98-130">Requirements</span></span>



| <span data-ttu-id="12d98-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="12d98-131">Requirement</span></span> | <span data-ttu-id="12d98-132">Value</span><span class="sxs-lookup"><span data-stu-id="12d98-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="12d98-133">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="12d98-133">Minimum supported client</span></span><br/> | <span data-ttu-id="12d98-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="12d98-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="12d98-135">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="12d98-135">Minimum supported server</span></span><br/> | <span data-ttu-id="12d98-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="12d98-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="12d98-137">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="12d98-137">Namespace</span></span><br/>                | <span data-ttu-id="12d98-138">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="12d98-138">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="12d98-139">MOF</span><span class="sxs-lookup"><span data-stu-id="12d98-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="12d98-140"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="12d98-140"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="12d98-141">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="12d98-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="12d98-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="12d98-142"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="12d98-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="12d98-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12d98-144">**\_SOFTWAREFEATURESOFTWAREELEMENTS CIM**</span><span class="sxs-lookup"><span data-stu-id="12d98-144">**CIM\_SoftwareFeatureSoftwareElements**</span></span>](cim-softwarefeaturesoftwareelements.md)
</dt> </dl>

 

