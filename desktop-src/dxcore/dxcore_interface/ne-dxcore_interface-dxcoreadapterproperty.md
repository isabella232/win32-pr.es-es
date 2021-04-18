---
title: 'DXCoreAdapterProperty '
description: Define constantes que especifican las propiedades del adaptador de DXCore.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 645f0a890aac9a50cdf2987c0736a85142a91aff
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105720153"
---
# <a name="dxcoreadapterproperty-enum"></a><span data-ttu-id="bf279-103">Enumeración DXCoreAdapterProperty</span><span class="sxs-lookup"><span data-stu-id="bf279-103">DXCoreAdapterProperty enum</span></span>

<span data-ttu-id="bf279-104">Define constantes que especifican las propiedades del adaptador de DXCore.</span><span class="sxs-lookup"><span data-stu-id="bf279-104">Defines constants that specify DXCore adapter properties.</span></span> <span data-ttu-id="bf279-105">Pase una de estas constantes al método [IDXCoreAdapter:: GetPropertySize](./nf-dxcore_interface-idxcoreadapter-getpropertysize.md) para recuperar el tamaño del búfer necesario para recibir el valor de la propiedad correspondiente. a continuación, pase la misma constante al método [IDXCoreAdapter:: GetProperty](./nf-dxcore_interface-idxcoreadapter-getproperty.md) para recuperar el valor de la propiedad en un búfer que asigne.</span><span class="sxs-lookup"><span data-stu-id="bf279-105">Pass one of these constants to the [IDXCoreAdapter::GetPropertySize](./nf-dxcore_interface-idxcoreadapter-getpropertysize.md) method to retrieve the buffer size necessary to receive the value of the corresponding property; then pass the same constant to the [IDXCoreAdapter::GetProperty](./nf-dxcore_interface-idxcoreadapter-getproperty.md) method to retrieve the property's value in a buffer that you allocate.</span></span>

## <a name="syntax"></a><span data-ttu-id="bf279-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bf279-106">Syntax</span></span>

```cpp
enum class DXCoreAdapterProperty : uint32_t
{
  InstanceLuid = 0,
  DriverVersion = 1,
  DriverDescription = 2,
  HardwareID = 3,
  KmdModelVersion = 4,
  ComputePreemptionGranularity = 5,
  GraphicsPreemptionGranularity = 6,
  DedicatedAdapterMemory = 7,
  DedicatedSystemMemory = 8,
  SharedSystemMemory = 9,
  AcgCompatible = 10,
  IsHardware = 11,
  IsIntegrated = 12,
  IsDetachable = 13
};
```

## <a name="constants"></a><span data-ttu-id="bf279-107">Constantes</span><span class="sxs-lookup"><span data-stu-id="bf279-107">Constants</span></span>

### <a name="instanceluid"></a><span data-ttu-id="bf279-108">InstanceLuid</span><span class="sxs-lookup"><span data-stu-id="bf279-108">InstanceLuid</span></span>

<span data-ttu-id="bf279-109">Especifica la propiedad del adaptador <em>InstanceLuid</em> , que contiene un identificador único local que representa el adaptador.</span><span class="sxs-lookup"><span data-stu-id="bf279-109">Specifies the <em>InstanceLuid</em> adapter property, which contains a locally unique identifier representing the adapter.</span></span> <span data-ttu-id="bf279-110">Este valor permanece constante mientras dure este adaptador.</span><span class="sxs-lookup"><span data-stu-id="bf279-110">This value remains constant for the lifetime of this adapter.</span></span> <span data-ttu-id="bf279-111">El LUID de un adaptador cambia al reiniciarse, actualizar controladores o deshabilitación o habilitación del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="bf279-111">The LUID of an adapter changes on reboot, driver upgrade, or device disablement/enablement.</span></span>

<span data-ttu-id="bf279-112">La propiedad del adaptador <em>InstanceLuid</em> tiene el tipo <a href="/windows/win32/api/winnt/ns-winnt-luid">LUID</a>.</span><span class="sxs-lookup"><span data-stu-id="bf279-112">The <em>InstanceLuid</em> adapter property has type <a href="/windows/win32/api/winnt/ns-winnt-luid">LUID</a>.</span></span>

