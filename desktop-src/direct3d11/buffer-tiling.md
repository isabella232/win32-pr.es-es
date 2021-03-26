---
title: Mosaico de búfer
description: Un recurso de búfer se divide en mosaicos de 64 KB, con un espacio vacío en el último mosaico si el tamaño no es múltiplo de 64 KB.
ms.assetid: 979EFCF3-1FE1-412A-A19D-F1B1CF86423B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 061fafa009e554499822c90c8fb6c0c8f34e47f9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103904636"
---
# <a name="buffer-tiling"></a>Mosaico de búfer

Un recurso de [búfer](overviews-direct3d-11-resources-buffers.md) se divide en mosaicos de 64 KB, con un espacio vacío en el último mosaico si el tamaño no es múltiplo de 64 KB.

Los búferes estructurados no deben tener ninguna restricción en el intervalo que se va a colocar en mosaico. Sin embargo, las posibles optimizaciones de rendimiento en el hardware para el uso de [**StructuredBuffers**](/windows/desktop/direct3dhlsl/sm5-object-structuredbuffer) se pueden sacrificar haciéndolos en primer lugar.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Cómo se organiza en mosaico el área de un recurso en mosaico](how-a-tiled-resource-s-area-is-tiled.md)
</dt> </dl>

 

 