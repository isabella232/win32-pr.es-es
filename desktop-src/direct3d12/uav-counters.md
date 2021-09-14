---
title: Contadores de UAV
description: Puede usar contadores unordered-access-view (UAV) para asociar un contador atómico de 32 bits a una vista de acceso desordenado (UAV).
ms.assetid: 0B77E238-E8CF-466B-9188-3DE96AF97F42
ms.localizationpriority: high
ms.topic: article
ms.date: 02/10/2020
ms.openlocfilehash: 94bc1492e3b984d96c76788430d2e63c0672ca76
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127242871"
---
# <a name="uav-counters"></a>Contadores de UAV
Puede usar contadores unordered-access-view (UAV) para asociar un contador atómico de 32 bits a una vista de acceso desordenado (UAV).

## <a name="differences-in-uav-counters-from-direct3d-11-to-direct3d-12"></a>Diferencias en los contadores UAV de Direct3D 11 a Direct3D 12
Tanto las aplicaciones de Direct3D 12 como las aplicaciones de Direct3D 11 usan las mismas funciones de sombreador de lenguaje de sombreador de alto nivel (HLSL) para acceder a los contadores UAV.

-   **IncrementCounter**
-   **DecrementCounter**
-   **Append**
-   **Consumo**

### <a name="direct3d-12"></a>Direct3D 12
En Direct3D 12, la aplicación asigna los valores de 32 bits, por lo que la CPU o la GPU pueden leer y escribir los valores de 32 bits, como cualquier otro recurso de Direct3D 12.

### <a name="direct3d-11"></a>Direct3D 11
Fuera de los sombreadores, con Direct3D 11 debe llamar a métodos de API para tener acceso a los contadores (por ejemplo, [ID3D11DeviceContext::CopyStructureCount).](/windows/win32/api/d3d11/nf-d3d11-id3d11devicecontext-copystructurecount)

## <a name="using-uav-counters"></a>Uso de contadores UAV
La aplicación es responsable de asignar 32 bits de almacenamiento para los contadores UAV. Este almacenamiento se puede asignar en un recurso diferente al que contiene los datos accesibles a través del UAV.

Consulte [**CreateUnorderedAccessView**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createunorderedaccessview), [**D3D12 \_ BUFFER \_ UAV \_ FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_buffer_uav_flags) y [**D3D12 \_ BUFFER \_ UAV**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_buffer_uav).

Si *se especifica pCounterResource* en la llamada a [**CreateUnorderedAccessView**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createunorderedaccessview), hay un contador asociado al UAV. En este caso:

-   *StructureByteStride* debe ser mayor que cero
-   El formato debe ser DXGI \_ FORMAT \_ UNKNOWN
-   No se debe establecer la marca RAW
-   Ambos recursos deben ser búferes
-   *CounterOffsetInBytes* debe ser un múltiplo de 4 bytes
-   *CounterOffsetInBytes* debe estar dentro del intervalo del recurso de contador
-   *pDesc* no puede ser NULL
-   *pResource* no puede ser NULL

Y tenga en cuenta los siguientes casos de uso:

-   Si *no se especifica pCounterResource,* *CounterOffsetInBytes* debe ser 0.
-   Si se establece la marca RAW, el formato debe ser DXGI FORMAT R32 TYPELESS y el \_ \_ recurso \_ UAV debe ser un búfer.
-   Si *no se establece pCounterResource,* *CounterOffsetInBytes* debe ser 0.
-   Si no se establece la marca RAW y *StructureByteStride* = 0, el formato debe ser un formato UAV válido.

Direct3D 12 quita la distinción entre los UAV append y counter (aunque la distinción sigue existiendo en el código de bytes HLSL).

El entorno de ejecución principal validará estas restricciones dentro de [**CreateUnorderedAccessView**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createunorderedaccessview).

Durante draw/dispatch, el recurso de contador debe estar en el estado [**D3D12 \_ RESOURCE \_ STATE \_ UNORDERED \_ ACCESS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states). Además, dentro de una sola llamada a Draw/Dispatch, no es válido que una aplicación acceda a la misma ubicación de memoria de 32 bits a través de dos contadores UAV independientes. La capa de depuración emitirá errores si se detecta alguno de ellos.

No hay ningún método "SetUnorderedAccessViewCounterValue" o "CopyStructureCount" porque las aplicaciones simplemente pueden copiar datos hacia y desde el valor del contador directamente.

Se admite la indexación dinámica de UAV con contadores.

Si un sombreador intenta acceder al contador de un UAV que no tiene un contador asociado, la capa de depuración emitirá una advertencia y se producirá un error en la página de GPU que hará que se quite el dispositivo de las aplicaciones.

Los contadores UAV se admiten en todos los tipos de montón (valor predeterminado, carga, reversión).

## <a name="related-topics"></a>Temas relacionados

* [Contadores y consultas](counters-and-queries.md)