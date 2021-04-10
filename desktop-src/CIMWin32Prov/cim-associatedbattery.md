---
description: La \_ dependencia AssociatedBattery de CIM asocia una batería a un dispositivo lógico. Utilice esta asociación para modelar baterías individuales que componen un sistema de alimentación ininterrumpida (SAI).
ms.assetid: f8d8b3d3-edc5-438a-8be6-3ea4d765085b
ms.tgt_platform: multiple
title: CIM_AssociatedBattery (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_AssociatedBattery
- CIM_AssociatedBattery.Dependent
- CIM_AssociatedBattery.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 98c6394df79e53698ab6394f8572768f3728c503
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275039"
---
# <a name="cim_associatedbattery-class"></a><span data-ttu-id="cd46c-104">\_Clase AssociatedBattery de CIM</span><span class="sxs-lookup"><span data-stu-id="cd46c-104">CIM\_AssociatedBattery class</span></span>

<span data-ttu-id="cd46c-105">La **dependencia \_ AssociatedBattery de CIM** asocia una batería a un dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="cd46c-105">The **CIM\_AssociatedBattery** dependency associates a battery with a logical device.</span></span> <span data-ttu-id="cd46c-106">Utilice esta asociación para modelar baterías individuales que componen un sistema de alimentación ininterrumpida (SAI).</span><span class="sxs-lookup"><span data-stu-id="cd46c-106">Use this association to model individual batteries that make up an uninterruptible power supply (UPS).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="cd46c-107">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="cd46c-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="cd46c-108">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="cd46c-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="cd46c-109">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="cd46c-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="cd46c-110">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="cd46c-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="cd46c-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="cd46c-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C578-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_AssociatedBattery : CIM_Dependency
{
  CIM_LogicalDevice REF Dependent;
  CIM_Battery       REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="cd46c-112">Miembros</span><span class="sxs-lookup"><span data-stu-id="cd46c-112">Members</span></span>

<span data-ttu-id="cd46c-113">La clase **CIM \_ AssociatedBattery** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="cd46c-113">The **CIM\_AssociatedBattery** class has these types of members:</span></span>

-   [<span data-ttu-id="cd46c-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="cd46c-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="cd46c-115">Propiedades</span><span class="sxs-lookup"><span data-stu-id="cd46c-115">Properties</span></span>

<span data-ttu-id="cd46c-116">La clase **CIM \_ AssociatedBattery** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="cd46c-116">The **CIM\_AssociatedBattery** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="cd46c-117">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="cd46c-117">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd46c-118">Tipo de datos **: \_ batería CIM**</span><span class="sxs-lookup"><span data-stu-id="cd46c-118">Data type: **CIM\_Battery**</span></span>
</dt> <dt>

<span data-ttu-id="cd46c-119">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="cd46c-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cd46c-120">Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente")</span><span class="sxs-lookup"><span data-stu-id="cd46c-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="cd46c-121">Una [**\_ batería CIM**](cim-battery.md) que describa la batería.</span><span class="sxs-lookup"><span data-stu-id="cd46c-121">A [**CIM\_Battery**](cim-battery.md) that describes the battery.</span></span>

</dd> <dt>

<span data-ttu-id="cd46c-122">**Dependientes**</span><span class="sxs-lookup"><span data-stu-id="cd46c-122">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd46c-123">Tipo de datos **: \_ LogicalDevice de CIM**</span><span class="sxs-lookup"><span data-stu-id="cd46c-123">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="cd46c-124">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="cd46c-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cd46c-125">Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependiente")</span><span class="sxs-lookup"><span data-stu-id="cd46c-125">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="cd46c-126">Un [**\_ LogicalDevice de CIM**](cim-logicaldevice.md) que contiene el dispositivo lógico que necesita o está asociado a la batería.</span><span class="sxs-lookup"><span data-stu-id="cd46c-126">A [**CIM\_LogicalDevice**](cim-logicaldevice.md) that contains the logical device needing or associated with the battery.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="cd46c-127">Observaciones</span><span class="sxs-lookup"><span data-stu-id="cd46c-127">Remarks</span></span>

<span data-ttu-id="cd46c-128">La clase **CIM \_ AssociatedBattery** se deriva de [**la \_ dependencia CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="cd46c-128">The **CIM\_AssociatedBattery** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="cd46c-129">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="cd46c-129">WMI does not implement this class.</span></span> <span data-ttu-id="cd46c-130">Para obtener más información sobre las clases derivadas de **CIM \_ AssociatedBattery**, vea [Win32 classes](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="cd46c-130">For more information about classes derived from **CIM\_AssociatedBattery**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="cd46c-131">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="cd46c-131">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="cd46c-132">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="cd46c-132">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="cd46c-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cd46c-133">Requirements</span></span>



| <span data-ttu-id="cd46c-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="cd46c-134">Requirement</span></span> | <span data-ttu-id="cd46c-135">Value</span><span class="sxs-lookup"><span data-stu-id="cd46c-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cd46c-136">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cd46c-136">Minimum supported client</span></span><br/> | <span data-ttu-id="cd46c-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="cd46c-137">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="cd46c-138">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cd46c-138">Minimum supported server</span></span><br/> | <span data-ttu-id="cd46c-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cd46c-139">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="cd46c-140">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="cd46c-140">Namespace</span></span><br/>                | <span data-ttu-id="cd46c-141">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="cd46c-141">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="cd46c-142">MOF</span><span class="sxs-lookup"><span data-stu-id="cd46c-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cd46c-143"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="cd46c-143"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="cd46c-144">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="cd46c-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cd46c-145"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cd46c-145"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cd46c-146">Vea también</span><span class="sxs-lookup"><span data-stu-id="cd46c-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd46c-147">**Dependencia de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="cd46c-147">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

