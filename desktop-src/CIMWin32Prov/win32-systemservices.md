---
description: La \_ clase WMI SystemServices Association de Win32 relaciona un equipo y un programa de servicio que existe en el sistema.
ms.assetid: b372e696-e1e0-4b1e-9fb8-83af8a75c405
ms.tgt_platform: multiple
title: Win32_SystemServices (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemServices
- Win32_SystemServices.GroupComponent
- Win32_SystemServices.PartComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: d8e61469729f3753256bc7fcf5598265b5c1b7dc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807442"
---
# <a name="win32_systemservices-class"></a><span data-ttu-id="9cd57-103">\_Clase Win32 SystemServices</span><span class="sxs-lookup"><span data-stu-id="9cd57-103">Win32\_SystemServices class</span></span>

<span data-ttu-id="9cd57-104">La [clase WMI](../wmisdk/retrieving-a-class.md) **\_ SystemServices** Association de Win32 relaciona un equipo y un programa de servicio que existe en el sistema.</span><span class="sxs-lookup"><span data-stu-id="9cd57-104">The **Win32\_SystemServices** association [WMI class](../wmisdk/retrieving-a-class.md) relates a computer system and a service program that exists on the system.</span></span>

<span data-ttu-id="9cd57-105">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="9cd57-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="9cd57-106">Las propiedades y los métodos están en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="9cd57-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="9cd57-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9cd57-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4F6-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SystemServices : CIM_SystemComponent
{
  Win32_ComputerSystem REF GroupComponent;
  Win32_Service        REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="9cd57-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="9cd57-108">Members</span></span>

<span data-ttu-id="9cd57-109">La **clase \_ SystemServices de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="9cd57-109">The **Win32\_SystemServices** class has these types of members:</span></span>

-   [<span data-ttu-id="9cd57-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="9cd57-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9cd57-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="9cd57-111">Properties</span></span>

<span data-ttu-id="9cd57-112">La **clase \_ SystemServices de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="9cd57-112">The **Win32\_SystemServices** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9cd57-113">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="9cd57-113">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cd57-114">Tipo de datos: **Win32 \_ ComputerSystem**</span><span class="sxs-lookup"><span data-stu-id="9cd57-114">Data type: **Win32\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="9cd57-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9cd57-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9cd57-116">Calificadores: [**clave**](../wmisdk/key-qualifier.md), [**invalidación**](../wmisdk/standard-qualifiers.md) ("GroupComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ ComputerSystem")</span><span class="sxs-lookup"><span data-stu-id="9cd57-116">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("GroupComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_ComputerSystem")</span></span>
</dt> </dl>

<span data-ttu-id="9cd57-117">Referencia a la instancia de que representa las propiedades del sistema del equipo en el que existe el servicio.</span><span class="sxs-lookup"><span data-stu-id="9cd57-117">Reference to the instance representing the properties of the computer system on which the service exists.</span></span>

</dd> <dt>

<span data-ttu-id="9cd57-118">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="9cd57-118">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9cd57-119">Tipo de datos **: \_ servicio Win32**</span><span class="sxs-lookup"><span data-stu-id="9cd57-119">Data type: **Win32\_Service**</span></span>
</dt> <dt>

<span data-ttu-id="9cd57-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9cd57-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9cd57-121">Calificadores: [**clave**](../wmisdk/key-qualifier.md), [**invalidación**](../wmisdk/standard-qualifiers.md) ("PartComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| servicio Win32 de WMI \_ ")</span><span class="sxs-lookup"><span data-stu-id="9cd57-121">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("PartComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_Service")</span></span>
</dt> </dl>

<span data-ttu-id="9cd57-122">Referencia a la instancia de que representa el servicio que existe en el sistema del equipo.</span><span class="sxs-lookup"><span data-stu-id="9cd57-122">Reference to the instance representing the service that exists on the computer system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9cd57-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9cd57-123">Remarks</span></span>

<span data-ttu-id="9cd57-124">La **clase \_ SystemServices de Win32** se deriva de [**\_ SystemComponent de CIM**](cim-systemcomponent.md).</span><span class="sxs-lookup"><span data-stu-id="9cd57-124">The **Win32\_SystemServices** class is derived from [**CIM\_SystemComponent**](cim-systemcomponent.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9cd57-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9cd57-125">Requirements</span></span>



| <span data-ttu-id="9cd57-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="9cd57-126">Requirement</span></span> | <span data-ttu-id="9cd57-127">Value</span><span class="sxs-lookup"><span data-stu-id="9cd57-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9cd57-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9cd57-128">Minimum supported client</span></span><br/> | <span data-ttu-id="9cd57-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9cd57-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="9cd57-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9cd57-130">Minimum supported server</span></span><br/> | <span data-ttu-id="9cd57-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9cd57-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="9cd57-132">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="9cd57-132">Namespace</span></span><br/>                | <span data-ttu-id="9cd57-133">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="9cd57-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="9cd57-134">MOF</span><span class="sxs-lookup"><span data-stu-id="9cd57-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9cd57-135"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9cd57-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="9cd57-136">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="9cd57-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9cd57-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9cd57-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9cd57-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="9cd57-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9cd57-139">**\_SYSTEMCOMPONENT CIM**</span><span class="sxs-lookup"><span data-stu-id="9cd57-139">**CIM\_SystemComponent**</span></span>](cim-systemcomponent.md)
</dt> <dt>

[<span data-ttu-id="9cd57-140">Clases de sistema operativo</span><span class="sxs-lookup"><span data-stu-id="9cd57-140">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
