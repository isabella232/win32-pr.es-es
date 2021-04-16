---
description: La \_ clase WMI LogicalProgramGroupDirectory Association de Win32 relaciona los grupos de programas lógicos (agrupaciones en el menú Inicio) y los directorios de archivos en los que se almacenan.
ms.assetid: 31a8b56a-d4fd-4cc5-9997-ec6211fe9425
ms.tgt_platform: multiple
title: Win32_LogicalProgramGroupDirectory (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_LogicalProgramGroupDirectory
- Win32_LogicalProgramGroupDirectory.Antecedent
- Win32_LogicalProgramGroupDirectory.Dependent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: d6ebaddd4455ba1b62832f940d78534c90cefeeb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659357"
---
# <a name="win32_logicalprogramgroupdirectory-class"></a><span data-ttu-id="e446f-103">\_Clase Win32 LogicalProgramGroupDirectory</span><span class="sxs-lookup"><span data-stu-id="e446f-103">Win32\_LogicalProgramGroupDirectory class</span></span>

<span data-ttu-id="e446f-104">La [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ LogicalProgramGroupDirectory** Association de Win32 relaciona los grupos de programas lógicos (agrupaciones en el menú **Inicio** ) y los directorios de archivos en los que se almacenan.</span><span class="sxs-lookup"><span data-stu-id="e446f-104">The **Win32\_LogicalProgramGroupDirectory** association [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) relates logical program groups (groupings in the **Start** menu) and the file directories in which they are stored.</span></span>

<span data-ttu-id="e446f-105">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="e446f-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="e446f-106">Las propiedades y los métodos están en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="e446f-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="e446f-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e446f-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), Privileges("SeRestorePrivilege"), UUID("{F25FE467-783E-11d2-90BF-0060081A46FD}"), AMENDMENT]
class Win32_LogicalProgramGroupDirectory : CIM_Dependency
{
  Win32_LogicalProgramGroup REF Antecedent;
  Win32_Directory           REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="e446f-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="e446f-108">Members</span></span>

<span data-ttu-id="e446f-109">La **clase \_ LogicalProgramGroupDirectory de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="e446f-109">The **Win32\_LogicalProgramGroupDirectory** class has these types of members:</span></span>

-   [<span data-ttu-id="e446f-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="e446f-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e446f-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="e446f-111">Properties</span></span>

<span data-ttu-id="e446f-112">La **clase \_ LogicalProgramGroupDirectory de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="e446f-112">The **Win32\_LogicalProgramGroupDirectory** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e446f-113">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="e446f-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e446f-114">Tipo de datos: **Win32 \_ LogicalProgramGroup**</span><span class="sxs-lookup"><span data-stu-id="e446f-114">Data type: **Win32\_LogicalProgramGroup**</span></span>
</dt> <dt>

<span data-ttu-id="e446f-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e446f-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e446f-116">Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ LogicalProgramGroup")</span><span class="sxs-lookup"><span data-stu-id="e446f-116">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_LogicalProgramGroup")</span></span>
</dt> </dl>

<span data-ttu-id="e446f-117">Referencia a la instancia de que representa el grupo de programas lógicos.</span><span class="sxs-lookup"><span data-stu-id="e446f-117">Reference to the instance representing the logical program group.</span></span>

</dd> <dt>

<span data-ttu-id="e446f-118">**Dependientes**</span><span class="sxs-lookup"><span data-stu-id="e446f-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e446f-119">Tipo de datos **: \_ directorio Win32**</span><span class="sxs-lookup"><span data-stu-id="e446f-119">Data type: **Win32\_Directory**</span></span>
</dt> <dt>

<span data-ttu-id="e446f-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e446f-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e446f-121">Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependiente"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| directorio Win32 de WMI \_ ")</span><span class="sxs-lookup"><span data-stu-id="e446f-121">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_Directory")</span></span>
</dt> </dl>

<span data-ttu-id="e446f-122">Referencia a la instancia de que representa el directorio de archivos para el grupo de programas lógicos.</span><span class="sxs-lookup"><span data-stu-id="e446f-122">Reference to the instance representing the file directory for the logical program group.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e446f-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e446f-123">Remarks</span></span>

<span data-ttu-id="e446f-124">La **clase \_ LogicalProgramGroupDirectory de Win32** se deriva de la [**\_ dependencia CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="e446f-124">The **Win32\_LogicalProgramGroupDirectory** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="e446f-125">El proceso de llamada que usa esta clase debe tener el privilegio de **\_ \_ nombre de restauración se** en el equipo en el que reside el registro.</span><span class="sxs-lookup"><span data-stu-id="e446f-125">The calling process that uses this class must have the **SE\_RESTORE\_NAME** privilege on the computer in which the registry resides.</span></span> <span data-ttu-id="e446f-126">Por ejemplo, si enumera esta clase en el equipo local, la cuenta con la que se ejecuta la aplicación debe tener este privilegio.</span><span class="sxs-lookup"><span data-stu-id="e446f-126">For example, if you enumerate this class on the local computer, the account under which your application runs must have this privilege.</span></span> <span data-ttu-id="e446f-127">Para obtener más información, vea [ejecutar operaciones con privilegios](/windows/desktop/WmiSdk/executing-privileged-operations).</span><span class="sxs-lookup"><span data-stu-id="e446f-127">For more information, see [Executing Privileged Operations](/windows/desktop/WmiSdk/executing-privileged-operations).</span></span>

## <a name="requirements"></a><span data-ttu-id="e446f-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e446f-128">Requirements</span></span>



| <span data-ttu-id="e446f-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="e446f-129">Requirement</span></span> | <span data-ttu-id="e446f-130">Value</span><span class="sxs-lookup"><span data-stu-id="e446f-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e446f-131">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e446f-131">Minimum supported client</span></span><br/> | <span data-ttu-id="e446f-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e446f-132">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e446f-133">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e446f-133">Minimum supported server</span></span><br/> | <span data-ttu-id="e446f-134">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e446f-134">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e446f-135">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="e446f-135">Namespace</span></span><br/>                | <span data-ttu-id="e446f-136">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="e446f-136">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="e446f-137">MOF</span><span class="sxs-lookup"><span data-stu-id="e446f-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e446f-138"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e446f-138"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="e446f-139">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="e446f-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e446f-140"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e446f-140"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e446f-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="e446f-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e446f-142">**Dependencia de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="e446f-142">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> <dt>

<span data-ttu-id="e446f-143">[Clases de sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="e446f-143">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

