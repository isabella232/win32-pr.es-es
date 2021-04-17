---
description: Representa un encabezado de un \_ objeto DisplayController de CIM.
ms.assetid: 2bb034d9-d1df-4cc8-a6a8-b6ad7289f582
title: CIM_VideoHead (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VideoHead
- CIM_VideoHead.CurrentBitsPerPixel
- CIM_VideoHead.CurrentHorizontalResolution
- CIM_VideoHead.CurrentVerticalResolution
- CIM_VideoHead.MaxRefreshRate
- CIM_VideoHead.MinRefreshRate
- CIM_VideoHead.CurrentRefreshRate
- CIM_VideoHead.CurrentScanMode
- CIM_VideoHead.OtherCurrentScanMode
- CIM_VideoHead.CurrentNumberOfRows
- CIM_VideoHead.CurrentNumberOfColumns
- CIM_VideoHead.CurrentNumberOfColors
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 22f8176c9bdbeae460dfa22ca395e7ed8dd8351e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687345"
---
# <a name="cim_videohead-class"></a><span data-ttu-id="bc073-103">\_Clase de Videopartida CIM</span><span class="sxs-lookup"><span data-stu-id="bc073-103">CIM\_VideoHead class</span></span>

<span data-ttu-id="bc073-104">Representa un encabezado de un [**objeto \_ DisplayController de CIM**](cim-displaycontroller.md) .</span><span class="sxs-lookup"><span data-stu-id="bc073-104">Represents one head of a [**CIM\_DisplayController**](cim-displaycontroller.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="bc073-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bc073-105">Syntax</span></span>

``` syntax
[Experimental, Abstract, Version("2.10.0"), UMLPackagePath("CIM::Device::Controller"), AMENDMENT]
class CIM_VideoHead : CIM_LogicalDevice
{
  uint32 CurrentBitsPerPixel;
  uint32 CurrentHorizontalResolution;
  uint32 CurrentVerticalResolution;
  uint32 MaxRefreshRate;
  uint32 MinRefreshRate;
  uint32 CurrentRefreshRate;
  uint16 CurrentScanMode;
  string OtherCurrentScanMode;
  uint32 CurrentNumberOfRows;
  uint32 CurrentNumberOfColumns;
  uint64 CurrentNumberOfColors;
};
```

## <a name="members"></a><span data-ttu-id="bc073-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="bc073-106">Members</span></span>

<span data-ttu-id="bc073-107">La clase de **\_ videopartida CIM** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="bc073-107">The **CIM\_VideoHead** class has these types of members:</span></span>

-   [<span data-ttu-id="bc073-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="bc073-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="bc073-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="bc073-109">Properties</span></span>

<span data-ttu-id="bc073-110">La clase de **\_ videopartida CIM** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="bc073-110">The **CIM\_VideoHead** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="bc073-111">**CurrentBitsPerPixel**</span><span class="sxs-lookup"><span data-stu-id="bc073-111">**CurrentBitsPerPixel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc073-112">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="bc073-112">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="bc073-113">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="bc073-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bc073-114">Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| vídeo \| 004,12 "), **punitivo** (" bit ")</span><span class="sxs-lookup"><span data-stu-id="bc073-114">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bits"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|004.12"), **PUnit** ("bit")</span></span>
</dt> </dl>

<span data-ttu-id="bc073-115">Número de bits usados para mostrar cada píxel.</span><span class="sxs-lookup"><span data-stu-id="bc073-115">The number of bits used to display each pixel.</span></span>

</dd> <dt>

<span data-ttu-id="bc073-116">**CurrentHorizontalResolution**</span><span class="sxs-lookup"><span data-stu-id="bc073-116">**CurrentHorizontalResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc073-117">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="bc073-117">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="bc073-118">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="bc073-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bc073-119">Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("píxeles"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| vídeo \| 004,11 "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) (" CIM \_ VideoHeadResolution. HorizontalResolution "), **punitivo** (" píxel ")</span><span class="sxs-lookup"><span data-stu-id="bc073-119">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Pixels"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|004.11"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_VideoHeadResolution.HorizontalResolution"), **PUnit** ("pixel")</span></span>
</dt> </dl>

<span data-ttu-id="bc073-120">Número actual de píxeles horizontales.</span><span class="sxs-lookup"><span data-stu-id="bc073-120">The current number of horizontal pixels.</span></span>

</dd> <dt>

