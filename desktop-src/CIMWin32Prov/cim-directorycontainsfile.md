---
description: La \_ clase CIM DirectoryContainsFile representa una asociación entre un directorio y los archivos contenidos en ese directorio.
ms.assetid: e05ec86e-c3cf-4589-9815-83850e0c84ed
ms.tgt_platform: multiple
title: CIM_DirectoryContainsFile (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DirectoryContainsFile
- CIM_DirectoryContainsFile.PartComponent
- CIM_DirectoryContainsFile.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 8bd1913352d19a1ed5889413eed5e7fc4640ac53
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907367"
---
# <a name="cim_directorycontainsfile-class"></a><span data-ttu-id="7e7ef-103">\_Clase DirectoryContainsFile de CIM</span><span class="sxs-lookup"><span data-stu-id="7e7ef-103">CIM\_DirectoryContainsFile class</span></span>

<span data-ttu-id="7e7ef-104">La clase **CIM \_ DirectoryContainsFile** representa una asociación entre un directorio y los archivos contenidos en ese directorio.</span><span class="sxs-lookup"><span data-stu-id="7e7ef-104">The **CIM\_DirectoryContainsFile** class represents an association between a directory and files contained within that directory.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="7e7ef-105">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="7e7ef-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="7e7ef-106">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="7e7ef-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="7e7ef-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="7e7ef-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="7e7ef-108">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="7e7ef-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="7e7ef-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7e7ef-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{6F9D4740-8324-11d2-AAD9-006008C78BC7}"), AMENDMENT]
class CIM_DirectoryContainsFile : CIM_Component
{
  CIM_DataFile  REF PartComponent;
  CIM_Directory REF GroupComponent;
};
```

## <a name="members"></a><span data-ttu-id="7e7ef-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="7e7ef-110">Members</span></span>

<span data-ttu-id="7e7ef-111">La clase **CIM \_ DirectoryContainsFile** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="7e7ef-111">The **CIM\_DirectoryContainsFile** class has these types of members:</span></span>

-   [<span data-ttu-id="7e7ef-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="7e7ef-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7e7ef-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="7e7ef-113">Properties</span></span>

<span data-ttu-id="7e7ef-114">La clase **CIM \_ DirectoryContainsFile** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="7e7ef-114">The **CIM\_DirectoryContainsFile** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7e7ef-115">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="7e7ef-115">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7e7ef-116">Tipo de datos **: \_ directorio CIM**</span><span class="sxs-lookup"><span data-stu-id="7e7ef-116">Data type: **CIM\_Directory**</span></span>
</dt> <dt>

<span data-ttu-id="7e7ef-117">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7e7ef-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7e7ef-118">Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**máx**](/windows/desktop/WmiSdk/standard-qualifiers) . (1)</span><span class="sxs-lookup"><span data-stu-id="7e7ef-118">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="7e7ef-119">Un [**\_ directorio CIM**](cim-directory.md) que describe el directorio.</span><span class="sxs-lookup"><span data-stu-id="7e7ef-119">A [**CIM\_Directory**](cim-directory.md) that describes the directory.</span></span>

</dd> <dt>

<span data-ttu-id="7e7ef-120">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="7e7ef-120">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7e7ef-121">Tipo de datos **: \_ archivo** de datos CIM</span><span class="sxs-lookup"><span data-stu-id="7e7ef-121">Data type: **CIM\_DataFile**</span></span>
</dt> <dt>

<span data-ttu-id="7e7ef-122">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7e7ef-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7e7ef-123">Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="7e7ef-123">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="7e7ef-124">Un [**\_ archivo de archivos CIM**](cim-datafile.md) que describe el LogicalFile contenido en el directorio.</span><span class="sxs-lookup"><span data-stu-id="7e7ef-124">A [**CIM\_DataFile**](cim-datafile.md) that describes the LogicalFile contained within the directory.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7e7ef-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7e7ef-125">Remarks</span></span>

<span data-ttu-id="7e7ef-126">WMI implementa la clase **CIM \_ DirectoryContainsFile** , que es una clase dinámica.</span><span class="sxs-lookup"><span data-stu-id="7e7ef-126">WMI implements the **CIM\_DirectoryContainsFile** class, which is a dynamic class.</span></span>

<span data-ttu-id="7e7ef-127">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="7e7ef-127">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="7e7ef-128">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="7e7ef-128">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="7e7ef-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7e7ef-129">Requirements</span></span>



| <span data-ttu-id="7e7ef-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="7e7ef-130">Requirement</span></span> | <span data-ttu-id="7e7ef-131">Value</span><span class="sxs-lookup"><span data-stu-id="7e7ef-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7e7ef-132">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7e7ef-132">Minimum supported client</span></span><br/> | <span data-ttu-id="7e7ef-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7e7ef-133">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="7e7ef-134">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7e7ef-134">Minimum supported server</span></span><br/> | <span data-ttu-id="7e7ef-135">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7e7ef-135">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="7e7ef-136">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="7e7ef-136">Namespace</span></span><br/>                | <span data-ttu-id="7e7ef-137">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="7e7ef-137">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="7e7ef-138">MOF</span><span class="sxs-lookup"><span data-stu-id="7e7ef-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7e7ef-139"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7e7ef-139"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="7e7ef-140">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="7e7ef-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7e7ef-141"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7e7ef-141"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7e7ef-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="7e7ef-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7e7ef-143">**\_Componente CIM**</span><span class="sxs-lookup"><span data-stu-id="7e7ef-143">**CIM\_Component**</span></span>](cim-component.md)
</dt> </dl>

 

