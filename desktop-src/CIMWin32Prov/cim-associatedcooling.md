---
description: La \_ Asociación AssociatedCooling de CIM indica si los ventiladores u otros dispositivos de refrigeración son específicos de un dispositivo (en lugar de proporcionar la refrigeración del gabinete o del contenedor).
ms.assetid: 7b20e429-593c-4365-a340-1aef9b0fadf5
ms.tgt_platform: multiple
title: CIM_AssociatedCooling (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_AssociatedCooling
- CIM_AssociatedCooling.Dependent
- CIM_AssociatedCooling.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: bb838129226b225f024917e8f8e77ddc92ddf2ff
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153294"
---
# <a name="cim_associatedcooling-class"></a><span data-ttu-id="19aa6-103">\_Clase AssociatedCooling de CIM</span><span class="sxs-lookup"><span data-stu-id="19aa6-103">CIM\_AssociatedCooling class</span></span>

<span data-ttu-id="19aa6-104">La **Asociación \_ AssociatedCooling de CIM** indica si los ventiladores u otros dispositivos de refrigeración son específicos de un dispositivo (en lugar de proporcionar la refrigeración del gabinete o del contenedor).</span><span class="sxs-lookup"><span data-stu-id="19aa6-104">The **CIM\_AssociatedCooling** association indicates when fans or other cooling devices are specific to a device (versus providing enclosure or cabinet cooling).</span></span>

<span data-ttu-id="19aa6-105">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="19aa6-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="19aa6-106">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="19aa6-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="19aa6-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="19aa6-107">Syntax</span></span>

``` syntax
[Abstract, UUID("{306F88F2-DB35-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_AssociatedCooling : CIM_Dependency
{
  CIM_LogicalDevice REF Dependent;
  CIM_CoolingDevice REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="19aa6-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="19aa6-108">Members</span></span>

<span data-ttu-id="19aa6-109">La clase **CIM \_ AssociatedCooling** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="19aa6-109">The **CIM\_AssociatedCooling** class has these types of members:</span></span>

-   [<span data-ttu-id="19aa6-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="19aa6-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="19aa6-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="19aa6-111">Properties</span></span>

<span data-ttu-id="19aa6-112">La clase **CIM \_ AssociatedCooling** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="19aa6-112">The **CIM\_AssociatedCooling** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="19aa6-113">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="19aa6-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="19aa6-114">Tipo de datos: **CIM \_ CoolingDevice**</span><span class="sxs-lookup"><span data-stu-id="19aa6-114">Data type: **CIM\_CoolingDevice**</span></span>
</dt> <dt>

<span data-ttu-id="19aa6-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="19aa6-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="19aa6-116">Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente")</span><span class="sxs-lookup"><span data-stu-id="19aa6-116">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="19aa6-117">Un [**\_ LogicalDevice de CIM**](cim-logicaldevice.md) que describe el dispositivo de enfriamiento.</span><span class="sxs-lookup"><span data-stu-id="19aa6-117">A [**CIM\_LogicalDevice**](cim-logicaldevice.md) that describes the cooling device.</span></span>

</dd> <dt>

<span data-ttu-id="19aa6-118">**Dependientes**</span><span class="sxs-lookup"><span data-stu-id="19aa6-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="19aa6-119">Tipo de datos **: \_ LogicalDevice de CIM**</span><span class="sxs-lookup"><span data-stu-id="19aa6-119">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="19aa6-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="19aa6-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="19aa6-121">Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependiente")</span><span class="sxs-lookup"><span data-stu-id="19aa6-121">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="19aa6-122">Un [**\_ LogicalDevice de CIM**](cim-logicaldevice.md) que hace referencia al dispositivo lógico que se refrigera.</span><span class="sxs-lookup"><span data-stu-id="19aa6-122">A [**CIM\_LogicalDevice**](cim-logicaldevice.md) that references the logical device being cooled.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="19aa6-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="19aa6-123">Remarks</span></span>

<span data-ttu-id="19aa6-124">La clase **CIM \_ AssociatedCooling** se deriva de [**la \_ dependencia CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="19aa6-124">The **CIM\_AssociatedCooling** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="19aa6-125">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="19aa6-125">WMI does not implement this class.</span></span>

<span data-ttu-id="19aa6-126">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="19aa6-126">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="19aa6-127">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="19aa6-127">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="19aa6-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="19aa6-128">Requirements</span></span>



| <span data-ttu-id="19aa6-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="19aa6-129">Requirement</span></span> | <span data-ttu-id="19aa6-130">Value</span><span class="sxs-lookup"><span data-stu-id="19aa6-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="19aa6-131">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="19aa6-131">Minimum supported client</span></span><br/> | <span data-ttu-id="19aa6-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="19aa6-132">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="19aa6-133">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="19aa6-133">Minimum supported server</span></span><br/> | <span data-ttu-id="19aa6-134">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="19aa6-134">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="19aa6-135">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="19aa6-135">Namespace</span></span><br/>                | <span data-ttu-id="19aa6-136">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="19aa6-136">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="19aa6-137">MOF</span><span class="sxs-lookup"><span data-stu-id="19aa6-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="19aa6-138"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="19aa6-138"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="19aa6-139">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="19aa6-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="19aa6-140"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="19aa6-140"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="19aa6-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="19aa6-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19aa6-142">**Dependencia de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="19aa6-142">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

