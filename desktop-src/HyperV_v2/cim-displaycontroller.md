---
description: Representa un controlador de pantalla.
ms.assetid: 14598ae6-58e2-46ca-8653-b57e5833a224
title: CIM_DisplayController (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DisplayController
- CIM_DisplayController.Description
- CIM_DisplayController.VideoProcessor
- CIM_DisplayController.VideoMemoryType
- CIM_DisplayController.OtherVideoMemoryType
- CIM_DisplayController.NumberOfVideoPages
- CIM_DisplayController.MaxMemorySupported
- CIM_DisplayController.AcceleratorCapabilities
- CIM_DisplayController.CapabilityDescriptions
- CIM_DisplayController.OtherVideoArchitecture
- CIM_DisplayController.VideoArchitecture
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 59db37a89ce1f57e01a6a9a27fb9c24177221b00
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687037"
---
# <a name="cim_displaycontroller-class"></a><span data-ttu-id="1a1af-103">\_Clase DisplayController de CIM</span><span class="sxs-lookup"><span data-stu-id="1a1af-103">CIM\_DisplayController class</span></span>

<span data-ttu-id="1a1af-104">Representa un controlador de pantalla.</span><span class="sxs-lookup"><span data-stu-id="1a1af-104">Represents a display controller.</span></span>

## <a name="syntax"></a><span data-ttu-id="1a1af-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1a1af-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.25.0"), UMLPackagePath("CIM::Device::Controller"), AMENDMENT]
class CIM_DisplayController : CIM_Controller
{
  string Description;
  string VideoProcessor;
  uint16 VideoMemoryType;
  string OtherVideoMemoryType;
  uint32 NumberOfVideoPages;
  uint32 MaxMemorySupported;
  uint16 AcceleratorCapabilities[];
  string CapabilityDescriptions[];
  string OtherVideoArchitecture;
  uint16 VideoArchitecture;
};
```

## <a name="members"></a><span data-ttu-id="1a1af-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="1a1af-106">Members</span></span>

<span data-ttu-id="1a1af-107">La clase **CIM \_ DisplayController** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="1a1af-107">The **CIM\_DisplayController** class has these types of members:</span></span>

-   [<span data-ttu-id="1a1af-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="1a1af-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1a1af-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="1a1af-109">Properties</span></span>

<span data-ttu-id="1a1af-110">La clase **CIM \_ DisplayController** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="1a1af-110">The **CIM\_DisplayController** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1a1af-111">**AcceleratorCapabilities**</span><span class="sxs-lookup"><span data-stu-id="1a1af-111">**AcceleratorCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a1af-112">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1a1af-112">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="1a1af-113">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1a1af-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1a1af-114">Calificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ DisplayController**.**CapabilityDescriptions**")</span><span class="sxs-lookup"><span data-stu-id="1a1af-114">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_DisplayController**.**CapabilityDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="1a1af-115">Las capacidades de gráficos y 3D del controlador de pantalla.</span><span class="sxs-lookup"><span data-stu-id="1a1af-115">The graphics and 3D capabilities of the display controller.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="1a1af-116">**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="1a1af-116">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="1a1af-117">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="1a1af-117">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Graphics_Accelerator"></span><span id="graphics_accelerator"></span><span id="GRAPHICS_ACCELERATOR"></span>

<span data-ttu-id="1a1af-118">**Acelerador de gráficos** (2)</span><span class="sxs-lookup"><span data-stu-id="1a1af-118">**Graphics Accelerator** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="3D_Accelerator"></span><span id="3d_accelerator"></span><span id="3D_ACCELERATOR"></span>

<span data-ttu-id="1a1af-119">**acelerador 3D** (3)</span><span class="sxs-lookup"><span data-stu-id="1a1af-119">**3D Accelerator** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="PCI_Fast_Write"></span><span id="pci_fast_write"></span><span id="PCI_FAST_WRITE"></span>

<span data-ttu-id="1a1af-120">**Escritura rápida de PCI** (4)</span><span class="sxs-lookup"><span data-stu-id="1a1af-120">**PCI Fast Write** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="MultiMonitor_Support"></span><span id="multimonitor_support"></span><span id="MULTIMONITOR_SUPPORT"></span>

<span data-ttu-id="1a1af-121">**Compatibilidad con multimonitor** (5)</span><span class="sxs-lookup"><span data-stu-id="1a1af-121">**MultiMonitor Support** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="PCI_Mastering"></span><span id="pci_mastering"></span><span id="PCI_MASTERING"></span>

<span data-ttu-id="1a1af-122">**Maestro de PCI** (6)</span><span class="sxs-lookup"><span data-stu-id="1a1af-122">**PCI Mastering** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Second_Monochrome_Adapter_Support"></span><span id="second_monochrome_adapter_support"></span><span id="SECOND_MONOCHROME_ADAPTER_SUPPORT"></span>

<span data-ttu-id="1a1af-123">**Segunda compatibilidad con adaptador monocromo** (7)</span><span class="sxs-lookup"><span data-stu-id="1a1af-123">**Second Monochrome Adapter Support** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Large_Memory_Address_Support"></span><span id="large_memory_address_support"></span><span id="LARGE_MEMORY_ADDRESS_SUPPORT"></span>

<span data-ttu-id="1a1af-124">**Compatibilidad con direcciones de memoria de gran tamaño** (8)</span><span class="sxs-lookup"><span data-stu-id="1a1af-124">**Large Memory Address Support** (8)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="1a1af-125">**CapabilityDescriptions**</span><span class="sxs-lookup"><span data-stu-id="1a1af-125">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a1af-126">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="1a1af-126">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="1a1af-127">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1a1af-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1a1af-128">Calificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ DisplayController**.**AcceleratorCapabilities**")</span><span class="sxs-lookup"><span data-stu-id="1a1af-128">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_DisplayController**.**AcceleratorCapabilities**")</span></span>
</dt> </dl>

<span data-ttu-id="1a1af-129">Explicaciones detalladas de las características de acelerador de vídeo de la matriz **AcceleratorCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="1a1af-129">Detailed explanations for video accelerator features of the **AcceleratorCapabilities** array.</span></span> <span data-ttu-id="1a1af-130">Los elementos de esta matriz se corresponden con los elementos de la matriz de **AcceleratorCapabilities**.</span><span class="sxs-lookup"><span data-stu-id="1a1af-130">The items in this array correspond to the array items in **AcceleratorCapabilities**.</span></span>

</dd> <dt>

<span data-ttu-id="1a1af-131">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="1a1af-131">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a1af-132">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="1a1af-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1a1af-133">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1a1af-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1a1af-134">Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Vídeo DMTF \| 004,18 ")</span><span class="sxs-lookup"><span data-stu-id="1a1af-134">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|004.18")</span></span>
</dt> </dl>

<span data-ttu-id="1a1af-135">Una descripción de texto del objeto.</span><span class="sxs-lookup"><span data-stu-id="1a1af-135">A text description of the object.</span></span>

</dd> <dt>

<span data-ttu-id="1a1af-136">**MaxMemorySupported**</span><span class="sxs-lookup"><span data-stu-id="1a1af-136">**MaxMemorySupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a1af-137">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1a1af-137">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1a1af-138">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1a1af-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1a1af-139">Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes"), **punitivo** ("byte")</span><span class="sxs-lookup"><span data-stu-id="1a1af-139">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bytes"), **PUnit** ("byte")</span></span>
</dt> </dl>

<span data-ttu-id="1a1af-140">Cantidad máxima de memoria admitida, en bytes.</span><span class="sxs-lookup"><span data-stu-id="1a1af-140">The maximum amount of memory supported, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="1a1af-141">**NumberOfVideoPages**</span><span class="sxs-lookup"><span data-stu-id="1a1af-141">**NumberOfVideoPages**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a1af-142">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1a1af-142">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1a1af-143">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1a1af-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1a1af-144">El número de páginas de vídeo admitidas dadas las resoluciones actuales y la memoria disponible.</span><span class="sxs-lookup"><span data-stu-id="1a1af-144">The number of video pages supported given the current resolutions and available memory.</span></span>

</dd> <dt>

<span data-ttu-id="1a1af-145">**OtherVideoArchitecture**</span><span class="sxs-lookup"><span data-stu-id="1a1af-145">**OtherVideoArchitecture**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a1af-146">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="1a1af-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1a1af-147">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1a1af-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1a1af-148">Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ DisplayController**.**Videoarquitectura**")</span><span class="sxs-lookup"><span data-stu-id="1a1af-148">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_DisplayController**.**VideoArchitecture**")</span></span>
</dt> </dl>

<span data-ttu-id="1a1af-149">Una descripción del tipo de arquitectura de vídeo cuando la propiedad **videoarchitecture** contiene "1" (otro).</span><span class="sxs-lookup"><span data-stu-id="1a1af-149">A description of the video architecture type when the **VideoArchitecture** property contains "1" (Other).</span></span>

</dd> <dt>

<span data-ttu-id="1a1af-150">**OtherVideoMemoryType**</span><span class="sxs-lookup"><span data-stu-id="1a1af-150">**OtherVideoMemoryType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a1af-151">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="1a1af-151">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1a1af-152">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1a1af-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1a1af-153">Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ DisplayController**.**VideoMemoryType**")</span><span class="sxs-lookup"><span data-stu-id="1a1af-153">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_DisplayController**.**VideoMemoryType**")</span></span>
</dt> </dl>

<span data-ttu-id="1a1af-154">El tipo de memoria de vídeo cuando la propiedad **VideoMemoryType** es "1" (otra).</span><span class="sxs-lookup"><span data-stu-id="1a1af-154">The video memory type when the **VideoMemoryType** property is "1" (Other).</span></span>

</dd> <dt>

<span data-ttu-id="1a1af-155">**Videoarquitectura**</span><span class="sxs-lookup"><span data-stu-id="1a1af-155">**VideoArchitecture**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a1af-156">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1a1af-156">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1a1af-157">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1a1af-157">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1a1af-158">La arquitectura de vídeo controladores de pantalla utilizada para generar la señal de vídeo.</span><span class="sxs-lookup"><span data-stu-id="1a1af-158">The display controllers video architecture used to generate the video signal.</span></span> <span data-ttu-id="1a1af-159">Normalmente, un procesador de vídeo dedicado genera la señal de vídeo de acuerdo con la arquitectura especificada.</span><span class="sxs-lookup"><span data-stu-id="1a1af-159">Usually, a dedicated video processor generates the video signal in accordance with the specified architecture.</span></span> <span data-ttu-id="1a1af-160">La arquitectura indica la capacidad máxima de resolución del controlador de pantalla.</span><span class="sxs-lookup"><span data-stu-id="1a1af-160">The architecture indicates of the maximum resolution capability of the display controller.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="1a1af-161">**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="1a1af-161">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="1a1af-162">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="1a1af-162">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="CGA"></span><span id="cga"></span>

<span data-ttu-id="1a1af-163">**CGA** (2)</span><span class="sxs-lookup"><span data-stu-id="1a1af-163">**CGA** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="EGA"></span><span id="ega"></span>

<span data-ttu-id="1a1af-164">**EGA** (3)</span><span class="sxs-lookup"><span data-stu-id="1a1af-164">**EGA** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="VGA"></span><span id="vga"></span>

<span data-ttu-id="1a1af-165">**VGA** (4)</span><span class="sxs-lookup"><span data-stu-id="1a1af-165">**VGA** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="SVGA"></span><span id="svga"></span>

<span data-ttu-id="1a1af-166">**SVGA** (5)</span><span class="sxs-lookup"><span data-stu-id="1a1af-166">**SVGA** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="MDA"></span><span id="mda"></span>

<span data-ttu-id="1a1af-167">**MDA** (6)</span><span class="sxs-lookup"><span data-stu-id="1a1af-167">**MDA** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="HGC"></span><span id="hgc"></span>

<span data-ttu-id="1a1af-168">**HGC** (7)</span><span class="sxs-lookup"><span data-stu-id="1a1af-168">**HGC** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="MCGA"></span><span id="mcga"></span>

<span data-ttu-id="1a1af-169">**MCGA** (8)</span><span class="sxs-lookup"><span data-stu-id="1a1af-169">**MCGA** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="8514A"></span><span id="8514a"></span>

<span data-ttu-id="1a1af-170">**8514A** (9)</span><span class="sxs-lookup"><span data-stu-id="1a1af-170">**8514A** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="XGA"></span><span id="xga"></span>

<span data-ttu-id="1a1af-171">**XGA** (10)</span><span class="sxs-lookup"><span data-stu-id="1a1af-171">**XGA** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Linear_Frame_Buffer"></span><span id="linear_frame_buffer"></span><span id="LINEAR_FRAME_BUFFER"></span>

<span data-ttu-id="1a1af-172">**Búfer de trama lineal** (11)</span><span class="sxs-lookup"><span data-stu-id="1a1af-172">**Linear Frame Buffer** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="PC-98"></span><span id="pc-98"></span>

<span data-ttu-id="1a1af-173">**PC-98** (160)</span><span class="sxs-lookup"><span data-stu-id="1a1af-173">**PC-98** (160)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="1a1af-174">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="1a1af-174">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="1a1af-175">**Proveedor reservado** (0x8000...)</span><span class="sxs-lookup"><span data-stu-id="1a1af-175">**Vendor Reserved** (0x8000..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="1a1af-176">**VideoMemoryType**</span><span class="sxs-lookup"><span data-stu-id="1a1af-176">**VideoMemoryType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a1af-177">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1a1af-177">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1a1af-178">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1a1af-178">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1a1af-179">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Vídeo DMTF \| 004,6 "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ DisplayController**.**OtherVideoMemoryType**")</span><span class="sxs-lookup"><span data-stu-id="1a1af-179">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Video\|004.6"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_DisplayController**.**OtherVideoMemoryType**")</span></span>
</dt> </dl>

<span data-ttu-id="1a1af-180">El tipo de memoria de vídeo.</span><span class="sxs-lookup"><span data-stu-id="1a1af-180">The type of video memory.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="1a1af-181">**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="1a1af-181">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="1a1af-182">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="1a1af-182">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="VRAM"></span><span id="vram"></span>

<span data-ttu-id="1a1af-183">**VRAM** (2)</span><span class="sxs-lookup"><span data-stu-id="1a1af-183">**VRAM** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="DRAM"></span><span id="dram"></span>

<span data-ttu-id="1a1af-184">**DRAM** (3)</span><span class="sxs-lookup"><span data-stu-id="1a1af-184">**DRAM** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="SRAM"></span><span id="sram"></span>

<span data-ttu-id="1a1af-185">**SRAM** (4)</span><span class="sxs-lookup"><span data-stu-id="1a1af-185">**SRAM** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="WRAM"></span><span id="wram"></span>

<span data-ttu-id="1a1af-186">**WRAM** (5)</span><span class="sxs-lookup"><span data-stu-id="1a1af-186">**WRAM** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="EDO_RAM"></span><span id="edo_ram"></span>

<span data-ttu-id="1a1af-187">**Edo RAM** (6)</span><span class="sxs-lookup"><span data-stu-id="1a1af-187">**EDO RAM** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Burst_Synchronous_DRAM"></span><span id="burst_synchronous_dram"></span><span id="BURST_SYNCHRONOUS_DRAM"></span>

<span data-ttu-id="1a1af-188">**DRAM sincrónica de ráfaga** (7)</span><span class="sxs-lookup"><span data-stu-id="1a1af-188">**Burst Synchronous DRAM** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Pipelined_Burst_SRAM"></span><span id="pipelined_burst_sram"></span><span id="PIPELINED_BURST_SRAM"></span>

<span data-ttu-id="1a1af-189">**SRAM de ráfaga canalizada** (8)</span><span class="sxs-lookup"><span data-stu-id="1a1af-189">**Pipelined Burst SRAM** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="CDRAM"></span><span id="cdram"></span>

<span data-ttu-id="1a1af-190">**CDRAM** (9)</span><span class="sxs-lookup"><span data-stu-id="1a1af-190">**CDRAM** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="3DRAM"></span><span id="3dram"></span>

<span data-ttu-id="1a1af-191">**3DRAM** (10)</span><span class="sxs-lookup"><span data-stu-id="1a1af-191">**3DRAM** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="SDRAM"></span><span id="sdram"></span>

<span data-ttu-id="1a1af-192">**SDRAM** (11)</span><span class="sxs-lookup"><span data-stu-id="1a1af-192">**SDRAM** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="SGRAM"></span><span id="sgram"></span>

<span data-ttu-id="1a1af-193">**SGRAM** (12)</span><span class="sxs-lookup"><span data-stu-id="1a1af-193">**SGRAM** (12)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="1a1af-194">**Videoprocesador**</span><span class="sxs-lookup"><span data-stu-id="1a1af-194">**VideoProcessor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a1af-195">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="1a1af-195">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1a1af-196">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1a1af-196">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1a1af-197">Una descripción de texto del controlador/procesador de vídeo.</span><span class="sxs-lookup"><span data-stu-id="1a1af-197">A text description of the video processor/controller.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1a1af-198">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1a1af-198">Requirements</span></span>



| <span data-ttu-id="1a1af-199">Requisito</span><span class="sxs-lookup"><span data-stu-id="1a1af-199">Requirement</span></span> | <span data-ttu-id="1a1af-200">Value</span><span class="sxs-lookup"><span data-stu-id="1a1af-200">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1a1af-201">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1a1af-201">Minimum supported client</span></span><br/> | <span data-ttu-id="1a1af-202">Windows 8</span><span class="sxs-lookup"><span data-stu-id="1a1af-202">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="1a1af-203">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1a1af-203">Minimum supported server</span></span><br/> | <span data-ttu-id="1a1af-204">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="1a1af-204">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="1a1af-205">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="1a1af-205">Namespace</span></span><br/>                | <span data-ttu-id="1a1af-206">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="1a1af-206">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="1a1af-207">MOF</span><span class="sxs-lookup"><span data-stu-id="1a1af-207">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1a1af-208"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1a1af-208"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="1a1af-209">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="1a1af-209">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1a1af-210"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="1a1af-210"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="1a1af-211">Vea también</span><span class="sxs-lookup"><span data-stu-id="1a1af-211">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1a1af-212">**\_Controlador CIM**</span><span class="sxs-lookup"><span data-stu-id="1a1af-212">**CIM\_Controller**</span></span>](cim-controller.md)
</dt> </dl>

 

