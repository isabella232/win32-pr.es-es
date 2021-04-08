---
description: La \_ clase WMI SystemUsers Association de Win32 relaciona un equipo y una cuenta de usuario en ese sistema.
ms.assetid: 0f6cba69-86f7-4795-a47d-6fb8ed0a00b8
ms.tgt_platform: multiple
title: Win32_SystemUsers (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemUsers
- Win32_SystemUsers.GroupComponent
- Win32_SystemUsers.PartComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: a2239983d5b9c080c60d301a557b5487f8cf7fcf
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104000784"
---
# <a name="win32_systemusers-class"></a><span data-ttu-id="2397a-103">\_Clase Win32 SystemUsers</span><span class="sxs-lookup"><span data-stu-id="2397a-103">Win32\_SystemUsers class</span></span>

<span data-ttu-id="2397a-104">La [clase WMI](../wmisdk/retrieving-a-class.md) **\_ SystemUsers** Association de Win32 relaciona un equipo y una cuenta de usuario en ese sistema.</span><span class="sxs-lookup"><span data-stu-id="2397a-104">The **Win32\_SystemUsers** association [WMI class](../wmisdk/retrieving-a-class.md) relates a computer system and a user account on that system.</span></span>

<span data-ttu-id="2397a-105">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="2397a-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="2397a-106">Las propiedades y los métodos están en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="2397a-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="2397a-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2397a-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4F2-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SystemUsers : CIM_SystemComponent
{
  Win32_ComputerSystem REF GroupComponent;
  Win32_UserAccount    REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="2397a-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="2397a-108">Members</span></span>

<span data-ttu-id="2397a-109">La **clase \_ SystemUsers de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="2397a-109">The **Win32\_SystemUsers** class has these types of members:</span></span>

-   [<span data-ttu-id="2397a-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="2397a-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2397a-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="2397a-111">Properties</span></span>

<span data-ttu-id="2397a-112">La **clase \_ SystemUsers de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="2397a-112">The **Win32\_SystemUsers** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2397a-113">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="2397a-113">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2397a-114">Tipo de datos: **Win32 \_ ComputerSystem**</span><span class="sxs-lookup"><span data-stu-id="2397a-114">Data type: **Win32\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="2397a-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2397a-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2397a-116">Calificadores: [**clave**](../wmisdk/key-qualifier.md), [**invalidación**](../wmisdk/standard-qualifiers.md) ("GroupComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ ComputerSystem")</span><span class="sxs-lookup"><span data-stu-id="2397a-116">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("GroupComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_ComputerSystem")</span></span>
</dt> </dl>

<span data-ttu-id="2397a-117">Referencia a la instancia de que representa el sistema del equipo que contiene la cuenta de usuario.</span><span class="sxs-lookup"><span data-stu-id="2397a-117">Reference to the instance representing the computer system containing the user account.</span></span>

</dd> <dt>

<span data-ttu-id="2397a-118">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="2397a-118">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2397a-119">Tipo de datos: **Win32 \_ cuentadeusuario**</span><span class="sxs-lookup"><span data-stu-id="2397a-119">Data type: **Win32\_UserAccount**</span></span>
</dt> <dt>

<span data-ttu-id="2397a-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2397a-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2397a-121">Calificadores: [**clave**](../wmisdk/key-qualifier.md), [**invalidación**](../wmisdk/standard-qualifiers.md) ("PartComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ cuentadeusuario")</span><span class="sxs-lookup"><span data-stu-id="2397a-121">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("PartComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_UserAccount")</span></span>
</dt> </dl>

<span data-ttu-id="2397a-122">Referencia a la instancia de que representa la cuenta de usuario en el sistema del equipo.</span><span class="sxs-lookup"><span data-stu-id="2397a-122">Reference to the instance representing the user account on the computer system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2397a-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2397a-123">Remarks</span></span>

<span data-ttu-id="2397a-124">La **clase \_ SystemUsers de Win32** se deriva de [**\_ SystemComponent de CIM**](cim-systemcomponent.md).</span><span class="sxs-lookup"><span data-stu-id="2397a-124">The **Win32\_SystemUsers** class is derived from [**CIM\_SystemComponent**](cim-systemcomponent.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2397a-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2397a-125">Requirements</span></span>



| <span data-ttu-id="2397a-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="2397a-126">Requirement</span></span> | <span data-ttu-id="2397a-127">Value</span><span class="sxs-lookup"><span data-stu-id="2397a-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2397a-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2397a-128">Minimum supported client</span></span><br/> | <span data-ttu-id="2397a-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2397a-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="2397a-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2397a-130">Minimum supported server</span></span><br/> | <span data-ttu-id="2397a-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2397a-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="2397a-132">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="2397a-132">Namespace</span></span><br/>                | <span data-ttu-id="2397a-133">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="2397a-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="2397a-134">MOF</span><span class="sxs-lookup"><span data-stu-id="2397a-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2397a-135"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2397a-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="2397a-136">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="2397a-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2397a-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2397a-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2397a-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="2397a-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2397a-139">**\_SYSTEMCOMPONENT CIM**</span><span class="sxs-lookup"><span data-stu-id="2397a-139">**CIM\_SystemComponent**</span></span>](cim-systemcomponent.md)
</dt> <dt>

[<span data-ttu-id="2397a-140">Clases de sistema operativo</span><span class="sxs-lookup"><span data-stu-id="2397a-140">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
