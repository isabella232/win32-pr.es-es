---
description: La \_ Asociación DirectorySpecificationFile de CIM representa el directorio que contiene el archivo especificado al hacer referencia a la \_ clase DIRECTORYSPECIFICATION de CIM.
ms.assetid: 57fe996e-6bd4-4070-9e99-460b2a36243f
ms.tgt_platform: multiple
title: CIM_DirectorySpecificationFile (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DirectorySpecificationFile
- CIM_DirectorySpecificationFile.DirectorySpecification
- CIM_DirectorySpecificationFile.FileSpecification
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1877d9864a76334c2b2e00fc7822adb09b91028b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153279"
---
# <a name="cim_directoryspecificationfile-class"></a><span data-ttu-id="797b9-103">\_Clase DirectorySpecificationFile de CIM</span><span class="sxs-lookup"><span data-stu-id="797b9-103">CIM\_DirectorySpecificationFile class</span></span>

<span data-ttu-id="797b9-104">La **Asociación \_ DirectorySpecificationFile de CIM** representa el directorio que contiene el archivo especificado al hacer referencia a la clase [**\_ DirectorySpecification de CIM**](cim-directoryspecification.md) .</span><span class="sxs-lookup"><span data-stu-id="797b9-104">The **CIM\_DirectorySpecificationFile** association represents the directory that contains the file specified by referencing the [**CIM\_DirectorySpecification**](cim-directoryspecification.md) class.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="797b9-105">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="797b9-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="797b9-106">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="797b9-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="797b9-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="797b9-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="797b9-108">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="797b9-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="797b9-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="797b9-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{BCD64CCE-DB29-11d2-85FC-0000F8102E5F}"), Association, AMENDMENT]
class CIM_DirectorySpecificationFile
{
  CIM_DirectorySpecification REF DirectorySpecification;
  CIM_FileSpecification      REF FileSpecification;
};
```

## <a name="members"></a><span data-ttu-id="797b9-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="797b9-110">Members</span></span>

<span data-ttu-id="797b9-111">La clase **CIM \_ DirectorySpecificationFile** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="797b9-111">The **CIM\_DirectorySpecificationFile** class has these types of members:</span></span>

-   [<span data-ttu-id="797b9-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="797b9-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="797b9-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="797b9-113">Properties</span></span>

<span data-ttu-id="797b9-114">La clase **CIM \_ DirectorySpecificationFile** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="797b9-114">The **CIM\_DirectorySpecificationFile** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="797b9-115">**DirectorySpecification**</span><span class="sxs-lookup"><span data-stu-id="797b9-115">**DirectorySpecification**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="797b9-116">Tipo de datos: **CIM \_ DirectorySpecification**</span><span class="sxs-lookup"><span data-stu-id="797b9-116">Data type: **CIM\_DirectorySpecification**</span></span>
</dt> <dt>

<span data-ttu-id="797b9-117">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="797b9-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="797b9-118">Calificadores: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span><span class="sxs-lookup"><span data-stu-id="797b9-118">Qualifiers: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span></span>
</dt> </dl>

<span data-ttu-id="797b9-119">Referencia a la especificación del directorio.</span><span class="sxs-lookup"><span data-stu-id="797b9-119">Reference to the directory specification.</span></span>

</dd> <dt>

<span data-ttu-id="797b9-120">**FileSpecification**</span><span class="sxs-lookup"><span data-stu-id="797b9-120">**FileSpecification**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="797b9-121">Tipo de datos: **CIM \_ FileSpecification**</span><span class="sxs-lookup"><span data-stu-id="797b9-121">Data type: **CIM\_FileSpecification**</span></span>
</dt> <dt>

<span data-ttu-id="797b9-122">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="797b9-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="797b9-123">Calificadores: [**mín**](/windows/desktop/WmiSdk/standard-qualifiers) . (0)</span><span class="sxs-lookup"><span data-stu-id="797b9-123">Qualifiers: [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span></span>
</dt> </dl>

<span data-ttu-id="797b9-124">Referencia a la especificación del archivo.</span><span class="sxs-lookup"><span data-stu-id="797b9-124">Reference to the file specification.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="797b9-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="797b9-125">Remarks</span></span>

<span data-ttu-id="797b9-126">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="797b9-126">WMI does not implement this class.</span></span>

<span data-ttu-id="797b9-127">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="797b9-127">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="797b9-128">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="797b9-128">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="797b9-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="797b9-129">Requirements</span></span>



| <span data-ttu-id="797b9-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="797b9-130">Requirement</span></span> | <span data-ttu-id="797b9-131">Value</span><span class="sxs-lookup"><span data-stu-id="797b9-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="797b9-132">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="797b9-132">Minimum supported client</span></span><br/> | <span data-ttu-id="797b9-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="797b9-133">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="797b9-134">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="797b9-134">Minimum supported server</span></span><br/> | <span data-ttu-id="797b9-135">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="797b9-135">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="797b9-136">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="797b9-136">Namespace</span></span><br/>                | <span data-ttu-id="797b9-137">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="797b9-137">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="797b9-138">MOF</span><span class="sxs-lookup"><span data-stu-id="797b9-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="797b9-139"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="797b9-139"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="797b9-140">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="797b9-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="797b9-141"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="797b9-141"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