### <a name="driverversion"></a><span data-ttu-id="bf279-113">DriverVersion</span><span class="sxs-lookup"><span data-stu-id="bf279-113">DriverVersion</span></span>

<span data-ttu-id="bf279-114">Especifica la propiedad del adaptador de <em>DriverVersion</em> , que contiene la versión del controlador, representada en <b>WORD</b>s como <b>LARGE_INTEGER</b>.</span><span class="sxs-lookup"><span data-stu-id="bf279-114">Specifies the <em>DriverVersion</em> adapter property, which contains the driver version, represented in <b>WORD</b>s as a <b>LARGE_INTEGER</b>.</span></span>

<span data-ttu-id="bf279-115">La propiedad del adaptador <em>DriverVersion</em> tiene el tipo <b>uint64_t</b>, que representa un valor booleano.</span><span class="sxs-lookup"><span data-stu-id="bf279-115">The <em>DriverVersion</em> adapter property has type <b>uint64_t</b>, representing a Boolean value.</span></span>

### <a name="driverdescription"></a><span data-ttu-id="bf279-116">DriverDescription</span><span class="sxs-lookup"><span data-stu-id="bf279-116">DriverDescription</span></span>

<span data-ttu-id="bf279-117">Especifica la propiedad del adaptador <em>DriverDescription</em> , que contiene una matriz terminada en NULL de <b>Char</b>s que describe el controlador, tal y como lo especifica el controlador, en codificación <a href="/windows/win32/intl/unicode">UTF-8</a> .</span><span class="sxs-lookup"><span data-stu-id="bf279-117">Specifies the <em>DriverDescription</em> adapter property, which contains a NULL-terminated array of <b>CHAR</b>s describing the driver, as specified by the driver, in <a href="/windows/win32/intl/unicode">UTF-8</a> encoding.</span></span>

<span data-ttu-id="bf279-118">La propiedad del adaptador <em>DriverDescription</em> tiene el tipo <b>Char \*</b>.</span><span class="sxs-lookup"><span data-stu-id="bf279-118">The <em>DriverDescription</em> adapter property has type <b>char\*</b>.</span></span>

### <a name="hardwareid"></a><span data-ttu-id="bf279-119">HardwareID</span><span class="sxs-lookup"><span data-stu-id="bf279-119">HardwareID</span></span>

<span data-ttu-id="bf279-120">Especifica la propiedad del adaptador de <em>HardwareID</em> , que representa las partes del identificador de hardware de PNP.</span><span class="sxs-lookup"><span data-stu-id="bf279-120">Specifies the <em>HardwareID</em> adapter property, which represents the PnP hardware ID parts.</span></span>

<span data-ttu-id="bf279-121">La propiedad del adaptador <em>HardwareID</em> tiene el tipo <a href="/windows/win32/dxcore/dxcore_interface/ns-dxcore_interface-dxcorehardwareid">DXCoreHardwareID</a>.</span><span class="sxs-lookup"><span data-stu-id="bf279-121">The <em>HardwareID</em> adapter property has type <a href="/windows/win32/dxcore/dxcore_interface/ns-dxcore_interface-dxcorehardwareid">DXCoreHardwareID</a>.</span></span>

### <a name="kmdmodelversion"></a><span data-ttu-id="bf279-122">KmdModelVersion</span><span class="sxs-lookup"><span data-stu-id="bf279-122">KmdModelVersion</span></span>

<span data-ttu-id="bf279-123">Especifica la propiedad de adaptador <em>KmdModelVersion</em> , que representa el modelo de controlador.</span><span class="sxs-lookup"><span data-stu-id="bf279-123">Specifies the <em>KmdModelVersion</em> adapter property, which represents the driver model.</span></span>

<span data-ttu-id="bf279-124">La propiedad del adaptador <em>KmdModelVersion</em> tiene el tipo <a href="/windows-hardware/drivers/ddi/content/d3dkmthk/ne-d3dkmthk-_qai_driverversion">D3DKMT_DRIVERVERSION</a>.</span><span class="sxs-lookup"><span data-stu-id="bf279-124">The <em>KmdModelVersion</em> adapter property has type <a href="/windows-hardware/drivers/ddi/content/d3dkmthk/ne-d3dkmthk-_qai_driverversion">D3DKMT_DRIVERVERSION</a>.</span></span>

