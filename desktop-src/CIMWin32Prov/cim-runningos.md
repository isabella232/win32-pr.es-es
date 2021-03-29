---
description: La \_ clase CIM Runnings representa el sistema operativo que se está ejecutando actualmente. Como máximo, un sistema operativo puede ejecutarse en cualquier momento en un sistema informático; es posible que no se haya iniciado el equipo o que el sistema operativo sea desconocido.
ms.assetid: 93e3d425-d751-4252-aa81-7d6774c8f8c5
ms.tgt_platform: multiple
title: CIM_RunningOS (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_RunningOS
- CIM_RunningOS.Dependent
- CIM_RunningOS.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1ff86af88342a1b8f0147ecd9721765794faf39e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807862"
---
# <a name="cim_runningos-class"></a><span data-ttu-id="57078-104">CIM \_ Runnings (clase)</span><span class="sxs-lookup"><span data-stu-id="57078-104">CIM\_RunningOS class</span></span>

<span data-ttu-id="57078-105">La clase **CIM \_ Runnings** representa el sistema operativo que se está ejecutando actualmente.</span><span class="sxs-lookup"><span data-stu-id="57078-105">The **CIM\_RunningOS** class represents the currently executing operating system.</span></span> <span data-ttu-id="57078-106">Como máximo, un sistema operativo puede ejecutarse en cualquier momento en un sistema informático; es posible que no se haya iniciado el equipo o que el sistema operativo sea desconocido.</span><span class="sxs-lookup"><span data-stu-id="57078-106">At most, one operating system can execute at any time on a computer system; the computer system may not be currently booted, or its operating system may be unknown.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="57078-107">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="57078-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="57078-108">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="57078-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="57078-109">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="57078-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="57078-110">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="57078-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="57078-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="57078-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{1F2EA300-DB37-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_RunningOS : CIM_Dependency
{
  CIM_ComputerSystem  REF Dependent;
  CIM_OperatingSystem REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="57078-112">Miembros</span><span class="sxs-lookup"><span data-stu-id="57078-112">Members</span></span>

<span data-ttu-id="57078-113">La clase **CIM \_ Runnings** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="57078-113">The **CIM\_RunningOS** class has these types of members:</span></span>

-   [<span data-ttu-id="57078-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="57078-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="57078-115">Propiedades</span><span class="sxs-lookup"><span data-stu-id="57078-115">Properties</span></span>

<span data-ttu-id="57078-116">La clase **CIM \_ Runnings** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="57078-116">The **CIM\_RunningOS** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="57078-117">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="57078-117">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="57078-118">Tipo de datos: **CIM \_ OperatingSystem**</span><span class="sxs-lookup"><span data-stu-id="57078-118">Data type: **CIM\_OperatingSystem**</span></span>
</dt> <dt>

<span data-ttu-id="57078-119">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="57078-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="57078-120">Calificadores: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente")</span><span class="sxs-lookup"><span data-stu-id="57078-120">Qualifiers: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="57078-121">Un [**\_ OperatingSystem de CIM**](cim-operatingsystem.md) que describe el sistema operativo que se ejecuta actualmente en el sistema del equipo.</span><span class="sxs-lookup"><span data-stu-id="57078-121">A [**CIM\_OperatingSystem**](cim-operatingsystem.md) that describes the operating system currently running on the computer system.</span></span>

</dd> <dt>

<span data-ttu-id="57078-122">**Dependientes**</span><span class="sxs-lookup"><span data-stu-id="57078-122">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="57078-123">Tipo de datos: **CIM \_ ComputerSystem**</span><span class="sxs-lookup"><span data-stu-id="57078-123">Data type: **CIM\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="57078-124">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="57078-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="57078-125">Calificadores: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span><span class="sxs-lookup"><span data-stu-id="57078-125">Qualifiers: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="57078-126">Un [**\_ ComputerSystem de CIM**](cim-computersystem.md) que describe el sistema del equipo.</span><span class="sxs-lookup"><span data-stu-id="57078-126">A [**CIM\_ComputerSystem**](cim-computersystem.md) that describes the computer system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="57078-127">Observaciones</span><span class="sxs-lookup"><span data-stu-id="57078-127">Remarks</span></span>

<span data-ttu-id="57078-128">La clase de **\_ ejecución de CIM** se deriva de la [**\_ dependencia CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="57078-128">The **CIM\_RunningOS** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="57078-129">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="57078-129">WMI does not implement this class.</span></span>

<span data-ttu-id="57078-130">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="57078-130">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="57078-131">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="57078-131">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="57078-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="57078-132">Requirements</span></span>



| <span data-ttu-id="57078-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="57078-133">Requirement</span></span> | <span data-ttu-id="57078-134">Value</span><span class="sxs-lookup"><span data-stu-id="57078-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="57078-135">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="57078-135">Minimum supported client</span></span><br/> | <span data-ttu-id="57078-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="57078-136">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="57078-137">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="57078-137">Minimum supported server</span></span><br/> | <span data-ttu-id="57078-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="57078-138">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="57078-139">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="57078-139">Namespace</span></span><br/>                | <span data-ttu-id="57078-140">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="57078-140">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="57078-141">MOF</span><span class="sxs-lookup"><span data-stu-id="57078-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="57078-142"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="57078-142"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="57078-143">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="57078-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="57078-144"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="57078-144"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="57078-145">Vea también</span><span class="sxs-lookup"><span data-stu-id="57078-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="57078-146">**Dependencia de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="57078-146">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

