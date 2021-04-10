---
description: La \_ clase abstracta WMI DeviceSettings de Win32 relaciona un dispositivo lógico y un valor de configuración que se puede aplicar a él.
ms.assetid: 4f6c4c26-8da9-4e2c-8b8c-cec658ac08d4
ms.tgt_platform: multiple
title: Win32_DeviceSettings (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_DeviceSettings
- Win32_DeviceSettings.Setting
- Win32_DeviceSettings.Element
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1cd9cae29cfa608c9f3c0c36ebfe3ca7f903c809
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275053"
---
# <a name="win32_devicesettings-class"></a><span data-ttu-id="9fedc-103">\_Clase Win32 DeviceSettings</span><span class="sxs-lookup"><span data-stu-id="9fedc-103">Win32\_DeviceSettings class</span></span>

<span data-ttu-id="9fedc-104">La [clase abstracta WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ DeviceSettings de Win32** relaciona un dispositivo lógico y un valor de configuración que se puede aplicar a él.</span><span class="sxs-lookup"><span data-stu-id="9fedc-104">The **Win32\_DeviceSettings** abstract, association [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) relates a logical device and a setting that can be applied to it.</span></span>

<span data-ttu-id="9fedc-105">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="9fedc-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="9fedc-106">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="9fedc-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="9fedc-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9fedc-107">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C4FD-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_DeviceSettings : CIM_ElementSetting
{
  CIM_Setting       REF Setting;
  CIM_LogicalDevice REF Element;
};
```

## <a name="members"></a><span data-ttu-id="9fedc-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="9fedc-108">Members</span></span>

<span data-ttu-id="9fedc-109">La **clase \_ DeviceSettings de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="9fedc-109">The **Win32\_DeviceSettings** class has these types of members:</span></span>

-   [<span data-ttu-id="9fedc-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="9fedc-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9fedc-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="9fedc-111">Properties</span></span>

<span data-ttu-id="9fedc-112">La **clase \_ DeviceSettings de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="9fedc-112">The **Win32\_DeviceSettings** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9fedc-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="9fedc-113">**Element**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9fedc-114">Tipo de datos **: \_ LogicalDevice de CIM**</span><span class="sxs-lookup"><span data-stu-id="9fedc-114">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="9fedc-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9fedc-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9fedc-116">Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("elemento"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| lógico CIM CIM \_ ")</span><span class="sxs-lookup"><span data-stu-id="9fedc-116">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Element"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\|CIM\_LogicalDevice")</span></span>
</dt> </dl>

<span data-ttu-id="9fedc-117">Un [**\_ LogicalDevice de CIM**](cim-logicaldevice.md) que representa las propiedades del dispositivo lógico en el que se puede aplicar la configuración.</span><span class="sxs-lookup"><span data-stu-id="9fedc-117">A [**CIM\_LogicalDevice**](cim-logicaldevice.md) that represents properties of the logical device on which the settings can be applied.</span></span>

</dd> <dt>

<span data-ttu-id="9fedc-118">**Configuración**</span><span class="sxs-lookup"><span data-stu-id="9fedc-118">**Setting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9fedc-119">Tipo de datos **: \_ configuración de CIM**</span><span class="sxs-lookup"><span data-stu-id="9fedc-119">Data type: **CIM\_Setting**</span></span>
</dt> <dt>

<span data-ttu-id="9fedc-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9fedc-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9fedc-121">Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("configuración"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| configuración CIM CIM \_ ")</span><span class="sxs-lookup"><span data-stu-id="9fedc-121">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Setting"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\|CIM\_Setting")</span></span>
</dt> </dl>

<span data-ttu-id="9fedc-122">[**\_ Configuración de CIM**](cim-setting.md) que representa la configuración que se puede aplicar al dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="9fedc-122">A [**CIM\_Setting**](cim-setting.md) that represents settings that can be applied to the logical device.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9fedc-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9fedc-123">Remarks</span></span>

<span data-ttu-id="9fedc-124">La **clase \_ DeviceSettings de Win32** se deriva de [**\_ ElementSetting de CIM**](cim-elementsetting.md).</span><span class="sxs-lookup"><span data-stu-id="9fedc-124">The **Win32\_DeviceSettings** class is derived from [**CIM\_ElementSetting**](cim-elementsetting.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9fedc-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9fedc-125">Requirements</span></span>



| <span data-ttu-id="9fedc-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="9fedc-126">Requirement</span></span> | <span data-ttu-id="9fedc-127">Value</span><span class="sxs-lookup"><span data-stu-id="9fedc-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9fedc-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9fedc-128">Minimum supported client</span></span><br/> | <span data-ttu-id="9fedc-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9fedc-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="9fedc-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9fedc-130">Minimum supported server</span></span><br/> | <span data-ttu-id="9fedc-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9fedc-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="9fedc-132">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="9fedc-132">Namespace</span></span><br/>                | <span data-ttu-id="9fedc-133">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="9fedc-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="9fedc-134">MOF</span><span class="sxs-lookup"><span data-stu-id="9fedc-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9fedc-135"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9fedc-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="9fedc-136">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="9fedc-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9fedc-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9fedc-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9fedc-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="9fedc-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9fedc-139">**\_ELEMENTSETTING CIM**</span><span class="sxs-lookup"><span data-stu-id="9fedc-139">**CIM\_ElementSetting**</span></span>](cim-elementsetting.md)
</dt> <dt>

[<span data-ttu-id="9fedc-140">Clases de hardware de sistema del equipo</span><span class="sxs-lookup"><span data-stu-id="9fedc-140">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

