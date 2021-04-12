---
description: La \_ clase WMI PrinterSetting Association de Win32 relaciona una impresora y sus valores de configuración.
ms.assetid: 5d0f0724-0583-449b-a6da-336e7c8e526e
ms.tgt_platform: multiple
title: Win32_PrinterSetting (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PrinterSetting
- Win32_PrinterSetting.Setting
- Win32_PrinterSetting.Element
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 90a77678e61b755550ebb1818c34ccdc3159a88c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104274966"
---
# <a name="win32_printersetting-class"></a><span data-ttu-id="d6baa-103">\_Clase Win32 PrinterSetting</span><span class="sxs-lookup"><span data-stu-id="d6baa-103">Win32\_PrinterSetting class</span></span>

<span data-ttu-id="d6baa-104">La [clase WMI](../wmisdk/retrieving-a-class.md) **\_ PrinterSetting** Association de Win32 relaciona una impresora y sus valores de configuración.</span><span class="sxs-lookup"><span data-stu-id="d6baa-104">The **Win32\_PrinterSetting** association [WMI class](../wmisdk/retrieving-a-class.md) relates a printer and its configuration settings.</span></span>

<span data-ttu-id="d6baa-105">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="d6baa-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="d6baa-106">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="d6baa-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="d6baa-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d6baa-107">Syntax</span></span>

``` syntax
class Win32_PrinterSetting : Win32_DeviceSettings
{
  CIM_Setting       REF Setting;
  CIM_LogicalDevice REF Element;
};
```

## <a name="members"></a><span data-ttu-id="d6baa-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="d6baa-108">Members</span></span>

<span data-ttu-id="d6baa-109">La **clase \_ PrinterSetting de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="d6baa-109">The **Win32\_PrinterSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="d6baa-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d6baa-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d6baa-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d6baa-111">Properties</span></span>

<span data-ttu-id="d6baa-112">La **clase \_ PrinterSetting de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="d6baa-112">The **Win32\_PrinterSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d6baa-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="d6baa-113">**Element**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d6baa-114">Tipo de datos **: \_ LogicalDevice de CIM**</span><span class="sxs-lookup"><span data-stu-id="d6baa-114">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="d6baa-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d6baa-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d6baa-116">Calificadores: [**key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("CIM \| CIM \_ LogicalDevice")</span><span class="sxs-lookup"><span data-stu-id="d6baa-116">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("CIM\|CIM\_LogicalDevice")</span></span>
</dt> </dl>

<span data-ttu-id="d6baa-117">Un [**\_ LogicalDevice de CIM**](cim-logicaldevice.md) que representa las propiedades del dispositivo lógico en el que se puede aplicar la configuración.</span><span class="sxs-lookup"><span data-stu-id="d6baa-117">A [**CIM\_LogicalDevice**](cim-logicaldevice.md) that represents properties of the logical device on which the settings can be applied.</span></span>

<span data-ttu-id="d6baa-118">Esta propiedad se hereda de [**Win32 \_ DeviceSettings**](win32-devicesettings.md).</span><span class="sxs-lookup"><span data-stu-id="d6baa-118">This property is inherited from [**Win32\_DeviceSettings**](win32-devicesettings.md).</span></span>

</dd> <dt>

<span data-ttu-id="d6baa-119">**Configuración**</span><span class="sxs-lookup"><span data-stu-id="d6baa-119">**Setting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d6baa-120">Tipo de datos **: \_ configuración de CIM**</span><span class="sxs-lookup"><span data-stu-id="d6baa-120">Data type: **CIM\_Setting**</span></span>
</dt> <dt>

<span data-ttu-id="d6baa-121">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d6baa-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d6baa-122">Calificadores: [**key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| configuración CIM CIM \_ ")</span><span class="sxs-lookup"><span data-stu-id="d6baa-122">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("CIM\|CIM\_Setting")</span></span>
</dt> </dl>

<span data-ttu-id="d6baa-123">[**\_ Configuración de CIM**](cim-setting.md) que representa la configuración que se puede aplicar al dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="d6baa-123">A [**CIM\_Setting**](cim-setting.md) that represents settings that can be applied to the logical device.</span></span>

<span data-ttu-id="d6baa-124">Esta propiedad se hereda de [**Win32 \_ DeviceSettings**](win32-devicesettings.md).</span><span class="sxs-lookup"><span data-stu-id="d6baa-124">This property is inherited from [**Win32\_DeviceSettings**](win32-devicesettings.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d6baa-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d6baa-125">Remarks</span></span>

<span data-ttu-id="d6baa-126">La **clase \_ PrinterSetting de Win32** se deriva de [**\_ DeviceSettings de Win32**](win32-devicesettings.md).</span><span class="sxs-lookup"><span data-stu-id="d6baa-126">The **Win32\_PrinterSetting** class is derived from [**Win32\_DeviceSettings**](win32-devicesettings.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d6baa-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d6baa-127">Requirements</span></span>



| <span data-ttu-id="d6baa-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="d6baa-128">Requirement</span></span> | <span data-ttu-id="d6baa-129">Value</span><span class="sxs-lookup"><span data-stu-id="d6baa-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="d6baa-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d6baa-130">Minimum supported client</span></span><br/> | <span data-ttu-id="d6baa-131">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d6baa-131">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="d6baa-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d6baa-132">Minimum supported server</span></span><br/> | <span data-ttu-id="d6baa-133">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d6baa-133">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="d6baa-134">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="d6baa-134">Namespace</span></span><br/>                | <span data-ttu-id="d6baa-135">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="d6baa-135">Root\\CIMV2</span></span><br/>                                                                        |
| <span data-ttu-id="d6baa-136">MOF</span><span class="sxs-lookup"><span data-stu-id="d6baa-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d6baa-137"><dt>Win32 \_ printer. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d6baa-137"><dt>Win32\_Printer.mof</dt></span></span> </dl> |
| <span data-ttu-id="d6baa-138">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d6baa-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d6baa-139"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d6baa-139"><dt>CIMWin32.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="d6baa-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="d6baa-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d6baa-141">**Win32 \_ DeviceSettings**</span><span class="sxs-lookup"><span data-stu-id="d6baa-141">**Win32\_DeviceSettings**</span></span>](win32-devicesettings.md)
</dt> <dt>

[<span data-ttu-id="d6baa-142">Clases de hardware de sistema del equipo</span><span class="sxs-lookup"><span data-stu-id="d6baa-142">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
