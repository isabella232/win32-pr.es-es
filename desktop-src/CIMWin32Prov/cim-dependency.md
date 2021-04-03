---
description: La \_ clase de dependencia CIM representa una asociación que establece relaciones de dependencia entre objetos.
ms.assetid: ff0d6b50-0920-443e-a984-e6a9ab4402b1
ms.tgt_platform: multiple
title: CIM_Dependency (clase) (proveedores WMI de CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Dependency
- CIM_Dependency.Antecedent
- CIM_Dependency.Dependent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 8b95d45efff51128b08dc5b6395309f49e85a79e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807525"
---
# <a name="cim_dependency-class-cimwin32-wmi-providers"></a><span data-ttu-id="3d36d-103">CIM_Dependency (clase) (proveedores WMI de CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="3d36d-103">CIM_Dependency class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="3d36d-104">La clase de **\_ dependencia CIM** representa una asociación que establece relaciones de dependencia entre objetos.</span><span class="sxs-lookup"><span data-stu-id="3d36d-104">The **CIM\_Dependency** class represents an association that establishes dependency relationships between objects.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="3d36d-105">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="3d36d-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="3d36d-106">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="3d36d-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="3d36d-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="3d36d-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="3d36d-108">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="3d36d-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="3d36d-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3d36d-109">Syntax</span></span>

``` syntax
[Association, Abstract, UUID("{8502C53A-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_Dependency
{
  CIM_ManagedSystemElement REF Antecedent;
  CIM_ManagedSystemElement REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="3d36d-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="3d36d-110">Members</span></span>

<span data-ttu-id="3d36d-111">La clase de **\_ dependencia CIM** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="3d36d-111">The **CIM\_Dependency** class has these types of members:</span></span>

-   [<span data-ttu-id="3d36d-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="3d36d-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3d36d-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="3d36d-113">Properties</span></span>

<span data-ttu-id="3d36d-114">La clase de **\_ dependencia CIM** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="3d36d-114">The **CIM\_Dependency** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3d36d-115">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="3d36d-115">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3d36d-116">Tipo de datos **: \_ ManagedSystemElement de CIM**</span><span class="sxs-lookup"><span data-stu-id="3d36d-116">Data type: **CIM\_ManagedSystemElement**</span></span>
</dt> <dt>

<span data-ttu-id="3d36d-117">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3d36d-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3d36d-118">Referencia al objeto independiente de esta asociación.</span><span class="sxs-lookup"><span data-stu-id="3d36d-118">Reference to the independent object in this association.</span></span>

</dd> <dt>

<span data-ttu-id="3d36d-119">**Dependientes**</span><span class="sxs-lookup"><span data-stu-id="3d36d-119">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3d36d-120">Tipo de datos **: \_ ManagedSystemElement de CIM**</span><span class="sxs-lookup"><span data-stu-id="3d36d-120">Data type: **CIM\_ManagedSystemElement**</span></span>
</dt> <dt>

<span data-ttu-id="3d36d-121">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3d36d-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3d36d-122">Referencia al objeto que depende de la propiedad **antecedente** .</span><span class="sxs-lookup"><span data-stu-id="3d36d-122">Reference to the object that is dependent on the **Antecedent** property.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3d36d-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3d36d-123">Remarks</span></span>

<span data-ttu-id="3d36d-124">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="3d36d-124">WMI does not implement this class.</span></span> <span data-ttu-id="3d36d-125">Para obtener más información sobre las clases derivadas de la **\_ dependencia CIM**, vea [clases Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="3d36d-125">For more information about classes derived from **CIM\_Dependency**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="3d36d-126">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="3d36d-126">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="3d36d-127">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="3d36d-127">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="3d36d-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3d36d-128">Requirements</span></span>



| <span data-ttu-id="3d36d-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="3d36d-129">Requirement</span></span> | <span data-ttu-id="3d36d-130">Value</span><span class="sxs-lookup"><span data-stu-id="3d36d-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3d36d-131">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3d36d-131">Minimum supported client</span></span><br/> | <span data-ttu-id="3d36d-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3d36d-132">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="3d36d-133">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3d36d-133">Minimum supported server</span></span><br/> | <span data-ttu-id="3d36d-134">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3d36d-134">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="3d36d-135">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="3d36d-135">Namespace</span></span><br/>                | <span data-ttu-id="3d36d-136">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="3d36d-136">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="3d36d-137">MOF</span><span class="sxs-lookup"><span data-stu-id="3d36d-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3d36d-138"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3d36d-138"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="3d36d-139">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="3d36d-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3d36d-140"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3d36d-140"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

 




