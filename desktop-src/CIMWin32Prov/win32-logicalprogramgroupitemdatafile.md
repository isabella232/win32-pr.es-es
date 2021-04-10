---
description: La \_ clase WMI LogicalProgramGroupItemDataFile Association de Win32 relaciona los elementos del grupo de programas del menú Inicio y los archivos en los que se almacenan.
ms.assetid: 9327c205-d0ad-4f2b-a65e-2a648e7c13e0
ms.tgt_platform: multiple
title: Win32_LogicalProgramGroupItemDataFile (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_LogicalProgramGroupItemDataFile
- Win32_LogicalProgramGroupItemDataFile.Antecedent
- Win32_LogicalProgramGroupItemDataFile.Dependent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: beec7074104482e4c6bc91ba7efeaea89104a011
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153546"
---
# <a name="win32_logicalprogramgroupitemdatafile-class"></a><span data-ttu-id="3dd71-103">\_Clase Win32 LogicalProgramGroupItemDataFile</span><span class="sxs-lookup"><span data-stu-id="3dd71-103">Win32\_LogicalProgramGroupItemDataFile class</span></span>

<span data-ttu-id="3dd71-104">La [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ LogicalProgramGroupItemDataFile** Association de Win32 relaciona los elementos del grupo de programas del menú **Inicio** y los archivos en los que se almacenan.</span><span class="sxs-lookup"><span data-stu-id="3dd71-104">The **Win32\_LogicalProgramGroupItemDataFile** association [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) relates the program group items of the **Start** menu and the files in which they are stored.</span></span>

<span data-ttu-id="3dd71-105">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="3dd71-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="3dd71-106">Las propiedades y los métodos están en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="3dd71-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="3dd71-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3dd71-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), Privileges("SeRestorePrivilege"), UUID("{08FFAD62-8050-11d2-90CE-0060081A46FD}"), AMENDMENT]
class Win32_LogicalProgramGroupItemDataFile : CIM_Dependency
{
  Win32_LogicalProgramGroupItem REF Antecedent;
  CIM_DataFile                  REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="3dd71-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="3dd71-108">Members</span></span>

<span data-ttu-id="3dd71-109">La **clase \_ LogicalProgramGroupItemDataFile de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="3dd71-109">The **Win32\_LogicalProgramGroupItemDataFile** class has these types of members:</span></span>

-   [<span data-ttu-id="3dd71-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="3dd71-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3dd71-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="3dd71-111">Properties</span></span>

<span data-ttu-id="3dd71-112">La **clase \_ LogicalProgramGroupItemDataFile de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="3dd71-112">The **Win32\_LogicalProgramGroupItemDataFile** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3dd71-113">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="3dd71-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3dd71-114">Tipo de datos: **Win32 \_ LogicalProgramGroupItem**</span><span class="sxs-lookup"><span data-stu-id="3dd71-114">Data type: **Win32\_LogicalProgramGroupItem**</span></span>
</dt> <dt>

<span data-ttu-id="3dd71-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3dd71-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3dd71-116">Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ LogicalProgramGroupItem")</span><span class="sxs-lookup"><span data-stu-id="3dd71-116">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_LogicalProgramGroupItem")</span></span>
</dt> </dl>

<span data-ttu-id="3dd71-117">Referencia a la instancia de que representa las agrupaciones de programas en el menú **Inicio** .</span><span class="sxs-lookup"><span data-stu-id="3dd71-117">Reference to the instance representing the program groupings in the **Start** menu.</span></span>

</dd> <dt>

<span data-ttu-id="3dd71-118">**Dependientes**</span><span class="sxs-lookup"><span data-stu-id="3dd71-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3dd71-119">Tipo de datos **: \_ archivo** de datos CIM</span><span class="sxs-lookup"><span data-stu-id="3dd71-119">Data type: **CIM\_DataFile**</span></span>
</dt> <dt>

<span data-ttu-id="3dd71-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3dd71-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3dd71-121">Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependiente"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \| CIM archivo de \_ archivos")</span><span class="sxs-lookup"><span data-stu-id="3dd71-121">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\|CIM\_DataFile")</span></span>
</dt> </dl>

<span data-ttu-id="3dd71-122">Referencia a la instancia de que representa la clase asociada al grupo de programas.</span><span class="sxs-lookup"><span data-stu-id="3dd71-122">Reference to the instance representing the class associated with the program group.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3dd71-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3dd71-123">Remarks</span></span>

<span data-ttu-id="3dd71-124">La **clase \_ LogicalProgramGroupItemDataFile de Win32** se deriva de la [**\_ dependencia CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="3dd71-124">The **Win32\_LogicalProgramGroupItemDataFile** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="3dd71-125">El proceso de llamada que usa esta clase debe tener el privilegio de **\_ \_ nombre de restauración se** en el equipo en el que reside el registro.</span><span class="sxs-lookup"><span data-stu-id="3dd71-125">The calling process that uses this class must have the **SE\_RESTORE\_NAME** privilege on the computer in which the registry resides.</span></span> <span data-ttu-id="3dd71-126">Por ejemplo, si enumera esta clase en el equipo local, la cuenta con la que se ejecuta la aplicación debe tener este privilegio.</span><span class="sxs-lookup"><span data-stu-id="3dd71-126">For example, if you enumerate this class on the local computer, the account under which your application runs must have this privilege.</span></span> <span data-ttu-id="3dd71-127">Para obtener más información, vea [ejecutar operaciones con privilegios](/windows/desktop/WmiSdk/executing-privileged-operations).</span><span class="sxs-lookup"><span data-stu-id="3dd71-127">For more information, see [Executing Privileged Operations](/windows/desktop/WmiSdk/executing-privileged-operations).</span></span>

## <a name="requirements"></a><span data-ttu-id="3dd71-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3dd71-128">Requirements</span></span>



| <span data-ttu-id="3dd71-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="3dd71-129">Requirement</span></span> | <span data-ttu-id="3dd71-130">Value</span><span class="sxs-lookup"><span data-stu-id="3dd71-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3dd71-131">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3dd71-131">Minimum supported client</span></span><br/> | <span data-ttu-id="3dd71-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3dd71-132">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="3dd71-133">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3dd71-133">Minimum supported server</span></span><br/> | <span data-ttu-id="3dd71-134">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3dd71-134">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="3dd71-135">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="3dd71-135">Namespace</span></span><br/>                | <span data-ttu-id="3dd71-136">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="3dd71-136">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="3dd71-137">MOF</span><span class="sxs-lookup"><span data-stu-id="3dd71-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3dd71-138"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3dd71-138"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="3dd71-139">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="3dd71-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3dd71-140"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3dd71-140"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3dd71-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="3dd71-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3dd71-142">**Dependencia de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="3dd71-142">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> <dt>

<span data-ttu-id="3dd71-143">[Clases de sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="3dd71-143">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

