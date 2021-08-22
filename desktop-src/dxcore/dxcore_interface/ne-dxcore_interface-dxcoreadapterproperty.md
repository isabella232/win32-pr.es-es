---
title: 'DXCoreAdapterProperty '
description: Define constantes que especifican las propiedades del adaptador de DXCore.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: aca9093eb85971621cf232b4713d811535619b59c3d07e0b8b490d063b9d7ac3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119042933"
---
# <a name="dxcoreadapterproperty-enum"></a>Enumeración DXCoreAdapterProperty

Define constantes que especifican las propiedades del adaptador de DXCore. Pase una de estas constantes al método [IDXCoreAdapter::GetPropertySize](./nf-dxcore_interface-idxcoreadapter-getpropertysize.md) para recuperar el tamaño de búfer necesario para recibir el valor de la propiedad correspondiente; a continuación, pase la misma constante al método [IDXCoreAdapter::GetProperty](./nf-dxcore_interface-idxcoreadapter-getproperty.md) para recuperar el valor de la propiedad en un búfer que asigne.

## <a name="syntax"></a>Syntax

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

Especifica la propiedad <em>del adaptador InstanceLuid,</em> que contiene un identificador único local que representa el adaptador. Este valor permanece constante durante la duración de este adaptador. El LUID de un adaptador cambia en el reinicio, la actualización del controlador o la deshabilitación o habilitación del dispositivo.

La <em>propiedad del adaptador InstanceLuid</em> tiene el tipo <a href="/windows/win32/api/winnt/ns-winnt-luid">LUID</a>.

### <a name="driverversion"></a>DriverVersion

Especifica la propiedad <em>del adaptador DriverVersion,</em> que contiene la versión del controlador, representada en <b>WORD</b>como un <b>LARGE_INTEGER</b>.

La <em>propiedad del adaptador DriverVersion</em> tiene el tipo <b>uint64_t</b>, que representa un valor booleano.

### <a name="driverdescription"></a>DriverDescription

Especifica la propiedad del adaptador <em>DriverDescription,</em> que contiene una matriz terminada en NULL de <b>CHAR</b>que describe el controlador, tal como especifica el controlador, en <a href="/windows/win32/intl/unicode">codificación UTF-8.</a>

La <em>propiedad del adaptador DriverDescription</em> tiene el tipo <b>char*.</b>

### <a name="hardwareid"></a>HardwareID

Especifica la propiedad <em>del adaptador HardwareID,</em> que representa las partes del identificador de hardware PnP.

La <em>propiedad del adaptador HardwareID</em> tiene el tipo <a href="/windows/win32/dxcore/dxcore_interface/ns-dxcore_interface-dxcorehardwareid">DXCoreHardwareID</a>.

### <a name="kmdmodelversion"></a>KmdModelVersion

Especifica la propiedad <em>del adaptador KmdModelVersion,</em> que representa el modelo de controlador.

La <em>propiedad del adaptador KmdModelVersion</em> tiene el tipo <a href="/windows-hardware/drivers/ddi/content/d3dkmthk/ne-d3dkmthk-_qai_driverversion">D3DKMT_DRIVERVERSION</a>.

### <a name="computepreemptiongranularity"></a>ComputePreemptionGranularity

Especifica la propiedad <em>del adaptador ComputePreemptionGranularity,</em> que representa la granularidad de adelantamiento de proceso.

La <em>propiedad del adaptador ComputePreemptionGranularity</em> tiene el tipo <b>uint16_t</b>, que representa <a href="/windows-hardware/drivers/ddi/content/d3dkmdt/ne-d3dkmdt-_d3dkmdt_compute_preemption_granularity">un D3DKMDT_COMPUTE_PREEMPTION_GRANULARITY</a> valor.

### <a name="graphicspreemptiongranularity"></a>GraphicsPreemptionGranularity

Especifica la propiedad <em>del adaptador GraphicsPreemptionGranularity,</em> que representa la granularidad de adelantamiento de gráficos.

La <em>propiedad del adaptador GraphicsPreemptionGranularity</em> tiene el tipo <b>uint16_t</b>, que representa <a href="/windows-hardware/drivers/ddi/content/d3dkmdt/ne-d3dkmdt-_d3dkmdt_graphics_preemption_granularity">un D3DKMDT_GRAPHICS_PREEMPTION_GRANULARITY</a> valor.

### <a name="dedicatedadaptermemory"></a>DedicatedAdapterMemory

Especifica la propiedad del adaptador <em>DedicatedAdapterMemory,</em> que representa el número de bytes de memoria de adaptador dedicada que no se comparten con la CPU.

La <em>propiedad del adaptador DedicatedVideoMemory</em> tiene el tipo <b>uint64_t</b>.

### <a name="dedicatedsystemmemory"></a>DedicatedSystemMemory

Especifica la propiedad del adaptador <em>DedicatedSystemMemory,</em> que representa el número de bytes de memoria del sistema dedicada que no se comparten con la CPU. Esta memoria se asigna desde la memoria del sistema disponible en tiempo de arranque.

La <em>propiedad del adaptador DedicatedSystemMemory</em> tiene el tipo <b>uint64_t</b>.

### <a name="sharedsystemmemory"></a>SharedSystemMemory

Especifica la propiedad <em>del adaptador SharedSystemMemory,</em> que representa el número de bytes de memoria compartida del sistema. Este es el valor máximo de memoria del sistema que puede consumir el adaptador durante la operación. Cualquier memoria accidental consumida por el controlador a medida que administra y usa la memoria de vídeo es adicional.

La <em>propiedad del adaptador SharedSystemMemory</em> tiene el tipo <b>uint64_t</b>.

### <a name="acgcompatible"></a>AcgCompatible

Especifica la propiedad <em>del adaptador AcgCompatible,</em> que indica si el adaptador es compatible con los procesos que aplican La protección de código arbitraria.

La <em>propiedad del adaptador AcgCompatible</em> tiene el tipo <b>bool</b>.

### <a name="ishardware"></a>IsHardware

Especifica la propiedad <em>del adaptador IsHardware,</em> que determina si se trata o no de un adaptador de hardware. Un adaptador que no es un adaptador de hardware es un adaptador de software.

La <em>propiedad del adaptador IsHardware</em> tiene el tipo <b>bool</b>.

### <a name="isintegrated"></a>IsIntegrated

Especifica la <em>propiedad del adaptador IsIntegrated,</em> que determina si se notifica que el adaptador es un procesador de gráficos integrado (iGPU).

La <em>propiedad del adaptador IsIntegrated</em> tiene el tipo <b>bool</b>.

### <a name="isdetachable"></a>IsDentes

Especifica la <em>propiedad del adaptador IsDe adapter,</em> que determina si se ha notificado que el adaptador es desasociable o extraíble.

La propiedad del adaptador de <em>IsDe adapter</em> tiene el <b>tipo bool</b>.

<b>Tenga en cuenta</b>. Incluso si <a href="/windows/win32/dxcore/dxcore_interface/nf-dxcore_interface-idxcoreadapter-getproperty">IDXCoreAdapter::GetProperty</a> indica para esta propiedad, el adaptador todavía tiene la capacidad de ser notificado como eliminado, como en caso de error de funcionamiento o de actualización `false` del controlador.

## <a name="see-also"></a>Vea también

[IDXCoreAdapter::GetPropertySize](./nf-dxcore_interface-idxcoreadapter-getpropertysize.md), [IDXCoreAdapter::GetProperty](./nf-dxcore_interface-idxcoreadapter-getproperty.md), [DXCore Reference](../dxcore-reference.md), [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md)