### <a name="computepreemptiongranularity"></a><span data-ttu-id="bf279-125">ComputePreemptionGranularity</span><span class="sxs-lookup"><span data-stu-id="bf279-125">ComputePreemptionGranularity</span></span>

<span data-ttu-id="bf279-126">Especifica la propiedad del adaptador de <em>ComputePreemptionGranularity</em> , que representa la granularidad de prevacía de proceso.</span><span class="sxs-lookup"><span data-stu-id="bf279-126">Specifies the <em>ComputePreemptionGranularity</em> adapter property, which represents the compute preemption granularity.</span></span>

<span data-ttu-id="bf279-127">La propiedad del adaptador <em>ComputePreemptionGranularity</em> tiene el tipo <b>uint16_t</b>, que representa un valor <a href="/windows-hardware/drivers/ddi/content/d3dkmdt/ne-d3dkmdt-_d3dkmdt_compute_preemption_granularity">D3DKMDT_COMPUTE_PREEMPTION_GRANULARITY</a> .</span><span class="sxs-lookup"><span data-stu-id="bf279-127">The <em>ComputePreemptionGranularity</em> adapter property has type <b>uint16_t</b>, representing a <a href="/windows-hardware/drivers/ddi/content/d3dkmdt/ne-d3dkmdt-_d3dkmdt_compute_preemption_granularity">D3DKMDT_COMPUTE_PREEMPTION_GRANULARITY</a> value.</span></span>

### <a name="graphicspreemptiongranularity"></a><span data-ttu-id="bf279-128">GraphicsPreemptionGranularity</span><span class="sxs-lookup"><span data-stu-id="bf279-128">GraphicsPreemptionGranularity</span></span>

<span data-ttu-id="bf279-129">Especifica la propiedad del adaptador de <em>GraphicsPreemptionGranularity</em> , que representa la granularidad del prevacío de los gráficos.</span><span class="sxs-lookup"><span data-stu-id="bf279-129">Specifies the <em>GraphicsPreemptionGranularity</em> adapter property, which represents the graphics preemption granularity.</span></span>

<span data-ttu-id="bf279-130">La propiedad del adaptador <em>GraphicsPreemptionGranularity</em> tiene el tipo <b>uint16_t</b>, que representa un valor <a href="/windows-hardware/drivers/ddi/content/d3dkmdt/ne-d3dkmdt-_d3dkmdt_graphics_preemption_granularity">D3DKMDT_GRAPHICS_PREEMPTION_GRANULARITY</a> .</span><span class="sxs-lookup"><span data-stu-id="bf279-130">The <em>GraphicsPreemptionGranularity</em> adapter property has type <b>uint16_t</b>, representing a <a href="/windows-hardware/drivers/ddi/content/d3dkmdt/ne-d3dkmdt-_d3dkmdt_graphics_preemption_granularity">D3DKMDT_GRAPHICS_PREEMPTION_GRANULARITY</a> value.</span></span>

### <a name="dedicatedadaptermemory"></a><span data-ttu-id="bf279-131">DedicatedAdapterMemory</span><span class="sxs-lookup"><span data-stu-id="bf279-131">DedicatedAdapterMemory</span></span>

<span data-ttu-id="bf279-132">Especifica la propiedad de adaptador <em>DedicatedAdapterMemory</em> , que representa el número de bytes de memoria de adaptador dedicada que no se comparten con la CPU.</span><span class="sxs-lookup"><span data-stu-id="bf279-132">Specifies the <em>DedicatedAdapterMemory</em> adapter property, which represents the number of bytes of dedicated adapter memory that are not shared with the CPU.</span></span>

<span data-ttu-id="bf279-133">La propiedad del adaptador <em>DedicatedVideoMemory</em> tiene el tipo <b>uint64_t</b>.</span><span class="sxs-lookup"><span data-stu-id="bf279-133">The <em>DedicatedVideoMemory</em> adapter property has type <b>uint64_t</b>.</span></span>

