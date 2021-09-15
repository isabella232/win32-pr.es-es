---
title: Control de tiempo (gráficos de Direct3D 12)
description: En esta sección se trata la consulta de marcas de tiempo y la calibración de los contadores de marca de tiempo de CPU y GPU.
ms.assetid: CC1E5BAB-4363-43FF-BF5B-6C9AEBECD6CA
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 979c51b3c88be184cb23afaa2008e90eaec1f9c5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127465548"
---
# <a name="timing-direct3d-12-graphics"></a>Control de tiempo (gráficos de Direct3D 12)

En esta sección se trata la consulta de marcas de tiempo y la calibración de los contadores de marca de tiempo de CPU y GPU.

## <a name="timestamp-frequency"></a>Frecuencia de marca de tiempo

La aplicación puede consultar la frecuencia de marca de tiempo de GPU por cola por comando (consulte el método [**ID3D12CommandQueue::GetTimestampFrequency).**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-gettimestampfrequency)

La frecuencia devuelta se mide en Hz (tics/s). Si la cola de comandos especificada no admite marcas [](queries.md) de tiempo (consulte la tabla en la sección Consultas), se produce un error en esta API (y devuelve **E_FAIL**). [**D3D12_COMMAND_LIST_TYPE_DIRECT**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type) y [**D3D12_COMMAND_LIST_TYPE_COMPUTE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type) siempre admiten marcas de tiempo. [**D3D12_COMMAND_LIST_TYPE_COPY**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type) opcionalmente admite marcas de tiempo [**si el miembro D3D12_FEATURE_DATA_D3D12_OPTIONS3::CopyQueueTimestampQueriesSupported**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options3) es **TRUE.**

## <a name="timestamp-calibration"></a>Calibración de marca de tiempo

D3D12 permite a las aplicaciones correlacionar los resultados obtenidos de las consultas de marca de tiempo con los resultados obtenidos al llamar a `QueryPerformanceCounter` . Esto se habilita mediante la llamada [**ID3D12CommandQueue::GetClockCmdbration**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-getclockcalibration).

[**GetClock Yabration**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-getclockcalibration) muestrea el contador de marca de tiempo de GPU para una cola de comandos determinada y muestrea el contador de CPU a través `QueryPerformanceCounter` de casi al mismo tiempo. De nuevo, se produce un error en esta API (al devolver E FAIL) si la cola de comandos especificada no admite marcas de tiempo (consulte la tabla \_ en el [tema](queries.md) Consultas).

Tenga en cuenta que los contadores de marca de tiempo de GPU y CPU no están necesariamente relacionados directamente con la velocidad del reloj de estos procesadores, sino que funcionan a partir de tics de marca de tiempo.

## <a name="timestamp-queries"></a>Consultas de marca de tiempo

Puede obtener marcas de tiempo como parte de una lista de comandos (en lugar de una llamada del lado cpu en una cola de comandos) a través de consultas de marca de tiempo. (Consulte [Consultas para](queries.md) obtener más información sobre las consultas en general). 

Todas las consultas de marca de tiempo usan el [**tipo D3D12_QUERY_TYPE_TIMESTAMP**](/windows/win32/api/d3d12/ne-d3d12-d3d12_query_type) para la consulta real. Sin embargo, debido a las limitaciones de hardware, [](/windows/win32/api/d3d12/ne-d3d12-d3d12_query_heap_type) [**D3D12_COMMAND_LIST_TYPE_DIRECT**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type) y [**D3D12_COMMAND_LIST_TYPE_COMPUTE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type) usan un D3D12_QUERY_HEAP_TYPE diferente del que [**D3D12_COMMAND_LIST_TYPE_COPY**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type) usa.

Las colas directas y de proceso [**usan D3D12_QUERY_HEAP_TYPE_TIMESTAMP**](/windows/win32/api/d3d12/ne-d3d12-d3d12_query_heap_type).

Las colas de copia [**usan D3D12_QUERY_HEAP_TYPE_COPY_QUEUE_TIMESTAMP**](/windows/win32/api/d3d12/ne-d3d12-d3d12_query_heap_type).

Las consultas de cola de copia solo se admiten [**si el miembro D3D12_FEATURE_DATA_D3D12_OPTIONS3::CopyQueueTimestampQueriesSupported**](/windows/win32/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options3) es **TRUE.**

Las consultas de marca de tiempo, una vez resueltas a través de [**ID3D12GraphicsCommandList::ResolveQueryData**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resolvequerydata), son **un UINT64** que representa los pasos, como lo devuelve [**ID3D12CommandQueue::GetClockControlbration**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-getclockcalibration)y, como tal, debe dividirse por la frecuencia de cola para obtener la longitud en segundos.

> [!IMPORTANT]
> Para obtener precisión, use aritmética de punto flotante al calcular intervalos de segundos o milisegundos de marcas de tiempo. Por ejemplo, use `queriedTicks / (double)Frequency` en lugar de `queriedTicks / Frequency`.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Contadores y consultas](counters-and-queries.md)
</dt> <dt>

[**ID3D12Device::SetStablePowerState**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-setstablepowerstate)
</dt> <dt>

[**ID3D12Object::SetName**](/windows/desktop/api/d3d12/nf-d3d12-id3d12object-setname)
</dt> <dt>

[**ID3DUserDefinedAnnotation**](/windows/desktop/api/d3d11_1/nn-d3d11_1-id3duserdefinedannotation)
</dt> <dt>

[Medición del rendimiento](performance-measurement.md)
</dt> </dl>
