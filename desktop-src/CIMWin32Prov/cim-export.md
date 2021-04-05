---
description: La \_ clase de exportación CIM representa una asociación entre un sistema de archivos local y sus directorios, que indican que los directorios especificados están disponibles para su montaje.
ms.assetid: 4c43ba5a-e003-4985-85b3-68ecf13a4bf5
ms.tgt_platform: multiple
title: CIM_Export (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Export
- CIM_Export.Directory
- CIM_Export.ExportedDirectoryName
- CIM_Export.LocalFS
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 447601b61fb79cfa779ea0cab75962c835210c52
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104000624"
---
# <a name="cim_export-class"></a><span data-ttu-id="cb4a1-103">CIM \_ Export (clase)</span><span class="sxs-lookup"><span data-stu-id="cb4a1-103">CIM\_Export class</span></span>

<span data-ttu-id="cb4a1-104">La clase de **\_ exportación CIM** representa una asociación entre un sistema de archivos local y sus directorios, que indican que los directorios especificados están disponibles para su montaje.</span><span class="sxs-lookup"><span data-stu-id="cb4a1-104">The **CIM\_Export** class represents an association between a local file system and its directories, which indicate that the specified directories are available for mount.</span></span> <span data-ttu-id="cb4a1-105">Al exportar un sistema de archivos completo, el directorio debe hacer referencia al directorio superior del sistema de archivos.</span><span class="sxs-lookup"><span data-stu-id="cb4a1-105">When exporting an entire file system, the directory should reference the topmost directory of the file system.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="cb4a1-106">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="cb4a1-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="cb4a1-107">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="cb4a1-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="cb4a1-108">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="cb4a1-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="cb4a1-109">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="cb4a1-109">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="cb4a1-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="cb4a1-110">Syntax</span></span>

``` syntax
[Abstract, Association, UUID("{75BCF4F8-DB46-11D2-B4C8-80080C7B6371}"), AMENDMENT]
class CIM_Export
{
  CIM_Directory       REF Directory;
  string                  ExportedDirectoryName;
  CIM_LocalFileSystem REF LocalFS;
};
```

## <a name="members"></a><span data-ttu-id="cb4a1-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="cb4a1-111">Members</span></span>

<span data-ttu-id="cb4a1-112">La clase de **\_ exportación CIM** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="cb4a1-112">The **CIM\_Export** class has these types of members:</span></span>

-   [<span data-ttu-id="cb4a1-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="cb4a1-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="cb4a1-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="cb4a1-114">Properties</span></span>

<span data-ttu-id="cb4a1-115">La **clase \_ Export CIM** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="cb4a1-115">The **CIM\_Export** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="cb4a1-116">**Directorio**</span><span class="sxs-lookup"><span data-stu-id="cb4a1-116">**Directory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cb4a1-117">Tipo de datos **: \_ directorio CIM**</span><span class="sxs-lookup"><span data-stu-id="cb4a1-117">Data type: **CIM\_Directory**</span></span>
</dt> <dt>

<span data-ttu-id="cb4a1-118">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="cb4a1-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cb4a1-119">Referencia al directorio exportado para el montaje de Network File System (NFS).</span><span class="sxs-lookup"><span data-stu-id="cb4a1-119">Reference to the directory exported for network file system (NFS) mount.</span></span>

</dd> <dt>

<span data-ttu-id="cb4a1-120">**ExportedDirectoryName**</span><span class="sxs-lookup"><span data-stu-id="cb4a1-120">**ExportedDirectoryName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cb4a1-121">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="cb4a1-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cb4a1-122">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="cb4a1-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cb4a1-123">Nombre con el que se exporta el directorio.</span><span class="sxs-lookup"><span data-stu-id="cb4a1-123">Name under which the directory is exported.</span></span>

</dd> <dt>

<span data-ttu-id="cb4a1-124">**LocalFS**</span><span class="sxs-lookup"><span data-stu-id="cb4a1-124">**LocalFS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cb4a1-125">Tipo de datos: **CIM \_ LocalFileSystem**</span><span class="sxs-lookup"><span data-stu-id="cb4a1-125">Data type: **CIM\_LocalFileSystem**</span></span>
</dt> <dt>

<span data-ttu-id="cb4a1-126">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="cb4a1-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cb4a1-127">Calificadores: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="cb4a1-127">Qualifiers: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="cb4a1-128">Referencia al sistema de archivos local.</span><span class="sxs-lookup"><span data-stu-id="cb4a1-128">Reference to the local file system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="cb4a1-129">Observaciones</span><span class="sxs-lookup"><span data-stu-id="cb4a1-129">Remarks</span></span>

<span data-ttu-id="cb4a1-130">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="cb4a1-130">WMI does not implement this class.</span></span>

<span data-ttu-id="cb4a1-131">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="cb4a1-131">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="cb4a1-132">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="cb4a1-132">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="cb4a1-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cb4a1-133">Requirements</span></span>



| <span data-ttu-id="cb4a1-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="cb4a1-134">Requirement</span></span> | <span data-ttu-id="cb4a1-135">Value</span><span class="sxs-lookup"><span data-stu-id="cb4a1-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cb4a1-136">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cb4a1-136">Minimum supported client</span></span><br/> | <span data-ttu-id="cb4a1-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="cb4a1-137">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="cb4a1-138">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cb4a1-138">Minimum supported server</span></span><br/> | <span data-ttu-id="cb4a1-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cb4a1-139">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="cb4a1-140">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="cb4a1-140">Namespace</span></span><br/>                | <span data-ttu-id="cb4a1-141">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="cb4a1-141">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="cb4a1-142">MOF</span><span class="sxs-lookup"><span data-stu-id="cb4a1-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cb4a1-143"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="cb4a1-143"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="cb4a1-144">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="cb4a1-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cb4a1-145"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cb4a1-145"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

