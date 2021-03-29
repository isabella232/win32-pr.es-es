---
description: La \_ clase AssociatedSensor de CIM asocia un sensor instalado a un dispositivo lógico. El sensor mide las propiedades críticas de entrada y salida, y puede incluirse con el dispositivo o instalarse cerca.
ms.assetid: 8ccaa37f-b95f-4582-a694-23bdc15b8c8b
ms.tgt_platform: multiple
title: CIM_AssociatedSensor (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_AssociatedSensor
- CIM_AssociatedSensor.Dependent
- CIM_AssociatedSensor.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 50eac6b8bd933762df0da0213c420f5895b74640
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907376"
---
# <a name="cim_associatedsensor-class"></a><span data-ttu-id="8e224-104">\_Clase AssociatedSensor de CIM</span><span class="sxs-lookup"><span data-stu-id="8e224-104">CIM\_AssociatedSensor class</span></span>

<span data-ttu-id="8e224-105">La **clase \_ AssociatedSensor de CIM** asocia un sensor instalado a un dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="8e224-105">The **CIM\_AssociatedSensor** class associates an installed sensor with a logical device.</span></span> <span data-ttu-id="8e224-106">El sensor mide las propiedades críticas de entrada y salida, y puede incluirse con el dispositivo o instalarse cerca.</span><span class="sxs-lookup"><span data-stu-id="8e224-106">The sensor measures critical input and output properties, and can be included with the device or installed nearby.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8e224-107">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="8e224-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="8e224-108">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="8e224-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="8e224-109">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="8e224-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="8e224-110">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="8e224-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="8e224-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8e224-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{956597A0-7D80-11D2-AAD3-006008C78BC7}"), AMENDMENT]
class CIM_AssociatedSensor : CIM_Dependency
{
  CIM_LogicalDevice REF Dependent;
  CIM_Sensor        REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="8e224-112">Miembros</span><span class="sxs-lookup"><span data-stu-id="8e224-112">Members</span></span>

<span data-ttu-id="8e224-113">La clase **CIM \_ AssociatedSensor** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="8e224-113">The **CIM\_AssociatedSensor** class has these types of members:</span></span>

-   [<span data-ttu-id="8e224-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="8e224-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8e224-115">Propiedades</span><span class="sxs-lookup"><span data-stu-id="8e224-115">Properties</span></span>

<span data-ttu-id="8e224-116">La clase **CIM \_ AssociatedSensor** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="8e224-116">The **CIM\_AssociatedSensor** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8e224-117">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="8e224-117">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e224-118">Tipo de datos **: \_ sensor CIM**</span><span class="sxs-lookup"><span data-stu-id="8e224-118">Data type: **CIM\_Sensor**</span></span>
</dt> <dt>

<span data-ttu-id="8e224-119">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8e224-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e224-120">Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente")</span><span class="sxs-lookup"><span data-stu-id="8e224-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="8e224-121">Un [**\_ sensor CIM**](cim-sensor.md) que describe el sensor.</span><span class="sxs-lookup"><span data-stu-id="8e224-121">A [**CIM\_Sensor**](cim-sensor.md) that describes the sensor.</span></span>

</dd> <dt>

<span data-ttu-id="8e224-122">**Dependientes**</span><span class="sxs-lookup"><span data-stu-id="8e224-122">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8e224-123">Tipo de datos **: \_ LogicalDevice de CIM**</span><span class="sxs-lookup"><span data-stu-id="8e224-123">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="8e224-124">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8e224-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8e224-125">Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependiente")</span><span class="sxs-lookup"><span data-stu-id="8e224-125">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="8e224-126">Un [**\_ LogicalDevice de CIM**](cim-logicaldevice.md) que describe el dispositivo lógico para el que el sensor mide la información.</span><span class="sxs-lookup"><span data-stu-id="8e224-126">A [**CIM\_LogicalDevice**](cim-logicaldevice.md) that describes the logical device for which information is measured by the sensor.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8e224-127">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8e224-127">Remarks</span></span>

<span data-ttu-id="8e224-128">La clase **CIM \_ AssociatedSensor** se deriva de [**la \_ dependencia CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="8e224-128">The **CIM\_AssociatedSensor** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="8e224-129">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="8e224-129">WMI does not implement this class.</span></span> <span data-ttu-id="8e224-130">Para obtener más información sobre las clases derivadas de **CIM \_ AssociatedSensor**, vea [Win32 classes](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="8e224-130">For more information about classes derived from **CIM\_AssociatedSensor**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="8e224-131">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="8e224-131">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="8e224-132">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="8e224-132">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="8e224-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8e224-133">Requirements</span></span>



| <span data-ttu-id="8e224-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="8e224-134">Requirement</span></span> | <span data-ttu-id="8e224-135">Value</span><span class="sxs-lookup"><span data-stu-id="8e224-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8e224-136">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8e224-136">Minimum supported client</span></span><br/> | <span data-ttu-id="8e224-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8e224-137">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="8e224-138">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8e224-138">Minimum supported server</span></span><br/> | <span data-ttu-id="8e224-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8e224-139">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="8e224-140">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="8e224-140">Namespace</span></span><br/>                | <span data-ttu-id="8e224-141">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="8e224-141">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="8e224-142">MOF</span><span class="sxs-lookup"><span data-stu-id="8e224-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8e224-143"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8e224-143"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="8e224-144">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="8e224-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8e224-145"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8e224-145"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8e224-146">Vea también</span><span class="sxs-lookup"><span data-stu-id="8e224-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8e224-147">**Dependencia de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="8e224-147">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

