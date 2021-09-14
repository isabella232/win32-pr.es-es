---
title: Contadores de salida de flujo
description: La salida de flujo es la capacidad de la GPU de escribir vértices en un búfer. Los contadores de salida de flujo supervisan el progreso.
ms.assetid: 7342DA09-25E9-4154-83BA-B03ADBB8B671
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df4d2f3a823f5f4b5d2d5f365235d7e3f8817207
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127072870"
---
# <a name="stream-output-counters"></a>Contadores de salida de flujo

La salida de flujo es la capacidad de la GPU de escribir vértices en un búfer. Los contadores de salida de flujo supervisan el progreso.

-   [Diferencias en los contadores de flujo de Direct3D 11 a Direct3D 12](#differences-in-stream-counters-from-direct3d-11-to-direct3d-12)
-   [BufferFilledSize](#bufferfilledsize)
-   [Temas relacionados](#related-topics)

## <a name="differences-in-stream-counters-from-direct3d-11-to-direct3d-12"></a>Diferencias en los contadores de flujo de Direct3D 11 a Direct3D 12

Como parte del proceso de salida del flujo, la GPU debe conocer la ubicación actual en el búfer en el que está escribiendo. En Direct3D 11, el controlador asigna memoria para almacenar esta ubicación y la única manera de que las aplicaciones manipulen este valor es a través del **método SOSetTargets.** En Direct3D 12, las aplicaciones asignan memoria para almacenar esta ubicación actual. No hay ninguna manera especial de manipular este valor y las aplicaciones pueden leer y escribir el valor con la CPU o GPU.

## <a name="bufferfilledsize"></a>BufferFilledSize

La aplicación es responsable de asignar almacenamiento para una cantidad de 32 bits denominada *BufferFilledSize*. Contiene el número de bytes de datos en el búfer de salida de flujo. Este almacenamiento se puede colocar en el mismo recurso o en otro diferente que el que contiene los datos de salida de flujo. La GPU tiene acceso a este valor en la fase de salida de flujo para determinar dónde anexar nuevos datos de vértices en el búfer. Además, la GPU tiene acceso a este valor para determinar cuándo se ha producido el desbordamiento.

Consulte la estructura [**D3D12 \_ STREAM OUTPUT \_ \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_stream_output_desc).

La capa de depuración validará lo siguiente [**en ID3D12GraphicsCommandList::SOSetTargets**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-sosettargets):

-   *BufferFilledSize* se encuentra en el intervalo implícito en {*OffsetInBytes*, *SizeInBytes*}, si se especifica un recurso que no es NULL.
-   *BufferFilledSizeOffsetInBytes* es un múltiplo de 4.
-   *BufferFilledSizeOffsetInBytes* está dentro del intervalo del recurso que lo contiene.
-   El recurso especificado es un búfer.

El tiempo de ejecución no validará el tipo de montón asociado al búfer de salida de flujo, ya que la salida del flujo se admite en todos los tipos de montón.

Las firmas raíz deben especificar si se usará la salida del flujo mediante las marcas [**D3D12 \_ ROOT \_ SIGNATURE \_ FLAGS.**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags)

La marca de firma raíz D3D12 ALLOW STREAM OUTPUT se puede especificar para las firmas raíz que se crearon en \_ \_ \_ \_ HLSL, de forma similar a como se especifican las \_ \_ otras marcas.

[**CreateGraphicsPipelineState**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-creategraphicspipelinestate) producirá un error si el sombreador de geometría contiene stream-output, pero la firma raíz no tiene establecida la marca D3D12 \_ ROOT SIGNATURE FLAG ALLOW STREAM \_ \_ \_ \_ \_ OUTPUT.

Cuando se usa un recurso como destino de salida de flujo, los recursos usados deben estar en el estado RESOURCE STATE STREAM OUT de D3D12. \_ \_ \_ \_ Esto se aplica tanto a los datos de vértice como a *BufferFilledSize* (que pueden estar en el mismo recurso o en recursos independientes).

No hay API especiales para establecer desplazamientos de búfer de salida de flujo porque las aplicaciones pueden escribir directamente en *BufferFilledSize* con la CPU o GPU.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Contadores y consultas](counters-and-queries.md)
</dt> </dl>

 

 




