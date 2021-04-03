---
description: La \_ clase WMI SerialPortSetting Association de Win32 relaciona un puerto serie y sus valores de configuración.
ms.assetid: 57856207-abe5-4d93-9a34-acfe30ccd80c
ms.tgt_platform: multiple
title: Win32_SerialPortSetting (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SerialPortSetting
- Win32_SerialPortSetting.Setting
- Win32_SerialPortSetting.Element
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 713cdb57b5ed7135529959d3c17f7453924ce1dc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103998123"
---
# <a name="win32_serialportsetting-class"></a><span data-ttu-id="dca2b-103">\_Clase Win32 SerialPortSetting</span><span class="sxs-lookup"><span data-stu-id="dca2b-103">Win32\_SerialPortSetting class</span></span>

<span data-ttu-id="dca2b-104">La [clase WMI](../wmisdk/retrieving-a-class.md) **\_ SerialPortSetting** Association de Win32 relaciona un puerto serie y sus valores de configuración.</span><span class="sxs-lookup"><span data-stu-id="dca2b-104">The **Win32\_SerialPortSetting** association [WMI class](../wmisdk/retrieving-a-class.md) relates a serial port and its configuration settings.</span></span>

<span data-ttu-id="dca2b-105">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="dca2b-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="dca2b-106">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="dca2b-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="dca2b-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="dca2b-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4FE-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SerialPortSetting : Win32_DeviceSettings
{
  Win32_SerialPortConfiguration REF Setting;
  Win32_SerialPort              REF Element;
};
```

## <a name="members"></a><span data-ttu-id="dca2b-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="dca2b-108">Members</span></span>

<span data-ttu-id="dca2b-109">La **clase \_ SerialPortSetting de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="dca2b-109">The **Win32\_SerialPortSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="dca2b-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="dca2b-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="dca2b-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="dca2b-111">Properties</span></span>

<span data-ttu-id="dca2b-112">La **clase \_ SerialPortSetting de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="dca2b-112">The **Win32\_SerialPortSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="dca2b-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="dca2b-113">**Element**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dca2b-114">Tipo de datos: de **Win32 \_ SerialPort**</span><span class="sxs-lookup"><span data-stu-id="dca2b-114">Data type: **Win32\_SerialPort**</span></span>
</dt> <dt>

<span data-ttu-id="dca2b-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="dca2b-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dca2b-116">Calificadores: [**override**](../wmisdk/standard-qualifiers.md) ("Element"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ SerialPort")</span><span class="sxs-lookup"><span data-stu-id="dca2b-116">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("Element"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_SerialPort")</span></span>
</dt> </dl>

<span data-ttu-id="dca2b-117">Un [**\_ SerialPort de Win32**](win32-serialport.md) que contiene las propiedades de un puerto serie en el sistema del equipo.</span><span class="sxs-lookup"><span data-stu-id="dca2b-117">A [**Win32\_SerialPort**](win32-serialport.md) that contains the properties of a serial port on the computer system.</span></span>

</dd> <dt>

<span data-ttu-id="dca2b-118">**Configuración**</span><span class="sxs-lookup"><span data-stu-id="dca2b-118">**Setting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dca2b-119">Tipo de datos: **Win32 \_ SerialPortConfiguration**</span><span class="sxs-lookup"><span data-stu-id="dca2b-119">Data type: **Win32\_SerialPortConfiguration**</span></span>
</dt> <dt>

<span data-ttu-id="dca2b-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="dca2b-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dca2b-121">Calificadores: [**override**](../wmisdk/standard-qualifiers.md) ("Setting"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ SerialPortConfiguration")</span><span class="sxs-lookup"><span data-stu-id="dca2b-121">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("Setting"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_SerialPortConfiguration")</span></span>
</dt> </dl>

<span data-ttu-id="dca2b-122">[**\_ SerialPortConfiguration de Win32**](win32-serialportconfiguration.md) que contiene el valor de configuración para el puerto serie.</span><span class="sxs-lookup"><span data-stu-id="dca2b-122">A [**Win32\_SerialPortConfiguration**](win32-serialportconfiguration.md) that contains the configuration setting for the serial port.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="dca2b-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="dca2b-123">Remarks</span></span>

<span data-ttu-id="dca2b-124">La **clase \_ SerialPortSetting de Win32** se deriva de [**\_ DeviceSettings de Win32**](win32-devicesettings.md).</span><span class="sxs-lookup"><span data-stu-id="dca2b-124">The **Win32\_SerialPortSetting** class is derived from [**Win32\_DeviceSettings**](win32-devicesettings.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="dca2b-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dca2b-125">Requirements</span></span>



| <span data-ttu-id="dca2b-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="dca2b-126">Requirement</span></span> | <span data-ttu-id="dca2b-127">Value</span><span class="sxs-lookup"><span data-stu-id="dca2b-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="dca2b-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dca2b-128">Minimum supported client</span></span><br/> | <span data-ttu-id="dca2b-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="dca2b-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="dca2b-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dca2b-130">Minimum supported server</span></span><br/> | <span data-ttu-id="dca2b-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="dca2b-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="dca2b-132">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="dca2b-132">Namespace</span></span><br/>                | <span data-ttu-id="dca2b-133">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="dca2b-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="dca2b-134">MOF</span><span class="sxs-lookup"><span data-stu-id="dca2b-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="dca2b-135"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="dca2b-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="dca2b-136">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="dca2b-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dca2b-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dca2b-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dca2b-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="dca2b-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dca2b-139">**Win32 \_ DeviceSettings**</span><span class="sxs-lookup"><span data-stu-id="dca2b-139">**Win32\_DeviceSettings**</span></span>](win32-devicesettings.md)
</dt> <dt>

[<span data-ttu-id="dca2b-140">Clases de hardware de sistema del equipo</span><span class="sxs-lookup"><span data-stu-id="dca2b-140">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
