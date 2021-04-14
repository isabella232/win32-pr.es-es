---
description: La \_ clase WMI SystemSetting Abstract Association de Win32 relaciona un equipo y una configuración general en ese sistema.
ms.assetid: 796ee263-2526-43f8-bd3d-23442b6bd4ca
ms.tgt_platform: multiple
title: Win32_SystemSetting (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemSetting
- Win32_SystemSetting.Element
- Win32_SystemSetting.Setting
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: e29b752d769cd347ce1cfdb729bf8c0c3959a4f5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496673"
---
# <a name="win32_systemsetting-class"></a><span data-ttu-id="e9345-103">\_Clase Win32 SystemSetting</span><span class="sxs-lookup"><span data-stu-id="e9345-103">Win32\_SystemSetting class</span></span>

<span data-ttu-id="e9345-104">La [clase WMI](../wmisdk/retrieving-a-class.md) **\_ SystemSetting** Abstract Association de Win32 relaciona un equipo y una configuración general en ese sistema.</span><span class="sxs-lookup"><span data-stu-id="e9345-104">The **Win32\_SystemSetting** abstract association [WMI class](../wmisdk/retrieving-a-class.md) relates a computer system and a general setting on that system.</span></span>

<span data-ttu-id="e9345-105">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="e9345-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="e9345-106">Las propiedades y los métodos están en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="e9345-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="e9345-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e9345-107">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C501-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SystemSetting : CIM_ElementSetting
{
  Win32_ComputerSystem REF Element;
  CIM_Setting          REF Setting;
};
```

## <a name="members"></a><span data-ttu-id="e9345-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="e9345-108">Members</span></span>

<span data-ttu-id="e9345-109">La **clase \_ SystemSetting de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="e9345-109">The **Win32\_SystemSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="e9345-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="e9345-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e9345-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="e9345-111">Properties</span></span>

<span data-ttu-id="e9345-112">La **clase \_ SystemSetting de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="e9345-112">The **Win32\_SystemSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e9345-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="e9345-113">**Element**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9345-114">Tipo de datos: **Win32 \_ ComputerSystem**</span><span class="sxs-lookup"><span data-stu-id="e9345-114">Data type: **Win32\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="e9345-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e9345-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e9345-116">Calificadores: [**clave**](../wmisdk/key-qualifier.md), [**invalidación**](../wmisdk/standard-qualifiers.md) ("elemento"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ ComputerSystem")</span><span class="sxs-lookup"><span data-stu-id="e9345-116">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Element"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_ComputerSystem")</span></span>
</dt> </dl>

<span data-ttu-id="e9345-117">Referencia a la instancia de que representa las propiedades de un equipo en el que se puede aplicar esta configuración.</span><span class="sxs-lookup"><span data-stu-id="e9345-117">Reference to the instance representing the properties of a computer system where this setting can be applied.</span></span>

</dd> <dt>

<span data-ttu-id="e9345-118">**Configuración**</span><span class="sxs-lookup"><span data-stu-id="e9345-118">**Setting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9345-119">Tipo de datos **: \_ configuración de CIM**</span><span class="sxs-lookup"><span data-stu-id="e9345-119">Data type: **CIM\_Setting**</span></span>
</dt> <dt>

<span data-ttu-id="e9345-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e9345-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e9345-121">Calificadores: [**clave**](../wmisdk/key-qualifier.md), [**invalidación**](../wmisdk/standard-qualifiers.md) ("configuración"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| configuración CIM CIM \_ ")</span><span class="sxs-lookup"><span data-stu-id="e9345-121">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Setting"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("CIM\|CIM\_Setting")</span></span>
</dt> </dl>

<span data-ttu-id="e9345-122">Referencia a la instancia de que representa las propiedades de la configuración que se puede aplicar al sistema del equipo.</span><span class="sxs-lookup"><span data-stu-id="e9345-122">Reference to the instance representing the properties of the setting that can be applied to the computer system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e9345-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e9345-123">Remarks</span></span>

<span data-ttu-id="e9345-124">La **clase \_ SystemSetting de Win32** se deriva de [**\_ ElementSetting de CIM**](cim-elementsetting.md).</span><span class="sxs-lookup"><span data-stu-id="e9345-124">The **Win32\_SystemSetting** class is derived from [**CIM\_ElementSetting**](cim-elementsetting.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e9345-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e9345-125">Requirements</span></span>



| <span data-ttu-id="e9345-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="e9345-126">Requirement</span></span> | <span data-ttu-id="e9345-127">Value</span><span class="sxs-lookup"><span data-stu-id="e9345-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e9345-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e9345-128">Minimum supported client</span></span><br/> | <span data-ttu-id="e9345-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e9345-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e9345-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e9345-130">Minimum supported server</span></span><br/> | <span data-ttu-id="e9345-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e9345-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e9345-132">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="e9345-132">Namespace</span></span><br/>                | <span data-ttu-id="e9345-133">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="e9345-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="e9345-134">MOF</span><span class="sxs-lookup"><span data-stu-id="e9345-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e9345-135"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e9345-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="e9345-136">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="e9345-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e9345-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e9345-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e9345-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="e9345-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9345-139">**\_ELEMENTSETTING CIM**</span><span class="sxs-lookup"><span data-stu-id="e9345-139">**CIM\_ElementSetting**</span></span>](cim-elementsetting.md)
</dt> <dt>

[<span data-ttu-id="e9345-140">Clases de sistema operativo</span><span class="sxs-lookup"><span data-stu-id="e9345-140">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
