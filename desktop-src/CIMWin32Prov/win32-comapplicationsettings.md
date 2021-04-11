---
description: La \_ clase WMI COMApplicationSettings Association de Win32 relaciona una aplicación DCOM y sus valores de configuración.
ms.assetid: b08eaff1-b42a-42f3-abf7-3664b6195acd
ms.tgt_platform: multiple
title: Win32_COMApplicationSettings (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_COMApplicationSettings
- Win32_COMApplicationSettings.Setting
- Win32_COMApplicationSettings.Element
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 8f2fd5953d770d541e704b7dc7fe8580e98b3066
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104274859"
---
# <a name="win32_comapplicationsettings-class"></a><span data-ttu-id="3d2b0-103">\_Clase Win32 COMApplicationSettings</span><span class="sxs-lookup"><span data-stu-id="3d2b0-103">Win32\_COMApplicationSettings class</span></span>

<span data-ttu-id="3d2b0-104">La [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ COMApplicationSettings** Association de Win32 relaciona una aplicación DCOM y sus valores de configuración.</span><span class="sxs-lookup"><span data-stu-id="3d2b0-104">The **Win32\_COMApplicationSettings** association [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) relates a DCOM application and its configuration settings.</span></span>

<span data-ttu-id="3d2b0-105">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="3d2b0-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="3d2b0-106">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="3d2b0-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="3d2b0-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3d2b0-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{E5D8A563-F6C0-11d2-B35E-00105A1F8569}"), AMENDMENT]
class Win32_COMApplicationSettings : CIM_ElementSetting
{
  Win32_DCOMApplicationSetting REF Setting;
  Win32_DCOMApplication        REF Element;
};
```

## <a name="members"></a><span data-ttu-id="3d2b0-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="3d2b0-108">Members</span></span>

<span data-ttu-id="3d2b0-109">La **clase \_ COMApplicationSettings de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="3d2b0-109">The **Win32\_COMApplicationSettings** class has these types of members:</span></span>

-   [<span data-ttu-id="3d2b0-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="3d2b0-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3d2b0-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="3d2b0-111">Properties</span></span>

<span data-ttu-id="3d2b0-112">La **clase \_ COMApplicationSettings de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="3d2b0-112">The **Win32\_COMApplicationSettings** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3d2b0-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="3d2b0-113">**Element**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3d2b0-114">Tipo de datos: **Win32 \_ DCOMApplication**</span><span class="sxs-lookup"><span data-stu-id="3d2b0-114">Data type: **Win32\_DCOMApplication**</span></span>
</dt> <dt>

<span data-ttu-id="3d2b0-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3d2b0-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3d2b0-116">Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("Element"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ DCOMApplication")</span><span class="sxs-lookup"><span data-stu-id="3d2b0-116">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Element"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_DCOMApplication")</span></span>
</dt> </dl>

<span data-ttu-id="3d2b0-117">[**\_ DCOMApplication de Win32**](win32-dcomapplication.md) que representa la aplicación DCOM en la que se aplica la configuración.</span><span class="sxs-lookup"><span data-stu-id="3d2b0-117">A [**Win32\_DCOMApplication**](win32-dcomapplication.md) that represents the DCOM application where the settings are applied.</span></span>

</dd> <dt>

<span data-ttu-id="3d2b0-118">**Configuración**</span><span class="sxs-lookup"><span data-stu-id="3d2b0-118">**Setting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3d2b0-119">Tipo de datos: **Win32 \_ DCOMApplicationSetting**</span><span class="sxs-lookup"><span data-stu-id="3d2b0-119">Data type: **Win32\_DCOMApplicationSetting**</span></span>
</dt> <dt>

<span data-ttu-id="3d2b0-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3d2b0-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3d2b0-121">Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("configuración"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ DCOMApplicationSetting")</span><span class="sxs-lookup"><span data-stu-id="3d2b0-121">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Setting"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_DCOMApplicationSetting")</span></span>
</dt> </dl>

<span data-ttu-id="3d2b0-122">[**\_ DCOMApplicationSetting de Win32**](win32-dcomapplicationsetting.md) que representa los valores de configuración asociados a la aplicación DCOM.</span><span class="sxs-lookup"><span data-stu-id="3d2b0-122">A [**Win32\_DCOMApplicationSetting**](win32-dcomapplicationsetting.md) that represents the configuration settings associated with the DCOM application.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3d2b0-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3d2b0-123">Remarks</span></span>

<span data-ttu-id="3d2b0-124">La **clase \_ COMApplicationSettings de Win32** se deriva de [**\_ ElementSetting de CIM**](cim-elementsetting.md).</span><span class="sxs-lookup"><span data-stu-id="3d2b0-124">The **Win32\_COMApplicationSettings** class is derived from [**CIM\_ElementSetting**](cim-elementsetting.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3d2b0-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3d2b0-125">Requirements</span></span>



| <span data-ttu-id="3d2b0-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="3d2b0-126">Requirement</span></span> | <span data-ttu-id="3d2b0-127">Value</span><span class="sxs-lookup"><span data-stu-id="3d2b0-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3d2b0-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3d2b0-128">Minimum supported client</span></span><br/> | <span data-ttu-id="3d2b0-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3d2b0-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="3d2b0-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3d2b0-130">Minimum supported server</span></span><br/> | <span data-ttu-id="3d2b0-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3d2b0-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="3d2b0-132">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="3d2b0-132">Namespace</span></span><br/>                | <span data-ttu-id="3d2b0-133">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="3d2b0-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="3d2b0-134">MOF</span><span class="sxs-lookup"><span data-stu-id="3d2b0-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3d2b0-135"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3d2b0-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="3d2b0-136">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="3d2b0-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3d2b0-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3d2b0-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3d2b0-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="3d2b0-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3d2b0-139">**\_ELEMENTSETTING CIM**</span><span class="sxs-lookup"><span data-stu-id="3d2b0-139">**CIM\_ElementSetting**</span></span>](cim-elementsetting.md)
</dt> <dt>

<span data-ttu-id="3d2b0-140">[Clases de sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="3d2b0-140">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

