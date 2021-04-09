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
# <a name="compressedanimationset"></a><span data-ttu-id="a1a49-103">CompressedAnimationSet</span><span class="sxs-lookup"><span data-stu-id="a1a49-103">CompressedAnimationSet</span></span>

<span data-ttu-id="a1a49-104">Contiene los datos del conjunto de animaciones.</span><span class="sxs-lookup"><span data-stu-id="a1a49-104">Contains animation set data.</span></span>

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

<span data-ttu-id="a1a49-105">Donde:</span><span class="sxs-lookup"><span data-stu-id="a1a49-105">Where:</span></span>

-   <span data-ttu-id="a1a49-106">CompressedBlockSize: tamaño total, en bytes, de los datos comprimidos en el búfer de datos de animación de fotogramas clave comprimidos.</span><span class="sxs-lookup"><span data-stu-id="a1a49-106">CompressedBlockSize - Total size, in bytes, of the compressed data in the compressed key frame animation data buffer.</span></span>
-   <span data-ttu-id="a1a49-107">TicksPerSec: número de TICs de fotogramas clave de animación que se producen por segundo.</span><span class="sxs-lookup"><span data-stu-id="a1a49-107">TicksPerSec - Number of animation key frame ticks that occur per second.</span></span>
-   <span data-ttu-id="a1a49-108">PlaybackType: tipo de bucle de reproducción establecido de la animación.</span><span class="sxs-lookup"><span data-stu-id="a1a49-108">PlaybackType - Type of the animation set playback loop.</span></span> <span data-ttu-id="a1a49-109">Consulte [**\_ tipo de D3DXPLAYBACK**](./d3dxplayback-type.md).</span><span class="sxs-lookup"><span data-stu-id="a1a49-109">See [**D3DXPLAYBACK\_TYPE**](./d3dxplayback-type.md).</span></span>
-   <span data-ttu-id="a1a49-110">BufferLength: tamaño mínimo de búfer, en bytes, necesario para contener datos de animación de fotogramas clave comprimidos.</span><span class="sxs-lookup"><span data-stu-id="a1a49-110">BufferLength - Minimum buffer size, in bytes, required to hold compressed key frame animation data.</span></span> <span data-ttu-id="a1a49-111">El valor es igual a ((CompressedBlockSize + 3)/4).</span><span class="sxs-lookup"><span data-stu-id="a1a49-111">Value is equal to ( ( CompressedBlockSize + 3 ) / 4 ).</span></span>
-   <span data-ttu-id="a1a49-112">CompressedData \[ BufferLength \] : una matriz de valores de datos comprimidos.</span><span class="sxs-lookup"><span data-stu-id="a1a49-112">CompressedData\[BufferLength\] - An array of compressed data values.</span></span>

## <a name="see-also"></a><span data-ttu-id="a1a49-113">Vea también</span><span class="sxs-lookup"><span data-stu-id="a1a49-113">See also</span></span>

<dl> <dt>

<span data-ttu-id="a1a49-114">[Templates](dx9-graphics-reference-x-file-format-templates.md) (Plantillas [C++])</span><span class="sxs-lookup"><span data-stu-id="a1a49-114">[Templates](dx9-graphics-reference-x-file-format-templates.md)</span></span>
</dt> <dt>

[<span data-ttu-id="a1a49-115">**XFILECOMPRESSEDANIMATIONSET**</span><span class="sxs-lookup"><span data-stu-id="a1a49-115">**XFILECOMPRESSEDANIMATIONSET**</span></span>](xfilecompressedanimationset.md)
</dt> </dl>

 

 
