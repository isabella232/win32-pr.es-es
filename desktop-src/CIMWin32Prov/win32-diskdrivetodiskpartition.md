---
description: La \_ clase WMI DiskDriveToDiskPartition Association de Win32 relaciona una unidad de disco y una partición existente.
ms.assetid: 82953097-ebfb-42b8-84b4-fb4ed19f3525
ms.tgt_platform: multiple
title: Win32_DiskDriveToDiskPartition (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_DiskDriveToDiskPartition
- Win32_DiskDriveToDiskPartition.Antecedent
- Win32_DiskDriveToDiskPartition.Dependent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b2bd5472bd4ad92ddde47f7d6a492916006a80cb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659676"
---
# <a name="win32_diskdrivetodiskpartition-class"></a><span data-ttu-id="93f27-103">\_Clase Win32 DiskDriveToDiskPartition</span><span class="sxs-lookup"><span data-stu-id="93f27-103">Win32\_DiskDriveToDiskPartition class</span></span>

<span data-ttu-id="93f27-104">La [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ DiskDriveToDiskPartition** Association de Win32 relaciona una unidad de disco y una partición existente.</span><span class="sxs-lookup"><span data-stu-id="93f27-104">The **Win32\_DiskDriveToDiskPartition** association [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) relates a disk drive and a partition existing on it.</span></span>

<span data-ttu-id="93f27-105">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="93f27-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="93f27-106">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="93f27-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="93f27-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="93f27-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4F9-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_DiskDriveToDiskPartition : CIM_MediaPresent
{
  Win32_DiskDrive     REF Antecedent;
  Win32_DiskPartition REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="93f27-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="93f27-108">Members</span></span>

<span data-ttu-id="93f27-109">La **clase \_ DiskDriveToDiskPartition de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="93f27-109">The **Win32\_DiskDriveToDiskPartition** class has these types of members:</span></span>

-   [<span data-ttu-id="93f27-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="93f27-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="93f27-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="93f27-111">Properties</span></span>

<span data-ttu-id="93f27-112">La **clase \_ DiskDriveToDiskPartition de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="93f27-112">The **Win32\_DiskDriveToDiskPartition** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="93f27-113">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="93f27-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93f27-114">Tipo de datos: **Win32 \_ DiskDrive**</span><span class="sxs-lookup"><span data-stu-id="93f27-114">Data type: **Win32\_DiskDrive**</span></span>
</dt> <dt>

<span data-ttu-id="93f27-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="93f27-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="93f27-116">Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ DiskDrive")</span><span class="sxs-lookup"><span data-stu-id="93f27-116">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_DiskDrive")</span></span>
</dt> </dl>

<span data-ttu-id="93f27-117">Referencia a la instancia de que representa las propiedades de la unidad de disco en la que existe la partición.</span><span class="sxs-lookup"><span data-stu-id="93f27-117">Reference to the instance representing the properties of the disk drive where the partition exists.</span></span>

</dd> <dt>

<span data-ttu-id="93f27-118">**Dependientes**</span><span class="sxs-lookup"><span data-stu-id="93f27-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93f27-119">Tipo de datos: **Win32 \_ DiskPartition**</span><span class="sxs-lookup"><span data-stu-id="93f27-119">Data type: **Win32\_DiskPartition**</span></span>
</dt> <dt>

<span data-ttu-id="93f27-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="93f27-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="93f27-121">Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependiente"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ DiskPartition")</span><span class="sxs-lookup"><span data-stu-id="93f27-121">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_DiskPartition")</span></span>
</dt> </dl>

<span data-ttu-id="93f27-122">Referencia a la instancia de que representa la partición de disco que reside en la unidad de disco.</span><span class="sxs-lookup"><span data-stu-id="93f27-122">Reference to the instance representing the disk partition residing on the disk drive.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="93f27-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="93f27-123">Remarks</span></span>

<span data-ttu-id="93f27-124">La **clase \_ DiskDriveToDiskPartition de Win32** se deriva de [**\_ MediaPresent de CIM**](cim-mediapresent.md).</span><span class="sxs-lookup"><span data-stu-id="93f27-124">The **Win32\_DiskDriveToDiskPartition** class is derived from [**CIM\_MediaPresent**](cim-mediapresent.md).</span></span>

<span data-ttu-id="93f27-125">Para obtener una explicación sobre cómo usar esta clase, consulte los artículos de blog [uso de PowerShell para asignar unidades de disco y particiones](https://blogs.technet.com/b/heyscriptingguy/archive/2012/12/17/use-powershell-to-map-disk-drives-and-partitions.aspx) , y de [cómo se pueden poner en correlación unidades lógicas y discos físicos](https://blogs.technet.com/b/heyscriptingguy/archive/2005/05/23/how-can-i-correlate-logical-drives-and-physical-disks.aspx) .</span><span class="sxs-lookup"><span data-stu-id="93f27-125">For a discussion on how to use this class, see the [Use PowerShell to Map Disk Drives and Partitions](https://blogs.technet.com/b/heyscriptingguy/archive/2012/12/17/use-powershell-to-map-disk-drives-and-partitions.aspx) and the [How Can I Correlate Logical Drives and Physical Disks?](https://blogs.technet.com/b/heyscriptingguy/archive/2005/05/23/how-can-i-correlate-logical-drives-and-physical-disks.aspx) blog articles.</span></span>

## <a name="examples"></a><span data-ttu-id="93f27-126">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="93f27-126">Examples</span></span>

<span data-ttu-id="93f27-127">En el ejemplo de PowerShell [usar PowerShell para recopilar información de puntos de montaje y de disco, partición o punto de montaje](https://Gallery.TechNet.Microsoft.Com/Use-Powershell-to-Gather-b5c746d0) se usa **Win32 \_ DiskDriveToDiskPartition** para devolver información acerca de los discos locales, las particiones y los puntos de montaje.</span><span class="sxs-lookup"><span data-stu-id="93f27-127">The [Use Powershell to Gather Disk/Partition/Mount Point Information](https://Gallery.TechNet.Microsoft.Com/Use-Powershell-to-Gather-b5c746d0) PowerShell sample uses **Win32\_DiskDriveToDiskPartition** to return information about local disks/partitions and mount points.</span></span>

## <a name="requirements"></a><span data-ttu-id="93f27-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="93f27-128">Requirements</span></span>



| <span data-ttu-id="93f27-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="93f27-129">Requirement</span></span> | <span data-ttu-id="93f27-130">Value</span><span class="sxs-lookup"><span data-stu-id="93f27-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="93f27-131">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="93f27-131">Minimum supported client</span></span><br/> | <span data-ttu-id="93f27-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="93f27-132">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="93f27-133">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="93f27-133">Minimum supported server</span></span><br/> | <span data-ttu-id="93f27-134">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="93f27-134">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="93f27-135">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="93f27-135">Namespace</span></span><br/>                | <span data-ttu-id="93f27-136">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="93f27-136">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="93f27-137">MOF</span><span class="sxs-lookup"><span data-stu-id="93f27-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="93f27-138"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="93f27-138"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="93f27-139">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="93f27-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="93f27-140"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="93f27-140"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="93f27-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="93f27-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93f27-142">**\_MEDIAPRESENT CIM**</span><span class="sxs-lookup"><span data-stu-id="93f27-142">**CIM\_MediaPresent**</span></span>](cim-mediapresent.md)
</dt> <dt>

<span data-ttu-id="93f27-143">[Clases de sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="93f27-143">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="93f27-144">Tareas de WMI: discos y sistemas de archivos</span><span class="sxs-lookup"><span data-stu-id="93f27-144">WMI Tasks: Disks and File Systems</span></span>](/windows/desktop/WmiSdk/wmi-tasks--disks-and-file-systems)
</dt> </dl>

 