### <a name="dedicatedsystemmemory"></a><span data-ttu-id="bf279-134">DedicatedSystemMemory</span><span class="sxs-lookup"><span data-stu-id="bf279-134">DedicatedSystemMemory</span></span>

<span data-ttu-id="bf279-135">Especifica la propiedad del adaptador <em>DedicatedSystemMemory</em> , que representa el número de bytes de la memoria del sistema dedicada que no se comparten con la CPU.</span><span class="sxs-lookup"><span data-stu-id="bf279-135">Specifies the <em>DedicatedSystemMemory</em> adapter property, which represents the number of bytes of dedicated system memory that are not shared with the CPU.</span></span> <span data-ttu-id="bf279-136">Esta memoria se asigna desde la memoria disponible del sistema durante el arranque.</span><span class="sxs-lookup"><span data-stu-id="bf279-136">This memory is allocated from available system memory at boot time.</span></span>

<span data-ttu-id="bf279-137">La propiedad del adaptador <em>DedicatedSystemMemory</em> tiene el tipo <b>uint64_t</b>.</span><span class="sxs-lookup"><span data-stu-id="bf279-137">The <em>DedicatedSystemMemory</em> adapter property has type <b>uint64_t</b>.</span></span>

### <a name="sharedsystemmemory"></a><span data-ttu-id="bf279-138">SharedSystemMemory</span><span class="sxs-lookup"><span data-stu-id="bf279-138">SharedSystemMemory</span></span>

<span data-ttu-id="bf279-139">Especifica la propiedad del adaptador <em>SharedSystemMemory</em> , que representa el número de bytes de la memoria compartida del sistema.</span><span class="sxs-lookup"><span data-stu-id="bf279-139">Specifies the <em>SharedSystemMemory</em> adapter property, which represents the number of bytes of shared system memory.</span></span> <span data-ttu-id="bf279-140">Este es el valor máximo de la memoria del sistema que puede consumir el adaptador durante la operación.</span><span class="sxs-lookup"><span data-stu-id="bf279-140">This is the maximum value of system memory that may be consumed by the adapter during operation.</span></span> <span data-ttu-id="bf279-141">Cualquier memoria incidental consumida por el controlador a medida que administra y usa la memoria de vídeo es adicional.</span><span class="sxs-lookup"><span data-stu-id="bf279-141">Any incidental memory consumed by the driver as it manages and uses video memory is additional.</span></span>

<span data-ttu-id="bf279-142">La propiedad del adaptador <em>SharedSystemMemory</em> tiene el tipo <b>uint64_t</b>.</span><span class="sxs-lookup"><span data-stu-id="bf279-142">The <em>SharedSystemMemory</em> adapter property has type <b>uint64_t</b>.</span></span>

### <a name="acgcompatible"></a><span data-ttu-id="bf279-143">AcgCompatible</span><span class="sxs-lookup"><span data-stu-id="bf279-143">AcgCompatible</span></span>

<span data-ttu-id="bf279-144">Especifica la propiedad del adaptador <em>AcgCompatible</em> , que indica si el adaptador es compatible con los procesos que aplican la protección de código arbitraria.</span><span class="sxs-lookup"><span data-stu-id="bf279-144">Specifies the <em>AcgCompatible</em> adapter property, which indicates whether the adapter is compatible with processes that enforce Arbitrary Code Guard.</span></span>

<span data-ttu-id="bf279-145">La propiedad del adaptador <em>AcgCompatible</em> tiene el tipo <b>bool</b>.</span><span class="sxs-lookup"><span data-stu-id="bf279-145">The <em>AcgCompatible</em> adapter property has type <b>bool</b>.</span></span>

### <a name="ishardware"></a><span data-ttu-id="bf279-146">IsHardware</span><span class="sxs-lookup"><span data-stu-id="bf279-146">IsHardware</span></span>

<span data-ttu-id="bf279-147">Especifica la propiedad del adaptador <em>IsHardware</em> , que determina si se trata de un adaptador de hardware.</span><span class="sxs-lookup"><span data-stu-id="bf279-147">Specifies the <em>IsHardware</em> adapter property, which determines whether or not this is a hardware adapter.</span></span> <span data-ttu-id="bf279-148">Un adaptador que no es un adaptador de hardware es un adaptador de software.</span><span class="sxs-lookup"><span data-stu-id="bf279-148">An adapter that's not a hardware adapter is a software adapter.</span></span>

