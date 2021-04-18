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
# <a name="dxcoreadapterproperty-enum"></a>Enumeración DXCoreAdapterProperty

Define constantes que especifican las propiedades del adaptador de DXCore. Pase una de estas constantes al método [IDXCoreAdapter:: GetPropertySize](./nf-dxcore_interface-idxcoreadapter-getpropertysize.md) para recuperar el tamaño del búfer necesario para recibir el valor de la propiedad correspondiente. a continuación, pase la misma constante al método [IDXCoreAdapter:: GetProperty](./nf-dxcore_interface-idxcoreadapter-getproperty.md) para recuperar el valor de la propiedad en un búfer que asigne.

## <a name="syntax"></a>Sintaxis

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

## <a name="constants"></a>Constantes

### <a name="instanceluid"></a>InstanceLuid

Especifica la propiedad del adaptador <em>InstanceLuid</em> , que contiene un identificador único local que representa el adaptador. Este valor permanece constante mientras dure este adaptador. El LUID de un adaptador cambia al reiniciarse, actualizar controladores o deshabilitación o habilitación del dispositivo.

La propiedad del adaptador <em>InstanceLuid</em> tiene el tipo <a href="/windows/win32/api/winnt/ns-winnt-luid">LUID</a>.

### <a name="driverversion"></a>DriverVersion

Especifica la propiedad del adaptador de <em>DriverVersion</em> , que contiene la versión del controlador, representada en <b>WORD</b>s como <b>LARGE_INTEGER</b>.

La propiedad del adaptador <em>DriverVersion</em> tiene el tipo <b>uint64_t</b>, que representa un valor booleano.

### <a name="driverdescription"></a>DriverDescription

Especifica la propiedad del adaptador <em>DriverDescription</em> , que contiene una matriz terminada en NULL de <b>Char</b>s que describe el controlador, tal y como lo especifica el controlador, en codificación <a href="/windows/win32/intl/unicode">UTF-8</a> .

La propiedad del adaptador <em>DriverDescription</em> tiene el tipo <b>Char *</b>.

### <a name="hardwareid"></a>HardwareID

Especifica la propiedad del adaptador de <em>HardwareID</em> , que representa las partes del identificador de hardware de PNP.

La propiedad del adaptador <em>HardwareID</em> tiene el tipo <a href="/windows/win32/dxcore/dxcore_interface/ns-dxcore_interface-dxcorehardwareid">DXCoreHardwareID</a>.

### <a name="kmdmodelversion"></a>KmdModelVersion

Especifica la propiedad de adaptador <em>KmdModelVersion</em> , que representa el modelo de controlador.

La propiedad del adaptador <em>KmdModelVersion</em> tiene el tipo <a href="/windows-hardware/drivers/ddi/content/d3dkmthk/ne-d3dkmthk-_qai_driverversion">D3DKMT_DRIVERVERSION</a>.

### <a name="computepreemptiongranularity"></a>ComputePreemptionGranularity

Especifica la propiedad del adaptador de <em>ComputePreemptionGranularity</em> , que representa la granularidad de prevacía de proceso.

La propiedad del adaptador <em>ComputePreemptionGranularity</em> tiene el tipo <b>uint16_t</b>, que representa un valor <a href="/windows-hardware/drivers/ddi/content/d3dkmdt/ne-d3dkmdt-_d3dkmdt_compute_preemption_granularity">D3DKMDT_COMPUTE_PREEMPTION_GRANULARITY</a> .

### <a name="graphicspreemptiongranularity"></a>GraphicsPreemptionGranularity

Especifica la propiedad del adaptador de <em>GraphicsPreemptionGranularity</em> , que representa la granularidad del prevacío de los gráficos.

La propiedad del adaptador <em>GraphicsPreemptionGranularity</em> tiene el tipo <b>uint16_t</b>, que representa un valor <a href="/windows-hardware/drivers/ddi/content/d3dkmdt/ne-d3dkmdt-_d3dkmdt_graphics_preemption_granularity">D3DKMDT_GRAPHICS_PREEMPTION_GRANULARITY</a> .

### <a name="dedicatedadaptermemory"></a>DedicatedAdapterMemory

Especifica la propiedad de adaptador <em>DedicatedAdapterMemory</em> , que representa el número de bytes de memoria de adaptador dedicada que no se comparten con la CPU.

La propiedad del adaptador <em>DedicatedVideoMemory</em> tiene el tipo <b>uint64_t</b>.

### <a name="dedicatedsystemmemory"></a>DedicatedSystemMemory

Especifica la propiedad del adaptador <em>DedicatedSystemMemory</em> , que representa el número de bytes de la memoria del sistema dedicada que no se comparten con la CPU. Esta memoria se asigna desde la memoria disponible del sistema durante el arranque.

La propiedad del adaptador <em>DedicatedSystemMemory</em> tiene el tipo <b>uint64_t</b>.

### <a name="sharedsystemmemory"></a>SharedSystemMemory

Especifica la propiedad del adaptador <em>SharedSystemMemory</em> , que representa el número de bytes de la memoria compartida del sistema. Este es el valor máximo de la memoria del sistema que puede consumir el adaptador durante la operación. Cualquier memoria incidental consumida por el controlador a medida que administra y usa la memoria de vídeo es adicional.

La propiedad del adaptador <em>SharedSystemMemory</em> tiene el tipo <b>uint64_t</b>.

### <a name="acgcompatible"></a>AcgCompatible

Especifica la propiedad del adaptador <em>AcgCompatible</em> , que indica si el adaptador es compatible con los procesos que aplican la protección de código arbitraria.

La propiedad del adaptador <em>AcgCompatible</em> tiene el tipo <b>bool</b>.

### <a name="ishardware"></a>IsHardware

Especifica la propiedad del adaptador <em>IsHardware</em> , que determina si se trata de un adaptador de hardware. Un adaptador que no es un adaptador de hardware es un adaptador de software.

La propiedad del adaptador <em>IsHardware</em> tiene el tipo <b>bool</b>.

### <a name="isintegrated"></a>IsIntegrated

Especifica la propiedad del adaptador de <em>IsIntegrated</em> , que determina si se ha detectado que el adaptador es un procesador de gráficos integrado (iGPU).

La propiedad del adaptador <em>IsIntegrated</em> tiene el tipo <b>bool</b>.

### <a name="isdetachable"></a>IsDetachable

Especifica la propiedad del adaptador de <em>IsDetachable</em> , que determina si el adaptador se ha comunicado para ser desasociable o extraíble.

La propiedad del adaptador <em>IsDetachable</em> tiene el tipo <b>bool</b>.

<b>Nota</b>: Incluso si <a href="/windows/win32/dxcore/dxcore_interface/nf-dxcore_interface-idxcoreadapter-getproperty">IDXCoreAdapter:: GetProperty</a> indica `false` para esta propiedad, el adaptador todavía tiene la posibilidad de que se le notifique como quitado, como en caso de error de funcionamiento o actualización del controlador.

## <a name="see-also"></a>Vea también

[IDXCoreAdapter:: GetPropertySize](./nf-dxcore_interface-idxcoreadapter-getpropertysize.md), [IDXCoreAdapter:: GetProperty](./nf-dxcore_interface-idxcoreadapter-getproperty.md), [referencia de DXCore](../dxcore-reference.md), [uso de DXCore para enumerar los adaptadores](../dxcore-enum-adapters.md)