---
title: Descriptores de copias
description: Los métodos ID3D12Device CopyDescriptors y ID3D12Device CopyDescriptorsSimple en la interfaz de dispositivo usan la CPU para copiar descriptores inmediatamente.
ms.assetid: 65AE4D96-6221-46B5-BF55-F86479FCF97C
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14fdec6c76f29800f2a0e42bde76b32ebc794275
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "74104510"
---
# <a name="copying-descriptors"></a>Descriptores de copias

Los métodos [**ID3D12Device:: CopyDescriptors**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-copydescriptors) y [**ID3D12Device:: CopyDescriptorsSimple**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-copydescriptorssimple) de la interfaz de dispositivo usan la CPU para copiar descriptores inmediatamente. Se puede llamar subprocesamiento libre siempre que varios subprocesos de la CPU o GPU no realicen ninguna escritura en conflicto.

## <a name="copying-descriptors-immediately-cpu-timeline"></a>Copia de descriptores inmediatamente (escala de tiempo de CPU)

El número de descriptores de origen (de los que se copia), especificado como un conjunto de intervalos de descriptor, debe ser igual al número de descriptores de destino (para copiar en), especificado como un conjunto independiente de intervalos de descriptor. De lo contrario, los intervalos de origen y destino no tienen que alinearse. Por ejemplo, un conjunto de descriptores dispersos podría copiarse en un destino contiguo, viceversa o en alguna combinación.

En la operación de copia pueden participar varios montones de descriptor, como origen y destino. El uso de identificadores de descriptor como parámetros significa que los métodos de copia no están relacionados con los montones en los que se encuentra ningún descriptor determinado, sino que son solo memoria.

Los tipos del montón descriptor que se copian de y a deben coincidir, por lo que los métodos toman un único tipo de montón de descriptor como entrada. El controlador debe conocer el tipo de montón de todos los descriptores de la operación de copia dada, por lo que sabe qué tamaño de los datos están implicados en la operación de copia. Es posible que el controlador también tenga que realizar trabajos de copia personalizados si un determinado tipo de montón de descriptores lo justifica: un detalle de implementación. Tenga en cuenta que, en caso contrario, los controladores de descriptores no identifican el tipo al que apuntan. por lo tanto, se requiere un parámetro adicional para la operación de copia.

Se proporciona una API alternativa a [**CopyDescriptors**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-copydescriptors) para el caso simple de copiar un único intervalo de descriptores de una ubicación a otra – [**CopyDescriptorsSimple**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-copydescriptorssimple).

Para estos métodos de copia de descriptores basados en dispositivos (escala de tiempo de CPU), los descriptores de origen deben provienen de un montón de descriptor visible sin sombreador. Los descriptores de destino pueden estar en cualquier montón de descriptores que esté visible en la CPU (sombreador visible o no).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Descriptores de](descriptors.md)
</dt> </dl>

 

 




