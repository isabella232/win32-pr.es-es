---
description: La \_ clase de asociación CIM SoftwareElementChecks relaciona un elemento de software con información de condición o ubicación que una característica puede necesitar.
ms.assetid: ff130fe9-ddb2-4e4f-86d3-53f1d8ed14aa
ms.tgt_platform: multiple
title: CIM_SoftwareElementChecks (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SoftwareElementChecks
- CIM_SoftwareElementChecks.Check
- CIM_SoftwareElementChecks.Element
- CIM_SoftwareElementChecks.Phase
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: ea6fcb02794174e825994f70270745741c9b7713
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907086"
---
# <a name="cim_softwareelementchecks-class"></a><span data-ttu-id="391c4-103">\_Clase SoftwareElementChecks de CIM</span><span class="sxs-lookup"><span data-stu-id="391c4-103">CIM\_SoftwareElementChecks class</span></span>

<span data-ttu-id="391c4-104">La clase de asociación **CIM \_ SoftwareElementChecks** relaciona un elemento de software con información de condición o ubicación que una característica puede necesitar.</span><span class="sxs-lookup"><span data-stu-id="391c4-104">The **CIM\_SoftwareElementChecks** association class relates a software element with condition or location information that a feature may require.</span></span>

<span data-ttu-id="391c4-105">Dado que los elementos de software en un estado listo para ejecutar no pueden pasar a otro Estado, el valor de la propiedad **Phase** está restringido a en estado para los objetos [**\_ SoftwareElement de CIM**](cim-softwareelement.md) en un estado listo para ejecutarse.</span><span class="sxs-lookup"><span data-stu-id="391c4-105">Because software elements in a ready-to-run state cannot transition into another state, the value of the **Phase** property is restricted to in-state for [**CIM\_SoftwareElement**](cim-softwareelement.md) objects in a ready-to-run state.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="391c4-106">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="391c4-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="391c4-107">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="391c4-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="391c4-108">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="391c4-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="391c4-109">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="391c4-109">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="391c4-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="391c4-110">Syntax</span></span>

``` syntax
[UUID("{24783E8A-DB31-11d2-85FC-0000F8102E5F}"), Association, Aggregation, Abstract, AMENDMENT]
class CIM_SoftwareElementChecks
{
  CIM_Check           REF Check;
  CIM_SoftwareElement REF Element;
  uint16                  Phase;
};
```

## <a name="members"></a><span data-ttu-id="391c4-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="391c4-111">Members</span></span>

<span data-ttu-id="391c4-112">La clase **CIM \_ SoftwareElementChecks** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="391c4-112">The **CIM\_SoftwareElementChecks** class has these types of members:</span></span>

-   [<span data-ttu-id="391c4-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="391c4-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="391c4-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="391c4-114">Properties</span></span>

<span data-ttu-id="391c4-115">La clase **CIM \_ SoftwareElementChecks** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="391c4-115">The **CIM\_SoftwareElementChecks** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="391c4-116">**Comprobación**</span><span class="sxs-lookup"><span data-stu-id="391c4-116">**Check**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="391c4-117">Tipo de datos **: \_ comprobación CIM**</span><span class="sxs-lookup"><span data-stu-id="391c4-117">Data type: **CIM\_Check**</span></span>
</dt> <dt>

<span data-ttu-id="391c4-118">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="391c4-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="391c4-119">Calificadores: [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (false), [**Weak**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="391c4-119">Qualifiers: [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (FALSE), [**Weak**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="391c4-120">Referencia a la comprobación.</span><span class="sxs-lookup"><span data-stu-id="391c4-120">Reference to the check.</span></span>

</dd> <dt>

<span data-ttu-id="391c4-121">**Element**</span><span class="sxs-lookup"><span data-stu-id="391c4-121">**Element**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="391c4-122">Tipo de datos: **CIM \_ SoftwareElement**</span><span class="sxs-lookup"><span data-stu-id="391c4-122">Data type: **CIM\_SoftwareElement**</span></span>
</dt> <dt>

<span data-ttu-id="391c4-123">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="391c4-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="391c4-124">Calificadores: [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="391c4-124">Qualifiers: [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="391c4-125">Referencia al elemento.</span><span class="sxs-lookup"><span data-stu-id="391c4-125">Reference to the element.</span></span>

</dd> <dt>

<span data-ttu-id="391c4-126">**Fase**</span><span class="sxs-lookup"><span data-stu-id="391c4-126">**Phase**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="391c4-127">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="391c4-127">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="391c4-128">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="391c4-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="391c4-129">Indica si la comprobación a la que se hace referencia es una comprobación en estado o una comprobación de estado siguiente.</span><span class="sxs-lookup"><span data-stu-id="391c4-129">Indicates whether the referenced check is an in-state check or a next-state check.</span></span>

<dt>

<span id="In-State"></span><span id="in-state"></span><span id="IN-STATE"></span>

<span data-ttu-id="391c4-130">**En estado** (0)</span><span class="sxs-lookup"><span data-stu-id="391c4-130">**In-State** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Next-State"></span><span id="next-state"></span><span id="NEXT-STATE"></span>

<span data-ttu-id="391c4-131">**Siguiente estado** (1)</span><span class="sxs-lookup"><span data-stu-id="391c4-131">**Next-State** (1)</span></span>


<span data-ttu-id="391c4-132"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="391c4-132"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="391c4-133">Observaciones</span><span class="sxs-lookup"><span data-stu-id="391c4-133">Remarks</span></span>

<span data-ttu-id="391c4-134">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="391c4-134">WMI does not implement this class.</span></span> <span data-ttu-id="391c4-135">Para las clases WMI derivadas de **CIM \_ SoftwareElementChecks**, vea [clases Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="391c4-135">For WMI classes derived from **CIM\_SoftwareElementChecks**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="391c4-136">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="391c4-136">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="391c4-137">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="391c4-137">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="391c4-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="391c4-138">Requirements</span></span>



| <span data-ttu-id="391c4-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="391c4-139">Requirement</span></span> | <span data-ttu-id="391c4-140">Value</span><span class="sxs-lookup"><span data-stu-id="391c4-140">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="391c4-141">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="391c4-141">Minimum supported client</span></span><br/> | <span data-ttu-id="391c4-142">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="391c4-142">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="391c4-143">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="391c4-143">Minimum supported server</span></span><br/> | <span data-ttu-id="391c4-144">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="391c4-144">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="391c4-145">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="391c4-145">Namespace</span></span><br/>                | <span data-ttu-id="391c4-146">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="391c4-146">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="391c4-147">MOF</span><span class="sxs-lookup"><span data-stu-id="391c4-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="391c4-148"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="391c4-148"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="391c4-149">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="391c4-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="391c4-150"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="391c4-150"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

