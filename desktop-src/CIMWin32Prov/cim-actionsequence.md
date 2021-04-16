---
description: La \_ Asociación ActionSequence de CIM define una serie de operaciones que transfieren el elemento de software (al que hace referencia la \_ Asociación SOFTWAREELEMENTACTIONS de CIM) al siguiente estado o quita el elemento de software de su estado actual.
ms.assetid: b539c424-bc2a-414b-b56c-72550004720f
ms.tgt_platform: multiple
title: CIM_ActionSequence (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ActionSequence
- CIM_ActionSequence.Next
- CIM_ActionSequence.Prior
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 71150d1ad9785d81579d8f305fe46bc6b7e57d00
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659528"
---
# <a name="cim_actionsequence-class"></a><span data-ttu-id="d10f7-103">\_Clase ActionSequence de CIM</span><span class="sxs-lookup"><span data-stu-id="d10f7-103">CIM\_ActionSequence class</span></span>

<span data-ttu-id="d10f7-104">La **Asociación \_ ActionSequence de CIM** define una serie de operaciones que transfieren el elemento de software (al que hace referencia la Asociación [**\_ SoftwareElementActions de CIM**](cim-softwareelementactions.md) ) al siguiente estado o quita el elemento de software de su estado actual.</span><span class="sxs-lookup"><span data-stu-id="d10f7-104">The **CIM\_ActionSequence** association defines a series of operations that transition the software element (referenced by the [**CIM\_SoftwareElementActions**](cim-softwareelementactions.md) association) to its next state, or removes the software element from its current state.</span></span>

<span data-ttu-id="d10f7-105">Las acciones de siguiente estado y las acciones de desinstalación asociadas a un elemento de software determinado deben ser una secuencia continua.</span><span class="sxs-lookup"><span data-stu-id="d10f7-105">The next-state actions and uninstall actions associated with a particular software element must be a continuous sequence.</span></span> <span data-ttu-id="d10f7-106">Dado que **CIM \_ ActionSequence** es una asociación, los bucles de la clase de [**\_ acción CIM**](cim-action.md) , con roles para la acción "anterior" y la acción "siguiente", forman una secuencia.</span><span class="sxs-lookup"><span data-stu-id="d10f7-106">Since **CIM\_ActionSequence** is an association, the loops on the [**CIM\_Action**](cim-action.md) class, with roles for the "prior" action and "next" action, form a sequence.</span></span>

<span data-ttu-id="d10f7-107">La necesidad de una secuencia continua implica:</span><span class="sxs-lookup"><span data-stu-id="d10f7-107">The need for a continuous sequence implies:</span></span>

-   <span data-ttu-id="d10f7-108">Dentro del conjunto de acciones de siguiente estado o desinstalación, solo hay una acción que no tiene una instancia de la Asociación **\_ ActionSequence de CIM** que hace referencia a ella en el rol "siguiente".</span><span class="sxs-lookup"><span data-stu-id="d10f7-108">Within the set of next-state or uninstall actions, there is only one action that does not have an instance of the **CIM\_ActionSequence** association referencing it in the "next" role.</span></span> <span data-ttu-id="d10f7-109">Esta es la primera acción de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="d10f7-109">This is the first action in the sequence.</span></span>
-   <span data-ttu-id="d10f7-110">Dentro del conjunto de acciones de siguiente estado o desinstalación, solo hay una acción que no tiene una instancia de la Asociación **\_ ActionSequence de CIM** que hace referencia a ella en el rol "anterior".</span><span class="sxs-lookup"><span data-stu-id="d10f7-110">Within the set of next-state or uninstall actions, there is only one action that does not have an instance of the **CIM\_ActionSequence** association referencing it in the "prior" role.</span></span> <span data-ttu-id="d10f7-111">Esta es la última acción de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="d10f7-111">This is the last action in the sequence.</span></span>
-   <span data-ttu-id="d10f7-112">Todas las demás acciones del conjunto de acciones de siguiente estado y desinstalación deben participar en dos instancias de la **Asociación \_ ActionSequence de CIM** , una en un rol "anterior" y otra en el rol "siguiente".</span><span class="sxs-lookup"><span data-stu-id="d10f7-112">All other actions within the set of next-state and uninstall actions must participate in two instances of the **CIM\_ActionSequence** association, one in a "prior" role and one in the "next" role.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d10f7-113">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="d10f7-113">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="d10f7-114">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="d10f7-114">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="d10f7-115">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="d10f7-115">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="d10f7-116">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="d10f7-116">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="d10f7-117">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d10f7-117">Syntax</span></span>

``` syntax
[Abstract, Association, UUID("{F127E50E-E3E0-11d2-8601-0000F8102E5F}"), AMENDMENT]
class CIM_ActionSequence
{
  CIM_Action REF Next;
  CIM_Action REF Prior;
};
```

## <a name="members"></a><span data-ttu-id="d10f7-118">Miembros</span><span class="sxs-lookup"><span data-stu-id="d10f7-118">Members</span></span>

<span data-ttu-id="d10f7-119">La clase **CIM \_ ActionSequence** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="d10f7-119">The **CIM\_ActionSequence** class has these types of members:</span></span>

-   [<span data-ttu-id="d10f7-120">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d10f7-120">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d10f7-121">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d10f7-121">Properties</span></span>

<span data-ttu-id="d10f7-122">La clase **CIM \_ ActionSequence** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="d10f7-122">The **CIM\_ActionSequence** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d10f7-123">**Siguiente**</span><span class="sxs-lookup"><span data-stu-id="d10f7-123">**Next**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d10f7-124">Tipo de datos **: \_ acción de CIM**</span><span class="sxs-lookup"><span data-stu-id="d10f7-124">Data type: **CIM\_Action**</span></span>
</dt> <dt>

<span data-ttu-id="d10f7-125">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d10f7-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d10f7-126">Calificadores: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span><span class="sxs-lookup"><span data-stu-id="d10f7-126">Qualifiers: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span></span>
</dt> </dl>

<span data-ttu-id="d10f7-127">Referencia a la siguiente acción.</span><span class="sxs-lookup"><span data-stu-id="d10f7-127">Reference to the next action.</span></span>

</dd> <dt>

<span data-ttu-id="d10f7-128">**Anticipa**</span><span class="sxs-lookup"><span data-stu-id="d10f7-128">**Prior**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d10f7-129">Tipo de datos **: \_ acción de CIM**</span><span class="sxs-lookup"><span data-stu-id="d10f7-129">Data type: **CIM\_Action**</span></span>
</dt> <dt>

<span data-ttu-id="d10f7-130">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d10f7-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d10f7-131">Calificadores: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span><span class="sxs-lookup"><span data-stu-id="d10f7-131">Qualifiers: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span></span>
</dt> </dl>

<span data-ttu-id="d10f7-132">Referencia a la acción anterior.</span><span class="sxs-lookup"><span data-stu-id="d10f7-132">Reference to the prior action.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d10f7-133">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d10f7-133">Remarks</span></span>

<span data-ttu-id="d10f7-134">Las clases de [**\_ acción CIM**](cim-action.md) que participan en esta asociación deben tener el mismo valor para la propiedad **Direction** .</span><span class="sxs-lookup"><span data-stu-id="d10f7-134">The [**CIM\_Action**](cim-action.md) classes participating in this association must have the same value for the **Direction** property.</span></span>

<span data-ttu-id="d10f7-135">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="d10f7-135">WMI does not implement this class.</span></span>

<span data-ttu-id="d10f7-136">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="d10f7-136">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="d10f7-137">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="d10f7-137">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="d10f7-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d10f7-138">Requirements</span></span>



| <span data-ttu-id="d10f7-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="d10f7-139">Requirement</span></span> | <span data-ttu-id="d10f7-140">Value</span><span class="sxs-lookup"><span data-stu-id="d10f7-140">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d10f7-141">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d10f7-141">Minimum supported client</span></span><br/> | <span data-ttu-id="d10f7-142">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d10f7-142">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d10f7-143">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d10f7-143">Minimum supported server</span></span><br/> | <span data-ttu-id="d10f7-144">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d10f7-144">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d10f7-145">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="d10f7-145">Namespace</span></span><br/>                | <span data-ttu-id="d10f7-146">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="d10f7-146">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="d10f7-147">MOF</span><span class="sxs-lookup"><span data-stu-id="d10f7-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d10f7-148"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d10f7-148"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="d10f7-149">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d10f7-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d10f7-150"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d10f7-150"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d10f7-151">Vea también</span><span class="sxs-lookup"><span data-stu-id="d10f7-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d10f7-152">Clases CIM</span><span class="sxs-lookup"><span data-stu-id="d10f7-152">CIM Classes</span></span>](/windows/desktop/WmiSdk/cimclas)
</dt> </dl>

 

