---
description: La \_ clase WMI DependentService Association de Win32 relaciona dos servicios base interdependientes.
ms.assetid: ba21fce3-f8f9-4886-b09d-a9e830376364
ms.tgt_platform: multiple
title: Win32_DependentService (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_DependentService
- Win32_DependentService.TypeOfDependency
- Win32_DependentService.Antecedent
- Win32_DependentService.Dependent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 047ec3411186f09f3d0e76da27158aa8ee91d4cc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153549"
---
# <a name="win32_dependentservice-class"></a><span data-ttu-id="7a780-103">\_Clase Win32 DependentService</span><span class="sxs-lookup"><span data-stu-id="7a780-103">Win32\_DependentService class</span></span>

<span data-ttu-id="7a780-104">La [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ DependentService** Association de Win32 relaciona dos servicios base interdependientes.</span><span class="sxs-lookup"><span data-stu-id="7a780-104">The **Win32\_DependentService** association [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) relates two interdependent base services.</span></span>

<span data-ttu-id="7a780-105">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="7a780-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="7a780-106">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="7a780-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="7a780-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7a780-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4FA-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_DependentService : CIM_ServiceServiceDependency
{
  uint16                TypeOfDependency;
  Win32_BaseService REF Antecedent;
  Win32_BaseService REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="7a780-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="7a780-108">Members</span></span>

<span data-ttu-id="7a780-109">La **clase \_ DependentService de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="7a780-109">The **Win32\_DependentService** class has these types of members:</span></span>

-   [<span data-ttu-id="7a780-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="7a780-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7a780-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="7a780-111">Properties</span></span>

<span data-ttu-id="7a780-112">La **clase \_ DependentService de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="7a780-112">The **Win32\_DependentService** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7a780-113">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="7a780-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7a780-114">Tipo de datos: **Win32 \_ BaseService**</span><span class="sxs-lookup"><span data-stu-id="7a780-114">Data type: **Win32\_BaseService**</span></span>
</dt> <dt>

<span data-ttu-id="7a780-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7a780-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7a780-116">Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ BaseService")</span><span class="sxs-lookup"><span data-stu-id="7a780-116">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_BaseService")</span></span>
</dt> </dl>

<span data-ttu-id="7a780-117">[**\_ BaseService de Win32**](win32-baseservice.md) que representa el servicio base basado en la propiedad **dependiente** de esta clase.</span><span class="sxs-lookup"><span data-stu-id="7a780-117">A [**Win32\_BaseService**](win32-baseservice.md) representing the base service relied upon by the **Dependent** property of this class.</span></span>

</dd> <dt>

<span data-ttu-id="7a780-118">**Dependientes**</span><span class="sxs-lookup"><span data-stu-id="7a780-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7a780-119">Tipo de datos: **Win32 \_ BaseService**</span><span class="sxs-lookup"><span data-stu-id="7a780-119">Data type: **Win32\_BaseService**</span></span>
</dt> <dt>

<span data-ttu-id="7a780-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7a780-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7a780-121">Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependiente"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ BaseService")</span><span class="sxs-lookup"><span data-stu-id="7a780-121">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_BaseService")</span></span>
</dt> </dl>

<span data-ttu-id="7a780-122">[**\_ BaseService de Win32**](win32-baseservice.md) que representa el servicio base que depende de la propiedad **Antecedent** de esta clase.</span><span class="sxs-lookup"><span data-stu-id="7a780-122">A [**Win32\_BaseService**](win32-baseservice.md) representing the base service that is dependent on the **Antecedent** property of this class.</span></span>

</dd> <dt>

<span data-ttu-id="7a780-123">**TypeOfDependency**</span><span class="sxs-lookup"><span data-stu-id="7a780-123">**TypeOfDependency**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7a780-124">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7a780-124">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7a780-125">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7a780-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7a780-126">Naturaleza de la dependencia entre servicios.</span><span class="sxs-lookup"><span data-stu-id="7a780-126">Nature of the service-to-service dependency.</span></span> <span data-ttu-id="7a780-127">Esta propiedad indica que el servicio asociado debe haber finalizado, debe iniciarse o no debe iniciarse para que el servicio funcione.</span><span class="sxs-lookup"><span data-stu-id="7a780-127">This property indicates that the associated service must have completed, must be started, or must not be started for the service to function.</span></span>

<span data-ttu-id="7a780-128">Esta propiedad se hereda de [**\_ ServiceServiceDependency CIM**](cim-serviceservicedependency.md).</span><span class="sxs-lookup"><span data-stu-id="7a780-128">This property is inherited from [**CIM\_ServiceServiceDependency**](cim-serviceservicedependency.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="7a780-129"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="7a780-129"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="7a780-130"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="7a780-130"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Service_Must_Have_Completed"></span><span id="service_must_have_completed"></span><span id="SERVICE_MUST_HAVE_COMPLETED"></span>

<span data-ttu-id="7a780-131"><span id="Service_Must_Have_Completed"></span><span id="service_must_have_completed"></span><span id="SERVICE_MUST_HAVE_COMPLETED"></span>El **servicio debe haberse completado** (2)</span><span class="sxs-lookup"><span data-stu-id="7a780-131"><span id="Service_Must_Have_Completed"></span><span id="service_must_have_completed"></span><span id="SERVICE_MUST_HAVE_COMPLETED"></span>**Service Must Have Completed** (2)</span></span>


</dt> <dd>

<span data-ttu-id="7a780-132">El servicio debe haberse completado.</span><span class="sxs-lookup"><span data-stu-id="7a780-132">Service must have completed.</span></span>

</dd> <dt>

<span id="Service_Must_Be_Started"></span><span id="service_must_be_started"></span><span id="SERVICE_MUST_BE_STARTED"></span>

<span data-ttu-id="7a780-133"><span id="Service_Must_Be_Started"></span><span id="service_must_be_started"></span><span id="SERVICE_MUST_BE_STARTED"></span>El **servicio debe iniciarse** (3)</span><span class="sxs-lookup"><span data-stu-id="7a780-133"><span id="Service_Must_Be_Started"></span><span id="service_must_be_started"></span><span id="SERVICE_MUST_BE_STARTED"></span>**Service Must Be Started** (3)</span></span>


</dt> <dd>

<span data-ttu-id="7a780-134">Debe iniciarse el servicio.</span><span class="sxs-lookup"><span data-stu-id="7a780-134">Service must be started.</span></span>

</dd> <dt>

<span id="Service_Must_Not_Be_Started"></span><span id="service_must_not_be_started"></span><span id="SERVICE_MUST_NOT_BE_STARTED"></span>

<span data-ttu-id="7a780-135"><span id="Service_Must_Not_Be_Started"></span><span id="service_must_not_be_started"></span><span id="SERVICE_MUST_NOT_BE_STARTED"></span>**No se debe iniciar el servicio** (4)</span><span class="sxs-lookup"><span data-stu-id="7a780-135"><span id="Service_Must_Not_Be_Started"></span><span id="service_must_not_be_started"></span><span id="SERVICE_MUST_NOT_BE_STARTED"></span>**Service Must Not Be Started** (4)</span></span>


</dt> <dd>

<span data-ttu-id="7a780-136">No se debe iniciar el servicio.</span><span class="sxs-lookup"><span data-stu-id="7a780-136">Service must not be started.</span></span>

</dd> </dl>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7a780-137">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7a780-137">Remarks</span></span>

<span data-ttu-id="7a780-138">La **clase \_ DependentService de Win32** se deriva de [**\_ ServiceServiceDependency de CIM**](cim-serviceservicedependency.md).</span><span class="sxs-lookup"><span data-stu-id="7a780-138">The **Win32\_DependentService** class is derived from [**CIM\_ServiceServiceDependency**](cim-serviceservicedependency.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7a780-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7a780-139">Requirements</span></span>



| <span data-ttu-id="7a780-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="7a780-140">Requirement</span></span> | <span data-ttu-id="7a780-141">Value</span><span class="sxs-lookup"><span data-stu-id="7a780-141">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7a780-142">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7a780-142">Minimum supported client</span></span><br/> | <span data-ttu-id="7a780-143">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7a780-143">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="7a780-144">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7a780-144">Minimum supported server</span></span><br/> | <span data-ttu-id="7a780-145">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7a780-145">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="7a780-146">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="7a780-146">Namespace</span></span><br/>                | <span data-ttu-id="7a780-147">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="7a780-147">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="7a780-148">MOF</span><span class="sxs-lookup"><span data-stu-id="7a780-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7a780-149"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7a780-149"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="7a780-150">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="7a780-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7a780-151"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7a780-151"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7a780-152">Vea también</span><span class="sxs-lookup"><span data-stu-id="7a780-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a780-153">**\_SERVICESERVICEDEPENDENCY CIM**</span><span class="sxs-lookup"><span data-stu-id="7a780-153">**CIM\_ServiceServiceDependency**</span></span>](cim-serviceservicedependency.md)
</dt> <dt>

<span data-ttu-id="7a780-154">[Clases de sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="7a780-154">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

