---
description: La \_ Asociación FileStorage de CIM vincula el sistema de archivos y los archivos lógicos que se dirigen a través del sistema de archivos.
ms.assetid: 1d0b698b-4c57-4a1c-8b00-0a6079be8dcc
ms.tgt_platform: multiple
title: CIM_FileStorage (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_FileStorage
- CIM_FileStorage.PartComponent
- CIM_FileStorage.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 3630bdf3250ce93765809df17e9318d3cd44f393
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659599"
---
# <a name="cim_filestorage-class"></a><span data-ttu-id="e2e47-103">\_Clase FileStorage de CIM</span><span class="sxs-lookup"><span data-stu-id="e2e47-103">CIM\_FileStorage class</span></span>

<span data-ttu-id="e2e47-104">La **Asociación \_ FileStorage de CIM** vincula el sistema de archivos y los archivos lógicos que se dirigen a través del sistema de archivos.</span><span class="sxs-lookup"><span data-stu-id="e2e47-104">The **CIM\_FileStorage** association links the file system and the logical files addressed through the file system.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e2e47-105">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="e2e47-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="e2e47-106">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="e2e47-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="e2e47-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="e2e47-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="e2e47-108">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="e2e47-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="e2e47-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e2e47-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{4A626026-DB36-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_FileStorage : CIM_Component
{
  CIM_LogicalFile REF PartComponent;
  CIM_FileSystem  REF GroupComponent;
};
```

## <a name="members"></a><span data-ttu-id="e2e47-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="e2e47-110">Members</span></span>

<span data-ttu-id="e2e47-111">La clase **CIM \_ FileStorage** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="e2e47-111">The **CIM\_FileStorage** class has these types of members:</span></span>

-   [<span data-ttu-id="e2e47-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="e2e47-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e2e47-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="e2e47-113">Properties</span></span>

<span data-ttu-id="e2e47-114">La clase **CIM \_ FileStorage** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="e2e47-114">The **CIM\_FileStorage** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e2e47-115">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="e2e47-115">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2e47-116">Tipo de datos **: \_ sistema de archivos CIM**</span><span class="sxs-lookup"><span data-stu-id="e2e47-116">Data type: **CIM\_FileSystem**</span></span>
</dt> <dt>

<span data-ttu-id="e2e47-117">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e2e47-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e2e47-118">Calificadores: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span><span class="sxs-lookup"><span data-stu-id="e2e47-118">Qualifiers: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span></span>
</dt> </dl>

<span data-ttu-id="e2e47-119">Un sistema de archivos [**CIM \_**](cim-filesystem.md) que describe el sistema de archivos.</span><span class="sxs-lookup"><span data-stu-id="e2e47-119">A [**CIM\_FileSystem**](cim-filesystem.md) describing the file system.</span></span>

</dd> <dt>

<span data-ttu-id="e2e47-120">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="e2e47-120">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2e47-121">Tipo de datos: **CIM \_ LogicalFile**</span><span class="sxs-lookup"><span data-stu-id="e2e47-121">Data type: **CIM\_LogicalFile**</span></span>
</dt> <dt>

<span data-ttu-id="e2e47-122">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e2e47-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e2e47-123">Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**débil**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="e2e47-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**Weak**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="e2e47-124">Un [**\_ LogicalFile de CIM**](cim-logicalfile.md) que describe el archivo lógico almacenado en el contexto del sistema de archivos.</span><span class="sxs-lookup"><span data-stu-id="e2e47-124">A [**CIM\_LogicalFile**](cim-logicalfile.md) describing the logical file stored in the context of the file system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e2e47-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e2e47-125">Remarks</span></span>

<span data-ttu-id="e2e47-126">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="e2e47-126">WMI does not implement this class.</span></span>

<span data-ttu-id="e2e47-127">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="e2e47-127">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="e2e47-128">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="e2e47-128">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="e2e47-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e2e47-129">Requirements</span></span>



| <span data-ttu-id="e2e47-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="e2e47-130">Requirement</span></span> | <span data-ttu-id="e2e47-131">Value</span><span class="sxs-lookup"><span data-stu-id="e2e47-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e2e47-132">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e2e47-132">Minimum supported client</span></span><br/> | <span data-ttu-id="e2e47-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e2e47-133">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e2e47-134">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e2e47-134">Minimum supported server</span></span><br/> | <span data-ttu-id="e2e47-135">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e2e47-135">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e2e47-136">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="e2e47-136">Namespace</span></span><br/>                | <span data-ttu-id="e2e47-137">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="e2e47-137">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="e2e47-138">MOF</span><span class="sxs-lookup"><span data-stu-id="e2e47-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e2e47-139"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e2e47-139"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="e2e47-140">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="e2e47-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e2e47-141"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e2e47-141"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e2e47-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="e2e47-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2e47-143">**\_Componente CIM**</span><span class="sxs-lookup"><span data-stu-id="e2e47-143">**CIM\_Component**</span></span>](cim-component.md)
</dt> </dl>

 

