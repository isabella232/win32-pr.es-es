---
title: WavePrefixCountBits función)
description: Devuelve la suma de todas las variables Booleanas especificadas establecidas en true en todas las calles activas con índices más pequeños que la calle actual.
ms.assetid: AEC9AFD7-6478-4397-B531-73990D30AA48
keywords:
- WavePrefixCountBits de función HLSL
topic_type:
- apiref
api_name:
- WavePrefixCountBits
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 72f35df1e463ff89441938e4cae19a890821baf9
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/04/2020
ms.locfileid: "104078607"
---
# <a name="waveprefixcountbits-function"></a><span data-ttu-id="e3c99-104">WavePrefixCountBits función)</span><span class="sxs-lookup"><span data-stu-id="e3c99-104">WavePrefixCountBits function</span></span>

<span data-ttu-id="e3c99-105">Devuelve la suma de todas las variables Booleanas especificadas establecidas en true en todas las calles activas con índices más pequeños que la calle actual.</span><span class="sxs-lookup"><span data-stu-id="e3c99-105">Returns the sum of all the specified boolean variables set to true across all active lanes with indices smaller than the current lane.</span></span>

## <a name="syntax"></a><span data-ttu-id="e3c99-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e3c99-106">Syntax</span></span>


``` syntax
uint WavePrefixCountBits(
   bool bBit
);
```



## <a name="parameters"></a><span data-ttu-id="e3c99-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e3c99-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e3c99-108">*bBit*</span><span class="sxs-lookup"><span data-stu-id="e3c99-108">*bBit*</span></span> 
</dt> <dd>

<span data-ttu-id="e3c99-109">Variables Booleanas especificadas.</span><span class="sxs-lookup"><span data-stu-id="e3c99-109">The specified boolean variables.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e3c99-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e3c99-110">Return value</span></span>

<span data-ttu-id="e3c99-111">La suma de todas las variables Booleanas especificadas establecidas en true en todas las calles activas con índices más pequeños que la calle actual.</span><span class="sxs-lookup"><span data-stu-id="e3c99-111">The sum of all the specified Boolean variables set to true across all active lanes with indices smaller than the current lane.</span></span>

## <a name="remarks"></a><span data-ttu-id="e3c99-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e3c99-112">Remarks</span></span>

<span data-ttu-id="e3c99-113">Esta función se admite desde el modelo de sombreador 6,0 en todas las fases del sombreador.</span><span class="sxs-lookup"><span data-stu-id="e3c99-113">This function is supported from shader model 6.0 in all shader stages.</span></span> 



 

## <a name="examples"></a><span data-ttu-id="e3c99-114">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="e3c99-114">Examples</span></span>

<span data-ttu-id="e3c99-115">En el código siguiente se describe cómo implementar una escritura compactada en una secuencia ordenada en la que el número de elementos escritos por Lane sea 1 o 0.</span><span class="sxs-lookup"><span data-stu-id="e3c99-115">The following code describes how to implement a compacted write to an ordered stream where the number of elements written per lane is either 1 or 0.</span></span>

``` syntax
bool bDoesThisLaneHaveAnAppendItem = <expr>;
// compute number of items to append for the whole wave
uint laneAppendOffset = WavePrefixCountBits( bDoesThisLaneHaveAnAppendItem );
uint appendCount = WaveActiveCountBits( bDoesThisLaneHaveAnAppendItem);
// update the output location for this whole wave
uint appendOffset;
if ( WaveIsFirstLane () )
{
    // this way, we only issue one atomic for the entire wave, which reduces contention
    // and keeps the output data for each lane in this wave together in the output buffer
    InterlockedAdd(bufferSize, appendCount, appendOffset);
}
appendOffset = WaveReadLaneFirst( appendOffset ); // broadcast value
appendOffset += laneAppendOffset; // and add in the offset for this lane
buffer[appendOffset] = myData; // write to the offset location for this lane
```

## <a name="see-also"></a><span data-ttu-id="e3c99-116">Vea también</span><span class="sxs-lookup"><span data-stu-id="e3c99-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3c99-117">Información general sobre el modelo de sombreador 6</span><span class="sxs-lookup"><span data-stu-id="e3c99-117">Overview of Shader Model 6</span></span>](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[<span data-ttu-id="e3c99-118">Modelo de sombreador 6</span><span class="sxs-lookup"><span data-stu-id="e3c99-118">Shader Model 6</span></span>](shader-model-6-0.md)
</dt> </dl>

 

 




