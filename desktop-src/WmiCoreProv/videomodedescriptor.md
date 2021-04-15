---
description: Contiene los elementos de descriptor de modo de la matriz MonitorSourceModes en la clase WmiMonitorListedSupportedSourceModes.
ms.assetid: 6d6c846d-caec-41a8-8a88-1c1e14bc0473
title: Clase VideoModeDescriptor
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- VideoModeDescriptor
- VideoModeDescriptor.CompositePolarityType
- VideoModeDescriptor.HorizontalActivePixels
- VideoModeDescriptor.HorizontalBlankingPixels
- VideoModeDescriptor.HorizontalBorder
- VideoModeDescriptor.HorizontalImageSize
- VideoModeDescriptor.HorizontalPolarityType
- VideoModeDescriptor.HorizontalRefreshRateDenominator
- VideoModeDescriptor.HorizontalRefreshRateNumerator
- VideoModeDescriptor.HorizontalSyncOffset
- VideoModeDescriptor.HorizontalSyncPulseWidth
- VideoModeDescriptor.IsInterlaced
- VideoModeDescriptor.IsSerrationRequired
- VideoModeDescriptor.IsSyncOnRGB
- VideoModeDescriptor.PixelClockRate
- VideoModeDescriptor.StereoModeType
- VideoModeDescriptor.SyncSignalType
- VideoModeDescriptor.VerticalActivePixels
- VideoModeDescriptor.VerticalBlankingPixels
- VideoModeDescriptor.VerticalBorder
- VideoModeDescriptor.VerticalImageSize
- VideoModeDescriptor.VerticalRefreshRateDenominator
- VideoModeDescriptor.VerticalRefreshRateNumerator
- VideoModeDescriptor.VerticalSyncOffset
- VideoModeDescriptor.VerticalPolarityType
- VideoModeDescriptor.VerticalSyncPulseWidth
- VideoModeDescriptor.VideoStandardType
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.openlocfilehash: 06094b24b6b8197eab89b65cd5a9a83f46b39f95
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361284"
---
# <a name="videomodedescriptor-class"></a><span data-ttu-id="80a0f-103">Clase VideoModeDescriptor</span><span class="sxs-lookup"><span data-stu-id="80a0f-103">VideoModeDescriptor class</span></span>

<span data-ttu-id="80a0f-104">La clase WMI **VideoModeDescriptorVideo** contiene los elementos de descriptor de modo de la matriz **MonitorSourceModes** en la clase [**WmiMonitorListedSupportedSourceModes**](wmimonitorlistedsupportedsourcemodes.md) .</span><span class="sxs-lookup"><span data-stu-id="80a0f-104">The **VideoModeDescriptorVideo** WMI class contains mode descriptor elements for the **MonitorSourceModes** array in the [**WmiMonitorListedSupportedSourceModes**](wmimonitorlistedsupportedsourcemodes.md) class.</span></span> <span data-ttu-id="80a0f-105">Estos elementos incluyen características de monitor como la frecuencia de actualización, las características de píxeles o el tamaño de la imagen.</span><span class="sxs-lookup"><span data-stu-id="80a0f-105">These elements include monitor features such as refresh rate, pixel characteristics, or image size.</span></span> <span data-ttu-id="80a0f-106">La clase **VideoModeDescriptorVideo** contiene información que es un superconjunto de los datos disponibles en los bloques de control de tiempo establecidos, estándar y detallados.</span><span class="sxs-lookup"><span data-stu-id="80a0f-106">The **VideoModeDescriptorVideo** class contains information that is a superset of the data available from established, standard, and detailed timing blocks.</span></span>

## <a name="syntax"></a><span data-ttu-id="80a0f-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="80a0f-107">Syntax</span></span>

``` syntax
class VideoModeDescriptor : WmiMonitorSupportedVideoModes
{
  uint8   CompositePolarityType;
  uint16  HorizontalActivePixels;
  uint16  HorizontalBlankingPixels;
  uint16  HorizontalBorder;
  uint16  HorizontalImageSize;
  uint8   HorizontalPolarityType;
  uint16  HorizontalRefreshRateDenominator;
  uint16  HorizontalRefreshRateNumerator;
  uint16  HorizontalSyncOffset;
  uint16  HorizontalSyncPulseWidth;
  boolean IsInterlaced;
  uint8   IsSerrationRequired;
  uint8   IsSyncOnRGB;
  uint32  PixelClockRate;
  uint8   StereoModeType;
  uint8   SyncSignalType;
  uint16  VerticalActivePixels;
  uint16  VerticalBlankingPixels;
  uint16  VerticalBorder;
  uint16  VerticalImageSize;
  uint16  VerticalRefreshRateDenominator;
  uint16  VerticalRefreshRateNumerator;
  uint16  VerticalSyncOffset;
  uint8   VerticalPolarityType;
  uint16  VerticalSyncPulseWidth;
  uint8   VideoStandardType;
};
```

## <a name="members"></a><span data-ttu-id="80a0f-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="80a0f-108">Members</span></span>

<span data-ttu-id="80a0f-109">La clase **VideoModeDescriptor** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="80a0f-109">The **VideoModeDescriptor** class has these types of members:</span></span>

