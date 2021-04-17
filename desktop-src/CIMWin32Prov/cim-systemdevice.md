---
description: La \_ Asociación SystemDevice de CIM representa una relación explícita en la que un sistema puede agregar dispositivos lógicos.
ms.assetid: df624a9f-0c10-44a3-8075-908e5e481e3c
ms.tgt_platform: multiple
title: CIM_SystemDevice (clase) (proveedores WMI de CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SystemDevice
- CIM_SystemDevice.PartComponent
- CIM_SystemDevice.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: dbff9a0ead8790de9ab323509c8b2f1392e6ed6e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659623"
---
# <a name="cim_systemdevice-class-cimwin32-wmi-providers"></a><span data-ttu-id="cf976-103">CIM_SystemDevice (clase) (proveedores WMI de CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="cf976-103">CIM_SystemDevice class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="cf976-104">La **Asociación \_ SystemDevice de CIM** representa una relación explícita en la que un sistema puede agregar dispositivos lógicos.</span><span class="sxs-lookup"><span data-stu-id="cf976-104">The **CIM\_SystemDevice** association represents an explicit relationship in which logical devices can be aggregated by a system.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="cf976-105">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="cf976-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="cf976-106">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="cf976-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="cf976-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="cf976-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="cf976-108">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="cf976-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="cf976-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="cf976-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{4B2C30D7-BAFE-11d2-85E5-0000F8102E5F}"), AMENDMENT]
class CIM_SystemDevice : CIM_SystemComponent
{
  CIM_LogicalDevice REF PartComponent;
  CIM_System        REF GroupComponent;
};
```

## <a name="members"></a><span data-ttu-id="cf976-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="cf976-110">Members</span></span>

<span data-ttu-id="cf976-111">La clase **CIM \_ SystemDevice** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="cf976-111">The **CIM\_SystemDevice** class has these types of members:</span></span>

-   [<span data-ttu-id="cf976-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="cf976-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="cf976-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="cf976-113">Properties</span></span>

<span data-ttu-id="cf976-114">La clase **CIM \_ SystemDevice** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="cf976-114">The **CIM\_SystemDevice** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="cf976-115">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="cf976-115">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf976-116">Tipo de datos **: \_ Sistema CIM**</span><span class="sxs-lookup"><span data-stu-id="cf976-116">Data type: **CIM\_System**</span></span>
</dt> <dt>

<span data-ttu-id="cf976-117">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="cf976-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cf976-118">Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="cf976-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="cf976-119">[**\_ Sistema CIM**](cim-system.md) que describe el sistema primario de la asociación.</span><span class="sxs-lookup"><span data-stu-id="cf976-119">A [**CIM\_System**](cim-system.md) that describes the parent system in the association.</span></span>

</dd> <dt>

<span data-ttu-id="cf976-120">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="cf976-120">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf976-121">Tipo de datos **: \_ LogicalDevice de CIM**</span><span class="sxs-lookup"><span data-stu-id="cf976-121">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="cf976-122">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="cf976-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cf976-123">Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**débil**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="cf976-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**Weak**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="cf976-124">Un [**\_ LogicalDevice de CIM**](cim-logicaldevice.md) que describe el dispositivo lógico que es un componente de un sistema.</span><span class="sxs-lookup"><span data-stu-id="cf976-124">A [**CIM\_LogicalDevice**](cim-logicaldevice.md) that describes the logical device that is a component of a system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="cf976-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="cf976-125">Remarks</span></span>

<span data-ttu-id="cf976-126">La clase **CIM \_ SystemDevice** se deriva de [**\_ SystemComponent de CIM**](cim-systemcomponent.md).</span><span class="sxs-lookup"><span data-stu-id="cf976-126">The **CIM\_SystemDevice** class is derived from [**CIM\_SystemComponent**](cim-systemcomponent.md).</span></span>

<span data-ttu-id="cf976-127">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="cf976-127">WMI does not implement this class.</span></span> <span data-ttu-id="cf976-128">Para las clases WMI derivadas de **CIM \_ SystemDevice**, vea [clases Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="cf976-128">For WMI classes derived from **CIM\_SystemDevice**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="cf976-129">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="cf976-129">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="cf976-130">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="cf976-130">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="cf976-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cf976-131">Requirements</span></span>



| <span data-ttu-id="cf976-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="cf976-132">Requirement</span></span> | <span data-ttu-id="cf976-133">Value</span><span class="sxs-lookup"><span data-stu-id="cf976-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cf976-134">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cf976-134">Minimum supported client</span></span><br/> | <span data-ttu-id="cf976-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="cf976-135">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="cf976-136">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cf976-136">Minimum supported server</span></span><br/> | <span data-ttu-id="cf976-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cf976-137">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="cf976-138">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="cf976-138">Namespace</span></span><br/>                | <span data-ttu-id="cf976-139">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="cf976-139">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="cf976-140">MOF</span><span class="sxs-lookup"><span data-stu-id="cf976-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cf976-141"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="cf976-141"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="cf976-142">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="cf976-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cf976-143"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cf976-143"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cf976-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="cf976-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf976-145">**\_SYSTEMCOMPONENT CIM**</span><span class="sxs-lookup"><span data-stu-id="cf976-145">**CIM\_SystemComponent**</span></span>](cim-systemcomponent.md)
</dt> </dl>

 

