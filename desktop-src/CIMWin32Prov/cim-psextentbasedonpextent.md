---
description: La \_ clase PSExtentBasedOnPExtent de CIM asocia las extensiones de espacio protegidas basadas en una extensión física.
ms.assetid: 4b89319c-022c-4ff4-91ec-70c435a5888a
ms.tgt_platform: multiple
title: CIM_PSExtentBasedOnPExtent (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PSExtentBasedOnPExtent
- CIM_PSExtentBasedOnPExtent.EndingAddress
- CIM_PSExtentBasedOnPExtent.StartingAddress
- CIM_PSExtentBasedOnPExtent.Dependent
- CIM_PSExtentBasedOnPExtent.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: d028cb99c2f2ca3c0afd8238a3c0c1c3b2e451a3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153053"
---
# <a name="cim_psextentbasedonpextent-class"></a><span data-ttu-id="88871-103">\_Clase PSExtentBasedOnPExtent de CIM</span><span class="sxs-lookup"><span data-stu-id="88871-103">CIM\_PSExtentBasedOnPExtent class</span></span>

<span data-ttu-id="88871-104">La **clase \_ PSExtentBasedOnPExtent de CIM** asocia las extensiones de espacio protegidas basadas en una extensión física.</span><span class="sxs-lookup"><span data-stu-id="88871-104">The **CIM\_PSExtentBasedOnPExtent** class associates protected space extents that are based on a physical extent.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="88871-105">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="88871-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="88871-106">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="88871-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="88871-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="88871-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="88871-108">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="88871-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="88871-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="88871-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{451FE14C-E3D3-11d2-8601-0000F8102E5F}"), AMENDMENT]
class CIM_PSExtentBasedOnPExtent : CIM_BasedOn
{
  uint64                       EndingAddress;
  uint64                       StartingAddress;
  CIM_ProtectedSpaceExtent REF Dependent;
  CIM_PhysicalExtent       REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="88871-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="88871-110">Members</span></span>

<span data-ttu-id="88871-111">La clase **CIM \_ PSExtentBasedOnPExtent** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="88871-111">The **CIM\_PSExtentBasedOnPExtent** class has these types of members:</span></span>

-   [<span data-ttu-id="88871-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="88871-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="88871-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="88871-113">Properties</span></span>

<span data-ttu-id="88871-114">La clase **CIM \_ PSExtentBasedOnPExtent** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="88871-114">The **CIM\_PSExtentBasedOnPExtent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="88871-115">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="88871-115">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88871-116">Tipo de datos: **CIM \_ PhysicalExtent**</span><span class="sxs-lookup"><span data-stu-id="88871-116">Data type: **CIM\_PhysicalExtent**</span></span>
</dt> <dt>

<span data-ttu-id="88871-117">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="88871-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="88871-118">Calificadores: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente")</span><span class="sxs-lookup"><span data-stu-id="88871-118">Qualifiers: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="88871-119">[**\_ PhysicalExtent CIM**](cim-physicalextent.md) que describe la extensión física.</span><span class="sxs-lookup"><span data-stu-id="88871-119">A [**CIM\_PhysicalExtent**](cim-physicalextent.md) that describes the physical extent.</span></span>

</dd> <dt>

<span data-ttu-id="88871-120">**Dependientes**</span><span class="sxs-lookup"><span data-stu-id="88871-120">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88871-121">Tipo de datos: **CIM \_ ProtectedSpaceExtent**</span><span class="sxs-lookup"><span data-stu-id="88871-121">Data type: **CIM\_ProtectedSpaceExtent**</span></span>
</dt> <dt>

<span data-ttu-id="88871-122">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="88871-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="88871-123">Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependiente")</span><span class="sxs-lookup"><span data-stu-id="88871-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="88871-124">Un [**\_ ProtectedSpaceExtent de CIM**](cim-protectedspaceextent.md) que describe la extensión de espacio protegido que se basa en la extensión física.</span><span class="sxs-lookup"><span data-stu-id="88871-124">A [**CIM\_ProtectedSpaceExtent**](cim-protectedspaceextent.md) that describes the protected space extent which is built on the physical extent.</span></span>

