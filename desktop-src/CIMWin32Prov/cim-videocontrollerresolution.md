---
description: La \_ clase CIM VideoControllerResolution representa los distintos modos de vídeo que puede admitir un controlador de vídeo.
ms.assetid: 954ac3fe-9777-460c-8929-853f19379256
ms.tgt_platform: multiple
title: CIM_VideoControllerResolution (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VideoControllerResolution
- CIM_VideoControllerResolution.Caption
- CIM_VideoControllerResolution.Description
- CIM_VideoControllerResolution.SettingID
- CIM_VideoControllerResolution.HorizontalResolution
- CIM_VideoControllerResolution.MaxRefreshRate
- CIM_VideoControllerResolution.MinRefreshRate
- CIM_VideoControllerResolution.NumberOfColors
- CIM_VideoControllerResolution.RefreshRate
- CIM_VideoControllerResolution.ScanMode
- CIM_VideoControllerResolution.VerticalResolution
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: d448d92d79163bc6a4e1056e88434081c5878159
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907507"
---
# <a name="cim_videocontrollerresolution-class"></a><span data-ttu-id="a875e-103">\_Clase VideoControllerResolution de CIM</span><span class="sxs-lookup"><span data-stu-id="a875e-103">CIM\_VideoControllerResolution class</span></span>

<span data-ttu-id="a875e-104">La clase **CIM \_ VideoControllerResolution** representa los distintos modos de vídeo que puede admitir un controlador de vídeo.</span><span class="sxs-lookup"><span data-stu-id="a875e-104">The **CIM\_VideoControllerResolution** class represents the various video modes that a video controller can support.</span></span> <span data-ttu-id="a875e-105">Los modos de vídeo se definen mediante las posibles resoluciones horizontales y verticales, la frecuencia de actualización, el modo de exploración y el número de valores de color admitidos por un controlador.</span><span class="sxs-lookup"><span data-stu-id="a875e-105">Video modes are defined by the possible horizontal and vertical resolutions, refresh rate, scan mode, and number of color settings supported by a controller.</span></span> <span data-ttu-id="a875e-106">Las soluciones en uso reales son los valores especificados en el objeto de [**\_ videocontroladora CIM**](cim-videocontroller.md) .</span><span class="sxs-lookup"><span data-stu-id="a875e-106">The actual resolutions in use are the values specified in the [**CIM\_VideoController**](cim-videocontroller.md) object.</span></span>

<span data-ttu-id="a875e-107">El hardware que no es compatible con Windows Display Driver Model (WDDM) devuelve valores de propiedad inexactos para las instancias de esta clase.</span><span class="sxs-lookup"><span data-stu-id="a875e-107">Hardware that is not compatible with Windows Display Driver Model (WDDM) returns inaccurate property values for instances of this class.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a875e-108">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="a875e-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="a875e-109">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="a875e-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="a875e-110">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="a875e-110">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="a875e-111">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="a875e-111">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="a875e-112">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a875e-112">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{1008CCEA-7BFF-11D2-AAD2-006008C78BC7}"), AMENDMENT]
class CIM_VideoControllerResolution : CIM_Setting
{
  string Caption;
  string Description;
  string SettingID;
  uint32 HorizontalResolution;
  uint32 MaxRefreshRate;
  uint32 MinRefreshRate;
  uint64 NumberOfColors;
  uint32 RefreshRate;
  uint16 ScanMode;
  uint32 VerticalResolution;
};
```

## <a name="members"></a><span data-ttu-id="a875e-113">Miembros</span><span class="sxs-lookup"><span data-stu-id="a875e-113">Members</span></span>

<span data-ttu-id="a875e-114">La clase **CIM \_ VideoControllerResolution** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="a875e-114">The **CIM\_VideoControllerResolution** class has these types of members:</span></span>

-   [<span data-ttu-id="a875e-115">Propiedades</span><span class="sxs-lookup"><span data-stu-id="a875e-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a875e-116">Propiedades</span><span class="sxs-lookup"><span data-stu-id="a875e-116">Properties</span></span>

<span data-ttu-id="a875e-117">La clase **CIM \_ VideoControllerResolution** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="a875e-117">The **CIM\_VideoControllerResolution** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a875e-118">**Caption**</span><span class="sxs-lookup"><span data-stu-id="a875e-118">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a875e-119">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a875e-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a875e-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a875e-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a875e-121">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="a875e-121">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="a875e-122">Breve descripción textual del objeto actual.</span><span class="sxs-lookup"><span data-stu-id="a875e-122">Short textual description of the current object.</span></span>

<span data-ttu-id="a875e-123">Esta propiedad se hereda de [**la \_ configuración de CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="a875e-123">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="a875e-124">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a875e-124">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a875e-125">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a875e-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a875e-126">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a875e-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a875e-127">Descripción textual del objeto actual.</span><span class="sxs-lookup"><span data-stu-id="a875e-127">Textual description of the current object.</span></span>

<span data-ttu-id="a875e-128">Esta propiedad se hereda de [**la \_ configuración de CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="a875e-128">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="a875e-129">**HorizontalResolution**</span><span class="sxs-lookup"><span data-stu-id="a875e-129">**HorizontalResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a875e-130">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a875e-130">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a875e-131">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a875e-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a875e-132">Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ controlador de videojuego CIM**](cim-videocontroller.md).**CurrentHorizontalResolution**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF. \|Resoluciones del monitor DMTF \| 002,2 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" píxeles ")</span><span class="sxs-lookup"><span data-stu-id="a875e-132">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_VideoController**](cim-videocontroller.md).**CurrentHorizontalResolution**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Monitor Resolutions\|002.2"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("pixels")</span></span>
</dt> </dl>

<span data-ttu-id="a875e-133">Resolución horizontal, en píxeles.</span><span class="sxs-lookup"><span data-stu-id="a875e-133">Horizontal resolution, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="a875e-134">**MaxRefreshRate**</span><span class="sxs-lookup"><span data-stu-id="a875e-134">**MaxRefreshRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a875e-135">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a875e-135">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a875e-136">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a875e-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a875e-137">Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ controlador de videojuego CIM**](cim-videocontroller.md).**MaxRefreshRate**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF. \|Resoluciones del monitor DMTF \| 002,7 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" hercios ")</span><span class="sxs-lookup"><span data-stu-id="a875e-137">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_VideoController**](cim-videocontroller.md).**MaxRefreshRate**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Monitor Resolutions\|002.7"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("hertz")</span></span>
</dt> </dl>

<span data-ttu-id="a875e-138">Frecuencia de actualización máxima cuando se admite un intervalo de tarifas en las resoluciones especificadas, en hercios.</span><span class="sxs-lookup"><span data-stu-id="a875e-138">Maximum refresh rate when a range of rates is supported at the specified resolutions, in hertz.</span></span>

</dd> <dt>

<span data-ttu-id="a875e-139">**MinRefreshRate**</span><span class="sxs-lookup"><span data-stu-id="a875e-139">**MinRefreshRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a875e-140">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a875e-140">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a875e-141">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a875e-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a875e-142">Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ controlador de videojuego CIM**](cim-videocontroller.md).**MinRefreshRate**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF. \|Resoluciones del monitor DMTF \| 002,6 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" hercios ")</span><span class="sxs-lookup"><span data-stu-id="a875e-142">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_VideoController**](cim-videocontroller.md).**MinRefreshRate**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Monitor Resolutions\|002.6"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("hertz")</span></span>
</dt> </dl>

<span data-ttu-id="a875e-143">Frecuencia de actualización mínima cuando se admite un intervalo de tarifas en las resoluciones especificadas, en hercios.</span><span class="sxs-lookup"><span data-stu-id="a875e-143">Minimum refresh rate when a range of rates is supported at the specified resolutions, in hertz.</span></span>

</dd> <dt>

<span data-ttu-id="a875e-144">**NumberOfColors**</span><span class="sxs-lookup"><span data-stu-id="a875e-144">**NumberOfColors**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a875e-145">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="a875e-145">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="a875e-146">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a875e-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a875e-147">Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ controlador de videojuego CIM**](cim-videocontroller.md).**CurrentNumberOfColors**")</span><span class="sxs-lookup"><span data-stu-id="a875e-147">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_VideoController**](cim-videocontroller.md).**CurrentNumberOfColors**")</span></span>
</dt> </dl>

<span data-ttu-id="a875e-148">Número de colores admitidos en la resolución actual.</span><span class="sxs-lookup"><span data-stu-id="a875e-148">Number of colors supported at the current resolution.</span></span>

<span data-ttu-id="a875e-149">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="a875e-149">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="a875e-150">**Frecuencia**</span><span class="sxs-lookup"><span data-stu-id="a875e-150">**RefreshRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a875e-151">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a875e-151">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a875e-152">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a875e-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a875e-153">Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ controlador de videojuego CIM**](cim-videocontroller.md).**CurrentRefreshRate**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF. \|Resoluciones del monitor DMTF \| 002,4 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" hercios ")</span><span class="sxs-lookup"><span data-stu-id="a875e-153">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_VideoController**](cim-videocontroller.md).**CurrentRefreshRate**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Monitor Resolutions\|002.4"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("hertz")</span></span>
</dt> </dl>

<span data-ttu-id="a875e-154">Frecuencia de actualización, en hercios.</span><span class="sxs-lookup"><span data-stu-id="a875e-154">Refresh rate, in hertz.</span></span> <span data-ttu-id="a875e-155">Si se admite un intervalo de tarifas, use las propiedades **MinRefreshRate** y **MaxRefreshRate** y establezca esta propiedad en 0.</span><span class="sxs-lookup"><span data-stu-id="a875e-155">If a range of rates is supported, use the **MinRefreshRate** and **MaxRefreshRate** properties, and set this property to 0.</span></span>

</dd> <dt>

<span data-ttu-id="a875e-156">**ScanMode**</span><span class="sxs-lookup"><span data-stu-id="a875e-156">**ScanMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a875e-157">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a875e-157">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a875e-158">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a875e-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a875e-159">Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ controlador de videojuego CIM**](cim-videocontroller.md).**CurrentScanMode**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF. \|Resoluciones del monitor DMTF \| 002,5 ")</span><span class="sxs-lookup"><span data-stu-id="a875e-159">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_VideoController**](cim-videocontroller.md).**CurrentScanMode**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Monitor Resolutions\|002.5")</span></span>
</dt> </dl>

<span data-ttu-id="a875e-160">Modo de recorrido en el que funciona el controlador.</span><span class="sxs-lookup"><span data-stu-id="a875e-160">Scan mode at which the controller operates.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="a875e-161"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="a875e-161"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="a875e-162"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="a875e-162"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="a875e-163"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**No compatible** (3)</span><span class="sxs-lookup"><span data-stu-id="a875e-163"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Non-Interlaced_Operation"></span><span id="non-interlaced_operation"></span><span id="NON-INTERLACED_OPERATION"></span>

<span data-ttu-id="a875e-164"><span id="Non-Interlaced_Operation"></span><span id="non-interlaced_operation"></span><span id="NON-INTERLACED_OPERATION"></span>**Operación no entrelazada** (4)</span><span class="sxs-lookup"><span data-stu-id="a875e-164"><span id="Non-Interlaced_Operation"></span><span id="non-interlaced_operation"></span><span id="NON-INTERLACED_OPERATION"></span>**Non-Interlaced Operation** (4)</span></span>


</dt> <dd>

<span data-ttu-id="a875e-165">Operación no entrelazada</span><span class="sxs-lookup"><span data-stu-id="a875e-165">Noninterlaced operation</span></span>

</dd> <dt>

<span id="Interlaced_Operation"></span><span id="interlaced_operation"></span><span id="INTERLACED_OPERATION"></span>

<span data-ttu-id="a875e-166"><span id="Interlaced_Operation"></span><span id="interlaced_operation"></span><span id="INTERLACED_OPERATION"></span>**Operación entrelazada** (5)</span><span class="sxs-lookup"><span data-stu-id="a875e-166"><span id="Interlaced_Operation"></span><span id="interlaced_operation"></span><span id="INTERLACED_OPERATION"></span>**Interlaced Operation** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="a875e-167">**SettingID**</span><span class="sxs-lookup"><span data-stu-id="a875e-167">**SettingID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a875e-168">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a875e-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a875e-169">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a875e-169">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a875e-170">Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("SettingID"), [**key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="a875e-170">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("SettingID"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="a875e-171">IDENTIFICADOR que sirve como parte de la clave de la instancia actual.</span><span class="sxs-lookup"><span data-stu-id="a875e-171">An ID that serves as part of the key for the current instance.</span></span>

</dd> <dt>

<span data-ttu-id="a875e-172">**VerticalResolution**</span><span class="sxs-lookup"><span data-stu-id="a875e-172">**VerticalResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a875e-173">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a875e-173">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a875e-174">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a875e-174">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a875e-175">Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ controlador de videojuego CIM**](cim-videocontroller.md).**CurrentVerticalResolution**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF. \|Resoluciones del monitor DMTF \| 002,3 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" píxeles ")</span><span class="sxs-lookup"><span data-stu-id="a875e-175">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_VideoController**](cim-videocontroller.md).**CurrentVerticalResolution**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Monitor Resolutions\|002.3"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("pixels")</span></span>
</dt> </dl>

<span data-ttu-id="a875e-176">Resolución vertical del controlador, en píxeles.</span><span class="sxs-lookup"><span data-stu-id="a875e-176">Controller's vertical resolution, in pixels.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a875e-177">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a875e-177">Remarks</span></span>

<span data-ttu-id="a875e-178">WMI implementa la clase **\_ VideoControllerResolution de CIM** .</span><span class="sxs-lookup"><span data-stu-id="a875e-178">WMI implements the **CIM\_VideoControllerResolution** class.</span></span> <span data-ttu-id="a875e-179">La clase **CIM \_ VideoControllerResolution** es una clase dinámica.</span><span class="sxs-lookup"><span data-stu-id="a875e-179">The **CIM\_VideoControllerResolution** class is a dynamic class.</span></span>

<span data-ttu-id="a875e-180">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="a875e-180">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="a875e-181">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="a875e-181">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

<span data-ttu-id="a875e-182">Tenga en cuenta que esta clase es una clase base.</span><span class="sxs-lookup"><span data-stu-id="a875e-182">Note that this class is a base class.</span></span> <span data-ttu-id="a875e-183">Si está intentando obtener acceso a su controladora de vídeo a través de WMI, puede que desee usar [**\_ videocontroller de Win32**](win32-videocontroller.md) en su lugar.</span><span class="sxs-lookup"><span data-stu-id="a875e-183">If you are attempting to access your video controller through WMI, you may wish to use [**Win32\_VideoController**](win32-videocontroller.md) instead.</span></span>

## <a name="requirements"></a><span data-ttu-id="a875e-184">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a875e-184">Requirements</span></span>



| <span data-ttu-id="a875e-185">Requisito</span><span class="sxs-lookup"><span data-stu-id="a875e-185">Requirement</span></span> | <span data-ttu-id="a875e-186">Value</span><span class="sxs-lookup"><span data-stu-id="a875e-186">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a875e-187">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a875e-187">Minimum supported client</span></span><br/> | <span data-ttu-id="a875e-188">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a875e-188">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a875e-189">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a875e-189">Minimum supported server</span></span><br/> | <span data-ttu-id="a875e-190">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a875e-190">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a875e-191">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="a875e-191">Namespace</span></span><br/>                | <span data-ttu-id="a875e-192">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="a875e-192">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="a875e-193">MOF</span><span class="sxs-lookup"><span data-stu-id="a875e-193">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a875e-194"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a875e-194"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="a875e-195">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="a875e-195">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a875e-196"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a875e-196"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a875e-197">Vea también</span><span class="sxs-lookup"><span data-stu-id="a875e-197">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a875e-198">**Configuración de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="a875e-198">**CIM\_Setting**</span></span>](cim-setting.md)
</dt> </dl>

 

