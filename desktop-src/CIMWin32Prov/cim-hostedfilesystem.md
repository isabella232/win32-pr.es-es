---
description: La \_ Asociación HostedFileSystem de CIM representa un vínculo entre el equipo y el sistema de archivos hospedado en el sistema del equipo.
ms.assetid: 1027fc6b-588b-4da8-8b3f-0c4c3328534a
ms.tgt_platform: multiple
title: CIM_HostedFileSystem (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_HostedFileSystem
- CIM_HostedFileSystem.PartComponent
- CIM_HostedFileSystem.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: eef90ea3f1ed743ec5bee0eefa5afebc8c340077
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153170"
---
# <a name="cim_hostedfilesystem-class"></a><span data-ttu-id="66a0b-103">\_Clase HostedFileSystem de CIM</span><span class="sxs-lookup"><span data-stu-id="66a0b-103">CIM\_HostedFileSystem class</span></span>

<span data-ttu-id="66a0b-104">La **Asociación \_ HostedFileSystem de CIM** representa un vínculo entre el equipo y el sistema de archivos hospedado en el sistema del equipo.</span><span class="sxs-lookup"><span data-stu-id="66a0b-104">The **CIM\_HostedFileSystem** association represents a link between the computer system and the file system hosted on the computer system.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="66a0b-105">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="66a0b-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="66a0b-106">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="66a0b-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="66a0b-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="66a0b-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="66a0b-108">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="66a0b-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="66a0b-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="66a0b-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{A2EFC898-E3D3-11d2-8601-0000F8102E5F}"), AMENDMENT]
class CIM_HostedFileSystem : CIM_SystemComponent
{
  CIM_FileSystem     REF PartComponent;
  CIM_ComputerSystem REF GroupComponent;
};
```

## <a name="members"></a><span data-ttu-id="66a0b-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="66a0b-110">Members</span></span>

<span data-ttu-id="66a0b-111">La clase **CIM \_ HostedFileSystem** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="66a0b-111">The **CIM\_HostedFileSystem** class has these types of members:</span></span>

-   [<span data-ttu-id="66a0b-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="66a0b-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="66a0b-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="66a0b-113">Properties</span></span>

<span data-ttu-id="66a0b-114">La clase **CIM \_ HostedFileSystem** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="66a0b-114">The **CIM\_HostedFileSystem** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="66a0b-115">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="66a0b-115">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66a0b-116">Tipo de datos: **CIM \_ ComputerSystem**</span><span class="sxs-lookup"><span data-stu-id="66a0b-116">Data type: **CIM\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="66a0b-117">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="66a0b-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="66a0b-118">Calificadores: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span><span class="sxs-lookup"><span data-stu-id="66a0b-118">Qualifiers: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span></span>
</dt> </dl>

<span data-ttu-id="66a0b-119">Un [**\_ ComputerSystem de CIM**](cim-computersystem.md) que describe el sistema del equipo.</span><span class="sxs-lookup"><span data-stu-id="66a0b-119">A [**CIM\_ComputerSystem**](cim-computersystem.md) that describes the computer system.</span></span>

</dd> <dt>

<span data-ttu-id="66a0b-120">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="66a0b-120">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="66a0b-121">Tipo de datos **: \_ sistema de archivos CIM**</span><span class="sxs-lookup"><span data-stu-id="66a0b-121">Data type: **CIM\_FileSystem**</span></span>
</dt> <dt>

<span data-ttu-id="66a0b-122">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="66a0b-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="66a0b-123">Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**débil**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="66a0b-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**Weak**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="66a0b-124">Un sistema de archivos [**CIM \_**](cim-filesystem.md) que describe el sistema de archivos propiedad del equipo.</span><span class="sxs-lookup"><span data-stu-id="66a0b-124">A [**CIM\_FileSystem**](cim-filesystem.md) that describes the file system owned by the computer system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="66a0b-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="66a0b-125">Remarks</span></span>

<span data-ttu-id="66a0b-126">La clase **CIM \_ HostedFileSystem** se deriva de [**\_ SystemComponent de CIM**](cim-systemcomponent.md).</span><span class="sxs-lookup"><span data-stu-id="66a0b-126">The **CIM\_HostedFileSystem** class is derived from [**CIM\_SystemComponent**](cim-systemcomponent.md).</span></span>

<span data-ttu-id="66a0b-127">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="66a0b-127">WMI does not implement this class.</span></span>

<span data-ttu-id="66a0b-128">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="66a0b-128">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="66a0b-129">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="66a0b-129">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="66a0b-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="66a0b-130">Requirements</span></span>



| <span data-ttu-id="66a0b-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="66a0b-131">Requirement</span></span> | <span data-ttu-id="66a0b-132">Value</span><span class="sxs-lookup"><span data-stu-id="66a0b-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="66a0b-133">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="66a0b-133">Minimum supported client</span></span><br/> | <span data-ttu-id="66a0b-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="66a0b-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="66a0b-135">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="66a0b-135">Minimum supported server</span></span><br/> | <span data-ttu-id="66a0b-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="66a0b-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="66a0b-137">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="66a0b-137">Namespace</span></span><br/>                | <span data-ttu-id="66a0b-138">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="66a0b-138">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="66a0b-139">MOF</span><span class="sxs-lookup"><span data-stu-id="66a0b-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="66a0b-140"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="66a0b-140"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="66a0b-141">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="66a0b-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="66a0b-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="66a0b-142"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="66a0b-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="66a0b-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66a0b-144">**\_SYSTEMCOMPONENT CIM**</span><span class="sxs-lookup"><span data-stu-id="66a0b-144">**CIM\_SystemComponent**</span></span>](cim-systemcomponent.md)
</dt> </dl>

 

