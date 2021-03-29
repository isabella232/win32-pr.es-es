---
description: La \_ dependencia AssociatedAlarm de CIM asocia una alarma a un dispositivo lógico.
ms.assetid: ed0ccc81-6d1b-45b0-abf0-7a2bd9a50193
ms.tgt_platform: multiple
title: CIM_AssociatedAlarm (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_AssociatedAlarm
- CIM_AssociatedAlarm.Dependent
- CIM_AssociatedAlarm.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: fe6a637482526feecc7528eadc70dc695dafca9b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807681"
---
# <a name="cim_associatedalarm-class"></a><span data-ttu-id="5a158-103">\_Clase AssociatedAlarm de CIM</span><span class="sxs-lookup"><span data-stu-id="5a158-103">CIM\_AssociatedAlarm class</span></span>

<span data-ttu-id="5a158-104">La **dependencia \_ AssociatedAlarm de CIM** asocia una alarma a un dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="5a158-104">The **CIM\_AssociatedAlarm** dependency associates an alarm with a logical device.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="5a158-105">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="5a158-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="5a158-106">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="5a158-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="5a158-107">La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="5a158-107">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="5a158-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5a158-108">Syntax</span></span>

``` syntax
[Abstract, UUID("{2280CB02-DB35-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_AssociatedAlarm : CIM_Dependency
{
  CIM_LogicalDevice REF Dependent;
  CIM_AlarmDevice   REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="5a158-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="5a158-109">Members</span></span>

<span data-ttu-id="5a158-110">La clase **CIM \_ AssociatedAlarm** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="5a158-110">The **CIM\_AssociatedAlarm** class has these types of members:</span></span>

-   [<span data-ttu-id="5a158-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="5a158-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5a158-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="5a158-112">Properties</span></span>

<span data-ttu-id="5a158-113">La clase **CIM \_ AssociatedAlarm** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="5a158-113">The **CIM\_AssociatedAlarm** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5a158-114">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="5a158-114">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a158-115">Tipo de datos: **CIM \_ AlarmDevice**</span><span class="sxs-lookup"><span data-stu-id="5a158-115">Data type: **CIM\_AlarmDevice**</span></span>
</dt> <dt>

<span data-ttu-id="5a158-116">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5a158-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5a158-117">Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente")</span><span class="sxs-lookup"><span data-stu-id="5a158-117">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="5a158-118">Un [**\_ AlarmDevice de CIM**](cim-alarmdevice.md) que contiene el dispositivo de alarma.</span><span class="sxs-lookup"><span data-stu-id="5a158-118">A [**CIM\_AlarmDevice**](cim-alarmdevice.md) that contains the alarm device.</span></span>

</dd> <dt>

<span data-ttu-id="5a158-119">**Dependientes**</span><span class="sxs-lookup"><span data-stu-id="5a158-119">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a158-120">Tipo de datos **: \_ LogicalDevice de CIM**</span><span class="sxs-lookup"><span data-stu-id="5a158-120">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="5a158-121">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5a158-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5a158-122">Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependiente")</span><span class="sxs-lookup"><span data-stu-id="5a158-122">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="5a158-123">Un [**\_ LogicalDevice de CIM**](cim-logicaldevice.md) que contiene el dispositivo lógico en el que se pone en alarma.</span><span class="sxs-lookup"><span data-stu-id="5a158-123">A [**CIM\_LogicalDevice**](cim-logicaldevice.md) that contains the logical device that is alarmed.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5a158-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5a158-124">Remarks</span></span>

<span data-ttu-id="5a158-125">La clase **CIM \_ AssociatedAlarm** se deriva de [**la \_ dependencia CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="5a158-125">The **CIM\_AssociatedAlarm** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="5a158-126">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="5a158-126">WMI does not implement this class.</span></span>

<span data-ttu-id="5a158-127">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="5a158-127">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="5a158-128">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="5a158-128">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="5a158-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5a158-129">Requirements</span></span>



| <span data-ttu-id="5a158-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="5a158-130">Requirement</span></span> | <span data-ttu-id="5a158-131">Value</span><span class="sxs-lookup"><span data-stu-id="5a158-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5a158-132">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5a158-132">Minimum supported client</span></span><br/> | <span data-ttu-id="5a158-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5a158-133">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="5a158-134">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5a158-134">Minimum supported server</span></span><br/> | <span data-ttu-id="5a158-135">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5a158-135">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="5a158-136">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="5a158-136">Namespace</span></span><br/>                | <span data-ttu-id="5a158-137">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="5a158-137">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="5a158-138">MOF</span><span class="sxs-lookup"><span data-stu-id="5a158-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5a158-139"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5a158-139"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="5a158-140">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="5a158-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5a158-141"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5a158-141"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5a158-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="5a158-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a158-143">**Dependencia de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="5a158-143">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

