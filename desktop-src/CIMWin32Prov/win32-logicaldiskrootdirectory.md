---
description: La \_ clase WMI LogicalDiskRootDirectory Association de Win32 relaciona un disco lógico y su estructura de directorios.
ms.assetid: 860cd28a-2a59-4ce3-be26-8fdc869c70d1
ms.tgt_platform: multiple
title: Win32_LogicalDiskRootDirectory (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_LogicalDiskRootDirectory
- Win32_LogicalDiskRootDirectory.GroupComponent
- Win32_LogicalDiskRootDirectory.PartComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: e4b015891a37c5cc92bbf102482f48306d537bb6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103906978"
---
# <a name="win32_logicaldiskrootdirectory-class"></a><span data-ttu-id="f89d7-103">\_Clase Win32 LogicalDiskRootDirectory</span><span class="sxs-lookup"><span data-stu-id="f89d7-103">Win32\_LogicalDiskRootDirectory class</span></span>

<span data-ttu-id="f89d7-104">La [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ LogicalDiskRootDirectory** Association de Win32 relaciona un disco lógico y su estructura de directorios.</span><span class="sxs-lookup"><span data-stu-id="f89d7-104">The **Win32\_LogicalDiskRootDirectory** association [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) relates a logical disk and its directory structure.</span></span>

<span data-ttu-id="f89d7-105">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="f89d7-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="f89d7-106">Las propiedades y los métodos están en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="f89d7-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="f89d7-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f89d7-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{F25FE468-783E-11d2-90BF-0060081A46FD}"), AMENDMENT]
class Win32_LogicalDiskRootDirectory : CIM_Component
{
  Win32_LogicalDisk REF GroupComponent;
  Win32_Directory   REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="f89d7-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="f89d7-108">Members</span></span>

<span data-ttu-id="f89d7-109">La **clase \_ LogicalDiskRootDirectory de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="f89d7-109">The **Win32\_LogicalDiskRootDirectory** class has these types of members:</span></span>

-   [<span data-ttu-id="f89d7-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f89d7-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f89d7-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f89d7-111">Properties</span></span>

<span data-ttu-id="f89d7-112">La **clase \_ LogicalDiskRootDirectory de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="f89d7-112">The **Win32\_LogicalDiskRootDirectory** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f89d7-113">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="f89d7-113">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f89d7-114">Tipo de datos: **Win32 \_ LogicalDisk**</span><span class="sxs-lookup"><span data-stu-id="f89d7-114">Data type: **Win32\_LogicalDisk**</span></span>
</dt> <dt>

<span data-ttu-id="f89d7-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f89d7-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f89d7-116">Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ LogicalDisk")</span><span class="sxs-lookup"><span data-stu-id="f89d7-116">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_LogicalDisk")</span></span>
</dt> </dl>

<span data-ttu-id="f89d7-117">Referencia a la instancia de que representa las propiedades del disco lógico.</span><span class="sxs-lookup"><span data-stu-id="f89d7-117">Reference to the instance representing the properties of the logical disk.</span></span>

</dd> <dt>

<span data-ttu-id="f89d7-118">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="f89d7-118">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f89d7-119">Tipo de datos **: \_ directorio Win32**</span><span class="sxs-lookup"><span data-stu-id="f89d7-119">Data type: **Win32\_Directory**</span></span>
</dt> <dt>

<span data-ttu-id="f89d7-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f89d7-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f89d7-121">Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| directorio Win32 de WMI \_ ")</span><span class="sxs-lookup"><span data-stu-id="f89d7-121">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_Directory")</span></span>
</dt> </dl>

<span data-ttu-id="f89d7-122">Referencia a la instancia de que representa las propiedades de la estructura de directorios de archivos.</span><span class="sxs-lookup"><span data-stu-id="f89d7-122">Reference to the instance representing the properties of the file directory structure.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f89d7-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f89d7-123">Remarks</span></span>

<span data-ttu-id="f89d7-124">La **clase \_ LogicalDiskRootDirectory de Win32** se deriva [**del \_ componente CIM**](cim-component.md).</span><span class="sxs-lookup"><span data-stu-id="f89d7-124">The **Win32\_LogicalDiskRootDirectory** class is derived from [**CIM\_Component**](cim-component.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f89d7-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f89d7-125">Requirements</span></span>



| <span data-ttu-id="f89d7-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="f89d7-126">Requirement</span></span> | <span data-ttu-id="f89d7-127">Value</span><span class="sxs-lookup"><span data-stu-id="f89d7-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f89d7-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f89d7-128">Minimum supported client</span></span><br/> | <span data-ttu-id="f89d7-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f89d7-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f89d7-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f89d7-130">Minimum supported server</span></span><br/> | <span data-ttu-id="f89d7-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f89d7-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f89d7-132">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="f89d7-132">Namespace</span></span><br/>                | <span data-ttu-id="f89d7-133">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="f89d7-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="f89d7-134">MOF</span><span class="sxs-lookup"><span data-stu-id="f89d7-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f89d7-135"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f89d7-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="f89d7-136">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f89d7-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f89d7-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f89d7-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f89d7-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="f89d7-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f89d7-139">**\_Componente CIM**</span><span class="sxs-lookup"><span data-stu-id="f89d7-139">**CIM\_Component**</span></span>](cim-component.md)
</dt> <dt>

<span data-ttu-id="f89d7-140">[Clases de sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f89d7-140">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

