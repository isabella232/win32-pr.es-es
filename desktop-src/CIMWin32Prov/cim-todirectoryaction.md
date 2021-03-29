---
description: La \_ Asociación ToDirectoryAction de CIM identifica el directorio de destino de la acción de archivo.
ms.assetid: f4dcd99c-4da8-447d-b6f7-7e3da63ca9c4
ms.tgt_platform: multiple
title: CIM_ToDirectoryAction (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ToDirectoryAction
- CIM_ToDirectoryAction.DestinationDirectory
- CIM_ToDirectoryAction.FileName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 10ed2f7c2e2b46e63e2cc02cc8e6ce09ab2688e0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807939"
---
# <a name="cim_todirectoryaction-class"></a><span data-ttu-id="17b57-103">\_Clase ToDirectoryAction de CIM</span><span class="sxs-lookup"><span data-stu-id="17b57-103">CIM\_ToDirectoryAction class</span></span>

<span data-ttu-id="17b57-104">La **Asociación \_ ToDirectoryAction de CIM** identifica el directorio de destino de la acción de archivo.</span><span class="sxs-lookup"><span data-stu-id="17b57-104">The **CIM\_ToDirectoryAction** association identifies the target directory for the file action.</span></span> <span data-ttu-id="17b57-105">Cuando se usa esta asociación, se supone que el directorio de destino fue creado por una acción anterior.</span><span class="sxs-lookup"><span data-stu-id="17b57-105">When this association is used, it is assumed that the target directory was created by a previous action.</span></span> <span data-ttu-id="17b57-106">Esta asociación no puede existir con una asociación [**\_ ToDirectorySpecification de CIM**](cim-todirectoryspecification.md) , ya que una acción de archivo solo puede incluir un único directorio de destino.</span><span class="sxs-lookup"><span data-stu-id="17b57-106">This association cannot exist with a [**CIM\_ToDirectorySpecification**](cim-todirectoryspecification.md) association since a file action can only involve a single target directory.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="17b57-107">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="17b57-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="17b57-108">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="17b57-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="17b57-109">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="17b57-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="17b57-110">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="17b57-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="17b57-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="17b57-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{B58D172E-DB31-11d2-85FC-0000F8102E5F}"), Association, AMENDMENT]
class CIM_ToDirectoryAction
{
  CIM_DirectoryAction REF DestinationDirectory;
  CIM_CopyFileAction  REF FileName;
};
```

## <a name="members"></a><span data-ttu-id="17b57-112">Miembros</span><span class="sxs-lookup"><span data-stu-id="17b57-112">Members</span></span>

<span data-ttu-id="17b57-113">La clase **CIM \_ ToDirectoryAction** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="17b57-113">The **CIM\_ToDirectoryAction** class has these types of members:</span></span>

-   [<span data-ttu-id="17b57-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="17b57-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="17b57-115">Propiedades</span><span class="sxs-lookup"><span data-stu-id="17b57-115">Properties</span></span>

<span data-ttu-id="17b57-116">La clase **CIM \_ ToDirectoryAction** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="17b57-116">The **CIM\_ToDirectoryAction** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="17b57-117">**DestinationDirectory**</span><span class="sxs-lookup"><span data-stu-id="17b57-117">**DestinationDirectory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="17b57-118">Tipo de datos: **CIM \_ DirectoryAction**</span><span class="sxs-lookup"><span data-stu-id="17b57-118">Data type: **CIM\_DirectoryAction**</span></span>
</dt> <dt>

<span data-ttu-id="17b57-119">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="17b57-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="17b57-120">Calificadores: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span><span class="sxs-lookup"><span data-stu-id="17b57-120">Qualifiers: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span></span>
</dt> </dl>

<span data-ttu-id="17b57-121">Referencia al directorio de destino.</span><span class="sxs-lookup"><span data-stu-id="17b57-121">Reference to the destination directory.</span></span>

</dd> <dt>

<span data-ttu-id="17b57-122">**FileName**</span><span class="sxs-lookup"><span data-stu-id="17b57-122">**FileName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="17b57-123">Tipo de datos: **CIM \_ CopyFileAction**</span><span class="sxs-lookup"><span data-stu-id="17b57-123">Data type: **CIM\_CopyFileAction**</span></span>
</dt> <dt>

<span data-ttu-id="17b57-124">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="17b57-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="17b57-125">Calificadores: [**mín**](/windows/desktop/WmiSdk/standard-qualifiers) . (0)</span><span class="sxs-lookup"><span data-stu-id="17b57-125">Qualifiers: [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span></span>
</dt> </dl>

<span data-ttu-id="17b57-126">Referencia al nombre de archivo.</span><span class="sxs-lookup"><span data-stu-id="17b57-126">Reference to the file name.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="17b57-127">Observaciones</span><span class="sxs-lookup"><span data-stu-id="17b57-127">Remarks</span></span>

<span data-ttu-id="17b57-128">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="17b57-128">WMI does not implement this class.</span></span>

<span data-ttu-id="17b57-129">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="17b57-129">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="17b57-130">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="17b57-130">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="17b57-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="17b57-131">Requirements</span></span>



| <span data-ttu-id="17b57-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="17b57-132">Requirement</span></span> | <span data-ttu-id="17b57-133">Value</span><span class="sxs-lookup"><span data-stu-id="17b57-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="17b57-134">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="17b57-134">Minimum supported client</span></span><br/> | <span data-ttu-id="17b57-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="17b57-135">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="17b57-136">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="17b57-136">Minimum supported server</span></span><br/> | <span data-ttu-id="17b57-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="17b57-137">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="17b57-138">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="17b57-138">Namespace</span></span><br/>                | <span data-ttu-id="17b57-139">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="17b57-139">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="17b57-140">MOF</span><span class="sxs-lookup"><span data-stu-id="17b57-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="17b57-141"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="17b57-141"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="17b57-142">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="17b57-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="17b57-143"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="17b57-143"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

