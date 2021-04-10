---
description: La \_ Asociación ToDirectorySpecification de CIM identifica el directorio de destino de la acción de archivo.
ms.assetid: ab31101f-1948-4b3d-baef-0d61d5898b21
ms.tgt_platform: multiple
title: CIM_ToDirectorySpecification (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ToDirectorySpecification
- CIM_ToDirectorySpecification.DestinationDirectory
- CIM_ToDirectorySpecification.FileName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: e0728f605e02195a6bf2bd4beb0ca67fe8744e12
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153572"
---
# <a name="cim_todirectoryspecification-class"></a><span data-ttu-id="a52ae-103">\_Clase ToDirectorySpecification de CIM</span><span class="sxs-lookup"><span data-stu-id="a52ae-103">CIM\_ToDirectorySpecification class</span></span>

<span data-ttu-id="a52ae-104">La **Asociación \_ ToDirectorySpecification de CIM** identifica el directorio de destino de la acción de archivo.</span><span class="sxs-lookup"><span data-stu-id="a52ae-104">The **CIM\_ToDirectorySpecification** association identifies the target directory for the file action.</span></span> <span data-ttu-id="a52ae-105">Cuando se usa esta asociación, se supone que ya existe el directorio de destino.</span><span class="sxs-lookup"><span data-stu-id="a52ae-105">When this association is used, it is assumed that the target directory already existed.</span></span> <span data-ttu-id="a52ae-106">Esta asociación no puede existir con una asociación [**\_ ToDirectoryAction de CIM**](cim-todirectoryaction.md) , ya que una acción de archivo solo puede incluir un único directorio de destino.</span><span class="sxs-lookup"><span data-stu-id="a52ae-106">This association cannot exist with a [**CIM\_ToDirectoryAction**](cim-todirectoryaction.md) association since a file action can only involve a single target directory.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a52ae-107">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="a52ae-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="a52ae-108">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="a52ae-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="a52ae-109">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="a52ae-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="a52ae-110">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="a52ae-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="a52ae-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a52ae-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{C3E25A3C-DB31-11d2-85FC-0000F8102E5F}"), Association, AMENDMENT]
class CIM_ToDirectorySpecification
{
  CIM_DirectorySpecification REF DestinationDirectory;
  CIM_CopyFileAction         REF FileName;
};
```

## <a name="members"></a><span data-ttu-id="a52ae-112">Miembros</span><span class="sxs-lookup"><span data-stu-id="a52ae-112">Members</span></span>

<span data-ttu-id="a52ae-113">La clase **CIM \_ ToDirectorySpecification** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="a52ae-113">The **CIM\_ToDirectorySpecification** class has these types of members:</span></span>

-   [<span data-ttu-id="a52ae-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="a52ae-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a52ae-115">Propiedades</span><span class="sxs-lookup"><span data-stu-id="a52ae-115">Properties</span></span>

<span data-ttu-id="a52ae-116">La clase **CIM \_ ToDirectorySpecification** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="a52ae-116">The **CIM\_ToDirectorySpecification** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a52ae-117">**DestinationDirectory**</span><span class="sxs-lookup"><span data-stu-id="a52ae-117">**DestinationDirectory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a52ae-118">Tipo de datos: **CIM \_ DirectorySpecification**</span><span class="sxs-lookup"><span data-stu-id="a52ae-118">Data type: **CIM\_DirectorySpecification**</span></span>
</dt> <dt>

<span data-ttu-id="a52ae-119">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a52ae-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a52ae-120">Calificadores: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span><span class="sxs-lookup"><span data-stu-id="a52ae-120">Qualifiers: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span></span>
</dt> </dl>

<span data-ttu-id="a52ae-121">Referencia al directorio de destino.</span><span class="sxs-lookup"><span data-stu-id="a52ae-121">Reference to the destination directory.</span></span>

</dd> <dt>

<span data-ttu-id="a52ae-122">**FileName**</span><span class="sxs-lookup"><span data-stu-id="a52ae-122">**FileName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a52ae-123">Tipo de datos: **CIM \_ CopyFileAction**</span><span class="sxs-lookup"><span data-stu-id="a52ae-123">Data type: **CIM\_CopyFileAction**</span></span>
</dt> <dt>

<span data-ttu-id="a52ae-124">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a52ae-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a52ae-125">Calificadores: [**mín**](/windows/desktop/WmiSdk/standard-qualifiers) . (0)</span><span class="sxs-lookup"><span data-stu-id="a52ae-125">Qualifiers: [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span></span>
</dt> </dl>

<span data-ttu-id="a52ae-126">Referencia al nombre de archivo.</span><span class="sxs-lookup"><span data-stu-id="a52ae-126">Reference to the file name.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a52ae-127">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a52ae-127">Remarks</span></span>

<span data-ttu-id="a52ae-128">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="a52ae-128">WMI does not implement this class.</span></span>

<span data-ttu-id="a52ae-129">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="a52ae-129">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="a52ae-130">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="a52ae-130">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="a52ae-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a52ae-131">Requirements</span></span>



| <span data-ttu-id="a52ae-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="a52ae-132">Requirement</span></span> | <span data-ttu-id="a52ae-133">Value</span><span class="sxs-lookup"><span data-stu-id="a52ae-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a52ae-134">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a52ae-134">Minimum supported client</span></span><br/> | <span data-ttu-id="a52ae-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a52ae-135">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a52ae-136">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a52ae-136">Minimum supported server</span></span><br/> | <span data-ttu-id="a52ae-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a52ae-137">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a52ae-138">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="a52ae-138">Namespace</span></span><br/>                | <span data-ttu-id="a52ae-139">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="a52ae-139">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="a52ae-140">MOF</span><span class="sxs-lookup"><span data-stu-id="a52ae-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a52ae-141"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a52ae-141"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="a52ae-142">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="a52ae-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a52ae-143"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a52ae-143"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