-   [<span data-ttu-id="80a0f-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="80a0f-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="80a0f-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="80a0f-111">Properties</span></span>

<span data-ttu-id="80a0f-112">La clase **VideoModeDescriptor** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="80a0f-112">The **VideoModeDescriptor** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="80a0f-113">**CompositePolarityType**</span><span class="sxs-lookup"><span data-stu-id="80a0f-113">**CompositePolarityType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80a0f-114">Tipo de datos: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="80a0f-114">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="80a0f-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="80a0f-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="80a0f-116">Tipo de polaridad compuesta.</span><span class="sxs-lookup"><span data-stu-id="80a0f-116">Composite polarity type.</span></span> <span data-ttu-id="80a0f-117">Esta es la polaridad de los impulsos de sincronización horizontal fuera de la sincronización vertical.</span><span class="sxs-lookup"><span data-stu-id="80a0f-117">This is polarity of horizontal sync pulses outside of vertical sync.</span></span>



| <span data-ttu-id="80a0f-118">Value</span><span class="sxs-lookup"><span data-stu-id="80a0f-118">Value</span></span>                                                                              | <span data-ttu-id="80a0f-119">Significado</span><span class="sxs-lookup"><span data-stu-id="80a0f-119">Meaning</span></span>                                                                    |
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <span data-ttu-id="80a0f-120"><dt>0 (0X0)</dt></span><span class="sxs-lookup"><span data-stu-id="80a0f-120"><dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="80a0f-121">La polaridad compuesta es positiva.</span><span class="sxs-lookup"><span data-stu-id="80a0f-121">Composite polarity is positive.</span></span><br/>                                 |
| <dl> <span data-ttu-id="80a0f-122"><dt>1 (0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="80a0f-122"><dt>1 (0x1)</dt></span></span> </dl> | <span data-ttu-id="80a0f-123">La polaridad compuesta es negativa.</span><span class="sxs-lookup"><span data-stu-id="80a0f-123">Composite polarity is negative.</span></span><br/>                                 |
| <dl> <span data-ttu-id="80a0f-124"><dt>2 (0X2)</dt></span><span class="sxs-lookup"><span data-stu-id="80a0f-124"><dt>2 (0x2)</dt></span></span> </dl> | <span data-ttu-id="80a0f-125">No es aplicable.</span><span class="sxs-lookup"><span data-stu-id="80a0f-125">Not applicable.</span></span> <span data-ttu-id="80a0f-126">El tipo de sincronización de señal debe ser compuesto digital.</span><span class="sxs-lookup"><span data-stu-id="80a0f-126">The signal sync type must be digital composite.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="80a0f-127">**HorizontalActivePixels**</span><span class="sxs-lookup"><span data-stu-id="80a0f-127">**HorizontalActivePixels**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80a0f-128">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="80a0f-128">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="80a0f-129">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="80a0f-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="80a0f-130">Número de píxeles activos horizontalmente.</span><span class="sxs-lookup"><span data-stu-id="80a0f-130">Number of horizontally active pixels.</span></span>

</dd> <dt>

<span data-ttu-id="80a0f-131">**HorizontalBlankingPixels**</span><span class="sxs-lookup"><span data-stu-id="80a0f-131">**HorizontalBlankingPixels**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80a0f-132">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="80a0f-132">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="80a0f-133">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="80a0f-133">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="80a0f-134">Número de píxeles en blanco horizontalmente</span><span class="sxs-lookup"><span data-stu-id="80a0f-134">Number of horizontally blanking pixels</span></span>

</dd> <dt>

<span data-ttu-id="80a0f-135">**HorizontalBorder**</span><span class="sxs-lookup"><span data-stu-id="80a0f-135">**HorizontalBorder**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80a0f-136">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="80a0f-136">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="80a0f-137">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="80a0f-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="80a0f-138">Borde horizontal.</span><span class="sxs-lookup"><span data-stu-id="80a0f-138">Horizontal border.</span></span>

</dd> <dt>

<span data-ttu-id="80a0f-139">**HorizontalImageSize**</span><span class="sxs-lookup"><span data-stu-id="80a0f-139">**HorizontalImageSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80a0f-140">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="80a0f-140">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="80a0f-141">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="80a0f-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="80a0f-142">Tamaño de la imagen horizontal en milímetros (mm).</span><span class="sxs-lookup"><span data-stu-id="80a0f-142">Horizontal image size in millimeters (mm).</span></span>

</dd> <dt>

<span data-ttu-id="80a0f-143">**HorizontalPolarityType**</span><span class="sxs-lookup"><span data-stu-id="80a0f-143">**HorizontalPolarityType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80a0f-144">Tipo de datos: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="80a0f-144">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="80a0f-145">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="80a0f-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="80a0f-146">Tipo de polaridad horizontal.</span><span class="sxs-lookup"><span data-stu-id="80a0f-146">Horizontal polarity type.</span></span>



| <span data-ttu-id="80a0f-147">Value</span><span class="sxs-lookup"><span data-stu-id="80a0f-147">Value</span></span>                                                                              | <span data-ttu-id="80a0f-148">Significado</span><span class="sxs-lookup"><span data-stu-id="80a0f-148">Meaning</span></span>                                                                   |
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <span data-ttu-id="80a0f-149"><dt>0 (0X0)</dt></span><span class="sxs-lookup"><span data-stu-id="80a0f-149"><dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="80a0f-150">La polaridad horizontal es positiva.</span><span class="sxs-lookup"><span data-stu-id="80a0f-150">Horizontal polarity is positive.</span></span><br/>                               |
| <dl> <span data-ttu-id="80a0f-151"><dt>1 (0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="80a0f-151"><dt>1 (0x1)</dt></span></span> </dl> | <span data-ttu-id="80a0f-152">La polaridad horizontal es negativa.</span><span class="sxs-lookup"><span data-stu-id="80a0f-152">Horizontal polarity is negative.</span></span><br/>                               |
| <dl> <span data-ttu-id="80a0f-153"><dt>2 (0X2)</dt></span><span class="sxs-lookup"><span data-stu-id="80a0f-153"><dt>2 (0x2)</dt></span></span> </dl> | <span data-ttu-id="80a0f-154">No es aplicable.</span><span class="sxs-lookup"><span data-stu-id="80a0f-154">Not applicable.</span></span> <span data-ttu-id="80a0f-155">El tipo de sincronización de señales debe ser independiente digital.</span><span class="sxs-lookup"><span data-stu-id="80a0f-155">The signal sync type must be digital separate.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="80a0f-156">**HorizontalRefreshRateDenominator**</span><span class="sxs-lookup"><span data-stu-id="80a0f-156">**HorizontalRefreshRateDenominator**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80a0f-157">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="80a0f-157">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="80a0f-158">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="80a0f-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="80a0f-159">Denominador de frecuencia de actualización horizontal.</span><span class="sxs-lookup"><span data-stu-id="80a0f-159">Horizontal refresh rate denominator.</span></span>

</dd> <dt>

<span data-ttu-id="80a0f-160">**HorizontalRefreshRateNumerator**</span><span class="sxs-lookup"><span data-stu-id="80a0f-160">**HorizontalRefreshRateNumerator**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80a0f-161">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="80a0f-161">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="80a0f-162">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="80a0f-162">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="80a0f-163">Numerador de frecuencia de actualización horizontal en hercios (Hz).</span><span class="sxs-lookup"><span data-stu-id="80a0f-163">Horizontal refresh rate numerator in Hertz (Hz).</span></span>

</dd> <dt>

<span data-ttu-id="80a0f-164">**HorizontalSyncOffset**</span><span class="sxs-lookup"><span data-stu-id="80a0f-164">**HorizontalSyncOffset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80a0f-165">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="80a0f-165">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="80a0f-166">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="80a0f-166">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="80a0f-167">Desplazamiento de sincronización horizontal.</span><span class="sxs-lookup"><span data-stu-id="80a0f-167">Horizontal sync offset.</span></span>

</dd> <dt>

<span data-ttu-id="80a0f-168">**HorizontalSyncPulseWidth**</span><span class="sxs-lookup"><span data-stu-id="80a0f-168">**HorizontalSyncPulseWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80a0f-169">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="80a0f-169">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="80a0f-170">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="80a0f-170">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="80a0f-171">Ancho del pulso de sincronización horizontal.</span><span class="sxs-lookup"><span data-stu-id="80a0f-171">Horizontal sync pulse width.</span></span>

</dd> <dt>

<span data-ttu-id="80a0f-172">**IsInterlaced**</span><span class="sxs-lookup"><span data-stu-id="80a0f-172">**IsInterlaced**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80a0f-173">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="80a0f-173">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="80a0f-174">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="80a0f-174">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="80a0f-175">Indica si el modo de presentación está entrelazado.</span><span class="sxs-lookup"><span data-stu-id="80a0f-175">Indicates whether the display mode is interlaced.</span></span>

</dd> <dt>

<span data-ttu-id="80a0f-176">**IsSerrationRequired**</span><span class="sxs-lookup"><span data-stu-id="80a0f-176">**IsSerrationRequired**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80a0f-177">Tipo de datos: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="80a0f-177">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="80a0f-178">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="80a0f-178">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="80a0f-179">Indica qué tipo de serration es obligatorio, si es necesario.</span><span class="sxs-lookup"><span data-stu-id="80a0f-179">Indicates what type of serration is required, if appropriate.</span></span>



| <span data-ttu-id="80a0f-180">Value</span><span class="sxs-lookup"><span data-stu-id="80a0f-180">Value</span></span>                                                                              | <span data-ttu-id="80a0f-181">Significado</span><span class="sxs-lookup"><span data-stu-id="80a0f-181">Meaning</span></span>                                                                                                  |
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="80a0f-182"><dt>0 (0X0)</dt></span><span class="sxs-lookup"><span data-stu-id="80a0f-182"><dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="80a0f-183">El controlador proporcionará la sincronización horizontal durante la sincronización vertical.</span><span class="sxs-lookup"><span data-stu-id="80a0f-183">Controller shall supply horizontal sync during vertical sync.</span></span><br/>                                 |
| <dl> <span data-ttu-id="80a0f-184"><dt>1 (0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="80a0f-184"><dt>1 (0x1)</dt></span></span> </dl> | <span data-ttu-id="80a0f-185">El controlador no proporcionará sincronización horizontal durante la sincronización vertical.</span><span class="sxs-lookup"><span data-stu-id="80a0f-185">Controller shall not supply horizontal sync during vertical sync.</span></span><br/>                             |
| <dl> <span data-ttu-id="80a0f-186"><dt>2 (0X2)</dt></span><span class="sxs-lookup"><span data-stu-id="80a0f-186"><dt>2 (0x2)</dt></span></span> </dl> | <span data-ttu-id="80a0f-187">No es aplicable.</span><span class="sxs-lookup"><span data-stu-id="80a0f-187">Not applicable.</span></span> <span data-ttu-id="80a0f-188">El tipo de sincronización de la señal debe ser bipolar, compuesto analógico o compuesto digital.</span><span class="sxs-lookup"><span data-stu-id="80a0f-188">The signal sync type must be bipolar, analog composite, or digital composite.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="80a0f-189">**IsSyncOnRGB**</span><span class="sxs-lookup"><span data-stu-id="80a0f-189">**IsSyncOnRGB**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80a0f-190">Tipo de datos: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="80a0f-190">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="80a0f-191">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="80a0f-191">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="80a0f-192">Indica qué líneas de señal de vídeo se deben sincronizar, si es necesario.</span><span class="sxs-lookup"><span data-stu-id="80a0f-192">Indicates which video signal lines should be synchronized, if appropriate.</span></span>



| <span data-ttu-id="80a0f-193">Value</span><span class="sxs-lookup"><span data-stu-id="80a0f-193">Value</span></span>                                                                              | <span data-ttu-id="80a0f-194">Significado</span><span class="sxs-lookup"><span data-stu-id="80a0f-194">Meaning</span></span>                                                                           |
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="80a0f-195"><dt>0 (0X0)</dt></span><span class="sxs-lookup"><span data-stu-id="80a0f-195"><dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="80a0f-196">El impulso de sincronización debe aparecer en las 3 líneas de señal de vídeo.</span><span class="sxs-lookup"><span data-stu-id="80a0f-196">Sync pulse should appear on all 3 video signal lines.</span></span><br/>                  |
| <dl> <span data-ttu-id="80a0f-197"><dt>1 (0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="80a0f-197"><dt>1 (0x1)</dt></span></span> </dl> | <span data-ttu-id="80a0f-198">El impulso de sincronización solo debe aparecer en la línea de señal de vídeo verde.</span><span class="sxs-lookup"><span data-stu-id="80a0f-198">Sync pulse should only appear on the green video signal line.</span></span><br/>          |
| <dl> <span data-ttu-id="80a0f-199"><dt>2 (0X2)</dt></span><span class="sxs-lookup"><span data-stu-id="80a0f-199"><dt>2 (0x2)</dt></span></span> </dl> | <span data-ttu-id="80a0f-200">No es aplicable.</span><span class="sxs-lookup"><span data-stu-id="80a0f-200">Not applicable.</span></span> <span data-ttu-id="80a0f-201">El tipo de sincronización de la señal debe ser compuesto bipolar análogo.</span><span class="sxs-lookup"><span data-stu-id="80a0f-201">The signal sync type must be bipolar analog composite.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="80a0f-202">**PixelClockRate**</span><span class="sxs-lookup"><span data-stu-id="80a0f-202">**PixelClockRate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80a0f-203">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="80a0f-203">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="80a0f-204">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="80a0f-204">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="80a0f-205">Velocidad de reloj de píxeles en hercios (Hz).</span><span class="sxs-lookup"><span data-stu-id="80a0f-205">Pixel clock rate in Hertz (Hz).</span></span>

</dd> <dt>

<span data-ttu-id="80a0f-206">**StereoModeType**</span><span class="sxs-lookup"><span data-stu-id="80a0f-206">**StereoModeType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80a0f-207">Tipo de datos: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="80a0f-207">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="80a0f-208">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="80a0f-208">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="80a0f-209">Tipo de modo estéreo.</span><span class="sxs-lookup"><span data-stu-id="80a0f-209">Stereo mode type.</span></span> <span data-ttu-id="80a0f-210">En la tabla siguiente se enumeran los valores posibles.</span><span class="sxs-lookup"><span data-stu-id="80a0f-210">The following table lists the possible values.</span></span>



| <span data-ttu-id="80a0f-211">Value</span><span class="sxs-lookup"><span data-stu-id="80a0f-211">Value</span></span>                                                                              | <span data-ttu-id="80a0f-212">Significado</span><span class="sxs-lookup"><span data-stu-id="80a0f-212">Meaning</span></span>                                                             |
|------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <dl> <span data-ttu-id="80a0f-213"><dt>0 (0X0)</dt></span><span class="sxs-lookup"><span data-stu-id="80a0f-213"><dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="80a0f-214">Sin estéreo.</span><span class="sxs-lookup"><span data-stu-id="80a0f-214">No stereo.</span></span><br/>                                               |
| <dl> <span data-ttu-id="80a0f-215"><dt>1 (0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="80a0f-215"><dt>1 (0x1)</dt></span></span> </dl> | <span data-ttu-id="80a0f-216">El campo estéreo secuencial con la imagen derecha en la sincronización estéreo.</span><span class="sxs-lookup"><span data-stu-id="80a0f-216">Field sequential stereo with right image on stereo sync.</span></span><br/> |
| <dl> <span data-ttu-id="80a0f-217"><dt>2 (0X2)</dt></span><span class="sxs-lookup"><span data-stu-id="80a0f-217"><dt>2 (0x2)</dt></span></span> </dl> | <span data-ttu-id="80a0f-218">El campo estéreo secuencial con la imagen izquierda en la sincronización estéreo.</span><span class="sxs-lookup"><span data-stu-id="80a0f-218">Field sequential stereo with left image on stereo sync.</span></span><br/>  |
| <dl> <span data-ttu-id="80a0f-219"><dt>3 (0X3)</dt></span><span class="sxs-lookup"><span data-stu-id="80a0f-219"><dt>3 (0x3)</dt></span></span> </dl> | <span data-ttu-id="80a0f-220">Estéreo intercalado bidireccionales con imagen derecha en líneas pares.</span><span class="sxs-lookup"><span data-stu-id="80a0f-220">2-way Interleaved Stereo with Right Image on Even Lines.</span></span><br/> |
| <dl> <span data-ttu-id="80a0f-221"><dt>4 (0x4)</dt></span><span class="sxs-lookup"><span data-stu-id="80a0f-221"><dt>4 (0x4)</dt></span></span> </dl> | <span data-ttu-id="80a0f-222">Estéreo intercalado bidireccionales con imagen izquierda en líneas pares.</span><span class="sxs-lookup"><span data-stu-id="80a0f-222">2-way Interleaved Stereo with Left Image on Even Lines.</span></span><br/>  |
| <dl> <span data-ttu-id="80a0f-223"><dt>5 (0X5)</dt></span><span class="sxs-lookup"><span data-stu-id="80a0f-223"><dt>5 (0x5)</dt></span></span> </dl> | <span data-ttu-id="80a0f-224">Estéreo bidireccional entrelazado.</span><span class="sxs-lookup"><span data-stu-id="80a0f-224">4-way Interleaved Stereo.</span></span><br/>                                |
| <dl> <span data-ttu-id="80a0f-225"><dt>6 (0x6)</dt></span><span class="sxs-lookup"><span data-stu-id="80a0f-225"><dt>6 (0x6)</dt></span></span> </dl> | <span data-ttu-id="80a0f-226">Estéreo entrelazado en paralelo.</span><span class="sxs-lookup"><span data-stu-id="80a0f-226">Side-by-Side Interleaved Stereo.</span></span><br/>                         |



 

</dd> <dt>

<span data-ttu-id="80a0f-227">**SyncSignalType**</span><span class="sxs-lookup"><span data-stu-id="80a0f-227">**SyncSignalType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80a0f-228">Tipo de datos: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="80a0f-228">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="80a0f-229">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="80a0f-229">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="80a0f-230">Tipo de sincronización de la señal.</span><span class="sxs-lookup"><span data-stu-id="80a0f-230">Signal sync type.</span></span> <span data-ttu-id="80a0f-231">En la tabla siguiente se enumeran los valores posibles.</span><span class="sxs-lookup"><span data-stu-id="80a0f-231">The following table lists the possible values.</span></span>



| <span data-ttu-id="80a0f-232">Value</span><span class="sxs-lookup"><span data-stu-id="80a0f-232">Value</span></span>                                                                              | <span data-ttu-id="80a0f-233">Significado</span><span class="sxs-lookup"><span data-stu-id="80a0f-233">Meaning</span></span>                             |
|------------------------------------------------------------------------------------|-------------------------------------|
| <dl> <span data-ttu-id="80a0f-234"><dt>0 (0X0)</dt></span><span class="sxs-lookup"><span data-stu-id="80a0f-234"><dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="80a0f-235">Compuesto analógico</span><span class="sxs-lookup"><span data-stu-id="80a0f-235">Analog Composite</span></span><br/>         |
| <dl> <span data-ttu-id="80a0f-236"><dt>1 (0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="80a0f-236"><dt>1 (0x1)</dt></span></span> </dl> | <span data-ttu-id="80a0f-237">Compuesto analógico bipolar</span><span class="sxs-lookup"><span data-stu-id="80a0f-237">Bipolar Analog Composite</span></span><br/> |
| <dl> <span data-ttu-id="80a0f-238"><dt>2 (0X2)</dt></span><span class="sxs-lookup"><span data-stu-id="80a0f-238"><dt>2 (0x2)</dt></span></span> </dl> | <span data-ttu-id="80a0f-239">Compuesto digital</span><span class="sxs-lookup"><span data-stu-id="80a0f-239">Digital Composite</span></span><br/>        |
| <dl> <span data-ttu-id="80a0f-240"><dt>3 (0X3)</dt></span><span class="sxs-lookup"><span data-stu-id="80a0f-240"><dt>3 (0x3)</dt></span></span> </dl> | <span data-ttu-id="80a0f-241">Independiente digital</span><span class="sxs-lookup"><span data-stu-id="80a0f-241">Digital Separate</span></span><br/>         |



 

</dd> <dt>

<span data-ttu-id="80a0f-242">**VerticalActivePixels**</span><span class="sxs-lookup"><span data-stu-id="80a0f-242">**VerticalActivePixels**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80a0f-243">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="80a0f-243">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="80a0f-244">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="80a0f-244">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="80a0f-245">Número de píxeles activos verticalmente.</span><span class="sxs-lookup"><span data-stu-id="80a0f-245">Number of vertically active pixels.</span></span>

</dd> <dt>

<span data-ttu-id="80a0f-246">**VerticalBlankingPixels**</span><span class="sxs-lookup"><span data-stu-id="80a0f-246">**VerticalBlankingPixels**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80a0f-247">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="80a0f-247">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="80a0f-248">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="80a0f-248">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="80a0f-249">Número de píxeles en blanco verticalmente.</span><span class="sxs-lookup"><span data-stu-id="80a0f-249">Number of vertically blanking pixels.</span></span>

</dd> <dt>

<span data-ttu-id="80a0f-250">**VerticalBorder**</span><span class="sxs-lookup"><span data-stu-id="80a0f-250">**VerticalBorder**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80a0f-251">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="80a0f-251">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="80a0f-252">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="80a0f-252">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="80a0f-253">Borde vertical.</span><span class="sxs-lookup"><span data-stu-id="80a0f-253">Vertical border.</span></span>

</dd> <dt>

<span data-ttu-id="80a0f-254">**VerticalImageSize**</span><span class="sxs-lookup"><span data-stu-id="80a0f-254">**VerticalImageSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80a0f-255">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="80a0f-255">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="80a0f-256">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="80a0f-256">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="80a0f-257">Tamaño de imagen vertical en milímetros (mm).</span><span class="sxs-lookup"><span data-stu-id="80a0f-257">Vertical image size in millimeters (mm).</span></span>

</dd> <dt>

<span data-ttu-id="80a0f-258">**VerticalPolarityType**</span><span class="sxs-lookup"><span data-stu-id="80a0f-258">**VerticalPolarityType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80a0f-259">Tipo de datos: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="80a0f-259">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="80a0f-260">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="80a0f-260">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="80a0f-261">Tipo de polaridad vertical.</span><span class="sxs-lookup"><span data-stu-id="80a0f-261">Vertical polarity type.</span></span>



| <span data-ttu-id="80a0f-262">Value</span><span class="sxs-lookup"><span data-stu-id="80a0f-262">Value</span></span>                                                                              | <span data-ttu-id="80a0f-263">Significado</span><span class="sxs-lookup"><span data-stu-id="80a0f-263">Meaning</span></span>                                                                   |
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <span data-ttu-id="80a0f-264"><dt>0 (0X0)</dt></span><span class="sxs-lookup"><span data-stu-id="80a0f-264"><dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="80a0f-265">La polaridad vertical es positiva.</span><span class="sxs-lookup"><span data-stu-id="80a0f-265">Vertical polarity is positive.</span></span><br/>                                 |
| <dl> <span data-ttu-id="80a0f-266"><dt>1 (0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="80a0f-266"><dt>1 (0x1)</dt></span></span> </dl> | <span data-ttu-id="80a0f-267">La polaridad vertical es negativa</span><span class="sxs-lookup"><span data-stu-id="80a0f-267">Vertical polarity is negative</span></span><br/>                                  |
| <dl> <span data-ttu-id="80a0f-268"><dt>2 (0X2)</dt></span><span class="sxs-lookup"><span data-stu-id="80a0f-268"><dt>2 (0x2)</dt></span></span> </dl> | <span data-ttu-id="80a0f-269">No es aplicable.</span><span class="sxs-lookup"><span data-stu-id="80a0f-269">Not applicable.</span></span> <span data-ttu-id="80a0f-270">El tipo de sincronización de señales debe ser independiente digital.</span><span class="sxs-lookup"><span data-stu-id="80a0f-270">The signal sync type must be digital separate.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="80a0f-271">**VerticalRefreshRateDenominator**</span><span class="sxs-lookup"><span data-stu-id="80a0f-271">**VerticalRefreshRateDenominator**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80a0f-272">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="80a0f-272">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="80a0f-273">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="80a0f-273">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="80a0f-274">Denominador de frecuencia de actualización vertical.</span><span class="sxs-lookup"><span data-stu-id="80a0f-274">Vertical refresh rate denominator.</span></span>

</dd> <dt>

<span data-ttu-id="80a0f-275">**VerticalRefreshRateNumerator**</span><span class="sxs-lookup"><span data-stu-id="80a0f-275">**VerticalRefreshRateNumerator**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80a0f-276">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="80a0f-276">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="80a0f-277">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="80a0f-277">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="80a0f-278">Numerador de frecuencia de actualización vertical en hercios (Hz).</span><span class="sxs-lookup"><span data-stu-id="80a0f-278">Vertical refresh rate numerator in Hertz (Hz).</span></span>

</dd> <dt>

<span data-ttu-id="80a0f-279">**VerticalSyncOffset**</span><span class="sxs-lookup"><span data-stu-id="80a0f-279">**VerticalSyncOffset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80a0f-280">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="80a0f-280">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="80a0f-281">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="80a0f-281">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="80a0f-282">Desplazamiento de sincronización vertical.</span><span class="sxs-lookup"><span data-stu-id="80a0f-282">Vertical sync offset.</span></span>

</dd> <dt>

<span data-ttu-id="80a0f-283">**VerticalSyncPulseWidth**</span><span class="sxs-lookup"><span data-stu-id="80a0f-283">**VerticalSyncPulseWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80a0f-284">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="80a0f-284">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="80a0f-285">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="80a0f-285">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="80a0f-286">Ancho del pulso de sincronización vertical.</span><span class="sxs-lookup"><span data-stu-id="80a0f-286">Vertical sync pulse width.</span></span>

</dd> <dt>

<span data-ttu-id="80a0f-287">VideoStandardType</span><span class="sxs-lookup"><span data-stu-id="80a0f-287">VideoStandardType</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80a0f-288">Tipo de datos: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="80a0f-288">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="80a0f-289">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="80a0f-289">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="80a0f-290">Tipo de vídeo estándar.</span><span class="sxs-lookup"><span data-stu-id="80a0f-290">Video standard type.</span></span>



| <span data-ttu-id="80a0f-291">Value</span><span class="sxs-lookup"><span data-stu-id="80a0f-291">Value</span></span>                                                                                | <span data-ttu-id="80a0f-292">Significado</span><span class="sxs-lookup"><span data-stu-id="80a0f-292">Meaning</span></span>                                                                                                        |
|--------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="80a0f-293"><dt>0 (0X0)</dt></span><span class="sxs-lookup"><span data-stu-id="80a0f-293"><dt>0 (0x0)</dt></span></span> </dl>   | <span data-ttu-id="80a0f-294">Otros</span><span class="sxs-lookup"><span data-stu-id="80a0f-294">Other</span></span><br/>                                                                                               |
| <dl> <span data-ttu-id="80a0f-295"><dt>1 (0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="80a0f-295"><dt>1 (0x1)</dt></span></span> </dl>   | <span data-ttu-id="80a0f-296">DMT DE VESA.</span><span class="sxs-lookup"><span data-stu-id="80a0f-296">VESA DMT.</span></span> <span data-ttu-id="80a0f-297">En Video Electronics estándar Association (VESA) Mostrar la especificación de temporización de monitores.</span><span class="sxs-lookup"><span data-stu-id="80a0f-297">From Video Electronics Standard Association (VESA) Display Monitor Timings specification.</span></span><br/> |
| <dl> <span data-ttu-id="80a0f-298"><dt>2 (0X2)</dt></span><span class="sxs-lookup"><span data-stu-id="80a0f-298"><dt>2 (0x2)</dt></span></span> </dl>   | <span data-ttu-id="80a0f-299">VESA GTF.</span><span class="sxs-lookup"><span data-stu-id="80a0f-299">VESA GTF.</span></span> <span data-ttu-id="80a0f-300">Del estándar de fórmula de temporización generalizada de VESA.</span><span class="sxs-lookup"><span data-stu-id="80a0f-300">From VESA Generalized Timing Formula standard.</span></span><br/>                                            |
| <dl> <span data-ttu-id="80a0f-301"><dt>3 (0X3)</dt></span><span class="sxs-lookup"><span data-stu-id="80a0f-301"><dt>3 (0x3)</dt></span></span> </dl>   | <span data-ttu-id="80a0f-302">VESA CVT/desde el estándar de intervalos de vídeo coordinado VESA.</span><span class="sxs-lookup"><span data-stu-id="80a0f-302">VESA CVT/ From VESA Coordinated Video Timings standard.</span></span><br/>                                             |
| <dl> <span data-ttu-id="80a0f-303"><dt>4 (0x4)</dt></span><span class="sxs-lookup"><span data-stu-id="80a0f-303"><dt>4 (0x4)</dt></span></span> </dl>   | <span data-ttu-id="80a0f-304">IBM</span><span class="sxs-lookup"><span data-stu-id="80a0f-304">IBM</span></span><br/>                                                                                                 |
| <dl> <span data-ttu-id="80a0f-305"><dt>5 (0X5)</dt></span><span class="sxs-lookup"><span data-stu-id="80a0f-305"><dt>5 (0x5)</dt></span></span> </dl>   | <span data-ttu-id="80a0f-306">MANZANOS</span><span class="sxs-lookup"><span data-stu-id="80a0f-306">APPLE</span></span><br/>                                                                                               |
| <dl> <span data-ttu-id="80a0f-307"><dt>6 (0x6)</dt></span><span class="sxs-lookup"><span data-stu-id="80a0f-307"><dt>6 (0x6)</dt></span></span> </dl>   | <span data-ttu-id="80a0f-308">NTSC M</span><span class="sxs-lookup"><span data-stu-id="80a0f-308">NTSC M</span></span><br/>                                                                                              |
| <dl> <span data-ttu-id="80a0f-309"><dt>7 (0X7)</dt></span><span class="sxs-lookup"><span data-stu-id="80a0f-309"><dt>7 (0x7)</dt></span></span> </dl>   | <span data-ttu-id="80a0f-310">NTSC J</span><span class="sxs-lookup"><span data-stu-id="80a0f-310">NTSC J</span></span><br/>                                                                                              |
| <dl> <span data-ttu-id="80a0f-311"><dt>8 (0x8)</dt></span><span class="sxs-lookup"><span data-stu-id="80a0f-311"><dt>8 (0x8)</dt></span></span> </dl>   | <span data-ttu-id="80a0f-312">NTSC 433</span><span class="sxs-lookup"><span data-stu-id="80a0f-312">NTSC 433</span></span><br/>                                                                                            |
| <dl> <span data-ttu-id="80a0f-313"><dt>9 (0x9)</dt></span><span class="sxs-lookup"><span data-stu-id="80a0f-313"><dt>9 (0x9)</dt></span></span> </dl>   | <span data-ttu-id="80a0f-314">PAL B</span><span class="sxs-lookup"><span data-stu-id="80a0f-314">PAL B</span></span><br/>                                                                                               |
| <dl> <span data-ttu-id="80a0f-315"><dt>10 (0xA)</dt></span><span class="sxs-lookup"><span data-stu-id="80a0f-315"><dt>10 (0xA)</dt></span></span> </dl>  | <span data-ttu-id="80a0f-316">PAL B1</span><span class="sxs-lookup"><span data-stu-id="80a0f-316">PAL B1</span></span><br/>                                                                                              |
| <dl> <span data-ttu-id="80a0f-317"><dt>11 (0xB)</dt></span><span class="sxs-lookup"><span data-stu-id="80a0f-317"><dt>11 (0xB)</dt></span></span> </dl>  | <span data-ttu-id="80a0f-318">PAL G</span><span class="sxs-lookup"><span data-stu-id="80a0f-318">PAL G</span></span><br/>                                                                                               |
| <dl> <span data-ttu-id="80a0f-319"><dt>12 (0xC)</dt></span><span class="sxs-lookup"><span data-stu-id="80a0f-319"><dt>12 (0xC)</dt></span></span> </dl>  | <span data-ttu-id="80a0f-320">PAL H</span><span class="sxs-lookup"><span data-stu-id="80a0f-320">PAL H</span></span><br/>                                                                                               |
| <dl> <span data-ttu-id="80a0f-321"><dt>13 (0xD)</dt></span><span class="sxs-lookup"><span data-stu-id="80a0f-321"><dt>13 (0xD)</dt></span></span> </dl>  | <span data-ttu-id="80a0f-322">PAL I</span><span class="sxs-lookup"><span data-stu-id="80a0f-322">PAL I</span></span><br/>                                                                                               |
| <dl> <span data-ttu-id="80a0f-323"><dt>14 (0xE)</dt></span><span class="sxs-lookup"><span data-stu-id="80a0f-323"><dt>14 (0xE)</dt></span></span> </dl>  | <span data-ttu-id="80a0f-324">PAL D</span><span class="sxs-lookup"><span data-stu-id="80a0f-324">PAL D</span></span><br/>                                                                                               |
| <dl> <span data-ttu-id="80a0f-325"><dt>15 (0xF)</dt></span><span class="sxs-lookup"><span data-stu-id="80a0f-325"><dt>15 (0xF)</dt></span></span> </dl>  | <span data-ttu-id="80a0f-326">PAL N</span><span class="sxs-lookup"><span data-stu-id="80a0f-326">PAL N</span></span><br/>                                                                                               |
| <dl> <span data-ttu-id="80a0f-327"><dt>16 (0x10)</dt></span><span class="sxs-lookup"><span data-stu-id="80a0f-327"><dt>16 (0x10)</dt></span></span> </dl> | <span data-ttu-id="80a0f-328">NC PAL</span><span class="sxs-lookup"><span data-stu-id="80a0f-328">PAL NC</span></span><br/>                                                                                              |
| <dl> <span data-ttu-id="80a0f-329"><dt>17 (0x11)</dt></span><span class="sxs-lookup"><span data-stu-id="80a0f-329"><dt>17 (0x11)</dt></span></span> </dl> | <span data-ttu-id="80a0f-330">SECAM B</span><span class="sxs-lookup"><span data-stu-id="80a0f-330">SECAM B</span></span><br/>                                                                                             |
| <dl> <span data-ttu-id="80a0f-331"><dt>18 (0X12)</dt></span><span class="sxs-lookup"><span data-stu-id="80a0f-331"><dt>18 (0x12)</dt></span></span> </dl> | <span data-ttu-id="80a0f-332">SECAM D</span><span class="sxs-lookup"><span data-stu-id="80a0f-332">SECAM D</span></span><br/>                                                                                             |
| <dl> <span data-ttu-id="80a0f-333"><dt>19 (0x13)</dt></span><span class="sxs-lookup"><span data-stu-id="80a0f-333"><dt>19 (0x13)</dt></span></span> </dl> | <span data-ttu-id="80a0f-334">SECAM G</span><span class="sxs-lookup"><span data-stu-id="80a0f-334">SECAM G</span></span><br/>                                                                                             |
| <dl> <span data-ttu-id="80a0f-335"><dt>20 (0x14)</dt></span><span class="sxs-lookup"><span data-stu-id="80a0f-335"><dt>20 (0x14)</dt></span></span> </dl> | <span data-ttu-id="80a0f-336">SECAM H</span><span class="sxs-lookup"><span data-stu-id="80a0f-336">SECAM H</span></span><br/>                                                                                             |
| <dl> <span data-ttu-id="80a0f-337"><dt>21 (0x15)</dt></span><span class="sxs-lookup"><span data-stu-id="80a0f-337"><dt>21 (0x15)</dt></span></span> </dl> | <span data-ttu-id="80a0f-338">SECAM K</span><span class="sxs-lookup"><span data-stu-id="80a0f-338">SECAM K</span></span><br/>                                                                                             |
| <dl> <span data-ttu-id="80a0f-339"><dt>22 (0x16)</dt></span><span class="sxs-lookup"><span data-stu-id="80a0f-339"><dt>22 (0x16)</dt></span></span> </dl> | <span data-ttu-id="80a0f-340">SECAM K1</span><span class="sxs-lookup"><span data-stu-id="80a0f-340">SECAM K1</span></span><br/>                                                                                            |
| <dl> <span data-ttu-id="80a0f-341"><dt>23 (0x17)</dt></span><span class="sxs-lookup"><span data-stu-id="80a0f-341"><dt>23 (0x17)</dt></span></span> </dl> | <span data-ttu-id="80a0f-342">SECAM L</span><span class="sxs-lookup"><span data-stu-id="80a0f-342">SECAM L</span></span><br/>                                                                                             |
| <dl> <span data-ttu-id="80a0f-343"><dt>24 (0x18)</dt></span><span class="sxs-lookup"><span data-stu-id="80a0f-343"><dt>24 (0x18)</dt></span></span> </dl> | <span data-ttu-id="80a0f-344">SECAM L1</span><span class="sxs-lookup"><span data-stu-id="80a0f-344">SECAM L1</span></span><br/>                                                                                            |
| <dl> <span data-ttu-id="80a0f-345"><dt>25 (0x19)</dt></span><span class="sxs-lookup"><span data-stu-id="80a0f-345"><dt>25 (0x19)</dt></span></span> </dl> | <span data-ttu-id="80a0f-346">EIA861</span><span class="sxs-lookup"><span data-stu-id="80a0f-346">EIA861</span></span><br/>                                                                                              |
| <dl> <span data-ttu-id="80a0f-347"><dt>26 (0x1A)</dt></span><span class="sxs-lookup"><span data-stu-id="80a0f-347"><dt>26 (0x1A)</dt></span></span> </dl> | <span data-ttu-id="80a0f-348">EIA861A</span><span class="sxs-lookup"><span data-stu-id="80a0f-348">EIA861A</span></span><br/>                                                                                             |
| <dl> <span data-ttu-id="80a0f-349"><dt>27 (0x1B)</dt></span><span class="sxs-lookup"><span data-stu-id="80a0f-349"><dt>27 (0x1B)</dt></span></span> </dl> | <span data-ttu-id="80a0f-350">EIA861B</span><span class="sxs-lookup"><span data-stu-id="80a0f-350">EIA861B</span></span><br/>                                                                                             |



 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="80a0f-351">Requisitos</span><span class="sxs-lookup"><span data-stu-id="80a0f-351">Requirements</span></span>



| <span data-ttu-id="80a0f-352">Requisito</span><span class="sxs-lookup"><span data-stu-id="80a0f-352">Requirement</span></span> | <span data-ttu-id="80a0f-353">Value</span><span class="sxs-lookup"><span data-stu-id="80a0f-353">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="80a0f-354">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="80a0f-354">Minimum supported client</span></span><br/> | <span data-ttu-id="80a0f-355">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="80a0f-355">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="80a0f-356">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="80a0f-356">Minimum supported server</span></span><br/> | <span data-ttu-id="80a0f-357">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="80a0f-357">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="80a0f-358">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="80a0f-358">Namespace</span></span><br/>                | <span data-ttu-id="80a0f-359">\\WMI raíz</span><span class="sxs-lookup"><span data-stu-id="80a0f-359">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="80a0f-360">MOF</span><span class="sxs-lookup"><span data-stu-id="80a0f-360">MOF</span></span><br/>                      | <dl> <span data-ttu-id="80a0f-361"><dt>WmiCore. mof</dt></span><span class="sxs-lookup"><span data-stu-id="80a0f-361"><dt>WmiCore.mof</dt></span></span> </dl> |
| <span data-ttu-id="80a0f-362">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="80a0f-362">DLL</span></span><br/>                      | <dl> <span data-ttu-id="80a0f-363"><dt>WmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="80a0f-363"><dt>WmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="80a0f-364">Vea también</span><span class="sxs-lookup"><span data-stu-id="80a0f-364">See also</span></span>

<dl> <dt>

[<span data-ttu-id="80a0f-365">**MSMonitorClass**</span><span class="sxs-lookup"><span data-stu-id="80a0f-365">**MSMonitorClass**</span></span>](msmonitorclass.md)
</dt> </dl>

 

 




