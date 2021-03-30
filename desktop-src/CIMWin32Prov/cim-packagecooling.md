---
description: La \_ Asociación PackageCooling de CIM representa la relación en la que se instala un dispositivo de enfriamiento en un paquete, como un chasis o un bastidor, para ayudar con la refrigeración del paquete.
ms.assetid: 0aaae8e1-6e70-4b26-8e56-dac5657e58c1
ms.tgt_platform: multiple
title: CIM_PackageCooling (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PackageCooling
- CIM_PackageCooling.Dependent
- CIM_PackageCooling.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1f88cd3f07983870bed8fd2d740f3bf9051019b4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104538956"
---
# <a name="cim_packagecooling-class"></a><span data-ttu-id="35c0c-103">\_Clase PackageCooling de CIM</span><span class="sxs-lookup"><span data-stu-id="35c0c-103">CIM\_PackageCooling class</span></span>

<span data-ttu-id="35c0c-104">La **Asociación \_ PackageCooling de CIM** representa la relación en la que se instala un dispositivo de enfriamiento en un paquete, como un chasis o un bastidor, para ayudar con la refrigeración del paquete.</span><span class="sxs-lookup"><span data-stu-id="35c0c-104">The **CIM\_PackageCooling** association represents the relationship in which a cooling device is installed in a package, such as a chassis or rack, to assist with the package's cooling.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="35c0c-105">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="35c0c-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="35c0c-106">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="35c0c-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="35c0c-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="35c0c-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="35c0c-108">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="35c0c-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="35c0c-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="35c0c-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{FAF76B8E-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_PackageCooling : CIM_Dependency
{
  CIM_PhysicalPackage REF Dependent;
  CIM_CoolingDevice   REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="35c0c-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="35c0c-110">Members</span></span>

<span data-ttu-id="35c0c-111">La clase **CIM \_ PackageCooling** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="35c0c-111">The **CIM\_PackageCooling** class has these types of members:</span></span>

-   [<span data-ttu-id="35c0c-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="35c0c-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="35c0c-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="35c0c-113">Properties</span></span>

<span data-ttu-id="35c0c-114">La clase **CIM \_ PackageCooling** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="35c0c-114">The **CIM\_PackageCooling** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="35c0c-115">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="35c0c-115">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35c0c-116">Tipo de datos: **CIM \_ CoolingDevice**</span><span class="sxs-lookup"><span data-stu-id="35c0c-116">Data type: **CIM\_CoolingDevice**</span></span>
</dt> <dt>

<span data-ttu-id="35c0c-117">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="35c0c-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="35c0c-118">Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente")</span><span class="sxs-lookup"><span data-stu-id="35c0c-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="35c0c-119">Un [**\_ CoolingDevice de CIM**](cim-coolingdevice.md) que describe el dispositivo de enfriamiento para el paquete.</span><span class="sxs-lookup"><span data-stu-id="35c0c-119">A [**CIM\_CoolingDevice**](cim-coolingdevice.md) that describes the cooling device for the package.</span></span>

</dd> <dt>

<span data-ttu-id="35c0c-120">**Dependientes**</span><span class="sxs-lookup"><span data-stu-id="35c0c-120">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="35c0c-121">Tipo de datos: **CIM \_ PhysicalPackage**</span><span class="sxs-lookup"><span data-stu-id="35c0c-121">Data type: **CIM\_PhysicalPackage**</span></span>
</dt> <dt>

<span data-ttu-id="35c0c-122">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="35c0c-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="35c0c-123">Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependiente")</span><span class="sxs-lookup"><span data-stu-id="35c0c-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="35c0c-124">Un [**\_ PhysicalPackage de CIM**](cim-physicalpackage.md) que describe el paquete físico cuyo entorno está refrigerado.</span><span class="sxs-lookup"><span data-stu-id="35c0c-124">A [**CIM\_PhysicalPackage**](cim-physicalpackage.md) that describes the physical package whose environment is cooled.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="35c0c-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="35c0c-125">Remarks</span></span>

<span data-ttu-id="35c0c-126">**CIM \_ PackageCooling** se deriva de [**la \_ dependencia CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="35c0c-126">**CIM\_PackageCooling** is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="35c0c-127">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="35c0c-127">WMI does not implement this class.</span></span>

<span data-ttu-id="35c0c-128">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="35c0c-128">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="35c0c-129">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="35c0c-129">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="35c0c-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="35c0c-130">Requirements</span></span>



| <span data-ttu-id="35c0c-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="35c0c-131">Requirement</span></span> | <span data-ttu-id="35c0c-132">Value</span><span class="sxs-lookup"><span data-stu-id="35c0c-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="35c0c-133">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="35c0c-133">Minimum supported client</span></span><br/> | <span data-ttu-id="35c0c-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="35c0c-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="35c0c-135">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="35c0c-135">Minimum supported server</span></span><br/> | <span data-ttu-id="35c0c-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="35c0c-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="35c0c-137">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="35c0c-137">Namespace</span></span><br/>                | <span data-ttu-id="35c0c-138">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="35c0c-138">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="35c0c-139">MOF</span><span class="sxs-lookup"><span data-stu-id="35c0c-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="35c0c-140"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="35c0c-140"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="35c0c-141">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="35c0c-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="35c0c-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="35c0c-142"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="35c0c-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="35c0c-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35c0c-144">**Dependencia de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="35c0c-144">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

