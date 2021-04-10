---
description: Una clase de asociación Modelo de información común (CIM) que establece relaciones entre un sistema y los elementos del sistema administrados en los que se compone.
ms.assetid: 11ad6dc1-a09a-4bab-bb1d-2131a8fdb812
ms.tgt_platform: multiple
title: CIM_SystemComponent (clase) (proveedores WMI de CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SystemComponent
- CIM_SystemComponent.PartComponent
- CIM_SystemComponent.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 9d9aae4e4ef916916f54bddea814844f23ed7315
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153238"
---
# <a name="cim_systemcomponent-class-cimwin32-wmi-providers"></a><span data-ttu-id="5aca8-103">CIM_SystemComponent (clase) (proveedores WMI de CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="5aca8-103">CIM_SystemComponent class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="5aca8-104">La **clase \_ SystemComponent de CIM** es una clase de asociación modelo de información común (CIM) que establece relaciones entre un sistema y los elementos del sistema administrados en los que se compone.</span><span class="sxs-lookup"><span data-stu-id="5aca8-104">The **CIM\_SystemComponent** class is a Common Information Model (CIM) association class that establishes relationships between a system and the managed system elements of which it is composed.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="5aca8-105">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="5aca8-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="5aca8-106">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="5aca8-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="5aca8-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="5aca8-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="5aca8-108">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="5aca8-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="5aca8-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5aca8-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{527BC6CE-BAFE-11d2-85E5-0000F8102E5F}"), AMENDMENT]
class CIM_SystemComponent : CIM_Component
{
  CIM_ManagedSystemElement REF PartComponent;
  CIM_System               REF GroupComponent;
};
```

## <a name="members"></a><span data-ttu-id="5aca8-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="5aca8-110">Members</span></span>

<span data-ttu-id="5aca8-111">La clase **CIM \_ SystemComponent** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="5aca8-111">The **CIM\_SystemComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="5aca8-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="5aca8-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5aca8-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="5aca8-113">Properties</span></span>

<span data-ttu-id="5aca8-114">La clase **CIM \_ SystemComponent** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="5aca8-114">The **CIM\_SystemComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5aca8-115">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="5aca8-115">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5aca8-116">Tipo de datos **: \_ Sistema CIM**</span><span class="sxs-lookup"><span data-stu-id="5aca8-116">Data type: **CIM\_System**</span></span>
</dt> <dt>

<span data-ttu-id="5aca8-117">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5aca8-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5aca8-118">Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span><span class="sxs-lookup"><span data-stu-id="5aca8-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span></span>
</dt> </dl>

<span data-ttu-id="5aca8-119">[**\_ Sistema CIM**](cim-system.md) que describe el sistema primario de la asociación.</span><span class="sxs-lookup"><span data-stu-id="5aca8-119">A [**CIM\_System**](cim-system.md) that describes the parent system in the association.</span></span>

</dd> <dt>

<span data-ttu-id="5aca8-120">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="5aca8-120">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5aca8-121">Tipo de datos **: \_ ManagedSystemElement de CIM**</span><span class="sxs-lookup"><span data-stu-id="5aca8-121">Data type: **CIM\_ManagedSystemElement**</span></span>
</dt> <dt>

<span data-ttu-id="5aca8-122">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5aca8-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5aca8-123">Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="5aca8-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="5aca8-124">Un [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md) que describe el elemento secundario que es un componente de un sistema.</span><span class="sxs-lookup"><span data-stu-id="5aca8-124">A [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md) that describes the child element that is a component of a system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5aca8-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5aca8-125">Remarks</span></span>

<span data-ttu-id="5aca8-126">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="5aca8-126">WMI does not implement this class.</span></span> <span data-ttu-id="5aca8-127">Para las clases WMI derivadas de **CIM \_ SystemComponent**, vea [clases Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="5aca8-127">For WMI classes derived from **CIM\_SystemComponent**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="5aca8-128">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="5aca8-128">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="5aca8-129">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="5aca8-129">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="5aca8-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5aca8-130">Requirements</span></span>



| <span data-ttu-id="5aca8-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="5aca8-131">Requirement</span></span> | <span data-ttu-id="5aca8-132">Value</span><span class="sxs-lookup"><span data-stu-id="5aca8-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5aca8-133">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5aca8-133">Minimum supported client</span></span><br/> | <span data-ttu-id="5aca8-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5aca8-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="5aca8-135">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5aca8-135">Minimum supported server</span></span><br/> | <span data-ttu-id="5aca8-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5aca8-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="5aca8-137">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="5aca8-137">Namespace</span></span><br/>                | <span data-ttu-id="5aca8-138">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="5aca8-138">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="5aca8-139">MOF</span><span class="sxs-lookup"><span data-stu-id="5aca8-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5aca8-140"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5aca8-140"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="5aca8-141">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="5aca8-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5aca8-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5aca8-142"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5aca8-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="5aca8-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5aca8-144">**\_Componente CIM**</span><span class="sxs-lookup"><span data-stu-id="5aca8-144">**CIM\_Component**</span></span>](cim-component.md)
</dt> </dl>

 

