---
title: Descriptores de copias
description: Los métodos ID3D12Device CopyDescriptors e ID3D12Device CopyDescriptorsSimple de la interfaz de dispositivo usan la CPU para copiar inmediatamente descriptores.
ms.assetid: 65AE4D96-6221-46B5-BF55-F86479FCF97C
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce02abfb433b36738de0fd62285e44b2f065ac017217a1e61f8c305e8ca76228
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120069705"
---
# <a name="copying-descriptors"></a>Descriptores de copias

Los [**métodos ID3D12Device::CopyDescriptors**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-copydescriptors) e [**ID3D12Device::CopyDescriptorsSimple**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-copydescriptorssimple) de la interfaz de dispositivo usan la CPU para copiar inmediatamente descriptores. Se pueden llamar subprocesos libres siempre y cuando varios subprocesos de la CPU o la GPU no realicen escrituras potencialmente conflictivas.

## <a name="copying-descriptors-immediately-cpu-timeline"></a>Copiar descriptores inmediatamente (escala de tiempo de CPU)

El número de descriptores de origen (desde los que se va a copiar), especificado como un conjunto de intervalos de descriptores, debe ser igual al número de descriptores de destino (en los que se va a copiar), especificado como un conjunto independiente de intervalos de descriptores. De lo contrario, los intervalos de origen y destino no tienen que realizar la alineación. Por ejemplo, un conjunto disperso de descriptores podría copiarse en un destino contiguo, viceversa o en alguna combinación.

Varios montones de descriptores pueden estar implicados en la operación de copia, tanto como origen como destino. El uso de identificadores de descriptor como parámetros significa que a los métodos de copia no les importa en qué montones se encuentra un descriptor determinado, ya que todos son solo memoria.

Los tipos de montón de descriptores que se copian de y para deben coincidir, por lo que los métodos toman un tipo de montón de descriptor único como entrada. El controlador debe conocer el tipo de montón de todos los descriptores de la operación de copia determinada, por lo que sabe qué tamaño de los datos está implicado en la operación de copia. Es posible que el controlador también tenga que realizar un trabajo de copia personalizado si un tipo de montón de descriptor determinado lo garantiza: un detalle de implementación. Tenga en cuenta que los propios identificadores de descriptor no identifican a qué tipo apuntan; por lo tanto, se requiere un parámetro adicional para la operación de copia.

Se proporciona una API alternativa a [**CopyDescriptors**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-copydescriptors) para el caso simple de copiar un único intervalo de descriptores de una ubicación a otra: [**CopyDescriptorsSimple.**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-copydescriptorssimple)

Para estos métodos de copia de descriptor basados en dispositivos (escala de tiempo de CPU), los descriptores de origen deben provienen de un montón de descriptores visibles que no sean de sombreador. Los descriptores de destino pueden estar en cualquier montón de descriptores que sea visible para la CPU (sombreador visible o no).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Descriptores de](descriptors.md)
</dt> </dl>

 

 




