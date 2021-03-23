---
title: Contadores de UAV
description: Puede usar contadores de acceso sin ordenar (UAV) para asociar un contador atómico de 32 bits con un desordenado-Access-View (UAV).
ms.assetid: 0B77E238-E8CF-466B-9188-3DE96AF97F42
ms.localizationpriority: high
ms.topic: article
ms.date: 02/10/2020
ms.openlocfilehash: 94bc1492e3b984d96c76788430d2e63c0672ca76
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/11/2020
ms.locfileid: "104549105"
---
# <a name="uav-counters"></a>Contadores de UAV
Puede usar contadores de acceso sin ordenar (UAV) para asociar un contador atómico de 32 bits con un desordenado-Access-View (UAV).

## <a name="differences-in-uav-counters-from-direct3d-11-to-direct3d-12"></a>Diferencias en los contadores de UAV de Direct3D 11 a Direct3D 12
Las aplicaciones de Direct3D 12 y Direct3D 11 usan las mismas funciones de sombreador de lenguaje de sombreado de alto nivel (HLSL) para tener acceso a los contadores de UAV.

-   **IncrementCounter**
-   **DecrementCounter**
-   **Append**
-   **Consumo**

### <a name="direct3d-12"></a>Direct3D 12
En Direct3D 12, la aplicación asigna los valores de 32 bits, por lo que los valores de 32 bits se pueden leer y escribir en la CPU o la GPU, como cualquier otro recurso de Direct3D 12.

### <a name="direct3d-11"></a>Direct3D 11
Fuera de los sombreadores, con Direct3D 11 debe llamar a los métodos de la API para tener acceso a los contadores (por ejemplo, [ID3D11DeviceContext:: CopyStructureCount](/windows/win32/api/d3d11/nf-d3d11-id3d11devicecontext-copystructurecount)).

## <a name="using-uav-counters"></a>Uso de contadores de UAV
La aplicación es responsable de asignar 32 bits de almacenamiento para los contadores de UAV. Este almacenamiento se puede asignar en otro recurso como el que contiene los datos accesibles a través de UAV.

Consulte [**CreateUnorderedAccessView**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createunorderedaccessview), [**D3D12 \_ buffer \_ UAV \_ Flags**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_buffer_uav_flags) y [**D3D12 \_ buffer \_ UAV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_buffer_uav).

Si *pCounterResource* se especifica en la llamada a [**CreateUnorderedAccessView**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createunorderedaccessview), hay un contador asociado al UAV. En este caso:

-   *StructureByteStride* debe ser mayor que cero
-   El formato debe tener el \_ formato DXGI \_ desconocido
-   No se debe establecer la marca sin formato
-   Ambos recursos deben ser búferes
-   *CounterOffsetInBytes* debe ser un múltiplo de 4 bytes
-   *CounterOffsetInBytes* debe estar en el intervalo del recurso de contador
-   *pDesc* no puede ser null
-   el *preorigen* no puede ser nulo

Y tenga en cuenta los siguientes casos de uso:

-   Si no se especifica *pCounterResource* , *CounterOffsetInBytes* debe ser 0.
-   Si se establece la marca sin formato, el formato debe ser DXGI \_ format \_ R32 \_ y el recurso UAV debe ser un búfer.
-   Si no se establece *pCounterResource* , *CounterOffsetInBytes* debe ser 0.
-   Si no se establece la marca sin formato y *StructureByteStride* = 0, el formato debe ser un formato UAV válido.

Direct3D 12 quita la distinción entre Append y Counter UAVs (aunque la distinción todavía existe en el código de bytes HLSL).

El entorno de tiempo de ejecución principal validará estas restricciones dentro de [**CreateUnorderedAccessView**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createunorderedaccessview).

Durante el envío y la distribución, el recurso de contador debe estar en el estado de [**\_ recurso D3D12 \_ \_ \_ acceso no ordenado**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states). Además, dentro de una única llamada a Draw/Dispatch, no es válido para una aplicación tener acceso a la misma ubicación de memoria de 32 bits a través de dos contadores de UAV independientes. La capa de depuración emitirá errores si se detecta cualquiera de ellos.

No hay ningún método "SetUnorderedAccessViewCounterValue" o "CopyStructureCount", ya que las aplicaciones solo pueden copiar directamente los datos hacia y desde el valor del contador.

Se admite la indexación dinámica de UAVs con contadores.

Si un sombreador intenta obtener acceso al contador de un UAV que no tiene un contador asociado, la capa de depuración emitirá una advertencia y se producirá un error de página de GPU que hará que se quite el dispositivo de la aplicación.

Los contadores de UAV se admiten en todos los tipos de montón (predeterminado, upload, readback).

## <a name="related-topics"></a>Temas relacionados

* [Contadores y consultas](counters-and-queries.md)