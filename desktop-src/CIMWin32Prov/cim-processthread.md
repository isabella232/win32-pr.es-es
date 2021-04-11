---
description: La \_ clase CIM ProcessThread representa un vínculo entre un proceso y los subprocesos que se ejecutan en el contexto del proceso.
ms.assetid: e71543c5-d9b3-4f98-93a6-08f977a26305
ms.tgt_platform: multiple
title: CIM_ProcessThread (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ProcessThread
- CIM_ProcessThread.PartComponent
- CIM_ProcessThread.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: afc29d1576355eda1f9e3dfd7ed55d2cca399d5b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104274887"
---
# <a name="cim_processthread-class"></a><span data-ttu-id="00d56-103">\_Clase ProcessThread de CIM</span><span class="sxs-lookup"><span data-stu-id="00d56-103">CIM\_ProcessThread class</span></span>

<span data-ttu-id="00d56-104">La clase **CIM \_ ProcessThread** representa un vínculo entre un proceso y los subprocesos que se ejecutan en el contexto del proceso.</span><span class="sxs-lookup"><span data-stu-id="00d56-104">The **CIM\_ProcessThread** class represents a link between a process and the threads running in the context of the process.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="00d56-105">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="00d56-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="00d56-106">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="00d56-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="00d56-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="00d56-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="00d56-108">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="00d56-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="00d56-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="00d56-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{B7E6042C-DB36-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_ProcessThread : CIM_Component
{
  CIM_Thread  REF PartComponent;
  CIM_Process REF GroupComponent;
};
```

## <a name="members"></a><span data-ttu-id="00d56-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="00d56-110">Members</span></span>

<span data-ttu-id="00d56-111">La clase **CIM \_ ProcessThread** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="00d56-111">The **CIM\_ProcessThread** class has these types of members:</span></span>

-   [<span data-ttu-id="00d56-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="00d56-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="00d56-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="00d56-113">Properties</span></span>

<span data-ttu-id="00d56-114">La clase **CIM \_ ProcessThread** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="00d56-114">The **CIM\_ProcessThread** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="00d56-115">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="00d56-115">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="00d56-116">Tipo de datos **: \_ proceso CIM**</span><span class="sxs-lookup"><span data-stu-id="00d56-116">Data type: **CIM\_Process**</span></span>
</dt> <dt>

<span data-ttu-id="00d56-117">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="00d56-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="00d56-118">Calificadores: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span><span class="sxs-lookup"><span data-stu-id="00d56-118">Qualifiers: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span></span>
</dt> </dl>

<span data-ttu-id="00d56-119">[**\_ Proceso CIM**](cim-process.md) que describe el proceso.</span><span class="sxs-lookup"><span data-stu-id="00d56-119">A [**CIM\_Process**](cim-process.md) that describes the process.</span></span>

</dd> <dt>

<span data-ttu-id="00d56-120">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="00d56-120">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="00d56-121">Tipo de datos **: \_ subproceso CIM**</span><span class="sxs-lookup"><span data-stu-id="00d56-121">Data type: **CIM\_Thread**</span></span>
</dt> <dt>

<span data-ttu-id="00d56-122">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="00d56-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="00d56-123">Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**débil**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="00d56-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**Weak**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="00d56-124">Un [**\_ subproceso CIM**](cim-thread.md) que describe el subproceso que se ejecuta en el contexto del proceso.</span><span class="sxs-lookup"><span data-stu-id="00d56-124">A [**CIM\_Thread**](cim-thread.md) that describes the thread running in the context of the process.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="00d56-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="00d56-125">Remarks</span></span>

<span data-ttu-id="00d56-126">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="00d56-126">WMI does not implement this class.</span></span>

<span data-ttu-id="00d56-127">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="00d56-127">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="00d56-128">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="00d56-128">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="00d56-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="00d56-129">Requirements</span></span>



| <span data-ttu-id="00d56-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="00d56-130">Requirement</span></span> | <span data-ttu-id="00d56-131">Value</span><span class="sxs-lookup"><span data-stu-id="00d56-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="00d56-132">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="00d56-132">Minimum supported client</span></span><br/> | <span data-ttu-id="00d56-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="00d56-133">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="00d56-134">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="00d56-134">Minimum supported server</span></span><br/> | <span data-ttu-id="00d56-135">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="00d56-135">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="00d56-136">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="00d56-136">Namespace</span></span><br/>                | <span data-ttu-id="00d56-137">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="00d56-137">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="00d56-138">MOF</span><span class="sxs-lookup"><span data-stu-id="00d56-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="00d56-139"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="00d56-139"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="00d56-140">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="00d56-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="00d56-141"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="00d56-141"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="00d56-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="00d56-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="00d56-143">**\_Componente CIM**</span><span class="sxs-lookup"><span data-stu-id="00d56-143">**CIM\_Component**</span></span>](cim-component.md)
</dt> </dl>

 

