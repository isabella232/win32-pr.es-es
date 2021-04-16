---
description: La \_ clase WMI de la Asociación Win32 Videosettings relaciona una configuración de vídeo y un controlador de vídeo que se puede aplicar a ella.
ms.assetid: 0cc42352-0a89-434d-a8b6-230c677de49c
ms.tgt_platform: multiple
title: Win32_VideoSettings (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_VideoSettings
- Win32_VideoSettings.Setting
- Win32_VideoSettings.Element
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 38e949b6b6501dc51b39448d72e6bf61f37fbecb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659430"
---
# <a name="win32_videosettings-class"></a><span data-ttu-id="ddc74-103">\_Clase Win32 Videosettings</span><span class="sxs-lookup"><span data-stu-id="ddc74-103">Win32\_VideoSettings class</span></span>

<span data-ttu-id="ddc74-104">La [clase WMI](../wmisdk/retrieving-a-class.md) de la Asociación **Win32 \_ videosettings** relaciona una configuración de vídeo y un controlador de vídeo que se puede aplicar a ella.</span><span class="sxs-lookup"><span data-stu-id="ddc74-104">The **Win32\_VideoSettings** association [WMI class](../wmisdk/retrieving-a-class.md) relates a video controller and video settings that can be applied to it.</span></span>

<span data-ttu-id="ddc74-105">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="ddc74-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="ddc74-106">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="ddc74-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="ddc74-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ddc74-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{1008CCEE-7BFF-11D2-AAD2-006008C78BC7}"), AMENDMENT]
class Win32_VideoSettings : CIM_VideoSetting
{
  CIM_VideoControllerResolution REF Setting;
  Win32_VideoController         REF Element;
};
```

## <a name="members"></a><span data-ttu-id="ddc74-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="ddc74-108">Members</span></span>

<span data-ttu-id="ddc74-109">La clase **Win32 \_ videosettings** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="ddc74-109">The **Win32\_VideoSettings** class has these types of members:</span></span>

-   [<span data-ttu-id="ddc74-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ddc74-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ddc74-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ddc74-111">Properties</span></span>

<span data-ttu-id="ddc74-112">La clase **Win32 \_ videosettings** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="ddc74-112">The **Win32\_VideoSettings** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ddc74-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="ddc74-113">**Element**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddc74-114">Tipo de datos **: \_ videocontroladora Win32**</span><span class="sxs-lookup"><span data-stu-id="ddc74-114">Data type: **Win32\_VideoController**</span></span>
</dt> <dt>

<span data-ttu-id="ddc74-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ddc74-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ddc74-116">Calificadores: [**clave**](../wmisdk/key-qualifier.md), [**invalidación**](../wmisdk/standard-qualifiers.md) ("Element"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ videocontroller")</span><span class="sxs-lookup"><span data-stu-id="ddc74-116">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Element"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI\|Win32\_VideoController")</span></span>
</dt> </dl>

<span data-ttu-id="ddc74-117">Un [**\_ videocontrolador de Win32**](win32-videocontroller.md) que contiene las propiedades del controlador de vídeo en el que se puede usar una configuración de vídeo.</span><span class="sxs-lookup"><span data-stu-id="ddc74-117">A [**Win32\_VideoController**](win32-videocontroller.md) containing the properties of the video controller that a video setting can be used on.</span></span>

</dd> <dt>

<span data-ttu-id="ddc74-118">**Configuración**</span><span class="sxs-lookup"><span data-stu-id="ddc74-118">**Setting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ddc74-119">Tipo de datos: **CIM \_ VideoControllerResolution**</span><span class="sxs-lookup"><span data-stu-id="ddc74-119">Data type: **CIM\_VideoControllerResolution**</span></span>
</dt> <dt>

<span data-ttu-id="ddc74-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ddc74-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ddc74-121">Calificadores: [**clave**](../wmisdk/key-qualifier.md), [**invalidación**](../wmisdk/standard-qualifiers.md) ("configuración"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("CIM \| CIM \_ VideoControllerResolution")</span><span class="sxs-lookup"><span data-stu-id="ddc74-121">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Setting"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("CIM\|CIM\_VideoControllerResolution")</span></span>
</dt> </dl>

<span data-ttu-id="ddc74-122">[**\_ VideoControllerResolution CIM**](cim-videocontrollerresolution.md) que contiene la configuración que se puede aplicar al controlador de vídeo.</span><span class="sxs-lookup"><span data-stu-id="ddc74-122">A [**CIM\_VideoControllerResolution**](cim-videocontrollerresolution.md) containing settings that can be applied to the video controller.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ddc74-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ddc74-123">Remarks</span></span>

<span data-ttu-id="ddc74-124">La clase **Win32 \_ videosettings** se deriva de [**la \_ configuración**](cim-videosetting.md)de videoconfiguración de CIM.</span><span class="sxs-lookup"><span data-stu-id="ddc74-124">The **Win32\_VideoSettings** class is derived from [**CIM\_VideoSetting**](cim-videosetting.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ddc74-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ddc74-125">Requirements</span></span>



| <span data-ttu-id="ddc74-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="ddc74-126">Requirement</span></span> | <span data-ttu-id="ddc74-127">Value</span><span class="sxs-lookup"><span data-stu-id="ddc74-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ddc74-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ddc74-128">Minimum supported client</span></span><br/> | <span data-ttu-id="ddc74-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ddc74-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ddc74-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ddc74-130">Minimum supported server</span></span><br/> | <span data-ttu-id="ddc74-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ddc74-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ddc74-132">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="ddc74-132">Namespace</span></span><br/>                | <span data-ttu-id="ddc74-133">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="ddc74-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="ddc74-134">MOF</span><span class="sxs-lookup"><span data-stu-id="ddc74-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ddc74-135"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ddc74-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="ddc74-136">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="ddc74-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ddc74-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ddc74-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ddc74-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="ddc74-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ddc74-139">**Videoconfiguración de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="ddc74-139">**CIM\_VideoSetting**</span></span>](cim-videosetting.md)
</dt> <dt>

[<span data-ttu-id="ddc74-140">Clases de hardware de sistema del equipo</span><span class="sxs-lookup"><span data-stu-id="ddc74-140">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
