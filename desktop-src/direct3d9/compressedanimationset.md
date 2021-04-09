---
description: Contiene los datos del conjunto de animaciones.
ms.assetid: 8d29b9fe-cc6e-48e3-b754-f00f17e4c80a
title: CompressedAnimationSet
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b6cdf8fde552583884604fa66ec1167183918ed5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080260"
---
# <a name="compressedanimationset"></a>CompressedAnimationSet

Contiene los datos del conjunto de animaciones.

``` syntax
template CompressedAnimationSet
{
    <7F9B00B3-F125-4890-876E-1C42BF697C4D>
    DWORD CompressedBlockSize;
    FLOAT TicksPerSec;
    DWORD PlaybackType;
    DWORD BufferLength;
    array DWORD CompressedData[BufferLength];
}
```

Donde:

-   CompressedBlockSize: tamaño total, en bytes, de los datos comprimidos en el búfer de datos de animación de fotogramas clave comprimidos.
-   TicksPerSec: número de TICs de fotogramas clave de animación que se producen por segundo.
-   PlaybackType: tipo de bucle de reproducción establecido de la animación. Consulte [**\_ tipo de D3DXPLAYBACK**](./d3dxplayback-type.md).
-   BufferLength: tamaño mínimo de búfer, en bytes, necesario para contener datos de animación de fotogramas clave comprimidos. El valor es igual a ((CompressedBlockSize + 3)/4).
-   CompressedData \[ BufferLength \] : una matriz de valores de datos comprimidos.

## <a name="see-also"></a>Vea también

<dl> <dt>

[Templates](dx9-graphics-reference-x-file-format-templates.md) (Plantillas [C++])
</dt> <dt>

[**XFILECOMPRESSEDANIMATIONSET**](xfilecompressedanimationset.md)
</dt> </dl>

 

 