<span data-ttu-id="bc073-121">**CurrentNumberOfColors**</span><span class="sxs-lookup"><span data-stu-id="bc073-121">**CurrentNumberOfColors**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc073-122">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="bc073-122">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="bc073-123">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="bc073-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bc073-124">Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ VideoHeadResolution. NumberOfColors")</span><span class="sxs-lookup"><span data-stu-id="bc073-124">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_VideoHeadResolution.NumberOfColors")</span></span>
</dt> </dl>

<span data-ttu-id="bc073-125">El número de colores admitidos en la resolución actual.</span><span class="sxs-lookup"><span data-stu-id="bc073-125">The number of colors supported at the current resolution.</span></span>

</dd> <dt>

<span data-ttu-id="bc073-126">**CurrentNumberOfColumns**</span><span class="sxs-lookup"><span data-stu-id="bc073-126">**CurrentNumberOfColumns**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc073-127">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="bc073-127">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="bc073-128">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="bc073-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bc073-129">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Vídeo DMTF \| 004,14 ")</span><span class="sxs-lookup"><span data-stu-id="bc073-129">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|004.14")</span></span>
</dt> </dl>

<span data-ttu-id="bc073-130">Si está en modo de carácter, el número de columnas del controlador de pantalla; de lo contrario, "0".</span><span class="sxs-lookup"><span data-stu-id="bc073-130">If in character mode, the number of columns for the display controller; otherwise, "0".</span></span>

</dd> <dt>

<span data-ttu-id="bc073-131">**CurrentNumberOfRows**</span><span class="sxs-lookup"><span data-stu-id="bc073-131">**CurrentNumberOfRows**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc073-132">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="bc073-132">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="bc073-133">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="bc073-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bc073-134">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Vídeo DMTF \| 004,13 ")</span><span class="sxs-lookup"><span data-stu-id="bc073-134">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|004.13")</span></span>
</dt> </dl>

<span data-ttu-id="bc073-135">Si está en modo de carácter, el número de filas del controlador de pantalla; de lo contrario, "0".</span><span class="sxs-lookup"><span data-stu-id="bc073-135">If in character mode, the number of rows for the display controller; otherwise, "0".</span></span>

</dd> <dt>

<span data-ttu-id="bc073-136">**CurrentRefreshRate**</span><span class="sxs-lookup"><span data-stu-id="bc073-136">**CurrentRefreshRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc073-137">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="bc073-137">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="bc073-138">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="bc073-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bc073-139">Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("hercios"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| vídeo \| 004,15 "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) (" CIM \_ VideoHeadResolution.), **punitivo** ("hercios")</span><span class="sxs-lookup"><span data-stu-id="bc073-139">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Hertz"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|004.15"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_VideoHeadResolution.RefreshRate"), **PUnit** ("hertz")</span></span>
</dt> </dl>

<span data-ttu-id="bc073-140">Frecuencia de actualización actual del controlador de pantalla, en hercios.</span><span class="sxs-lookup"><span data-stu-id="bc073-140">The current refresh rate of the display controller, in hertz.</span></span>

</dd> <dt>

<span data-ttu-id="bc073-141">**CurrentScanMode**</span><span class="sxs-lookup"><span data-stu-id="bc073-141">**CurrentScanMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc073-142">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="bc073-142">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="bc073-143">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="bc073-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bc073-144">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| vídeo \| 004,8 "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ videohead**.**OtherCurrentScanMode**, CIM \_ VideoHeadResolution. ScanMode ")</span><span class="sxs-lookup"><span data-stu-id="bc073-144">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|004.8"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_VideoHead**.**OtherCurrentScanMode**, CIM\_VideoHeadResolution.ScanMode")</span></span>
</dt> </dl>

<span data-ttu-id="bc073-145">El modo de exploración actual del controlador de pantalla.</span><span class="sxs-lookup"><span data-stu-id="bc073-145">The current scan mode of the display controller.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="bc073-146">**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="bc073-146">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="bc073-147">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="bc073-147">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="bc073-148">**No compatible** (2)</span><span class="sxs-lookup"><span data-stu-id="bc073-148">**Not Supported** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Non-Interlaced_Operation"></span><span id="non-interlaced_operation"></span><span id="NON-INTERLACED_OPERATION"></span>

<span data-ttu-id="bc073-149">**Operación no entrelazada** (3)</span><span class="sxs-lookup"><span data-stu-id="bc073-149">**Non-Interlaced Operation** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Interlaced_Operation"></span><span id="interlaced_operation"></span><span id="INTERLACED_OPERATION"></span>