<span data-ttu-id="bf279-149">La propiedad del adaptador <em>IsHardware</em> tiene el tipo <b>bool</b>.</span><span class="sxs-lookup"><span data-stu-id="bf279-149">The <em>IsHardware</em> adapter property has type <b>bool</b>.</span></span>

### <a name="isintegrated"></a><span data-ttu-id="bf279-150">IsIntegrated</span><span class="sxs-lookup"><span data-stu-id="bf279-150">IsIntegrated</span></span>

<span data-ttu-id="bf279-151">Especifica la propiedad del adaptador de <em>IsIntegrated</em> , que determina si se ha detectado que el adaptador es un procesador de gráficos integrado (iGPU).</span><span class="sxs-lookup"><span data-stu-id="bf279-151">Specifies the <em>IsIntegrated</em> adapter property, which determines whether the adapter is reported to be an integrated graphics processor (iGPU).</span></span>

<span data-ttu-id="bf279-152">La propiedad del adaptador <em>IsIntegrated</em> tiene el tipo <b>bool</b>.</span><span class="sxs-lookup"><span data-stu-id="bf279-152">The <em>IsIntegrated</em> adapter property has type <b>bool</b>.</span></span>

### <a name="isdetachable"></a><span data-ttu-id="bf279-153">IsDetachable</span><span class="sxs-lookup"><span data-stu-id="bf279-153">IsDetachable</span></span>

<span data-ttu-id="bf279-154">Especifica la propiedad del adaptador de <em>IsDetachable</em> , que determina si el adaptador se ha comunicado para ser desasociable o extraíble.</span><span class="sxs-lookup"><span data-stu-id="bf279-154">Specifies the <em>IsDetachable</em> adapter property, which determines whether the adapter has been reported to be detachable, or removable.</span></span>

<span data-ttu-id="bf279-155">La propiedad del adaptador <em>IsDetachable</em> tiene el tipo <b>bool</b>.</span><span class="sxs-lookup"><span data-stu-id="bf279-155">The <em>IsDetachable</em> adapter property has type <b>bool</b>.</span></span>

<span data-ttu-id="bf279-156"><b>Nota</b>:</span><span class="sxs-lookup"><span data-stu-id="bf279-156"><b>Note</b>.</span></span> <span data-ttu-id="bf279-157">Incluso si <a href="/windows/win32/dxcore/dxcore_interface/nf-dxcore_interface-idxcoreadapter-getproperty">IDXCoreAdapter:: GetProperty</a> indica `false` para esta propiedad, el adaptador todavía tiene la posibilidad de que se le notifique como quitado, como en caso de error de funcionamiento o actualización del controlador.</span><span class="sxs-lookup"><span data-stu-id="bf279-157">Even if <a href="/windows/win32/dxcore/dxcore_interface/nf-dxcore_interface-idxcoreadapter-getproperty">IDXCoreAdapter::GetProperty</a> indicates `false` for this property, the adapter still has the ability to be reported as removed, such as in the case of malfunction, or driver update.</span></span>

## <a name="see-also"></a><span data-ttu-id="bf279-158">Vea también</span><span class="sxs-lookup"><span data-stu-id="bf279-158">See also</span></span>

<span data-ttu-id="bf279-159">[IDXCoreAdapter:: GetPropertySize](./nf-dxcore_interface-idxcoreadapter-getpropertysize.md), [IDXCoreAdapter:: GetProperty](./nf-dxcore_interface-idxcoreadapter-getproperty.md), [referencia de DXCore](../dxcore-reference.md), [uso de DXCore para enumerar los adaptadores](../dxcore-enum-adapters.md)</span><span class="sxs-lookup"><span data-stu-id="bf279-159">[IDXCoreAdapter::GetPropertySize](./nf-dxcore_interface-idxcoreadapter-getpropertysize.md), [IDXCoreAdapter::GetProperty](./nf-dxcore_interface-idxcoreadapter-getproperty.md), [DXCore Reference](../dxcore-reference.md), [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md)</span></span>