---
description: La \_ clase CIM BIOSLoadedInNV asocia un elemento BIOS y el almacenamiento no volátil en el que se carga.
ms.assetid: 11641616-e11d-49ff-bfe4-f95fe27f00b8
ms.tgt_platform: multiple
title: CIM_BIOSLoadedInNV (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_BIOSLoadedInNV
- CIM_BIOSLoadedInNV.Dependent
- CIM_BIOSLoadedInNV.Antecedent
- CIM_BIOSLoadedInNV.EndingAddress
- CIM_BIOSLoadedInNV.StartingAddress
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 0de07e1d4b886ad14f6a7fd8dbb96c1c0f2d2079
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104000673"
---
# <a name="cim_biosloadedinnv-class"></a><span data-ttu-id="637a4-103">\_Clase BIOSLoadedInNV de CIM</span><span class="sxs-lookup"><span data-stu-id="637a4-103">CIM\_BIOSLoadedInNV class</span></span>

<span data-ttu-id="637a4-104">La clase **CIM \_ BIOSLoadedInNV** asocia un elemento BIOS y el almacenamiento no volátil en el que se carga.</span><span class="sxs-lookup"><span data-stu-id="637a4-104">The **CIM\_BIOSLoadedInNV** class associates a BIOS element and the non-volatile storage in which it is loaded.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="637a4-105">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="637a4-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="637a4-106">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="637a4-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="637a4-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="637a4-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="637a4-108">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="637a4-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="637a4-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="637a4-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{524ED194-DB35-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_BIOSLoadedInNV : CIM_Dependency
{
  CIM_BIOSElement        REF Dependent;
  CIM_NonVolatileStorage REF Antecedent;
  uint64                     EndingAddress;
  uint64                     StartingAddress;
};
```

## <a name="members"></a><span data-ttu-id="637a4-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="637a4-110">Members</span></span>

<span data-ttu-id="637a4-111">La clase **CIM \_ BIOSLoadedInNV** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="637a4-111">The **CIM\_BIOSLoadedInNV** class has these types of members:</span></span>

-   [<span data-ttu-id="637a4-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="637a4-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="637a4-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="637a4-113">Properties</span></span>

<span data-ttu-id="637a4-114">La clase **CIM \_ BIOSLoadedInNV** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="637a4-114">The **CIM\_BIOSLoadedInNV** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="637a4-115">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="637a4-115">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="637a4-116">Tipo de datos: **CIM \_ NonVolatileStorage**</span><span class="sxs-lookup"><span data-stu-id="637a4-116">Data type: **CIM\_NonVolatileStorage**</span></span>
</dt> <dt>

<span data-ttu-id="637a4-117">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="637a4-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="637a4-118">Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente")</span><span class="sxs-lookup"><span data-stu-id="637a4-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="637a4-119">Un [**\_ NonVolatileStorage de CIM**](cim-nonvolatilestorage.md) que describe el almacenamiento no volátil.</span><span class="sxs-lookup"><span data-stu-id="637a4-119">A [**CIM\_NonVolatileStorage**](cim-nonvolatilestorage.md) that describes the non-volatile storage.</span></span>

</dd> <dt>

<span data-ttu-id="637a4-120">**Dependientes**</span><span class="sxs-lookup"><span data-stu-id="637a4-120">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="637a4-121">Tipo de datos: **CIM \_ BIOSElement**</span><span class="sxs-lookup"><span data-stu-id="637a4-121">Data type: **CIM\_BIOSElement**</span></span>
</dt> <dt>

<span data-ttu-id="637a4-122">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="637a4-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="637a4-123">Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependiente")</span><span class="sxs-lookup"><span data-stu-id="637a4-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="637a4-124">Un [**\_ BIOSElement de CIM**](cim-bioselement.md) que describe el BIOS almacenado en la extensión no volátil.</span><span class="sxs-lookup"><span data-stu-id="637a4-124">A [**CIM\_BIOSElement**](cim-bioselement.md) that describes the BIOS stored in the non-volatile extent.</span></span>

</dd> <dt>

<span data-ttu-id="637a4-125">**EndingAddress**</span><span class="sxs-lookup"><span data-stu-id="637a4-125">**EndingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="637a4-126">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="637a4-126">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="637a4-127">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="637a4-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="637a4-128">Dirección final en la que se encuentra el BIOS en el almacenamiento no volátil.</span><span class="sxs-lookup"><span data-stu-id="637a4-128">Ending address where the BIOS is located in non-volatile storage.</span></span>

<span data-ttu-id="637a4-129">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="637a4-129">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="637a4-130">**StartingAddress**</span><span class="sxs-lookup"><span data-stu-id="637a4-130">**StartingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="637a4-131">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="637a4-131">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="637a4-132">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="637a4-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="637a4-133">Dirección inicial en la que se encuentra el BIOS en el almacenamiento no volátil.</span><span class="sxs-lookup"><span data-stu-id="637a4-133">Starting address where the BIOS is located in non-volatile storage.</span></span>

<span data-ttu-id="637a4-134">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="637a4-134">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="637a4-135">Observaciones</span><span class="sxs-lookup"><span data-stu-id="637a4-135">Remarks</span></span>

<span data-ttu-id="637a4-136">La clase **CIM \_ BIOSLoadedInNV** se deriva de [**la \_ dependencia CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="637a4-136">The **CIM\_BIOSLoadedInNV** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="637a4-137">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="637a4-137">WMI does not implement this class.</span></span>

<span data-ttu-id="637a4-138">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="637a4-138">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="637a4-139">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="637a4-139">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="637a4-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="637a4-140">Requirements</span></span>



| <span data-ttu-id="637a4-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="637a4-141">Requirement</span></span> | <span data-ttu-id="637a4-142">Value</span><span class="sxs-lookup"><span data-stu-id="637a4-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="637a4-143">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="637a4-143">Minimum supported client</span></span><br/> | <span data-ttu-id="637a4-144">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="637a4-144">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="637a4-145">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="637a4-145">Minimum supported server</span></span><br/> | <span data-ttu-id="637a4-146">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="637a4-146">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="637a4-147">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="637a4-147">Namespace</span></span><br/>                | <span data-ttu-id="637a4-148">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="637a4-148">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="637a4-149">MOF</span><span class="sxs-lookup"><span data-stu-id="637a4-149">MOF</span></span><br/>                      | <dl> <span data-ttu-id="637a4-150"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="637a4-150"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="637a4-151">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="637a4-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="637a4-152"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="637a4-152"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="637a4-153">Vea también</span><span class="sxs-lookup"><span data-stu-id="637a4-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="637a4-154">**Dependencia de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="637a4-154">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

