---
description: La \_ clase CIM MonitorResolution representa la relación entre las resoluciones horizontal y vertical, y la frecuencia de actualización y el modo de recorrido de un monitor de escritorio. Los valores se especifican en el objeto de controlador de vídeo.
ms.assetid: 064620dd-2d92-42d0-9167-35867830a077
ms.tgt_platform: multiple
title: CIM_MonitorResolution (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MonitorResolution
- CIM_MonitorResolution.Caption
- CIM_MonitorResolution.Description
- CIM_MonitorResolution.SettingID
- CIM_MonitorResolution.HorizontalResolution
- CIM_MonitorResolution.MaxRefreshRate
- CIM_MonitorResolution.MinRefreshRate
- CIM_MonitorResolution.RefreshRate
- CIM_MonitorResolution.ScanMode
- CIM_MonitorResolution.VerticalResolution
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b359a2e7eccf31b32aced8a2ea9f85fb6dc48b7a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104000686"
---
# <a name="cim_monitorresolution-class"></a><span data-ttu-id="72e1b-104">\_Clase MonitorResolution de CIM</span><span class="sxs-lookup"><span data-stu-id="72e1b-104">CIM\_MonitorResolution class</span></span>

<span data-ttu-id="72e1b-105">La clase **CIM \_ MonitorResolution** representa la relación entre las resoluciones horizontal y vertical, y la frecuencia de actualización y el modo de recorrido de un monitor de escritorio.</span><span class="sxs-lookup"><span data-stu-id="72e1b-105">The **CIM\_MonitorResolution** class represents the relationship between horizontal and vertical resolutions and the refresh rate and scan mode for a desktop monitor.</span></span> <span data-ttu-id="72e1b-106">Los valores se especifican en el objeto de controlador de vídeo.</span><span class="sxs-lookup"><span data-stu-id="72e1b-106">Values are specified in the video controller object.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="72e1b-107">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="72e1b-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="72e1b-108">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="72e1b-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="72e1b-109">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="72e1b-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="72e1b-110">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="72e1b-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="72e1b-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="72e1b-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{1008CCEC-7BFF-11D2-AAD2-006008C78BC7}"), AMENDMENT]
class CIM_MonitorResolution : CIM_Setting
{
  string Caption;
  string Description;
  string SettingID;
  uint32 HorizontalResolution;
  uint32 MaxRefreshRate;
  uint32 MinRefreshRate;
  uint32 RefreshRate;
  uint16 ScanMode;
  uint32 VerticalResolution;
};
```

## <a name="members"></a><span data-ttu-id="72e1b-112">Miembros</span><span class="sxs-lookup"><span data-stu-id="72e1b-112">Members</span></span>

<span data-ttu-id="72e1b-113">La clase **CIM \_ MonitorResolution** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="72e1b-113">The **CIM\_MonitorResolution** class has these types of members:</span></span>

-   [<span data-ttu-id="72e1b-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="72e1b-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="72e1b-115">Propiedades</span><span class="sxs-lookup"><span data-stu-id="72e1b-115">Properties</span></span>

<span data-ttu-id="72e1b-116">La clase **CIM \_ MonitorResolution** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="72e1b-116">The **CIM\_MonitorResolution** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="72e1b-117">**Caption**</span><span class="sxs-lookup"><span data-stu-id="72e1b-117">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="72e1b-118">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="72e1b-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="72e1b-119">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="72e1b-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="72e1b-120">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="72e1b-120">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="72e1b-121">Breve descripción textual del objeto actual.</span><span class="sxs-lookup"><span data-stu-id="72e1b-121">Short textual description of the current object.</span></span>

<span data-ttu-id="72e1b-122">Esta propiedad se hereda de [**la \_ configuración de CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="72e1b-122">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="72e1b-123">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="72e1b-123">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="72e1b-124">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="72e1b-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="72e1b-125">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="72e1b-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="72e1b-126">Descripción textual del objeto actual.</span><span class="sxs-lookup"><span data-stu-id="72e1b-126">Textual description of the current object.</span></span>

<span data-ttu-id="72e1b-127">Esta propiedad se hereda de [**la \_ configuración de CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="72e1b-127">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="72e1b-128">**HorizontalResolution**</span><span class="sxs-lookup"><span data-stu-id="72e1b-128">**HorizontalResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="72e1b-129">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="72e1b-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="72e1b-130">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="72e1b-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="72e1b-131">Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ controlador de videojuego CIM**](cim-videocontroller.md).**CurrentHorizontalResolution**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF. \|Resoluciones del monitor DMTF \| 002,2 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" píxeles ")</span><span class="sxs-lookup"><span data-stu-id="72e1b-131">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_VideoController**](cim-videocontroller.md).**CurrentHorizontalResolution**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Monitor Resolutions\|002.2"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("pixels")</span></span>
</dt> </dl>

<span data-ttu-id="72e1b-132">Resolución horizontal del monitor, en píxeles.</span><span class="sxs-lookup"><span data-stu-id="72e1b-132">Monitor's horizontal resolution, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="72e1b-133">**MaxRefreshRate**</span><span class="sxs-lookup"><span data-stu-id="72e1b-133">**MaxRefreshRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="72e1b-134">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="72e1b-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="72e1b-135">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="72e1b-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="72e1b-136">Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ controlador de videojuego CIM**](cim-videocontroller.md).**MaxRefreshRate**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF. \|Resoluciones del monitor DMTF \| 002,7 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" hercios ")</span><span class="sxs-lookup"><span data-stu-id="72e1b-136">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_VideoController**](cim-videocontroller.md).**MaxRefreshRate**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Monitor Resolutions\|002.7"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("hertz")</span></span>
</dt> </dl>

<span data-ttu-id="72e1b-137">Frecuencia de actualización máxima del monitor, en hercios, cuando se admite un intervalo de tarifas en las resoluciones especificadas.</span><span class="sxs-lookup"><span data-stu-id="72e1b-137">Monitor's maximum refresh rate, in hertz, when a range of rates is supported at the specified resolutions.</span></span>

</dd> <dt>

<span data-ttu-id="72e1b-138">**MinRefreshRate**</span><span class="sxs-lookup"><span data-stu-id="72e1b-138">**MinRefreshRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="72e1b-139">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="72e1b-139">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="72e1b-140">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="72e1b-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="72e1b-141">Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ controlador de videojuego CIM**](cim-videocontroller.md).**MinRefreshRate**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF. \|Resoluciones del monitor DMTF \| 002,6 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" hercios ")</span><span class="sxs-lookup"><span data-stu-id="72e1b-141">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_VideoController**](cim-videocontroller.md).**MinRefreshRate**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Monitor Resolutions\|002.6"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("hertz")</span></span>
</dt> </dl>

<span data-ttu-id="72e1b-142">Frecuencia de actualización mínima del monitor, en hercios, cuando se admite un intervalo de tarifas en las resoluciones especificadas.</span><span class="sxs-lookup"><span data-stu-id="72e1b-142">Monitor's minimum refresh rate, in hertz, when a range of rates is supported at the specified resolutions.</span></span>

</dd> <dt>

<span data-ttu-id="72e1b-143">**Frecuencia**</span><span class="sxs-lookup"><span data-stu-id="72e1b-143">**RefreshRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="72e1b-144">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="72e1b-144">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="72e1b-145">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="72e1b-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="72e1b-146">Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ controlador de videojuego CIM**](cim-videocontroller.md).**CurrentRefreshRate**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF. \|Resoluciones del monitor DMTF \| 002,4 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" hercios ")</span><span class="sxs-lookup"><span data-stu-id="72e1b-146">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_VideoController**](cim-videocontroller.md).**CurrentRefreshRate**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Monitor Resolutions\|002.4"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("hertz")</span></span>
</dt> </dl>

<span data-ttu-id="72e1b-147">Frecuencia de actualización del monitor, en hercios.</span><span class="sxs-lookup"><span data-stu-id="72e1b-147">Monitor's refresh rate, in hertz.</span></span> <span data-ttu-id="72e1b-148">Si se admite un intervalo de tarifas, use las propiedades **MinRefreshRate** y **MaxRefreshRate** y establezca esta propiedad en 0.</span><span class="sxs-lookup"><span data-stu-id="72e1b-148">If a range of rates is supported, use the **MinRefreshRate** and **MaxRefreshRate** properties, and set this property to 0.</span></span>

</dd> <dt>

<span data-ttu-id="72e1b-149">**ScanMode**</span><span class="sxs-lookup"><span data-stu-id="72e1b-149">**ScanMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="72e1b-150">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="72e1b-150">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="72e1b-151">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="72e1b-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="72e1b-152">Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ controlador de videojuego CIM**](cim-videocontroller.md).**CurrentScanMode**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF. \|Resoluciones del monitor DMTF \| 002,5 ")</span><span class="sxs-lookup"><span data-stu-id="72e1b-152">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_VideoController**](cim-videocontroller.md).**CurrentScanMode**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Monitor Resolutions\|002.5")</span></span>
</dt> </dl>

<span data-ttu-id="72e1b-153">Modo de exploración que utiliza el monitor.</span><span class="sxs-lookup"><span data-stu-id="72e1b-153">Scan mode that the monitor uses.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="72e1b-154">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="72e1b-154">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="72e1b-155">**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="72e1b-155">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="72e1b-156">**No compatible** (3)</span><span class="sxs-lookup"><span data-stu-id="72e1b-156">**Not Supported** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Non-Interlaced_Operation"></span><span id="non-interlaced_operation"></span><span id="NON-INTERLACED_OPERATION"></span>

<span data-ttu-id="72e1b-157">**Operación no entrelazada** (4)</span><span class="sxs-lookup"><span data-stu-id="72e1b-157">**Non-Interlaced Operation** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Interlaced_Operation"></span><span id="interlaced_operation"></span><span id="INTERLACED_OPERATION"></span>

<span data-ttu-id="72e1b-158">**Operación entrelazada** (5)</span><span class="sxs-lookup"><span data-stu-id="72e1b-158">**Interlaced Operation** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="72e1b-159">**SettingID**</span><span class="sxs-lookup"><span data-stu-id="72e1b-159">**SettingID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="72e1b-160">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="72e1b-160">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="72e1b-161">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="72e1b-161">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="72e1b-162">Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("SettingID"), [**key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="72e1b-162">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("SettingID"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="72e1b-163">Sirve como parte de la clave de la instancia actual.</span><span class="sxs-lookup"><span data-stu-id="72e1b-163">Serves as part of the key for the current instance.</span></span>

</dd> <dt>

<span data-ttu-id="72e1b-164">**VerticalResolution**</span><span class="sxs-lookup"><span data-stu-id="72e1b-164">**VerticalResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="72e1b-165">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="72e1b-165">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="72e1b-166">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="72e1b-166">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="72e1b-167">Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ controlador de videojuego CIM**](cim-videocontroller.md).**CurrentVerticalResolution**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF. \|Resoluciones del monitor DMTF \| 002,3 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" píxeles ")</span><span class="sxs-lookup"><span data-stu-id="72e1b-167">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_VideoController**](cim-videocontroller.md).**CurrentVerticalResolution**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Monitor Resolutions\|002.3"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("pixels")</span></span>
</dt> </dl>

<span data-ttu-id="72e1b-168">Resolución vertical del monitor en píxeles.</span><span class="sxs-lookup"><span data-stu-id="72e1b-168">Monitor's vertical resolution in pixels.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="72e1b-169">Observaciones</span><span class="sxs-lookup"><span data-stu-id="72e1b-169">Remarks</span></span>

<span data-ttu-id="72e1b-170">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="72e1b-170">WMI does not implement this class.</span></span>

<span data-ttu-id="72e1b-171">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="72e1b-171">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="72e1b-172">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="72e1b-172">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="72e1b-173">Requisitos</span><span class="sxs-lookup"><span data-stu-id="72e1b-173">Requirements</span></span>



| <span data-ttu-id="72e1b-174">Requisito</span><span class="sxs-lookup"><span data-stu-id="72e1b-174">Requirement</span></span> | <span data-ttu-id="72e1b-175">Value</span><span class="sxs-lookup"><span data-stu-id="72e1b-175">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="72e1b-176">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="72e1b-176">Minimum supported client</span></span><br/> | <span data-ttu-id="72e1b-177">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="72e1b-177">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="72e1b-178">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="72e1b-178">Minimum supported server</span></span><br/> | <span data-ttu-id="72e1b-179">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="72e1b-179">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="72e1b-180">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="72e1b-180">Namespace</span></span><br/>                | <span data-ttu-id="72e1b-181">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="72e1b-181">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="72e1b-182">MOF</span><span class="sxs-lookup"><span data-stu-id="72e1b-182">MOF</span></span><br/>                      | <dl> <span data-ttu-id="72e1b-183"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="72e1b-183"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="72e1b-184">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="72e1b-184">DLL</span></span><br/>                      | <dl> <span data-ttu-id="72e1b-185"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="72e1b-185"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="72e1b-186">Vea también</span><span class="sxs-lookup"><span data-stu-id="72e1b-186">See also</span></span>

<dl> <dt>

[<span data-ttu-id="72e1b-187">**Configuración de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="72e1b-187">**CIM\_Setting**</span></span>](cim-setting.md)
</dt> </dl>

 

