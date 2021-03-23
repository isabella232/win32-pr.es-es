---
title: Contadores de salida de flujo
description: La salida de flujo es la capacidad de la GPU de escribir vértices en un búfer. Los contadores de salida de flujo supervisan el progreso.
ms.assetid: 7342DA09-25E9-4154-83BA-B03ADBB8B671
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df4d2f3a823f5f4b5d2d5f365235d7e3f8817207
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "74104581"
---
# <a name="stream-output-counters"></a>Contadores de salida de flujo

La salida de flujo es la capacidad de la GPU de escribir vértices en un búfer. Los contadores de salida de flujo supervisan el progreso.

-   [Diferencias en los contadores de flujo de Direct3D 11 a Direct3D 12](#differences-in-stream-counters-from-direct3d-11-to-direct3d-12)
-   [BufferFilledSize](#bufferfilledsize)
-   [Temas relacionados](#related-topics)

## <a name="differences-in-stream-counters-from-direct3d-11-to-direct3d-12"></a>Diferencias en los contadores de flujo de Direct3D 11 a Direct3D 12

Como parte del proceso de salida de la secuencia, la GPU tiene que conocer la ubicación actual en el búfer en el que está escribiendo. En Direct3D 11, la memoria para almacenar esta ubicación está asignada por el controlador y la única manera en que las aplicaciones manipulan este valor es a través del método **SOSetTargets** . En Direct3D 12, las aplicaciones asignan memoria para almacenar esta ubicación actual. No hay ninguna manera especial de manipular este valor y las aplicaciones pueden leer y escribir el valor con la CPU o la GPU.

## <a name="bufferfilledsize"></a>BufferFilledSize

La aplicación es responsable de la asignación de almacenamiento para una cantidad de 32 bits llamada *BufferFilledSize*. Contiene el número de bytes de datos en el búfer de salida de flujo. Este almacenamiento se puede colocar en el mismo recurso, o en otro diferente, que el que contiene los datos de salida de la secuencia. La GPU tiene acceso a este valor en la fase Stream-Output para determinar dónde se deben anexar los nuevos datos de vértice en el búfer. Además, la GPU accede a este valor para determinar cuándo se ha producido el desbordamiento.

Consulte la D3D12 de la estructura de [**\_ salida de Stream \_ \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_stream_output_desc).

El nivel de depuración validará lo siguiente en [**ID3D12GraphicsCommandList:: SOSetTargets**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-sosettargets):

-   *BufferFilledSize* se encuentra en el intervalo implícito por {*OffsetInBytes*, *SizeInBytes*}, si se especifica un recurso que no es NULL.
-   *BufferFilledSizeOffsetInBytes* es un múltiplo de 4.
-   *BufferFilledSizeOffsetInBytes* está dentro del intervalo del recurso que lo contiene.
-   El recurso especificado es un búfer.

El runtime no validará el tipo de montón asociado al búfer de salida de flujo, ya que la salida de flujo se admite en todos los tipos de montón.

Las signaturas de raíz deben especificar si se va a utilizar la salida de flujo mediante las marcas de la [**\_ \_ firma \_ raíz de D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) .

\_La marca de firma raíz de D3D12 \_ \_ \_ permite \_ \_ especificar la salida de secuencia para las signaturas raíz creadas en HLSL, de forma similar a la forma en que se especifican las demás marcas.

[**CreateGraphicsPipelineState**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-creategraphicspipelinestate) producirá un error si el sombreador de geometría contiene el flujo de salida, pero la firma raíz no tiene el \_ indicador de firma raíz D3D12 \_ permitir el marcador de salida de \_ \_ \_ secuencia \_ establecido.

Cuando se usa un recurso como destino de salida de flujo, los recursos usados deben estar en el estado de la \_ transmisión por secuencias de estado de recurso D3D12 \_ \_ \_ . Esto se aplica tanto a los datos de vértice como a los *BufferFilledSize* (que pueden estar en el mismo o en recursos independientes).

No hay ninguna API especial para establecer desplazamientos de búfer de salida de flujo, ya que las aplicaciones pueden escribir en *BufferFilledSize* directamente con la CPU o la GPU.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Contadores y consultas](counters-and-queries.md)
</dt> </dl>

 

 