<span data-ttu-id="bc073-150">**Operación entrelazada** (4)</span><span class="sxs-lookup"><span data-stu-id="bc073-150">**Interlaced Operation** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="bc073-151">**CurrentVerticalResolution**</span><span class="sxs-lookup"><span data-stu-id="bc073-151">**CurrentVerticalResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc073-152">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="bc073-152">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="bc073-153">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="bc073-153">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bc073-154">Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("píxeles"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| vídeo \| 004,10 "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) (" CIM \_ VideoHeadResolution. VerticalResolution "), **punitivo** (" píxel ")</span><span class="sxs-lookup"><span data-stu-id="bc073-154">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Pixels"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|004.10"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_VideoHeadResolution.VerticalResolution"), **PUnit** ("pixel")</span></span>
</dt> </dl>

<span data-ttu-id="bc073-155">Número actual de píxeles verticales.</span><span class="sxs-lookup"><span data-stu-id="bc073-155">The current number of vertical pixels.</span></span>

</dd> <dt>

<span data-ttu-id="bc073-156">**MaxRefreshRate**</span><span class="sxs-lookup"><span data-stu-id="bc073-156">**MaxRefreshRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc073-157">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="bc073-157">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="bc073-158">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="bc073-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bc073-159">Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("hercios"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| vídeo \| 004,5 "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) (" CIM \_ VideoHeadResolution. MaxRefreshRate "), **punitivo** (" hercios ")</span><span class="sxs-lookup"><span data-stu-id="bc073-159">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Hertz"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|004.5"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_VideoHeadResolution.MaxRefreshRate"), **PUnit** ("hertz")</span></span>
</dt> </dl>

<span data-ttu-id="bc073-160">La frecuencia máxima de actualización del controlador de pantalla, en hercios.</span><span class="sxs-lookup"><span data-stu-id="bc073-160">The maximum refresh rate of the display controller, in hertz.</span></span>

</dd> <dt>

<span data-ttu-id="bc073-161">**MinRefreshRate**</span><span class="sxs-lookup"><span data-stu-id="bc073-161">**MinRefreshRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc073-162">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="bc073-162">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="bc073-163">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="bc073-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bc073-164">Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("hercios"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| vídeo \| 004,4 "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) (" CIM \_ VideoHeadResolution. MinRefreshRate "), **punitivo** (" hercios ")</span><span class="sxs-lookup"><span data-stu-id="bc073-164">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Hertz"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|004.4"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_VideoHeadResolution.MinRefreshRate"), **PUnit** ("hertz")</span></span>
</dt> </dl>

<span data-ttu-id="bc073-165">La frecuencia de actualización mínima del controlador de pantalla, en hercios.</span><span class="sxs-lookup"><span data-stu-id="bc073-165">The minimum refresh rate of the display controller, in hertz.</span></span>

</dd> <dt>

<span data-ttu-id="bc073-166">**OtherCurrentScanMode**</span><span class="sxs-lookup"><span data-stu-id="bc073-166">**OtherCurrentScanMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bc073-167">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="bc073-167">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bc073-168">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="bc073-168">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bc073-169">Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ videohead**.**CurrentScanMode**, CIM \_ VideoHeadResolution. OtherScanMode ")</span><span class="sxs-lookup"><span data-stu-id="bc073-169">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_VideoHead**.**CurrentScanMode**, CIM\_VideoHeadResolution.OtherScanMode")</span></span>
</dt> </dl>

<span data-ttu-id="bc073-170">Descripción del modo de examen actual cuando la propiedad **CurrentScanMode** es "1" (otra).</span><span class="sxs-lookup"><span data-stu-id="bc073-170">A description of current scan mode when the **CurrentScanMode** property is "1" (other).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="bc073-171">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bc073-171">Requirements</span></span>



| <span data-ttu-id="bc073-172">Requisito</span><span class="sxs-lookup"><span data-stu-id="bc073-172">Requirement</span></span> | <span data-ttu-id="bc073-173">Value</span><span class="sxs-lookup"><span data-stu-id="bc073-173">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bc073-174">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bc073-174">Minimum supported client</span></span><br/> | <span data-ttu-id="bc073-175">Windows 8</span><span class="sxs-lookup"><span data-stu-id="bc073-175">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="bc073-176">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bc073-176">Minimum supported server</span></span><br/> | <span data-ttu-id="bc073-177">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="bc073-177">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="bc073-178">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="bc073-178">Namespace</span></span><br/>                | <span data-ttu-id="bc073-179">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="bc073-179">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="bc073-180">MOF</span><span class="sxs-lookup"><span data-stu-id="bc073-180">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bc073-181"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="bc073-181"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="bc073-182">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="bc073-182">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bc073-183"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="bc073-183"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="bc073-184">Vea también</span><span class="sxs-lookup"><span data-stu-id="bc073-184">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc073-185">**LogicalDevice de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="bc073-185">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> </dl>

 

