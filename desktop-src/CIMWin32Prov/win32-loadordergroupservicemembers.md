---
description: La \_ clase WMI LoadOrderGroupServiceMembers Association de Win32 relaciona un grupo de orden de carga y un servicio base.
ms.assetid: 60fa8292-b9d1-48f2-bd26-e5c9276006fc
ms.tgt_platform: multiple
title: Win32_LoadOrderGroupServiceMembers (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_LoadOrderGroupServiceMembers
- Win32_LoadOrderGroupServiceMembers.GroupComponent
- Win32_LoadOrderGroupServiceMembers.PartComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 557e9b029dcbdac06e24d1630f00488696792e25
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907491"
---
# <a name="win32_loadordergroupservicemembers-class"></a><span data-ttu-id="2c835-103">\_Clase Win32 LoadOrderGroupServiceMembers</span><span class="sxs-lookup"><span data-stu-id="2c835-103">Win32\_LoadOrderGroupServiceMembers class</span></span>

<span data-ttu-id="2c835-104">La [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ LoadOrderGroupServiceMembers** Association de Win32 relaciona un grupo de orden de carga y un servicio base.</span><span class="sxs-lookup"><span data-stu-id="2c835-104">The **Win32\_LoadOrderGroupServiceMembers** association [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) relates a load order group and a base service.</span></span>

> [!Note]  
> <span data-ttu-id="2c835-105">[**Win32 \_**](win32-systemdriver.md) Los objetos SystemDriver son miembros de ese grupo de orden de carga.</span><span class="sxs-lookup"><span data-stu-id="2c835-105">[**Win32\_SystemDriver**](win32-systemdriver.md) objects are members of that load order group.</span></span> <span data-ttu-id="2c835-106">No todos los servicios son miembros de grupos y no todos los grupos tienen servicios dentro de ellos.</span><span class="sxs-lookup"><span data-stu-id="2c835-106">Not all services are members of groups, and not all groups have services within them.</span></span>

 

<span data-ttu-id="2c835-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="2c835-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="2c835-108">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="2c835-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="2c835-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2c835-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4EF-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_LoadOrderGroupServiceMembers : CIM_Component
{
  Win32_LoadOrderGroup REF GroupComponent;
  Win32_BaseService    REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="2c835-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="2c835-110">Members</span></span>

<span data-ttu-id="2c835-111">La **clase \_ LoadOrderGroupServiceMembers de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="2c835-111">The **Win32\_LoadOrderGroupServiceMembers** class has these types of members:</span></span>

-   [<span data-ttu-id="2c835-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="2c835-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2c835-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="2c835-113">Properties</span></span>

<span data-ttu-id="2c835-114">La **clase \_ LoadOrderGroupServiceMembers de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="2c835-114">The **Win32\_LoadOrderGroupServiceMembers** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2c835-115">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="2c835-115">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c835-116">Tipo de datos: **Win32 \_ LoadOrderGroup**</span><span class="sxs-lookup"><span data-stu-id="2c835-116">Data type: **Win32\_LoadOrderGroup**</span></span>
</dt> <dt>

<span data-ttu-id="2c835-117">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2c835-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2c835-118">Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ LoadOrderGroup")</span><span class="sxs-lookup"><span data-stu-id="2c835-118">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_LoadOrderGroup")</span></span>
</dt> </dl>

<span data-ttu-id="2c835-119">Referencia a la instancia de que representa las propiedades del grupo de orden de carga asociadas al servicio base.</span><span class="sxs-lookup"><span data-stu-id="2c835-119">Reference to the instance representing the load order group properties associated with the base service.</span></span>

</dd> <dt>

<span data-ttu-id="2c835-120">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="2c835-120">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c835-121">Tipo de datos: **Win32 \_ BaseService**</span><span class="sxs-lookup"><span data-stu-id="2c835-121">Data type: **Win32\_BaseService**</span></span>
</dt> <dt>

<span data-ttu-id="2c835-122">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2c835-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2c835-123">Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ BaseService")</span><span class="sxs-lookup"><span data-stu-id="2c835-123">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_BaseService")</span></span>
</dt> </dl>

<span data-ttu-id="2c835-124">Referencia a la instancia de que representa el servicio que es miembro de un grupo de orden de carga.</span><span class="sxs-lookup"><span data-stu-id="2c835-124">Reference to the instance representing the service that is a member of a load order group.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2c835-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2c835-125">Remarks</span></span>

<span data-ttu-id="2c835-126">La **clase \_ LoadOrderGroupServiceMembers de Win32** se deriva [**del \_ componente CIM**](cim-component.md).</span><span class="sxs-lookup"><span data-stu-id="2c835-126">The **Win32\_LoadOrderGroupServiceMembers** class is derived from [**CIM\_Component**](cim-component.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2c835-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2c835-127">Requirements</span></span>



| <span data-ttu-id="2c835-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="2c835-128">Requirement</span></span> | <span data-ttu-id="2c835-129">Value</span><span class="sxs-lookup"><span data-stu-id="2c835-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2c835-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2c835-130">Minimum supported client</span></span><br/> | <span data-ttu-id="2c835-131">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2c835-131">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="2c835-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2c835-132">Minimum supported server</span></span><br/> | <span data-ttu-id="2c835-133">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2c835-133">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="2c835-134">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="2c835-134">Namespace</span></span><br/>                | <span data-ttu-id="2c835-135">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="2c835-135">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="2c835-136">MOF</span><span class="sxs-lookup"><span data-stu-id="2c835-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2c835-137"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2c835-137"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="2c835-138">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="2c835-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2c835-139"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2c835-139"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2c835-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="2c835-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c835-141">**\_Componente CIM**</span><span class="sxs-lookup"><span data-stu-id="2c835-141">**CIM\_Component**</span></span>](cim-component.md)
</dt> <dt>

<span data-ttu-id="2c835-142">[Clases de sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="2c835-142">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

