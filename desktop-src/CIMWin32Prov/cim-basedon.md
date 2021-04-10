---
description: La \_ clase basada en CIM representa una asociación que describe cómo se pueden ensamblar las extensiones de almacenamiento de las extensiones de nivel inferior.
ms.assetid: 82132012-5851-4be8-82db-edbdb50b70e5
ms.tgt_platform: multiple
title: CIM_BasedOn (clase) (proveedores WMI de CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_BasedOn
- CIM_BasedOn.Dependent
- CIM_BasedOn.Antecedent
- CIM_BasedOn.EndingAddress
- CIM_BasedOn.StartingAddress
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 5e25cd9a5f194df8c5cbc0c7dc24a4777cee3417
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275036"
---
# <a name="cim_basedon-class-cimwin32-wmi-providers"></a><span data-ttu-id="48906-103">CIM_BasedOn (clase) (proveedores WMI de CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="48906-103">CIM_BasedOn class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="48906-104">La **clase \_ basada en CIM** representa una asociación que describe cómo se pueden ensamblar las extensiones de almacenamiento de las extensiones de nivel inferior.</span><span class="sxs-lookup"><span data-stu-id="48906-104">The **CIM\_BasedOn** class represents an association that describes how storage extents can be assembled from lower-level extents.</span></span> <span data-ttu-id="48906-105">Por ejemplo, las extensiones físicas incluyen extensiones de espacio protegido.</span><span class="sxs-lookup"><span data-stu-id="48906-105">For example, physical extents include protected space extents.</span></span> <span data-ttu-id="48906-106">Por lo tanto, los conjuntos de volúmenes se ensamblan a partir de una o más extensiones de espacio físico o protegido.</span><span class="sxs-lookup"><span data-stu-id="48906-106">Thus, volume sets are assembled from one or more physical or protected space extents.</span></span> <span data-ttu-id="48906-107">La memoria caché se puede definir de forma independiente y realizada en un elemento físico, o bien se puede basar en extensiones de almacenamiento volátiles o no volátiles.</span><span class="sxs-lookup"><span data-stu-id="48906-107">Cache memory can be defined independently and realized in a physical element, or it can be based on volatile or non-volatile storage extents.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="48906-108">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="48906-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="48906-109">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="48906-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="48906-110">La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="48906-110">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="48906-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="48906-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C53E-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_BasedOn : CIM_Dependency
{
  CIM_StorageExtent REF Dependent;
  CIM_StorageExtent REF Antecedent;
  uint64                EndingAddress;
  uint64                StartingAddress;
};
```

## <a name="members"></a><span data-ttu-id="48906-112">Miembros</span><span class="sxs-lookup"><span data-stu-id="48906-112">Members</span></span>

<span data-ttu-id="48906-113">La **clase \_ basada en CIM** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="48906-113">The **CIM\_BasedOn** class has these types of members:</span></span>

-   [<span data-ttu-id="48906-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="48906-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="48906-115">Propiedades</span><span class="sxs-lookup"><span data-stu-id="48906-115">Properties</span></span>

<span data-ttu-id="48906-116">La **clase \_ basada en CIM** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="48906-116">The **CIM\_BasedOn** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="48906-117">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="48906-117">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48906-118">Tipo de datos: **CIM \_ StorageExtent**</span><span class="sxs-lookup"><span data-stu-id="48906-118">Data type: **CIM\_StorageExtent**</span></span>
</dt> <dt>

<span data-ttu-id="48906-119">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="48906-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="48906-120">Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente")</span><span class="sxs-lookup"><span data-stu-id="48906-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="48906-121">Un [**\_ StorageExtent de CIM**](cim-storageextent.md) que describe la extensión de almacenamiento de nivel inferior.</span><span class="sxs-lookup"><span data-stu-id="48906-121">A [**CIM\_StorageExtent**](cim-storageextent.md) that describes the lower level storage extent.</span></span>

</dd> <dt>

<span data-ttu-id="48906-122">**Dependientes**</span><span class="sxs-lookup"><span data-stu-id="48906-122">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48906-123">Tipo de datos: **CIM \_ StorageExtent**</span><span class="sxs-lookup"><span data-stu-id="48906-123">Data type: **CIM\_StorageExtent**</span></span>
</dt> <dt>

<span data-ttu-id="48906-124">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="48906-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="48906-125">Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependiente")</span><span class="sxs-lookup"><span data-stu-id="48906-125">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="48906-126">Un [**\_ StorageExtent de CIM**](cim-storageextent.md) que describe la extensión de almacenamiento de nivel superior.</span><span class="sxs-lookup"><span data-stu-id="48906-126">A [**CIM\_StorageExtent**](cim-storageextent.md) that describes the higher level storage extent.</span></span>

</dd> <dt>

<span data-ttu-id="48906-127">**EndingAddress**</span><span class="sxs-lookup"><span data-stu-id="48906-127">**EndingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48906-128">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="48906-128">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="48906-129">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="48906-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="48906-130">Indica el final de la extensión de alto nivel en el almacenamiento de nivel inferior.</span><span class="sxs-lookup"><span data-stu-id="48906-130">Indicates the end of the high-level extent in lower-level storage.</span></span> <span data-ttu-id="48906-131">Esta propiedad es útil cuando se asignan extensiones no contiguas a una agrupación de nivel superior.</span><span class="sxs-lookup"><span data-stu-id="48906-131">This property is useful when mapping non-contiguous extents into a higher-level grouping.</span></span>

<span data-ttu-id="48906-132">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="48906-132">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="48906-133">**StartingAddress**</span><span class="sxs-lookup"><span data-stu-id="48906-133">**StartingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48906-134">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="48906-134">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="48906-135">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="48906-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="48906-136">Indica el principio de la extensión de alto nivel en el almacenamiento de nivel inferior.</span><span class="sxs-lookup"><span data-stu-id="48906-136">Indicates the beginning of the high-level extent in lower-level storage.</span></span>

<span data-ttu-id="48906-137">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="48906-137">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="48906-138">Observaciones</span><span class="sxs-lookup"><span data-stu-id="48906-138">Remarks</span></span>

<span data-ttu-id="48906-139">La **clase \_ basada en CIM** se deriva de [**la \_ dependencia CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="48906-139">The **CIM\_BasedOn** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="48906-140">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="48906-140">WMI does not implement this class.</span></span>

<span data-ttu-id="48906-141">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="48906-141">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="48906-142">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="48906-142">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="48906-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="48906-143">Requirements</span></span>



| <span data-ttu-id="48906-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="48906-144">Requirement</span></span> | <span data-ttu-id="48906-145">Value</span><span class="sxs-lookup"><span data-stu-id="48906-145">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="48906-146">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="48906-146">Minimum supported client</span></span><br/> | <span data-ttu-id="48906-147">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="48906-147">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="48906-148">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="48906-148">Minimum supported server</span></span><br/> | <span data-ttu-id="48906-149">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="48906-149">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="48906-150">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="48906-150">Namespace</span></span><br/>                | <span data-ttu-id="48906-151">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="48906-151">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="48906-152">MOF</span><span class="sxs-lookup"><span data-stu-id="48906-152">MOF</span></span><br/>                      | <dl> <span data-ttu-id="48906-153"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="48906-153"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="48906-154">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="48906-154">DLL</span></span><br/>                      | <dl> <span data-ttu-id="48906-155"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="48906-155"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="48906-156">Vea también</span><span class="sxs-lookup"><span data-stu-id="48906-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="48906-157">**Dependencia de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="48906-157">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

