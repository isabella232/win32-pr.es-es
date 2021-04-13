---
description: La clase de Asociación de CIM \_ instalados representa un vínculo entre el equipo y el sistema operativo instalado.
ms.assetid: 6db5b5a2-91b6-4540-83b8-bb9c86c7f94e
ms.tgt_platform: multiple
title: CIM_InstalledOS (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_InstalledOS
- CIM_InstalledOS.PartComponent
- CIM_InstalledOS.GroupComponent
- CIM_InstalledOS.PrimaryOS
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 53e01be6a87fa6e5ef91ad6e8a81dbbddff4a576
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104538974"
---
# <a name="cim_installedos-class"></a><span data-ttu-id="cc803-103">\_Clase de instalado CIM</span><span class="sxs-lookup"><span data-stu-id="cc803-103">CIM\_InstalledOS class</span></span>

<span data-ttu-id="cc803-104">La clase de Asociación de **CIM \_ instalados** representa un vínculo entre el equipo y el sistema operativo instalado.</span><span class="sxs-lookup"><span data-stu-id="cc803-104">The **CIM\_InstalledOS** association class represents a link between the computer system and the installed operating system.</span></span> <span data-ttu-id="cc803-105">Un sistema operativo se instala cuando está en la extensión de almacenamiento de un sistema (por ejemplo, se copia en una unidad de disco o se descarga en memoria).</span><span class="sxs-lookup"><span data-stu-id="cc803-105">An operating system is installed when it is in a computer system's storage extent (for example, copied to a disk drive or downloaded to memory).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="cc803-106">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="cc803-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="cc803-107">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="cc803-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="cc803-108">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="cc803-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="cc803-109">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="cc803-109">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="cc803-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="cc803-110">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C575-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_InstalledOS : CIM_SystemComponent
{
  CIM_OperatingSystem REF PartComponent;
  CIM_ComputerSystem  REF GroupComponent;
  boolean                 PrimaryOS;
};
```

## <a name="members"></a><span data-ttu-id="cc803-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="cc803-111">Members</span></span>

<span data-ttu-id="cc803-112">La clase de **\_ instalado CIM** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="cc803-112">The **CIM\_InstalledOS** class has these types of members:</span></span>

-   [<span data-ttu-id="cc803-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="cc803-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="cc803-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="cc803-114">Properties</span></span>

<span data-ttu-id="cc803-115">La **clase \_ instalado CIM** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="cc803-115">The **CIM\_InstalledOS** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="cc803-116">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="cc803-116">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cc803-117">Tipo de datos: **CIM \_ ComputerSystem**</span><span class="sxs-lookup"><span data-stu-id="cc803-117">Data type: **CIM\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="cc803-118">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="cc803-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cc803-119">Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="cc803-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="cc803-120">Un [**\_ ComputerSystem de CIM**](cim-computersystem.md) que describe el sistema del equipo.</span><span class="sxs-lookup"><span data-stu-id="cc803-120">A [**CIM\_ComputerSystem**](cim-computersystem.md) describing the computer system.</span></span>

</dd> <dt>

<span data-ttu-id="cc803-121">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="cc803-121">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cc803-122">Tipo de datos: **CIM \_ OperatingSystem**</span><span class="sxs-lookup"><span data-stu-id="cc803-122">Data type: **CIM\_OperatingSystem**</span></span>
</dt> <dt>

<span data-ttu-id="cc803-123">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="cc803-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cc803-124">Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**débil**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="cc803-124">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**Weak**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="cc803-125">Un [**\_ OperatingSystem de CIM**](cim-operatingsystem.md) que describe el sistema operativo instalado en el sistema del equipo.</span><span class="sxs-lookup"><span data-stu-id="cc803-125">A [**CIM\_OperatingSystem**](cim-operatingsystem.md) that describes the operating system installed on the computer system.</span></span>

</dd> <dt>

<span data-ttu-id="cc803-126">**Principalesos**</span><span class="sxs-lookup"><span data-stu-id="cc803-126">**PrimaryOS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cc803-127">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="cc803-127">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="cc803-128">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="cc803-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cc803-129">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Sistema operativo DMTF \| 001,4 ")</span><span class="sxs-lookup"><span data-stu-id="cc803-129">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operating System\|001.4")</span></span>
</dt> </dl>

<span data-ttu-id="cc803-130">Si es **true**, el sistema operativo instalado es el sistema operativo predeterminado del equipo.</span><span class="sxs-lookup"><span data-stu-id="cc803-130">If **TRUE**, the installed operating system is the default operating system for the computer system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="cc803-131">Observaciones</span><span class="sxs-lookup"><span data-stu-id="cc803-131">Remarks</span></span>

<span data-ttu-id="cc803-132">La clase de **\_ instalado CIM** se deriva de [**\_ SystemComponent CIM**](cim-systemcomponent.md).</span><span class="sxs-lookup"><span data-stu-id="cc803-132">The **CIM\_InstalledOS** class is derived from [**CIM\_SystemComponent**](cim-systemcomponent.md).</span></span>

<span data-ttu-id="cc803-133">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="cc803-133">WMI does not implement this class.</span></span> <span data-ttu-id="cc803-134">Para ver las clases derivadas de **CIM \_ instalado**, vea [clases Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="cc803-134">For classes derived from **CIM\_InstalledOS**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="cc803-135">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="cc803-135">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="cc803-136">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="cc803-136">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="cc803-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cc803-137">Requirements</span></span>



| <span data-ttu-id="cc803-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="cc803-138">Requirement</span></span> | <span data-ttu-id="cc803-139">Value</span><span class="sxs-lookup"><span data-stu-id="cc803-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cc803-140">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cc803-140">Minimum supported client</span></span><br/> | <span data-ttu-id="cc803-141">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="cc803-141">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="cc803-142">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cc803-142">Minimum supported server</span></span><br/> | <span data-ttu-id="cc803-143">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cc803-143">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="cc803-144">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="cc803-144">Namespace</span></span><br/>                | <span data-ttu-id="cc803-145">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="cc803-145">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="cc803-146">MOF</span><span class="sxs-lookup"><span data-stu-id="cc803-146">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cc803-147"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="cc803-147"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="cc803-148">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="cc803-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cc803-149"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cc803-149"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cc803-150">Vea también</span><span class="sxs-lookup"><span data-stu-id="cc803-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cc803-151">**\_SYSTEMCOMPONENT CIM**</span><span class="sxs-lookup"><span data-stu-id="cc803-151">**CIM\_SystemComponent**</span></span>](cim-systemcomponent.md)
</dt> </dl>

 

