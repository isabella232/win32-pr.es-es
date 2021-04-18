---
description: La \_ clase CIM ComputerSystemDMA representa una asociación entre un equipo y sus canales de acceso directo a memoria (DMA) disponibles.
ms.assetid: 7d5bce4b-973f-4452-b403-a2196bd4017a
ms.tgt_platform: multiple
title: CIM_ComputerSystemDMA (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ComputerSystemDMA
- CIM_ComputerSystemDMA.PartComponent
- CIM_ComputerSystemDMA.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 23748a3b10c11878069a81cd82f7f69d0ab75792
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659630"
---
# <a name="cim_computersystemdma-class"></a><span data-ttu-id="d00e7-103">\_Clase ComputerSystemDMA de CIM</span><span class="sxs-lookup"><span data-stu-id="d00e7-103">CIM\_ComputerSystemDMA class</span></span>

<span data-ttu-id="d00e7-104">La clase **CIM \_ ComputerSystemDMA** representa una asociación entre un equipo y sus canales de acceso directo a memoria (DMA) disponibles.</span><span class="sxs-lookup"><span data-stu-id="d00e7-104">The **CIM\_ComputerSystemDMA** class represents an association between a computer system and its available direct memory access (DMA) channels.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d00e7-105">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="d00e7-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="d00e7-106">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="d00e7-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="d00e7-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="d00e7-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="d00e7-108">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="d00e7-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="d00e7-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d00e7-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{9B81340B-E3D3-11d2-8601-0000F8102E5F}"), AMENDMENT]
class CIM_ComputerSystemDMA : CIM_ComputerSystemResource
{
  CIM_DMA            REF PartComponent;
  CIM_ComputerSystem REF GroupComponent;
};
```

## <a name="members"></a><span data-ttu-id="d00e7-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="d00e7-110">Members</span></span>

<span data-ttu-id="d00e7-111">La clase **CIM \_ ComputerSystemDMA** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="d00e7-111">The **CIM\_ComputerSystemDMA** class has these types of members:</span></span>

-   [<span data-ttu-id="d00e7-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d00e7-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d00e7-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d00e7-113">Properties</span></span>

<span data-ttu-id="d00e7-114">La clase **CIM \_ ComputerSystemDMA** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="d00e7-114">The **CIM\_ComputerSystemDMA** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d00e7-115">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="d00e7-115">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d00e7-116">Tipo de datos: **CIM \_ ComputerSystem**</span><span class="sxs-lookup"><span data-stu-id="d00e7-116">Data type: **CIM\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="d00e7-117">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d00e7-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d00e7-118">Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span><span class="sxs-lookup"><span data-stu-id="d00e7-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span></span>
</dt> </dl>

<span data-ttu-id="d00e7-119">Un [**\_ ComputerSystem de CIM**](cim-computersystem.md) que describe el equipo asociado con el DMA.</span><span class="sxs-lookup"><span data-stu-id="d00e7-119">A [**CIM\_ComputerSystem**](cim-computersystem.md) that describes the computer associated with the DMA.</span></span>

</dd> <dt>

<span data-ttu-id="d00e7-120">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="d00e7-120">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d00e7-121">Tipo de datos **: \_ DMA de CIM**</span><span class="sxs-lookup"><span data-stu-id="d00e7-121">Data type: **CIM\_DMA**</span></span>
</dt> <dt>

<span data-ttu-id="d00e7-122">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d00e7-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d00e7-123">Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**débil**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="d00e7-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**Weak**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="d00e7-124">Un [**\_ DMA de CIM**](cim-dma.md) que describe un canal DMA del sistema del equipo.</span><span class="sxs-lookup"><span data-stu-id="d00e7-124">A [**CIM\_DMA**](cim-dma.md) that describes a DMA channel of the computer system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d00e7-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d00e7-125">Remarks</span></span>

<span data-ttu-id="d00e7-126">La clase **CIM \_ ComputerSystemDMA** se deriva de [**\_ ComputerSystemResource de CIM**](cim-computersystemresource.md).</span><span class="sxs-lookup"><span data-stu-id="d00e7-126">The **CIM\_ComputerSystemDMA** class is derived from [**CIM\_ComputerSystemResource**](cim-computersystemresource.md).</span></span>

<span data-ttu-id="d00e7-127">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="d00e7-127">WMI does not implement this class.</span></span>

<span data-ttu-id="d00e7-128">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="d00e7-128">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="d00e7-129">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="d00e7-129">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="d00e7-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d00e7-130">Requirements</span></span>



| <span data-ttu-id="d00e7-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="d00e7-131">Requirement</span></span> | <span data-ttu-id="d00e7-132">Value</span><span class="sxs-lookup"><span data-stu-id="d00e7-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d00e7-133">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d00e7-133">Minimum supported client</span></span><br/> | <span data-ttu-id="d00e7-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d00e7-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d00e7-135">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d00e7-135">Minimum supported server</span></span><br/> | <span data-ttu-id="d00e7-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d00e7-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d00e7-137">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="d00e7-137">Namespace</span></span><br/>                | <span data-ttu-id="d00e7-138">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="d00e7-138">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="d00e7-139">MOF</span><span class="sxs-lookup"><span data-stu-id="d00e7-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d00e7-140"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d00e7-140"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="d00e7-141">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d00e7-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d00e7-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d00e7-142"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d00e7-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="d00e7-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d00e7-144">**\_COMPUTERSYSTEMRESOURCE CIM**</span><span class="sxs-lookup"><span data-stu-id="d00e7-144">**CIM\_ComputerSystemResource**</span></span>](cim-computersystemresource.md)
</dt> </dl>

 

