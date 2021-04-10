---
description: La \_ clase CIM ErrorCountersForDevice asocia la \_ clase DEVICEERRORCOUNTS de CIM al dispositivo lógico al que se aplica.
ms.assetid: 200971ab-df85-4a45-beb3-4ffe11ce92dc
ms.tgt_platform: multiple
title: CIM_ErrorCountersForDevice (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ErrorCountersForDevice
- CIM_ErrorCountersForDevice.Element
- CIM_ErrorCountersForDevice.Stats
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 7c4e11b1f58cae7b544b251044657bb737525b37
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907298"
---
# <a name="cim_errorcountersfordevice-class"></a><span data-ttu-id="ff862-103">\_Clase ErrorCountersForDevice de CIM</span><span class="sxs-lookup"><span data-stu-id="ff862-103">CIM\_ErrorCountersForDevice class</span></span>

<span data-ttu-id="ff862-104">La clase **CIM \_ ErrorCountersForDevice** asocia la clase [**\_ DeviceErrorCounts de CIM**](cim-deviceerrorcounts.md) al dispositivo lógico al que se aplica.</span><span class="sxs-lookup"><span data-stu-id="ff862-104">The **CIM\_ErrorCountersForDevice** class associates the [**CIM\_DeviceErrorCounts**](cim-deviceerrorcounts.md) class to the logical device to which it applies.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ff862-105">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="ff862-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="ff862-106">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="ff862-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="ff862-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="ff862-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="ff862-108">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="ff862-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="ff862-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ff862-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{2D79F3A0-D025-11d2-85F5-0000F8102E5F}"), AMENDMENT]
class CIM_ErrorCountersForDevice : CIM_Statistics
{
  CIM_LogicalDevice     REF Element;
  CIM_DeviceErrorCounts REF Stats;
};
```

## <a name="members"></a><span data-ttu-id="ff862-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="ff862-110">Members</span></span>

<span data-ttu-id="ff862-111">La clase **CIM \_ ErrorCountersForDevice** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="ff862-111">The **CIM\_ErrorCountersForDevice** class has these types of members:</span></span>

-   [<span data-ttu-id="ff862-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ff862-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ff862-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ff862-113">Properties</span></span>

<span data-ttu-id="ff862-114">La clase **CIM \_ ErrorCountersForDevice** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="ff862-114">The **CIM\_ErrorCountersForDevice** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ff862-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="ff862-115">**Element**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ff862-116">Tipo de datos **: \_ LogicalDevice de CIM**</span><span class="sxs-lookup"><span data-stu-id="ff862-116">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="ff862-117">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ff862-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ff862-118">Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Element"), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="ff862-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Element"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="ff862-119">Un [**\_ LogicalDevice de CIM**](cim-logicaldevice.md) que describe el dispositivo al que se aplican los contadores de errores.</span><span class="sxs-lookup"><span data-stu-id="ff862-119">A [**CIM\_LogicalDevice**](cim-logicaldevice.md) that describes the device to which the error counters apply.</span></span>

</dd> <dt>

<span data-ttu-id="ff862-120">**Stats**</span><span class="sxs-lookup"><span data-stu-id="ff862-120">**Stats**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ff862-121">Tipo de datos: **CIM \_ DeviceErrorCounts**</span><span class="sxs-lookup"><span data-stu-id="ff862-121">Data type: **CIM\_DeviceErrorCounts**</span></span>
</dt> <dt>

<span data-ttu-id="ff862-122">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ff862-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ff862-123">Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("estadísticas"), [**débil**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="ff862-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Stats"), [**Weak**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="ff862-124">Un [**\_ DeviceErrorCounts de CIM**](cim-deviceerrorcounts.md) que describe el objeto estadístico (en este caso, la clase de contador de errores).</span><span class="sxs-lookup"><span data-stu-id="ff862-124">A [**CIM\_DeviceErrorCounts**](cim-deviceerrorcounts.md) describing the statistical object - in this case, the error counter class.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ff862-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ff862-125">Remarks</span></span>

<span data-ttu-id="ff862-126">La clase **CIM \_ ErrorCountersForDevice** se hereda de [**las \_ estadísticas CIM**](cim-statistics.md).</span><span class="sxs-lookup"><span data-stu-id="ff862-126">The **CIM\_ErrorCountersForDevice** class is inherited from [**CIM\_Statistics**](cim-statistics.md).</span></span>

<span data-ttu-id="ff862-127">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="ff862-127">WMI does not implement this class.</span></span>

<span data-ttu-id="ff862-128">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="ff862-128">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="ff862-129">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="ff862-129">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="ff862-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ff862-130">Requirements</span></span>



| <span data-ttu-id="ff862-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="ff862-131">Requirement</span></span> | <span data-ttu-id="ff862-132">Value</span><span class="sxs-lookup"><span data-stu-id="ff862-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ff862-133">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ff862-133">Minimum supported client</span></span><br/> | <span data-ttu-id="ff862-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ff862-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ff862-135">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ff862-135">Minimum supported server</span></span><br/> | <span data-ttu-id="ff862-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ff862-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ff862-137">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="ff862-137">Namespace</span></span><br/>                | <span data-ttu-id="ff862-138">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="ff862-138">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="ff862-139">MOF</span><span class="sxs-lookup"><span data-stu-id="ff862-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ff862-140"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ff862-140"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="ff862-141">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="ff862-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ff862-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ff862-142"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ff862-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="ff862-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ff862-144">**Estadísticas de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="ff862-144">**CIM\_Statistics**</span></span>](cim-statistics.md)
</dt> </dl>

 

