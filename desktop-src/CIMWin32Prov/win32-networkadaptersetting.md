---
description: La \_ clase WMI NetworkAdapterSetting Association de Win32 relaciona un adaptador de red y sus valores de configuración.
ms.assetid: 6fc646c3-05f9-4c92-8598-07ea20fffaca
ms.tgt_platform: multiple
title: Win32_NetworkAdapterSetting (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterSetting
- Win32_NetworkAdapterSetting.Setting
- Win32_NetworkAdapterSetting.Element
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: c51ef9ed790c902a6a662dc3ebc45df97fa29721
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659705"
---
# <a name="win32_networkadaptersetting-class"></a><span data-ttu-id="acef5-103">\_Clase Win32 NetworkAdapterSetting</span><span class="sxs-lookup"><span data-stu-id="acef5-103">Win32\_NetworkAdapterSetting class</span></span>

<span data-ttu-id="acef5-104">La [clase WMI](../wmisdk/retrieving-a-class.md) **\_ NetworkAdapterSetting** Association de Win32 relaciona un adaptador de red y sus valores de configuración.</span><span class="sxs-lookup"><span data-stu-id="acef5-104">The **Win32\_NetworkAdapterSetting** association [WMI class](../wmisdk/retrieving-a-class.md) relates a network adapter and its configuration settings.</span></span>

<span data-ttu-id="acef5-105">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="acef5-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="acef5-106">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="acef5-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="acef5-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="acef5-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C50A-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_NetworkAdapterSetting : Win32_DeviceSettings
{
  Win32_NetworkAdapterConfiguration REF Setting;
  Win32_NetworkAdapter              REF Element;
};
```

## <a name="members"></a><span data-ttu-id="acef5-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="acef5-108">Members</span></span>

<span data-ttu-id="acef5-109">La **clase \_ NetworkAdapterSetting de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="acef5-109">The **Win32\_NetworkAdapterSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="acef5-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="acef5-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="acef5-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="acef5-111">Properties</span></span>

<span data-ttu-id="acef5-112">La **clase \_ NetworkAdapterSetting de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="acef5-112">The **Win32\_NetworkAdapterSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="acef5-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="acef5-113">**Element**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="acef5-114">Tipo de datos: **Win32 \_ adaptador** de datos</span><span class="sxs-lookup"><span data-stu-id="acef5-114">Data type: **Win32\_NetworkAdapter**</span></span>
</dt> <dt>

<span data-ttu-id="acef5-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="acef5-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="acef5-116">Calificadores: [**override**](../wmisdk/standard-qualifiers.md) ("Element"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ adaptador de la</span><span class="sxs-lookup"><span data-stu-id="acef5-116">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("Element"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_NetworkAdapter")</span></span>
</dt> </dl>

<span data-ttu-id="acef5-117">Un adaptador de red [**Win32 \_**](win32-networkadapter.md) que describe las propiedades del adaptador de red que usa una configuración de adaptador de red determinada.</span><span class="sxs-lookup"><span data-stu-id="acef5-117">A [**Win32\_NetworkAdapter**](win32-networkadapter.md) that describes the properties of the network adapter that is using a particular network adapter setting.</span></span>

</dd> <dt>

<span data-ttu-id="acef5-118">**Configuración**</span><span class="sxs-lookup"><span data-stu-id="acef5-118">**Setting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="acef5-119">Tipo de datos: **Win32 \_ NetworkAdapterConfiguration**</span><span class="sxs-lookup"><span data-stu-id="acef5-119">Data type: **Win32\_NetworkAdapterConfiguration**</span></span>
</dt> <dt>

<span data-ttu-id="acef5-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="acef5-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="acef5-121">Calificadores: [**override**](../wmisdk/standard-qualifiers.md) ("Setting"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ NetworkAdapterConfiguration")</span><span class="sxs-lookup"><span data-stu-id="acef5-121">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("Setting"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_NetworkAdapterConfiguration")</span></span>
</dt> </dl>

<span data-ttu-id="acef5-122">[**\_ NetworkAdapterConfiguration de Win32**](win32-networkadapterconfiguration.md) que describe los valores de configuración utilizados en el adaptador de red.</span><span class="sxs-lookup"><span data-stu-id="acef5-122">A [**Win32\_NetworkAdapterConfiguration**](win32-networkadapterconfiguration.md) that describes the configuration settings used on the network adapter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="acef5-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="acef5-123">Remarks</span></span>

<span data-ttu-id="acef5-124">La **clase \_ NetworkAdapterSetting de Win32** se deriva de [**\_ DeviceSettings de Win32**](win32-devicesettings.md).</span><span class="sxs-lookup"><span data-stu-id="acef5-124">The **Win32\_NetworkAdapterSetting** class is derived from [**Win32\_DeviceSettings**](win32-devicesettings.md).</span></span>

<span data-ttu-id="acef5-125">Para obtener información sobre cómo usar las clases de asociación, vea [ASSOCIATORS OF Statement](../wmisdk/associators-of-statement.md).</span><span class="sxs-lookup"><span data-stu-id="acef5-125">For information on how to use association classes, see [ASSOCIATORS OF Statement](../wmisdk/associators-of-statement.md).</span></span>

## <a name="examples"></a><span data-ttu-id="acef5-126">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="acef5-126">Examples</span></span>

<span data-ttu-id="acef5-127">En el siguiente ejemplo de VBScript se usa **Win32 \_ NetworkAdapterSetting** para identificar la dirección IP en la conexión de área local.</span><span class="sxs-lookup"><span data-stu-id="acef5-127">The following VBScript sample uses **Win32\_NetworkAdapterSetting** to identify the IP Address on the Local Area Connection.</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject( _
    "winmgmts:\\" & strComputer & "\root\cimv2")
Set colNics = objWMIService.ExecQuery _
    ("Select * From Win32_NetworkAdapter " _
        & "Where NetConnectionID = " & _
        "'Local Area Connection'")
 
For Each objNic in colNics
    Set colNicConfigs = objWMIService.ExecQuery _
      ("ASSOCIATORS OF " _
          & "{Win32_NetworkAdapter.DeviceID='" & _
      objNic.DeviceID & "'}" & _
      " WHERE AssocClass=Win32_NetworkAdapterSetting")
    For Each objNicConfig In colNicConfigs
        For Each strIPAddress in objNicConfig.IPAddress
            Wscript.Echo "IP Address: " &  strIPAddress
        Next
    Next
Next
```



## <a name="requirements"></a><span data-ttu-id="acef5-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="acef5-128">Requirements</span></span>



| <span data-ttu-id="acef5-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="acef5-129">Requirement</span></span> | <span data-ttu-id="acef5-130">Value</span><span class="sxs-lookup"><span data-stu-id="acef5-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="acef5-131">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="acef5-131">Minimum supported client</span></span><br/> | <span data-ttu-id="acef5-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="acef5-132">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="acef5-133">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="acef5-133">Minimum supported server</span></span><br/> | <span data-ttu-id="acef5-134">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="acef5-134">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="acef5-135">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="acef5-135">Namespace</span></span><br/>                | <span data-ttu-id="acef5-136">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="acef5-136">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="acef5-137">MOF</span><span class="sxs-lookup"><span data-stu-id="acef5-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="acef5-138"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="acef5-138"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="acef5-139">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="acef5-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="acef5-140"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="acef5-140"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="acef5-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="acef5-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="acef5-142">**Win32 \_ DeviceSettings**</span><span class="sxs-lookup"><span data-stu-id="acef5-142">**Win32\_DeviceSettings**</span></span>](win32-devicesettings.md)
</dt> <dt>

[<span data-ttu-id="acef5-143">Clases de hardware de sistema del equipo</span><span class="sxs-lookup"><span data-stu-id="acef5-143">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="acef5-144">Tareas de WMI: redes</span><span class="sxs-lookup"><span data-stu-id="acef5-144">WMI Tasks: Networking</span></span>](../wmisdk/wmi-tasks--networking.md)
</dt> </dl>

 

 
