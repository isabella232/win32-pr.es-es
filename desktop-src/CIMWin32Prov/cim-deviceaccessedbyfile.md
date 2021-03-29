---
description: La \_ clase de asociación CIM DeviceAccessedByFile especifica el dispositivo lógico al que se tiene acceso mediante la clase DEVICEFILE CIM a la que se hace referencia \_ .
ms.assetid: 8ba44f40-8b84-4f5c-b719-aded10877654
ms.tgt_platform: multiple
title: CIM_DeviceAccessedByFile (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DeviceAccessedByFile
- CIM_DeviceAccessedByFile.Dependent
- CIM_DeviceAccessedByFile.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: cf84d2e7943dfe6da88f81ef6963190553f028e7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907300"
---
# <a name="cim_deviceaccessedbyfile-class"></a><span data-ttu-id="42f91-103">\_Clase DeviceAccessedByFile de CIM</span><span class="sxs-lookup"><span data-stu-id="42f91-103">CIM\_DeviceAccessedByFile class</span></span>

<span data-ttu-id="42f91-104">La clase de asociación **CIM \_ DeviceAccessedByFile** especifica el dispositivo lógico al que se tiene acceso mediante la clase [**\_ DeviceFile CIM**](cim-devicefile.md) a la que se hace referencia.</span><span class="sxs-lookup"><span data-stu-id="42f91-104">The **CIM\_DeviceAccessedByFile** association class specifies the logical device accessed by using the referenced [**CIM\_DeviceFile**](cim-devicefile.md) class.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="42f91-105">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="42f91-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="42f91-106">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="42f91-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="42f91-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="42f91-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="42f91-108">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="42f91-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="42f91-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="42f91-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{05D1FFF2-DB36-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_DeviceAccessedByFile : CIM_Dependency
{
  CIM_LogicalDevice REF Dependent;
  CIM_DeviceFile    REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="42f91-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="42f91-110">Members</span></span>

<span data-ttu-id="42f91-111">La clase **CIM \_ DeviceAccessedByFile** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="42f91-111">The **CIM\_DeviceAccessedByFile** class has these types of members:</span></span>

-   [<span data-ttu-id="42f91-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="42f91-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="42f91-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="42f91-113">Properties</span></span>

<span data-ttu-id="42f91-114">La clase **CIM \_ DeviceAccessedByFile** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="42f91-114">The **CIM\_DeviceAccessedByFile** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="42f91-115">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="42f91-115">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42f91-116">Tipo de datos: **CIM \_ DeviceFile**</span><span class="sxs-lookup"><span data-stu-id="42f91-116">Data type: **CIM\_DeviceFile**</span></span>
</dt> <dt>

<span data-ttu-id="42f91-117">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="42f91-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="42f91-118">Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente")</span><span class="sxs-lookup"><span data-stu-id="42f91-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="42f91-119">Un [**\_ DeviceFile de CIM**](cim-devicefile.md) que describe el archivo de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="42f91-119">A [**CIM\_DeviceFile**](cim-devicefile.md) that describes the device file.</span></span>

</dd> <dt>

<span data-ttu-id="42f91-120">**Dependientes**</span><span class="sxs-lookup"><span data-stu-id="42f91-120">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42f91-121">Tipo de datos **: \_ LogicalDevice de CIM**</span><span class="sxs-lookup"><span data-stu-id="42f91-121">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="42f91-122">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="42f91-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="42f91-123">Calificadores: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span><span class="sxs-lookup"><span data-stu-id="42f91-123">Qualifiers: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="42f91-124">Un [**\_ LogicalDevice de CIM**](cim-logicaldevice.md) que describe el dispositivo al que se accede mediante el archivo de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="42f91-124">A [**CIM\_LogicalDevice**](cim-logicaldevice.md) that describes the device that is accessed using the device file.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="42f91-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="42f91-125">Remarks</span></span>

<span data-ttu-id="42f91-126">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="42f91-126">WMI does not implement this class.</span></span>

<span data-ttu-id="42f91-127">La clase **CIM \_ DeviceAccessedByFile** se deriva de [**la \_ dependencia CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="42f91-127">The **CIM\_DeviceAccessedByFile** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="42f91-128">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="42f91-128">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="42f91-129">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="42f91-129">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="42f91-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="42f91-130">Requirements</span></span>



| <span data-ttu-id="42f91-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="42f91-131">Requirement</span></span> | <span data-ttu-id="42f91-132">Value</span><span class="sxs-lookup"><span data-stu-id="42f91-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="42f91-133">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="42f91-133">Minimum supported client</span></span><br/> | <span data-ttu-id="42f91-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="42f91-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="42f91-135">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="42f91-135">Minimum supported server</span></span><br/> | <span data-ttu-id="42f91-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="42f91-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="42f91-137">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="42f91-137">Namespace</span></span><br/>                | <span data-ttu-id="42f91-138">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="42f91-138">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="42f91-139">MOF</span><span class="sxs-lookup"><span data-stu-id="42f91-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="42f91-140"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="42f91-140"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="42f91-141">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="42f91-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="42f91-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="42f91-142"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="42f91-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="42f91-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42f91-144">**Dependencia de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="42f91-144">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

