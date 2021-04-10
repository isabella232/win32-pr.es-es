---
description: La \_ clase WMI SystemNetworkConnections Association de Win32 relaciona una conexión de red y el sistema del equipo en el que reside.
ms.assetid: 7c47f653-74a9-4729-a72c-94930181f8c9
ms.tgt_platform: multiple
title: Win32_SystemNetworkConnections (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemNetworkConnections
- Win32_SystemNetworkConnections.GroupComponent
- Win32_SystemNetworkConnections.PartComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: e90562dd4f98a00cf848fb83a9e3051b387241e4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153493"
---
# <a name="win32_systemnetworkconnections-class"></a><span data-ttu-id="d9939-103">\_Clase Win32 SystemNetworkConnections</span><span class="sxs-lookup"><span data-stu-id="d9939-103">Win32\_SystemNetworkConnections class</span></span>

<span data-ttu-id="d9939-104">La [clase WMI](../wmisdk/retrieving-a-class.md) **\_ SystemNetworkConnections** Association de Win32 relaciona una conexión de red y el sistema del equipo en el que reside.</span><span class="sxs-lookup"><span data-stu-id="d9939-104">The **Win32\_SystemNetworkConnections** association [WMI class](../wmisdk/retrieving-a-class.md) relates a network connection and the computer system on which it resides.</span></span>

<span data-ttu-id="d9939-105">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="d9939-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="d9939-106">Las propiedades y los métodos están en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="d9939-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="d9939-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d9939-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4F7-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SystemNetworkConnections : CIM_SystemComponent
{
  Win32_ComputerSystem    REF GroupComponent;
  Win32_NetworkConnection REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="d9939-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="d9939-108">Members</span></span>

<span data-ttu-id="d9939-109">La **clase \_ SystemNetworkConnections de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="d9939-109">The **Win32\_SystemNetworkConnections** class has these types of members:</span></span>

-   [<span data-ttu-id="d9939-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d9939-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d9939-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d9939-111">Properties</span></span>

<span data-ttu-id="d9939-112">La **clase \_ SystemNetworkConnections de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="d9939-112">The **Win32\_SystemNetworkConnections** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d9939-113">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="d9939-113">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9939-114">Tipo de datos: **Win32 \_ ComputerSystem**</span><span class="sxs-lookup"><span data-stu-id="d9939-114">Data type: **Win32\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="d9939-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d9939-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d9939-116">Calificadores: [**clave**](../wmisdk/key-qualifier.md), [**invalidación**](../wmisdk/standard-qualifiers.md) ("GroupComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ ComputerSystem")</span><span class="sxs-lookup"><span data-stu-id="d9939-116">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("GroupComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_ComputerSystem")</span></span>
</dt> </dl>

<span data-ttu-id="d9939-117">Referencia a la instancia de que representa el sistema del equipo conectado a la red.</span><span class="sxs-lookup"><span data-stu-id="d9939-117">Reference to the instance representing the computer system connected to the network.</span></span>

</dd> <dt>

<span data-ttu-id="d9939-118">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="d9939-118">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9939-119">Tipo de datos: **Win32 \_ NetworkConnection**</span><span class="sxs-lookup"><span data-stu-id="d9939-119">Data type: **Win32\_NetworkConnection**</span></span>
</dt> <dt>

<span data-ttu-id="d9939-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d9939-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d9939-121">Calificadores: [**clave**](../wmisdk/key-qualifier.md), [**invalidación**](../wmisdk/standard-qualifiers.md) ("PartComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ NetworkConnection")</span><span class="sxs-lookup"><span data-stu-id="d9939-121">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("PartComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_NetworkConnection")</span></span>
</dt> </dl>

<span data-ttu-id="d9939-122">Referencia a la instancia de que representa la conexión de red a este equipo.</span><span class="sxs-lookup"><span data-stu-id="d9939-122">Reference to the instance representing the network connection to this computer system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d9939-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d9939-123">Remarks</span></span>

<span data-ttu-id="d9939-124">La **clase \_ SystemNetworkConnections de Win32** se deriva de [**\_ SystemComponent de CIM**](cim-systemcomponent.md).</span><span class="sxs-lookup"><span data-stu-id="d9939-124">The **Win32\_SystemNetworkConnections** class is derived from [**CIM\_SystemComponent**](cim-systemcomponent.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d9939-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d9939-125">Requirements</span></span>



| <span data-ttu-id="d9939-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="d9939-126">Requirement</span></span> | <span data-ttu-id="d9939-127">Value</span><span class="sxs-lookup"><span data-stu-id="d9939-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d9939-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d9939-128">Minimum supported client</span></span><br/> | <span data-ttu-id="d9939-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d9939-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d9939-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d9939-130">Minimum supported server</span></span><br/> | <span data-ttu-id="d9939-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d9939-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d9939-132">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="d9939-132">Namespace</span></span><br/>                | <span data-ttu-id="d9939-133">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="d9939-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="d9939-134">MOF</span><span class="sxs-lookup"><span data-stu-id="d9939-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d9939-135"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d9939-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="d9939-136">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d9939-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d9939-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d9939-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d9939-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="d9939-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d9939-139">**\_SYSTEMCOMPONENT CIM**</span><span class="sxs-lookup"><span data-stu-id="d9939-139">**CIM\_SystemComponent**</span></span>](cim-systemcomponent.md)
</dt> <dt>

[<span data-ttu-id="d9939-140">Clases de sistema operativo</span><span class="sxs-lookup"><span data-stu-id="d9939-140">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
