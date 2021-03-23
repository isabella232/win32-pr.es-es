---
title: Temporización (gráficos de Direct3D 12)
description: En esta sección se explica cómo consultar las marcas de tiempo y calibrar los contadores de GPU y de marca de tiempo de la CPU.
ms.assetid: CC1E5BAB-4363-43FF-BF5B-6C9AEBECD6CA
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 979c51b3c88be184cb23afaa2008e90eaec1f9c5
ms.sourcegitcommit: a1f58e231315e95bbf9178994f8c52303fc0d4a1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/21/2020
ms.locfileid: "104549185"
---
# <a name="timing-direct3d-12-graphics"></a>Temporización (gráficos de Direct3D 12)

En esta sección se explica cómo consultar las marcas de tiempo y calibrar los contadores de GPU y de marca de tiempo de la CPU.

## <a name="timestamp-frequency"></a>Frecuencia de marca de tiempo

La aplicación puede consultar la frecuencia de la marca de tiempo de la GPU en cada cola de comandos (consulte el método [**ID3D12CommandQueue:: GetTimestampFrequency**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-gettimestampfrequency) ).

La frecuencia devuelta se mide en Hz (TICs/seg.). Si la cola de comandos especificada no admite marcas de tiempo (vea la tabla en la sección [consultas](queries.md) ), se produce un error en esta API (y se devuelve **E_FAIL**). [**D3D12_COMMAND_LIST_TYPE_DIRECT**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type) y [**D3D12_COMMAND_LIST_TYPE_COMPUTE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type) admiten marcas de tiempo siempre. [**D3D12_COMMAND_LIST_TYPE_COPY**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type) opcionalmente admite marcas de tiempo si el miembro [**D3D12_FEATURE_DATA_D3D12_OPTIONS3:: CopyQueueTimestampQueriesSupported**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options3) es **true**.

## <a name="timestamp-calibration"></a>Calibración de marca de tiempo

D3D12 permite a las aplicaciones correlacionar los resultados obtenidos de las consultas de marca de tiempo con los resultados obtenidos de la llamada a `QueryPerformanceCounter` . Esta opción está habilitada por la llamada a [**ID3D12CommandQueue:: GetClockCalibration**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-getclockcalibration).

[**GetClockCalibration**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-getclockcalibration) muestrea el contador de marca de tiempo de GPU para una cola de comandos determinada y muestrea el contador de CPU a través `QueryPerformanceCounter` de casi al mismo tiempo. De nuevo, se produce un error en esta API (se devuelve E \_ produce un error) si la cola de comandos especificada no admite marcas de tiempo (vea la tabla en el tema [consultas](queries.md) ).

Tenga en cuenta que los contadores de marca de tiempo de la GPU y la CPU no están necesariamente relacionados directamente con la velocidad del reloj de estos procesadores, sino que trabajan desde TICs de marca de tiempo.

## <a name="timestamp-queries"></a>Consultas de marca de tiempo

Puede obtener marcas de tiempo como parte de una lista de comandos (en lugar de una llamada del lado de la CPU en una cola de comandos) mediante consultas de marca de tiempo. (Consulte [consultas](queries.md) para obtener más información acerca de las consultas en general). 

Todas las consultas de marca de tiempo usan el tipo [**D3D12_QUERY_TYPE_TIMESTAMP**](/windows/win32/api/d3d12/ne-d3d12-d3d12_query_type) para la consulta real. Sin embargo, debido a las limitaciones de hardware, [**D3D12_COMMAND_LIST_TYPE_DIRECT**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type) y [**D3D12_COMMAND_LIST_TYPE_COMPUTE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type) usar un [**D3D12_QUERY_HEAP_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_query_heap_type) diferente del que utiliza [**D3D12_COMMAND_LIST_TYPE_COPY**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type) .

Las colas directas y de proceso usan [**D3D12_QUERY_HEAP_TYPE_TIMESTAMP**](/windows/win32/api/d3d12/ne-d3d12-d3d12_query_heap_type).

Las colas de copia usan [**D3D12_QUERY_HEAP_TYPE_COPY_QUEUE_TIMESTAMP**](/windows/win32/api/d3d12/ne-d3d12-d3d12_query_heap_type).

Las consultas Copy Queue solo se admiten si el miembro [**D3D12_FEATURE_DATA_D3D12_OPTIONS3:: CopyQueueTimestampQueriesSupported**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options3) es **true**.

Las consultas de marca de tiempo, una vez resueltas a través de [**ID3D12GraphicsCommandList:: ResolveQueryData**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resolvequerydata), son un **UINT64** que representa TICs, tal como lo devuelve [**ID3D12CommandQueue:: GetClockCalibration**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-getclockcalibration)y, como tal, debe dividirse por la frecuencia de la cola para obtener la longitud en segundos.

> [!IMPORTANT]
> Para obtener precisión, use aritmética de punto flotante al calcular los intervalos de segundos o milisegundos de las marcas de tiempo. Por ejemplo, use `queriedTicks / (double)Frequency` en lugar de `queriedTicks / Frequency`.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Contadores y consultas](counters-and-queries.md)
</dt> <dt>

[**ID3D12Device::SetStablePowerState**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-setstablepowerstate)
</dt> <dt>

[**ID3D12Object:: SetName**](/windows/desktop/api/d3d12/nf-d3d12-id3d12object-setname)
</dt> <dt>

[**ID3DUserDefinedAnnotation**](/windows/desktop/api/d3d11_1/nn-d3d11_1-id3duserdefinedannotation)
</dt> <dt>

[Medición del rendimiento](performance-measurement.md)
</dt> </dl>
