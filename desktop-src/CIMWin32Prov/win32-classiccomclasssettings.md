---
description: La \_ clase WMI ClassicCOMClassSettings Association de Win32 relaciona una clase de modelo de objetos componentes (com) y la configuración utilizada para configurar las instancias de la clase com.
ms.assetid: 50f253cc-b8ae-41ac-b01f-ea816f5ca3d4
ms.tgt_platform: multiple
title: Win32_ClassicCOMClassSettings (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ClassicCOMClassSettings
- Win32_ClassicCOMClassSettings.Setting
- Win32_ClassicCOMClassSettings.Element
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: fb9c190157742aeca7c1ba6008a784005d054ca6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907015"
---
# <a name="win32_classiccomclasssettings-class"></a><span data-ttu-id="95579-103">\_Clase Win32 ClassicCOMClassSettings</span><span class="sxs-lookup"><span data-stu-id="95579-103">Win32\_ClassicCOMClassSettings class</span></span>

<span data-ttu-id="95579-104">La [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ ClassicCOMClassSettings** Association de Win32 relaciona una clase de modelo de objetos componentes (com) y la configuración utilizada para configurar las instancias de la clase com.</span><span class="sxs-lookup"><span data-stu-id="95579-104">The **Win32\_ClassicCOMClassSettings** association [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) relates a Component Object Model (COM) class and the settings used to configure instances of the COM class.</span></span>

<span data-ttu-id="95579-105">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="95579-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="95579-106">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="95579-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="95579-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="95579-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{E5D8A564-F6C0-11d2-B35E-00105A1F8569}"), AMENDMENT]
class Win32_ClassicCOMClassSettings : CIM_ElementSetting
{
  Win32_ClassicCOMClassSetting REF Setting;
  Win32_ClassicCOMClass        REF Element;
};
```

## <a name="members"></a><span data-ttu-id="95579-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="95579-108">Members</span></span>

<span data-ttu-id="95579-109">La **clase \_ ClassicCOMClassSettings de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="95579-109">The **Win32\_ClassicCOMClassSettings** class has these types of members:</span></span>

-   [<span data-ttu-id="95579-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="95579-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="95579-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="95579-111">Properties</span></span>

<span data-ttu-id="95579-112">La **clase \_ ClassicCOMClassSettings de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="95579-112">The **Win32\_ClassicCOMClassSettings** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="95579-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="95579-113">**Element**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95579-114">Tipo de datos: **Win32 \_ ClassicCOMClass**</span><span class="sxs-lookup"><span data-stu-id="95579-114">Data type: **Win32\_ClassicCOMClass**</span></span>
</dt> <dt>

<span data-ttu-id="95579-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="95579-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="95579-116">Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("Element"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ ClassicCOMClass")</span><span class="sxs-lookup"><span data-stu-id="95579-116">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Element"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_ClassicCOMClass")</span></span>
</dt> </dl>

<span data-ttu-id="95579-117">[**\_ ClassicCOMClass de Win32**](win32-classiccomclass.md) que representa la clase com donde se aplica la configuración.</span><span class="sxs-lookup"><span data-stu-id="95579-117">A [**Win32\_ClassicCOMClass**](win32-classiccomclass.md) that represents the COM class where the settings are applied.</span></span>

</dd> <dt>

<span data-ttu-id="95579-118">**Configuración**</span><span class="sxs-lookup"><span data-stu-id="95579-118">**Setting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="95579-119">Tipo de datos: **Win32 \_ ClassicCOMClassSetting**</span><span class="sxs-lookup"><span data-stu-id="95579-119">Data type: **Win32\_ClassicCOMClassSetting**</span></span>
</dt> <dt>

<span data-ttu-id="95579-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="95579-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="95579-121">Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("configuración"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ ClassicCOMClassSetting")</span><span class="sxs-lookup"><span data-stu-id="95579-121">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Setting"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_ClassicCOMClassSetting")</span></span>
</dt> </dl>

<span data-ttu-id="95579-122">[**\_ ClassicCOMClassSetting de Win32**](win32-classiccomclasssetting.md) que representa los valores de configuración asociados a la clase com.</span><span class="sxs-lookup"><span data-stu-id="95579-122">A [**Win32\_ClassicCOMClassSetting**](win32-classiccomclasssetting.md) that represents configuration settings associated with the COM class.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="95579-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="95579-123">Remarks</span></span>

<span data-ttu-id="95579-124">La **clase \_ ClassicCOMClassSettings de Win32** se deriva de [**\_ ElementSetting de CIM**](cim-elementsetting.md).</span><span class="sxs-lookup"><span data-stu-id="95579-124">The **Win32\_ClassicCOMClassSettings** class is derived from [**CIM\_ElementSetting**](cim-elementsetting.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="95579-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="95579-125">Requirements</span></span>



| <span data-ttu-id="95579-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="95579-126">Requirement</span></span> | <span data-ttu-id="95579-127">Value</span><span class="sxs-lookup"><span data-stu-id="95579-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="95579-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="95579-128">Minimum supported client</span></span><br/> | <span data-ttu-id="95579-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="95579-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="95579-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="95579-130">Minimum supported server</span></span><br/> | <span data-ttu-id="95579-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="95579-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="95579-132">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="95579-132">Namespace</span></span><br/>                | <span data-ttu-id="95579-133">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="95579-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="95579-134">MOF</span><span class="sxs-lookup"><span data-stu-id="95579-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="95579-135"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="95579-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="95579-136">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="95579-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="95579-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="95579-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="95579-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="95579-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95579-139">**\_ELEMENTSETTING CIM**</span><span class="sxs-lookup"><span data-stu-id="95579-139">**CIM\_ElementSetting**</span></span>](cim-elementsetting.md)
</dt> <dt>

<span data-ttu-id="95579-140">[Clases de sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="95579-140">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

