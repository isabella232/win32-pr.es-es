---
description: La \_ clase CIM LogicalIdentity es una asociación abstracta y genérica que indica que dos elementos lógicos representan distintos aspectos de la misma entidad subyacente.
ms.assetid: 624a52bf-001d-4f18-af77-87a5d1cfa1ff
ms.tgt_platform: multiple
title: CIM_LogicalIdentity (clase) (proveedores WMI de CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalIdentity
- CIM_LogicalIdentity.SameElement
- CIM_LogicalIdentity.SystemElement
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 52780144a48cbb424ee037f71a56e238bb864311
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103998171"
---
# <a name="cim_logicalidentity-class-cimwin32-wmi-providers"></a><span data-ttu-id="706b7-103">CIM_LogicalIdentity (clase) (proveedores WMI de CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="706b7-103">CIM_LogicalIdentity class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="706b7-104">La clase **CIM \_ LogicalIdentity** es una asociación abstracta y genérica que indica que dos elementos lógicos representan distintos aspectos de la misma entidad subyacente.</span><span class="sxs-lookup"><span data-stu-id="706b7-104">The **CIM\_LogicalIdentity** class is an abstract and generic association that indicates that two logical elements represent different aspects of the same underlying entity.</span></span> <span data-ttu-id="706b7-105">La Asociación transmite lo que se puede definir con varias herencia y está restringido a los aspectos lógicos de un elemento del sistema administrado.</span><span class="sxs-lookup"><span data-stu-id="706b7-105">The association conveys what can be defined with multiple inheritance and is restricted to the logical aspects of a managed system element.</span></span> <span data-ttu-id="706b7-106">En la mayoría de los escenarios, la relación de identidad viene determinada por la equivalencia de claves u otras propiedades de identificación de los elementos relacionados.</span><span class="sxs-lookup"><span data-stu-id="706b7-106">In most scenarios, the identity relationship is determined by the equivalence of keys, or some other identifying properties of the related elements.</span></span>

<span data-ttu-id="706b7-107">La Asociación solo se debe usar en escenarios que se hayan entendido bien, lo que permite una mayor definición y aclaración concretas en las subclases.</span><span class="sxs-lookup"><span data-stu-id="706b7-107">The association should only be used in scenarios that are well understood, allowing more concrete definition and clarification in subclasses.</span></span> <span data-ttu-id="706b7-108">Un escenario en el que la relación es razonable, por ejemplo, representa un dispositivo que es una entidad de bus y una entidad funcional en la que el dispositivo es una entidad USB (bus) y de teclado (funcional).</span><span class="sxs-lookup"><span data-stu-id="706b7-108">A scenario where the relationship is reasonable, for example, represents a device that is both a bus entity and a functional entity where the device is a USB (bus) and keyboard (functional) entity.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="706b7-109">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="706b7-109">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="706b7-110">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="706b7-110">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="706b7-111">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="706b7-111">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="706b7-112">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="706b7-112">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="706b7-113">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="706b7-113">Syntax</span></span>

``` syntax
class CIM_LogicalIdentity
{
  CIM_LogicalElement REF SameElement;
  CIM_LogicalElement REF SystemElement;
};
```

## <a name="members"></a><span data-ttu-id="706b7-114">Miembros</span><span class="sxs-lookup"><span data-stu-id="706b7-114">Members</span></span>

<span data-ttu-id="706b7-115">La clase **CIM \_ LogicalIdentity** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="706b7-115">The **CIM\_LogicalIdentity** class has these types of members:</span></span>

-   [<span data-ttu-id="706b7-116">Propiedades</span><span class="sxs-lookup"><span data-stu-id="706b7-116">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="706b7-117">Propiedades</span><span class="sxs-lookup"><span data-stu-id="706b7-117">Properties</span></span>

<span data-ttu-id="706b7-118">La clase **CIM \_ LogicalIdentity** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="706b7-118">The **CIM\_LogicalIdentity** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="706b7-119">**SameElement**</span><span class="sxs-lookup"><span data-stu-id="706b7-119">**SameElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="706b7-120">Tipo de datos: **CIM \_ LogicalElement**</span><span class="sxs-lookup"><span data-stu-id="706b7-120">Data type: **CIM\_LogicalElement**</span></span>
</dt> <dt>

<span data-ttu-id="706b7-121">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="706b7-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="706b7-122">Referencia a un aspecto alternativo de la entidad del sistema.</span><span class="sxs-lookup"><span data-stu-id="706b7-122">Reference to an alternate aspect of the system entity.</span></span>

</dd> <dt>

<span data-ttu-id="706b7-123">**SystemElement**</span><span class="sxs-lookup"><span data-stu-id="706b7-123">**SystemElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="706b7-124">Tipo de datos: **CIM \_ LogicalElement**</span><span class="sxs-lookup"><span data-stu-id="706b7-124">Data type: **CIM\_LogicalElement**</span></span>
</dt> <dt>

<span data-ttu-id="706b7-125">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="706b7-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="706b7-126">Referencia a un aspecto del elemento lógico.</span><span class="sxs-lookup"><span data-stu-id="706b7-126">Reference to one aspect of the logical element.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="706b7-127">Observaciones</span><span class="sxs-lookup"><span data-stu-id="706b7-127">Remarks</span></span>

<span data-ttu-id="706b7-128">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="706b7-128">WMI does not implement this class.</span></span> <span data-ttu-id="706b7-129">Para las clases derivadas de **CIM \_ LogicalIdentity**, vea [clases Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="706b7-129">For classes derived from **CIM\_LogicalIdentity**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="706b7-130">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="706b7-130">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="706b7-131">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="706b7-131">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="706b7-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="706b7-132">Requirements</span></span>



| <span data-ttu-id="706b7-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="706b7-133">Requirement</span></span> | <span data-ttu-id="706b7-134">Value</span><span class="sxs-lookup"><span data-stu-id="706b7-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="706b7-135">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="706b7-135">Minimum supported client</span></span><br/> | <span data-ttu-id="706b7-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="706b7-136">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="706b7-137">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="706b7-137">Minimum supported server</span></span><br/> | <span data-ttu-id="706b7-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="706b7-138">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="706b7-139">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="706b7-139">Namespace</span></span><br/>                | <span data-ttu-id="706b7-140">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="706b7-140">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="706b7-141">MOF</span><span class="sxs-lookup"><span data-stu-id="706b7-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="706b7-142"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="706b7-142"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="706b7-143">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="706b7-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="706b7-144"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="706b7-144"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

 




