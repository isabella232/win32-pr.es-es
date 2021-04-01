---
description: La \_ clase OSProcess de CIM asocia el sistema operativo y uno o más procesos que se ejecutan en el contexto del sistema operativo.
ms.assetid: 59d52b29-9d97-464f-bbbc-4191305df8c7
ms.tgt_platform: multiple
title: CIM_OSProcess (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_OSProcess
- CIM_OSProcess.PartComponent
- CIM_OSProcess.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 9b11738669c87b402f12932ad65237a512360427
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907041"
---
# <a name="cim_osprocess-class"></a><span data-ttu-id="2590b-103">\_Clase OSProcess de CIM</span><span class="sxs-lookup"><span data-stu-id="2590b-103">CIM\_OSProcess class</span></span>

<span data-ttu-id="2590b-104">La **clase \_ OSProcess de CIM** asocia el sistema operativo y uno o más procesos que se ejecutan en el contexto del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="2590b-104">The **CIM\_OSProcess** class associates the operating system and one or more processes running in the context of the operating system.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2590b-105">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="2590b-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="2590b-106">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="2590b-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="2590b-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="2590b-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="2590b-108">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="2590b-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="2590b-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2590b-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{A361A7AE-DB36-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_OSProcess : CIM_Component
{
  CIM_Process         REF PartComponent;
  CIM_OperatingSystem REF GroupComponent;
};
```

## <a name="members"></a><span data-ttu-id="2590b-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="2590b-110">Members</span></span>

<span data-ttu-id="2590b-111">La clase **CIM \_ OSProcess** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="2590b-111">The **CIM\_OSProcess** class has these types of members:</span></span>

-   [<span data-ttu-id="2590b-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="2590b-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2590b-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="2590b-113">Properties</span></span>

<span data-ttu-id="2590b-114">La clase **CIM \_ OSProcess** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="2590b-114">The **CIM\_OSProcess** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2590b-115">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="2590b-115">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2590b-116">Tipo de datos: **CIM \_ OperatingSystem**</span><span class="sxs-lookup"><span data-stu-id="2590b-116">Data type: **CIM\_OperatingSystem**</span></span>
</dt> <dt>

<span data-ttu-id="2590b-117">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2590b-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2590b-118">Calificadores: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span><span class="sxs-lookup"><span data-stu-id="2590b-118">Qualifiers: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span></span>
</dt> </dl>

<span data-ttu-id="2590b-119">Un [**\_ OperatingSystem de CIM**](cim-operatingsystem.md) que describe el sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="2590b-119">A [**CIM\_OperatingSystem**](cim-operatingsystem.md) describing the operating system.</span></span>

</dd> <dt>

<span data-ttu-id="2590b-120">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="2590b-120">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2590b-121">Tipo de datos **: \_ proceso CIM**</span><span class="sxs-lookup"><span data-stu-id="2590b-121">Data type: **CIM\_Process**</span></span>
</dt> <dt>

<span data-ttu-id="2590b-122">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2590b-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2590b-123">Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**débil**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="2590b-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**Weak**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="2590b-124">Un [**\_ proceso CIM**](cim-process.md) que describe el proceso que se ejecuta en el contexto del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="2590b-124">A [**CIM\_Process**](cim-process.md) describing the process running in the context of the operating system</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2590b-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2590b-125">Remarks</span></span>

<span data-ttu-id="2590b-126">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="2590b-126">WMI does not implement this class.</span></span>

<span data-ttu-id="2590b-127">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="2590b-127">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="2590b-128">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="2590b-128">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="2590b-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2590b-129">Requirements</span></span>



| <span data-ttu-id="2590b-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="2590b-130">Requirement</span></span> | <span data-ttu-id="2590b-131">Value</span><span class="sxs-lookup"><span data-stu-id="2590b-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2590b-132">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2590b-132">Minimum supported client</span></span><br/> | <span data-ttu-id="2590b-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2590b-133">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="2590b-134">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2590b-134">Minimum supported server</span></span><br/> | <span data-ttu-id="2590b-135">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2590b-135">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="2590b-136">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="2590b-136">Namespace</span></span><br/>                | <span data-ttu-id="2590b-137">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="2590b-137">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="2590b-138">MOF</span><span class="sxs-lookup"><span data-stu-id="2590b-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2590b-139"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2590b-139"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="2590b-140">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="2590b-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2590b-141"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2590b-141"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2590b-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="2590b-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2590b-143">**\_Componente CIM**</span><span class="sxs-lookup"><span data-stu-id="2590b-143">**CIM\_Component**</span></span>](cim-component.md)
</dt> </dl>

 

