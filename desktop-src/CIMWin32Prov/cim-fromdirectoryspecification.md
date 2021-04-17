---
description: La \_ Asociación FromDirectorySpecification de CIM identifica el directorio de origen para la acción de archivo.
ms.assetid: 031ff95f-aa68-4b05-92a6-97a5e0d8956f
ms.tgt_platform: multiple
title: CIM_FromDirectorySpecification (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_FromDirectorySpecification
- CIM_FromDirectorySpecification.FileName
- CIM_FromDirectorySpecification.SourceDirectory
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 7690514b46d89bdf1aa926438456c49598034700
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659597"
---
# <a name="cim_fromdirectoryspecification-class"></a><span data-ttu-id="3ab3d-103">\_Clase FromDirectorySpecification de CIM</span><span class="sxs-lookup"><span data-stu-id="3ab3d-103">CIM\_FromDirectorySpecification class</span></span>

<span data-ttu-id="3ab3d-104">La **Asociación \_ FromDirectorySpecification de CIM** identifica el directorio de origen para la acción de archivo.</span><span class="sxs-lookup"><span data-stu-id="3ab3d-104">The **CIM\_FromDirectorySpecification** association identifies the source directory for the file action.</span></span> <span data-ttu-id="3ab3d-105">Cuando se usa esta asociación, se supone que el directorio de origen ya existe.</span><span class="sxs-lookup"><span data-stu-id="3ab3d-105">When this association is used, the assumption is that the source directory already exists.</span></span> <span data-ttu-id="3ab3d-106">Esta asociación no puede existir con una asociación [**\_ FromDirectoryAction de CIM**](cim-fromdirectoryaction.md) ; una acción de archivo solo puede incluir un único directorio de origen.</span><span class="sxs-lookup"><span data-stu-id="3ab3d-106">This association cannot exist with a [**CIM\_FromDirectoryAction**](cim-fromdirectoryaction.md) association; a file action can only involve a single source directory.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="3ab3d-107">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="3ab3d-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="3ab3d-108">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="3ab3d-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="3ab3d-109">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="3ab3d-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="3ab3d-110">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="3ab3d-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="3ab3d-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3ab3d-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{6715375E-DB2A-11d2-85FC-0000F8102E5F}"), Association, AMENDMENT]
class CIM_FromDirectorySpecification
{
  CIM_FileAction             REF FileName;
  CIM_DirectorySpecification REF SourceDirectory;
};
```

## <a name="members"></a><span data-ttu-id="3ab3d-112">Miembros</span><span class="sxs-lookup"><span data-stu-id="3ab3d-112">Members</span></span>

<span data-ttu-id="3ab3d-113">La clase **CIM \_ FromDirectorySpecification** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="3ab3d-113">The **CIM\_FromDirectorySpecification** class has these types of members:</span></span>

-   [<span data-ttu-id="3ab3d-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="3ab3d-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3ab3d-115">Propiedades</span><span class="sxs-lookup"><span data-stu-id="3ab3d-115">Properties</span></span>

<span data-ttu-id="3ab3d-116">La clase **CIM \_ FromDirectorySpecification** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="3ab3d-116">The **CIM\_FromDirectorySpecification** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3ab3d-117">**FileName**</span><span class="sxs-lookup"><span data-stu-id="3ab3d-117">**FileName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ab3d-118">Tipo de datos: **CIM \_ FileAction**</span><span class="sxs-lookup"><span data-stu-id="3ab3d-118">Data type: **CIM\_FileAction**</span></span>
</dt> <dt>

<span data-ttu-id="3ab3d-119">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3ab3d-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3ab3d-120">Calificadores: [**mín**](/windows/desktop/WmiSdk/standard-qualifiers) . (0)</span><span class="sxs-lookup"><span data-stu-id="3ab3d-120">Qualifiers: [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span></span>
</dt> </dl>

<span data-ttu-id="3ab3d-121">Referencia al nombre de archivo.</span><span class="sxs-lookup"><span data-stu-id="3ab3d-121">Reference to the file name.</span></span>

</dd> <dt>

<span data-ttu-id="3ab3d-122">**SourceDirectory**</span><span class="sxs-lookup"><span data-stu-id="3ab3d-122">**SourceDirectory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ab3d-123">Tipo de datos: **CIM \_ DirectorySpecification**</span><span class="sxs-lookup"><span data-stu-id="3ab3d-123">Data type: **CIM\_DirectorySpecification**</span></span>
</dt> <dt>

<span data-ttu-id="3ab3d-124">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3ab3d-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3ab3d-125">Calificadores: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span><span class="sxs-lookup"><span data-stu-id="3ab3d-125">Qualifiers: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span></span>
</dt> </dl>

<span data-ttu-id="3ab3d-126">Referencia al directorio de origen.</span><span class="sxs-lookup"><span data-stu-id="3ab3d-126">Reference to the source directory.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3ab3d-127">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3ab3d-127">Remarks</span></span>

<span data-ttu-id="3ab3d-128">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="3ab3d-128">WMI does not implement this class.</span></span>

<span data-ttu-id="3ab3d-129">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="3ab3d-129">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="3ab3d-130">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="3ab3d-130">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="3ab3d-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3ab3d-131">Requirements</span></span>



| <span data-ttu-id="3ab3d-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="3ab3d-132">Requirement</span></span> | <span data-ttu-id="3ab3d-133">Value</span><span class="sxs-lookup"><span data-stu-id="3ab3d-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3ab3d-134">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3ab3d-134">Minimum supported client</span></span><br/> | <span data-ttu-id="3ab3d-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3ab3d-135">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="3ab3d-136">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3ab3d-136">Minimum supported server</span></span><br/> | <span data-ttu-id="3ab3d-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3ab3d-137">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="3ab3d-138">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="3ab3d-138">Namespace</span></span><br/>                | <span data-ttu-id="3ab3d-139">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="3ab3d-139">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="3ab3d-140">MOF</span><span class="sxs-lookup"><span data-stu-id="3ab3d-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3ab3d-141"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3ab3d-141"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="3ab3d-142">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="3ab3d-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3ab3d-143"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3ab3d-143"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

