---
description: La \_ Asociación de componentes CIM representa las partes de una relación entre MSEs.
ms.assetid: a074e2f7-b092-4d3c-be5e-2069b643431b
ms.tgt_platform: multiple
title: CIM_Component (clase) (proveedores WMI de CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Component
- CIM_Component.GroupComponent
- CIM_Component.PartComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 8b516118bc0cd6f12285933b1c15e7f2801ad40d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907334"
---
# <a name="cim_component-class-cimwin32-wmi-providers"></a><span data-ttu-id="b5cfd-103">CIM_Component (clase) (proveedores WMI de CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="b5cfd-103">CIM_Component class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="b5cfd-104">La Asociación de **\_ componentes CIM** representa las partes de una relación entre MSEs.</span><span class="sxs-lookup"><span data-stu-id="b5cfd-104">The **CIM\_Component** association represents the parts of a relationship between MSEs.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b5cfd-105">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="b5cfd-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="b5cfd-106">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="b5cfd-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="b5cfd-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="b5cfd-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="b5cfd-108">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="b5cfd-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="b5cfd-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b5cfd-109">Syntax</span></span>

``` syntax
[Association, Abstract, Aggregation, UUID("{8502C573-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_Component
{
  CIM_ManagedSystemElement REF GroupComponent;
  CIM_ManagedSystemElement REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="b5cfd-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="b5cfd-110">Members</span></span>

<span data-ttu-id="b5cfd-111">La clase de **\_ componentes CIM** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="b5cfd-111">The **CIM\_Component** class has these types of members:</span></span>

-   [<span data-ttu-id="b5cfd-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b5cfd-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b5cfd-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b5cfd-113">Properties</span></span>

<span data-ttu-id="b5cfd-114">La clase de **\_ componentes CIM** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="b5cfd-114">The **CIM\_Component** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b5cfd-115">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="b5cfd-115">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5cfd-116">Tipo de datos **: \_ ManagedSystemElement de CIM**</span><span class="sxs-lookup"><span data-stu-id="b5cfd-116">Data type: **CIM\_ManagedSystemElement**</span></span>
</dt> <dt>

<span data-ttu-id="b5cfd-117">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b5cfd-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b5cfd-118">Calificadores: [ **agregado**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="b5cfd-118">Qualifiers: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="b5cfd-119">Un [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md) que describe el elemento primario de la asociación.</span><span class="sxs-lookup"><span data-stu-id="b5cfd-119">A [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md) that describes the parent element in the association.</span></span>

</dd> <dt>

<span data-ttu-id="b5cfd-120">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="b5cfd-120">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b5cfd-121">Tipo de datos **: \_ ManagedSystemElement de CIM**</span><span class="sxs-lookup"><span data-stu-id="b5cfd-121">Data type: **CIM\_ManagedSystemElement**</span></span>
</dt> <dt>

<span data-ttu-id="b5cfd-122">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b5cfd-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b5cfd-123">Un [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md) que describe el elemento secundario de la asociación.</span><span class="sxs-lookup"><span data-stu-id="b5cfd-123">A [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md) that describes the child element in the association.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b5cfd-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b5cfd-124">Remarks</span></span>

<span data-ttu-id="b5cfd-125">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="b5cfd-125">WMI does not implement this class.</span></span> <span data-ttu-id="b5cfd-126">Para obtener más información sobre las clases derivadas del **\_ componente CIM**, vea [clases Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="b5cfd-126">For more information about classes derived from **CIM\_Component**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="b5cfd-127">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="b5cfd-127">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="b5cfd-128">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="b5cfd-128">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="b5cfd-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b5cfd-129">Requirements</span></span>



| <span data-ttu-id="b5cfd-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="b5cfd-130">Requirement</span></span> | <span data-ttu-id="b5cfd-131">Value</span><span class="sxs-lookup"><span data-stu-id="b5cfd-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b5cfd-132">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b5cfd-132">Minimum supported client</span></span><br/> | <span data-ttu-id="b5cfd-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b5cfd-133">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b5cfd-134">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b5cfd-134">Minimum supported server</span></span><br/> | <span data-ttu-id="b5cfd-135">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b5cfd-135">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b5cfd-136">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="b5cfd-136">Namespace</span></span><br/>                | <span data-ttu-id="b5cfd-137">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="b5cfd-137">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="b5cfd-138">MOF</span><span class="sxs-lookup"><span data-stu-id="b5cfd-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b5cfd-139"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b5cfd-139"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="b5cfd-140">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b5cfd-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b5cfd-141"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b5cfd-141"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

