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
# <a name="waveprefixcountbits-function"></a>WavePrefixCountBits función)

Devuelve la suma de todas las variables Booleanas especificadas establecidas en true en todas las calles activas con índices más pequeños que la calle actual.

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

Variables Booleanas especificadas.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

La suma de todas las variables Booleanas especificadas establecidas en true en todas las calles activas con índices más pequeños que la calle actual.

## <a name="remarks"></a>Observaciones

Esta función se admite desde el modelo de sombreador 6,0 en todas las fases del sombreador. 



 

## <a name="examples"></a>Ejemplos

En el código siguiente se describe cómo implementar una escritura compactada en una secuencia ordenada en la que el número de elementos escritos por Lane sea 1 o 0.

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

[Información general sobre el modelo de sombreador 6](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[Modelo de sombreador 6](shader-model-6-0.md)
</dt> </dl>

 

 




