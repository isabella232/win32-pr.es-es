---
title: Función WavePrefixCountBits
description: Devuelve la suma de todas las variables booleanas especificadas establecidas en true en todos los carriles activos con índices menores que el actual.
ms.assetid: AEC9AFD7-6478-4397-B531-73990D30AA48
keywords:
- Función HLSL de WavePrefixCountBits
topic_type:
- apiref
api_name:
- WavePrefixCountBits
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 048b63d24e87d97f0e0223083a91694c0471b9e38ad21afbc487c02d711d720d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118504681"
---
# <a name="waveprefixcountbits-function"></a>Función WavePrefixCountBits

Devuelve la suma de todas las variables booleanas especificadas establecidas en true en todos los carriles activos con índices menores que el actual.

## <a name="syntax"></a>Sintaxis


``` syntax
uint WavePrefixCountBits(
   bool bBit
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*bBit* 
</dt> <dd>

Variables booleanas especificadas.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Suma de todas las variables booleanas especificadas establecidas en true en todos los carriles activos con índices menores que el actual.

## <a name="remarks"></a>Comentarios

Esta función se admite desde el modelo de sombreador 6.0 en todas las fases del sombreador. 



 

## <a name="examples"></a>Ejemplos

En el código siguiente se describe cómo implementar una escritura compactada en una secuencia ordenada donde el número de elementos escritos por cada calle es 1 o 0.

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

## <a name="see-also"></a>Vea también

<dl> <dt>

[Información general del modelo de sombreador 6](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[Shader Model 6](shader-model-6-0.md)
</dt> </dl>

 

 




