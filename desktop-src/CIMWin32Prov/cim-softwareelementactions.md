---
description: La \_ Asociación SoftwareElementActions de CIM identifica las acciones de un elemento de software.
ms.assetid: 2f8a584c-dff0-48f8-bc5f-2b833b5c0b18
ms.tgt_platform: multiple
title: CIM_SoftwareElementActions (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SoftwareElementActions
- CIM_SoftwareElementActions.Action
- CIM_SoftwareElementActions.Element
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1f51cc122cdf354be9611ca1cca4ebcbe1635d14
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659441"
---
# <a name="cim_softwareelementactions-class"></a><span data-ttu-id="077f5-103">\_Clase SoftwareElementActions de CIM</span><span class="sxs-lookup"><span data-stu-id="077f5-103">CIM\_SoftwareElementActions class</span></span>

<span data-ttu-id="077f5-104">La **Asociación \_ SoftwareElementActions de CIM** identifica las acciones de un elemento de software.</span><span class="sxs-lookup"><span data-stu-id="077f5-104">The **CIM\_SoftwareElementActions** association identifies the actions for a software element.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="077f5-105">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="077f5-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="077f5-106">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="077f5-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="077f5-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="077f5-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="077f5-108">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="077f5-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="077f5-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="077f5-109">Syntax</span></span>

``` syntax
[UUID("{4B82D255-E3CD-11d2-8601-0000F8102E5F}"), Association, Aggregation, Abstract, AMENDMENT]
class CIM_SoftwareElementActions
{
  CIM_Action          REF Action;
  CIM_SoftwareElement REF Element;
};
```

## <a name="members"></a><span data-ttu-id="077f5-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="077f5-110">Members</span></span>

<span data-ttu-id="077f5-111">La clase **CIM \_ SoftwareElementActions** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="077f5-111">The **CIM\_SoftwareElementActions** class has these types of members:</span></span>

-   [<span data-ttu-id="077f5-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="077f5-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="077f5-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="077f5-113">Properties</span></span>

<span data-ttu-id="077f5-114">La clase **CIM \_ SoftwareElementActions** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="077f5-114">The **CIM\_SoftwareElementActions** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="077f5-115">**Acción**</span><span class="sxs-lookup"><span data-stu-id="077f5-115">**Action**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="077f5-116">Tipo de datos **: \_ acción de CIM**</span><span class="sxs-lookup"><span data-stu-id="077f5-116">Data type: **CIM\_Action**</span></span>
</dt> <dt>

<span data-ttu-id="077f5-117">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="077f5-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="077f5-118">Calificadores: [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (false), [**Weak**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="077f5-118">Qualifiers: [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (FALSE), [**Weak**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="077f5-119">Referencia a una instancia de [**\_ acción de CIM**](cim-action.md) .</span><span class="sxs-lookup"><span data-stu-id="077f5-119">Reference to a [**CIM\_Action**](cim-action.md) instance.</span></span>

</dd> <dt>

<span data-ttu-id="077f5-120">**Element**</span><span class="sxs-lookup"><span data-stu-id="077f5-120">**Element**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="077f5-121">Tipo de datos: **CIM \_ SoftwareElement**</span><span class="sxs-lookup"><span data-stu-id="077f5-121">Data type: **CIM\_SoftwareElement**</span></span>
</dt> <dt>

<span data-ttu-id="077f5-122">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="077f5-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="077f5-123">Calificadores: [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="077f5-123">Qualifiers: [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="077f5-124">Referencia a una instancia de [**\_ SoftwareElement de CIM**](cim-softwareelement.md) .</span><span class="sxs-lookup"><span data-stu-id="077f5-124">Reference to a [**CIM\_SoftwareElement**](cim-softwareelement.md) instance.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="077f5-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="077f5-125">Remarks</span></span>

<span data-ttu-id="077f5-126">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="077f5-126">WMI does not implement this class.</span></span> <span data-ttu-id="077f5-127">Para las clases WMI derivadas de **CIM \_ SoftwareElementActions**, vea [clases Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="077f5-127">For WMI classes derived from **CIM\_SoftwareElementActions**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="077f5-128">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="077f5-128">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="077f5-129">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="077f5-129">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="077f5-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="077f5-130">Requirements</span></span>



| <span data-ttu-id="077f5-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="077f5-131">Requirement</span></span> | <span data-ttu-id="077f5-132">Value</span><span class="sxs-lookup"><span data-stu-id="077f5-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="077f5-133">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="077f5-133">Minimum supported client</span></span><br/> | <span data-ttu-id="077f5-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="077f5-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="077f5-135">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="077f5-135">Minimum supported server</span></span><br/> | <span data-ttu-id="077f5-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="077f5-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="077f5-137">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="077f5-137">Namespace</span></span><br/>                | <span data-ttu-id="077f5-138">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="077f5-138">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="077f5-139">MOF</span><span class="sxs-lookup"><span data-stu-id="077f5-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="077f5-140"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="077f5-140"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="077f5-141">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="077f5-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="077f5-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="077f5-142"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

