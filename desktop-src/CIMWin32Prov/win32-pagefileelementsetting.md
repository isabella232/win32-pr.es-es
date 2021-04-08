---
description: La \_ clase WMI PageFileElementSetting Association de Win32 relaciona la configuración inicial de un archivo de paginación y el estado de esos valores durante el uso normal.
ms.assetid: efc1f20d-166e-4e27-9767-f6ec0bbd6c14
ms.tgt_platform: multiple
title: Win32_PageFileElementSetting (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PageFileElementSetting
- Win32_PageFileElementSetting.Element
- Win32_PageFileElementSetting.Setting
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: dfc1087225894cef2895cf41af5e5297769a4041
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104000753"
---
# <a name="win32_pagefileelementsetting-class"></a><span data-ttu-id="02d6a-103">\_Clase Win32 PageFileElementSetting</span><span class="sxs-lookup"><span data-stu-id="02d6a-103">Win32\_PageFileElementSetting class</span></span>

<span data-ttu-id="02d6a-104">La [clase WMI](../wmisdk/retrieving-a-class.md) **\_ PageFileElementSetting** Association de Win32 relaciona la configuración inicial de un archivo de paginación y el estado de esos valores durante el uso normal.</span><span class="sxs-lookup"><span data-stu-id="02d6a-104">The **Win32\_PageFileElementSetting** association [WMI class](../wmisdk/retrieving-a-class.md) relates the initial settings of a page file and the state of those settings during normal use.</span></span>

<span data-ttu-id="02d6a-105">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="02d6a-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="02d6a-106">Las propiedades y los métodos están en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="02d6a-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="02d6a-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="02d6a-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8E7F70E8-C856-11D2-B364-00105A1F77A1}"), AMENDMENT]
class Win32_PageFileElementSetting : CIM_ElementSetting
{
  Win32_PageFileUsage   REF Element;
  Win32_PageFileSetting REF Setting;
};
```

## <a name="members"></a><span data-ttu-id="02d6a-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="02d6a-108">Members</span></span>

<span data-ttu-id="02d6a-109">La **clase \_ PageFileElementSetting de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="02d6a-109">The **Win32\_PageFileElementSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="02d6a-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="02d6a-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="02d6a-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="02d6a-111">Properties</span></span>

<span data-ttu-id="02d6a-112">La **clase \_ PageFileElementSetting de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="02d6a-112">The **Win32\_PageFileElementSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="02d6a-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="02d6a-113">**Element**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="02d6a-114">Tipo de datos: **Win32 \_ PageFileUsage**</span><span class="sxs-lookup"><span data-stu-id="02d6a-114">Data type: **Win32\_PageFileUsage**</span></span>
</dt> <dt>

<span data-ttu-id="02d6a-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="02d6a-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="02d6a-116">Calificadores: [**clave**](../wmisdk/key-qualifier.md), [**invalidación**](../wmisdk/standard-qualifiers.md) ("Element"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ PageFileUsage")</span><span class="sxs-lookup"><span data-stu-id="02d6a-116">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Element"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_PageFileUsage")</span></span>
</dt> </dl>

<span data-ttu-id="02d6a-117">Referencia a la instancia de que representa las propiedades de un archivo de paginación mientras el sistema Win32 está en uso.</span><span class="sxs-lookup"><span data-stu-id="02d6a-117">Reference to the instance representing the properties of a page file while the Win32 system is in use.</span></span>

</dd> <dt>

<span data-ttu-id="02d6a-118">**Configuración**</span><span class="sxs-lookup"><span data-stu-id="02d6a-118">**Setting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="02d6a-119">Tipo de datos: **Win32 \_ PageFileSetting**</span><span class="sxs-lookup"><span data-stu-id="02d6a-119">Data type: **Win32\_PageFileSetting**</span></span>
</dt> <dt>

<span data-ttu-id="02d6a-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="02d6a-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="02d6a-121">Calificadores: [**clave**](../wmisdk/key-qualifier.md), [**invalidación**](../wmisdk/standard-qualifiers.md) ("configuración"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ PageFileSetting")</span><span class="sxs-lookup"><span data-stu-id="02d6a-121">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Setting"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_PageFileSetting")</span></span>
</dt> </dl>

<span data-ttu-id="02d6a-122">Referencia a la instancia de que representa la configuración inicial de un archivo de paginación cuando se está iniciando el sistema Win32.</span><span class="sxs-lookup"><span data-stu-id="02d6a-122">Reference to the instance representing the initial settings of a page file when the Win32 system is starting up.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="02d6a-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="02d6a-123">Remarks</span></span>

<span data-ttu-id="02d6a-124">La **clase \_ PageFileElementSetting de Win32** se deriva de [**\_ ElementSetting de CIM**](cim-elementsetting.md).</span><span class="sxs-lookup"><span data-stu-id="02d6a-124">The **Win32\_PageFileElementSetting** class is derived from [**CIM\_ElementSetting**](cim-elementsetting.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="02d6a-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="02d6a-125">Requirements</span></span>



| <span data-ttu-id="02d6a-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="02d6a-126">Requirement</span></span> | <span data-ttu-id="02d6a-127">Value</span><span class="sxs-lookup"><span data-stu-id="02d6a-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="02d6a-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="02d6a-128">Minimum supported client</span></span><br/> | <span data-ttu-id="02d6a-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="02d6a-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="02d6a-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="02d6a-130">Minimum supported server</span></span><br/> | <span data-ttu-id="02d6a-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="02d6a-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="02d6a-132">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="02d6a-132">Namespace</span></span><br/>                | <span data-ttu-id="02d6a-133">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="02d6a-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="02d6a-134">MOF</span><span class="sxs-lookup"><span data-stu-id="02d6a-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="02d6a-135"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="02d6a-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="02d6a-136">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="02d6a-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="02d6a-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="02d6a-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="02d6a-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="02d6a-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02d6a-139">**\_ELEMENTSETTING CIM**</span><span class="sxs-lookup"><span data-stu-id="02d6a-139">**CIM\_ElementSetting**</span></span>](cim-elementsetting.md)
</dt> <dt>

[<span data-ttu-id="02d6a-140">Clases de sistema operativo</span><span class="sxs-lookup"><span data-stu-id="02d6a-140">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