</dd> <dt>

<span data-ttu-id="88871-125">**EndingAddress**</span><span class="sxs-lookup"><span data-stu-id="88871-125">**EndingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88871-126">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="88871-126">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="88871-127">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="88871-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="88871-128">Indica el final de la extensión de alto nivel en el almacenamiento de nivel inferior.</span><span class="sxs-lookup"><span data-stu-id="88871-128">Indicates the end of the high-level extent in lower-level storage.</span></span> <span data-ttu-id="88871-129">Esta propiedad es útil cuando se asignan extensiones no contiguas a una agrupación de nivel superior.</span><span class="sxs-lookup"><span data-stu-id="88871-129">This property is useful when mapping non-contiguous extents into a higher-level grouping.</span></span>

<span data-ttu-id="88871-130">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="88871-130">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="88871-131">Esta propiedad se hereda de [**\_ BasedOn CIM**](cim-basedon.md).</span><span class="sxs-lookup"><span data-stu-id="88871-131">This property is inherited from [**CIM\_BasedOn**](cim-basedon.md).</span></span>

</dd> <dt>

<span data-ttu-id="88871-132">**StartingAddress**</span><span class="sxs-lookup"><span data-stu-id="88871-132">**StartingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88871-133">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="88871-133">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="88871-134">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="88871-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="88871-135">Indica el principio de la extensión de alto nivel en el almacenamiento de nivel inferior.</span><span class="sxs-lookup"><span data-stu-id="88871-135">Indicates the beginning of the high-level extent in lower-level storage.</span></span>

<span data-ttu-id="88871-136">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="88871-136">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="88871-137">Esta propiedad se hereda de [**\_ BasedOn CIM**](cim-basedon.md).</span><span class="sxs-lookup"><span data-stu-id="88871-137">This property is inherited from [**CIM\_BasedOn**](cim-basedon.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="88871-138">Observaciones</span><span class="sxs-lookup"><span data-stu-id="88871-138">Remarks</span></span>

<span data-ttu-id="88871-139">La clase **CIM \_ PSExtentBasedOnPExtent** se deriva de [**la \_ BasedOn CIM**](cim-basedon.md).</span><span class="sxs-lookup"><span data-stu-id="88871-139">The **CIM\_PSExtentBasedOnPExtent** class is derived from [**CIM\_BasedOn**](cim-basedon.md).</span></span>

<span data-ttu-id="88871-140">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="88871-140">WMI does not implement this class.</span></span>

<span data-ttu-id="88871-141">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="88871-141">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="88871-142">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="88871-142">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="88871-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="88871-143">Requirements</span></span>



| <span data-ttu-id="88871-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="88871-144">Requirement</span></span> | <span data-ttu-id="88871-145">Value</span><span class="sxs-lookup"><span data-stu-id="88871-145">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="88871-146">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="88871-146">Minimum supported client</span></span><br/> | <span data-ttu-id="88871-147">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="88871-147">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="88871-148">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="88871-148">Minimum supported server</span></span><br/> | <span data-ttu-id="88871-149">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="88871-149">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="88871-150">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="88871-150">Namespace</span></span><br/>                | <span data-ttu-id="88871-151">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="88871-151">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="88871-152">MOF</span><span class="sxs-lookup"><span data-stu-id="88871-152">MOF</span></span><br/>                      | <dl> <span data-ttu-id="88871-153"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="88871-153"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="88871-154">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="88871-154">DLL</span></span><br/>                      | <dl> <span data-ttu-id="88871-155"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="88871-155"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="88871-156">Vea también</span><span class="sxs-lookup"><span data-stu-id="88871-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="88871-157">**\_BasedOn CIM**</span><span class="sxs-lookup"><span data-stu-id="88871-157">**CIM\_BasedOn**</span></span>](cim-basedon.md)
</dt> </dl>

 

