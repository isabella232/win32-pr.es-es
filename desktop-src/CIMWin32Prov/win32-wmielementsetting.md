---
description: La \_ clase WMI WMIElementSetting Association de Win32 relaciona un servicio que se ejecuta en el sistema de Windows y la configuración de WMI que puede usar.
ms.assetid: 00e9f882-5f54-4042-a916-2f90ed9a37c0
ms.tgt_platform: multiple
title: Win32_WMIElementSetting (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_WMIElementSetting
- Win32_WMIElementSetting.Element
- Win32_WMIElementSetting.Setting
api_type:
- DllExport
api_location:
- Wbemcore.dll
ms.openlocfilehash: 41f79614fd0931759d502bbd61c7f4143e9e7dc9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907009"
---
# <a name="win32_wmielementsetting-class"></a><span data-ttu-id="e9a80-103">\_Clase Win32 WMIElementSetting</span><span class="sxs-lookup"><span data-stu-id="e9a80-103">Win32\_WMIElementSetting class</span></span>

<span data-ttu-id="e9a80-104">La [clase WMI](../wmisdk/retrieving-a-class.md) **\_ WMIElementSetting** Association de Win32 relaciona un servicio que se ejecuta en el sistema de Windows y la configuración de WMI que puede usar.</span><span class="sxs-lookup"><span data-stu-id="e9a80-104">The **Win32\_WMIElementSetting** association [WMI class](../wmisdk/retrieving-a-class.md) relates a service running in the Windows system and the WMI settings it can use.</span></span>

<span data-ttu-id="e9a80-105">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="e9a80-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="e9a80-106">Las propiedades y los métodos están en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="e9a80-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="e9a80-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e9a80-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("WBEMCORE"), UUID("{A83EF167-CA8D-11d2-B33D-00104BCC4B4A}"), AMENDMENT]
class Win32_WMIElementSetting : CIM_ElementSetting
{
  Win32_Service    REF Element;
  Win32_WMISetting REF Setting;
};
```

## <a name="members"></a><span data-ttu-id="e9a80-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="e9a80-108">Members</span></span>

<span data-ttu-id="e9a80-109">La **clase \_ WMIElementSetting de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="e9a80-109">The **Win32\_WMIElementSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="e9a80-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="e9a80-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e9a80-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="e9a80-111">Properties</span></span>

<span data-ttu-id="e9a80-112">La **clase \_ WMIElementSetting de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="e9a80-112">The **Win32\_WMIElementSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e9a80-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="e9a80-113">**Element**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9a80-114">Tipo de datos **: \_ servicio Win32**</span><span class="sxs-lookup"><span data-stu-id="e9a80-114">Data type: **Win32\_Service**</span></span>
</dt> <dt>

<span data-ttu-id="e9a80-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e9a80-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e9a80-116">Calificadores: [**clave**](../wmisdk/key-qualifier.md), [**invalidación**](../wmisdk/standard-qualifiers.md) ("elemento"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| servicio Win32 de WMI \_ ")</span><span class="sxs-lookup"><span data-stu-id="e9a80-116">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Element"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_Service")</span></span>
</dt> </dl>

<span data-ttu-id="e9a80-117">Referencia a la instancia de que representa el servicio de Windows mediante o en la exposición de las propiedades WMI.</span><span class="sxs-lookup"><span data-stu-id="e9a80-117">Reference to the instance representing the Windows service using or surfacing WMI properties.</span></span>

</dd> <dt>

<span data-ttu-id="e9a80-118">**Configuración**</span><span class="sxs-lookup"><span data-stu-id="e9a80-118">**Setting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e9a80-119">Tipo de datos: **Win32 \_ WMISetting**</span><span class="sxs-lookup"><span data-stu-id="e9a80-119">Data type: **Win32\_WMISetting**</span></span>
</dt> <dt>

<span data-ttu-id="e9a80-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e9a80-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e9a80-121">Calificadores: [**clave**](../wmisdk/key-qualifier.md), [**invalidación**](../wmisdk/standard-qualifiers.md) ("configuración"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ WMISetting")</span><span class="sxs-lookup"><span data-stu-id="e9a80-121">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Setting"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_WMISetting")</span></span>
</dt> </dl>

<span data-ttu-id="e9a80-122">Referencia a la instancia de que representa la configuración de WMI disponible para el servicio de Windows.</span><span class="sxs-lookup"><span data-stu-id="e9a80-122">Reference to the instance representing the WMI settings available to the Windows service.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e9a80-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e9a80-123">Remarks</span></span>

<span data-ttu-id="e9a80-124">La **clase \_ WMIElementSetting de Win32** se deriva de [**\_ ElementSetting de CIM**](cim-elementsetting.md).</span><span class="sxs-lookup"><span data-stu-id="e9a80-124">The **Win32\_WMIElementSetting** class is derived from [**CIM\_ElementSetting**](cim-elementsetting.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e9a80-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e9a80-125">Requirements</span></span>



| <span data-ttu-id="e9a80-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="e9a80-126">Requirement</span></span> | <span data-ttu-id="e9a80-127">Value</span><span class="sxs-lookup"><span data-stu-id="e9a80-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e9a80-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e9a80-128">Minimum supported client</span></span><br/> | <span data-ttu-id="e9a80-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e9a80-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e9a80-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e9a80-130">Minimum supported server</span></span><br/> | <span data-ttu-id="e9a80-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e9a80-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e9a80-132">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="e9a80-132">Namespace</span></span><br/>                | <span data-ttu-id="e9a80-133">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="e9a80-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="e9a80-134">MOF</span><span class="sxs-lookup"><span data-stu-id="e9a80-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e9a80-135"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e9a80-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="e9a80-136">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="e9a80-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e9a80-137"><dt>Wbemcore.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e9a80-137"><dt>Wbemcore.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e9a80-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="e9a80-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9a80-139">**\_ELEMENTSETTING CIM**</span><span class="sxs-lookup"><span data-stu-id="e9a80-139">**CIM\_ElementSetting**</span></span>](cim-elementsetting.md)
</dt> <dt>

[<span data-ttu-id="e9a80-140">Clases de administración de servicios WMI</span><span class="sxs-lookup"><span data-stu-id="e9a80-140">WMI Service Management Classes</span></span>](./wmi-service-management-classes.md)
</dt> </dl>

 

 
